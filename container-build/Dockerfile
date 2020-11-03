# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
EXPOSE 8080
RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
	chmod -R 770 /var/log/httpd /var/run/httpd
