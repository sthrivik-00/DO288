FROM quay.io/sthrivik_00/newnginx

LABEL io.openshift.expose.service="8080:http"

RUN sed -i -e 's/listen       80/listen       8080/g' /etc/nginx/conf.d/default.conf  && \
	sed -i -e 's/listen  [::]:80/isten  [::]:8080/g' /etc/nginx/conf.d/default.conf && \
	chgrp -R 0 /var/run /usr/share/nginx/html	&& \
	chmod -R g=u /var/run /usr/share/nginx/html

