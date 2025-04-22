# Stage 1: Builder
FROM node:18-alpine AS builder

WORKDIR /usr/src/app

# Install build tools and UPX
# Combine update and add, clean up cache afterwards
RUN apk update && apk add --no-cache python3 make g++ upx && rm -rf /var/cache/apk/*

# Copy package files - copy lock file separately for better caching
COPY package.json ./
COPY package-lock.json ./

# Use npm ci for faster, deterministic installs based on lock file
RUN npm ci --verbose

# Copy the rest of the application source code
COPY . .

# Build the standalone executable for Alpine Linux
RUN npx pkg . --targets node18-alpine-x64 --output js-compressor

FROM alpine:3.21 

WORKDIR /usr/src/app

# Copy only the compiled executable from the builder stage (no longer UPX compressed)
COPY --from=builder /usr/src/app/js-compressor .

# Define the entrypoint for the container
ENTRYPOINT ["/usr/src/app/js-compressor"]