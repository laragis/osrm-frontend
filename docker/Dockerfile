FROM node:18-alpine

# Enables customized options using environment variables
ENV OSRM_BACKEND='http://localhost:5000'
ENV OSRM_CENTER='38.8995,-77.0269'
ENV OSRM_ZOOM='13'
ENV OSRM_LANGUAGE='en'
ENV OSRM_LABEL='Car (fastest)'
ENV OSRM_MAPBOX_TOKEN='pk.eyJ1IjoibXNsZWUiLCJhIjoiclpiTWV5SSJ9.P_h8r37vD8jpIH1A6i1VRg'

# Copy package.json
RUN mkdir -p /src

WORKDIR /src

COPY package.json .

# Install app dependencies
RUN yarn install

# Create app directory
COPY . .

# Run App
EXPOSE 9966
CMD ["yarn", "start"]
