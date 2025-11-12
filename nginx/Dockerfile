#Use Nginx with Alpine Linux as the base image
FROM nginx:1.27-alpine

# Copy custom nginx config
COPY ./nginx.conf /etc/nginx/conf.d/default.conf

# Expose port
EXPOSE 80

# Optional healthcheck
HEALTHCHECK CMD wget --no-verbose --tries=1 --spider http://wasp_poc-frontend-1:5173/ || exit 1

#runs the Nginx web server in foreground mode instead of as a background daemon
CMD ["nginx", "-g", "daemon off;"]