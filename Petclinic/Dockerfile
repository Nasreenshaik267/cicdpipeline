/FROM openjdk:8
//EXPOSE 8082
//ADD target/petclinic.war petclinic.war
//ENTRYPOINT ["java","-jar","/petclinic.war"]




# Use the official Nginx base image
FROM nginx:alpine

# Maintainer info (optional)
LABEL maintainer="nasreen416@example.com"

# Remove the default nginx website
RUN rm -rf /usr/share/nginx/html/*

# Copy your custom application files (from Jenkins workspace)
COPY ./Petclinic/target/ /usr/share/nginx/html/

# Expose Nginx default port
EXPOSE 80

# Start Nginx in foreground
CMD ["nginx", "-g", "daemon off;"]
