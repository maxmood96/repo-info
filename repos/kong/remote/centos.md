## `kong:centos`

```console
$ docker pull kong@sha256:3fe8d93506c4976dc7064155c720395f645bc6bee47963dc6707c73ef7c378c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:99d3e60ecb45b768810ee30bed38b0bb4ac0500ab30ff263d64042d6d2f4412a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127049642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04063013f8670afb5951aa9ffa990adb8472dfae45152dfe62cacc367793fd2a`
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
# Thu, 20 Aug 2020 23:20:41 GMT
ARG KONG_VERSION=2.1.3
# Thu, 20 Aug 2020 23:20:41 GMT
ENV KONG_VERSION=2.1.3
# Thu, 20 Aug 2020 23:20:41 GMT
ARG KONG_SHA256=be97835859ca05de3db5144bb59c8bdd4e46bd7a65fdd5f7ec500cb445eb62e3
# Thu, 20 Aug 2020 23:21:03 GMT
# ARGS: KONG_SHA256=be97835859ca05de3db5144bb59c8bdd4e46bd7a65fdd5f7ec500cb445eb62e3
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib zlib-devel 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Thu, 20 Aug 2020 23:21:04 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Thu, 20 Aug 2020 23:21:04 GMT
USER kong
# Thu, 20 Aug 2020 23:21:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 20 Aug 2020 23:21:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 20 Aug 2020 23:21:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Aug 2020 23:21:05 GMT
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
	-	`sha256:b00205bf0b6ef1a3c09336bd78195efefea9c80768935055e829c6d5b7beebdd`  
		Last Modified: Thu, 20 Aug 2020 23:22:12 GMT  
		Size: 51.2 MB (51185594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b5c5d2d7225b7c09662be5dac557ea867c0850015f901d24a69927c69604cf`  
		Last Modified: Thu, 20 Aug 2020 23:22:01 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
