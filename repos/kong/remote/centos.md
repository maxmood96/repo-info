## `kong:centos`

```console
$ docker pull kong@sha256:1f78e6d9b2768da70648254442b63008e426f449f5cc100a81cfbda5cedc4da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:f819025d9dfa747e6c756046e29373d084b0b40214c60c562998245767be22f0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127040867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81ced2a83ce483cd795e4986e692871a8cb8ebbb9d3b1c5335e227967cd670c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 10 Aug 2020 18:20:08 GMT
ADD file:61908381d3142ffba798ae9a904476d19b197ab79d0338f14bec0f76649df8d4 in / 
# Mon, 10 Aug 2020 18:20:09 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200809 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-08-09 00:00:00+01:00
# Mon, 10 Aug 2020 18:20:09 GMT
CMD ["/bin/bash"]
# Mon, 10 Aug 2020 18:37:24 GMT
LABEL maintainer=Kong <support@konghq.com>
# Mon, 10 Aug 2020 18:37:24 GMT
ARG ASSET=ce
# Mon, 10 Aug 2020 18:37:25 GMT
ENV ASSET=ce
# Mon, 10 Aug 2020 18:37:25 GMT
ARG EE_PORTS
# Mon, 10 Aug 2020 18:37:25 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Mon, 10 Aug 2020 18:37:25 GMT
ARG KONG_VERSION=2.1.1
# Mon, 10 Aug 2020 18:37:25 GMT
ENV KONG_VERSION=2.1.1
# Mon, 10 Aug 2020 18:37:25 GMT
ARG KONG_SHA256=3ea097a450a916d94498e1e1b8ae6dbf0089c3007227f07156d9d8467a82c9c4
# Mon, 10 Aug 2020 18:37:49 GMT
# ARGS: KONG_SHA256=3ea097a450a916d94498e1e1b8ae6dbf0089c3007227f07156d9d8467a82c9c4
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib zlib-devel 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Mon, 10 Aug 2020 18:37:49 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Mon, 10 Aug 2020 18:37:49 GMT
USER kong
# Mon, 10 Aug 2020 18:37:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 10 Aug 2020 18:37:50 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 10 Aug 2020 18:37:50 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Aug 2020 18:37:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:75f829a71a1c5277a7abf55495ac8d16759691d980bf1d931795e5eb68a294c0`  
		Last Modified: Mon, 10 Aug 2020 18:21:46 GMT  
		Size: 75.9 MB (75863188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c636c1fa5b3254b7692cb41da3aee6a2547a919e7a84290bd6f7c05f9ef334`  
		Last Modified: Mon, 10 Aug 2020 18:39:00 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729bccb80ef50e74afac787b24bd8e20f94c02a2b1e1eaa9b32aafee1497414`  
		Last Modified: Mon, 10 Aug 2020 18:39:12 GMT  
		Size: 51.2 MB (51176819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7a5154508e105a09f298c17bd73d5775ef441f4b2a6177a64d3849bbf3b1d4`  
		Last Modified: Mon, 10 Aug 2020 18:39:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
