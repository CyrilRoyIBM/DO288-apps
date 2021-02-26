# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent
LABEL io.k8s.description="A basic Apache HTTP CRO Server child image, uses ONBUILD" \
      io.k8s.display-name="Apache HTTP Server Lapoutre" \
      io.openshift.expose-services="8080:http" \
      io.openshift.tags="apache, httpd, CRO, Lapoutre"
EXPOSE 8081
RUN sed -i 's#Listen 80#Listen 8081#' /etc/httpd/conf/httpd.conf && \
	chgrp -R 0 /var/log/httpd /var/run/httpd && \
	chmod -R 770 /var/log/httpd /var/run/httpd
#USER 1001
USER root
