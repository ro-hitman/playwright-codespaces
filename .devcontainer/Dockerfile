# Use official Playwright image (includes browsers & Node.js)
FROM mcr.microsoft.com/playwright:v1.44.1-jammy

# Set working directory
WORKDIR /workspace

# Copy package.json first (to leverage caching)
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy project files
COPY . .

# Run Playwright install to ensure browsers are ready
RUN npx playwright install --with-deps
