## `kong:centos`

```console
$ docker pull kong@sha256:24859fdc4ec94d813fc09fe5ba61be9ea9becf8f6d09d7c5b956b650b1bfdd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:60b12ba268c4a866d1add6a80ddf5db9b21b999d17618670423ca69285b996db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127391058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a456825d3bd4323426411c3664b786e230578fb4d643fc59c1a756933ca42d63`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 13 Jan 2021 21:21:11 GMT
ARG KONG_VERSION=2.3.0
# Wed, 13 Jan 2021 21:21:11 GMT
ENV KONG_VERSION=2.3.0
# Wed, 13 Jan 2021 21:21:12 GMT
ARG KONG_SHA256=306dade5e8c5a8342b2c489a30aa587eacd31be22dff078b787285d301408cd3
# Wed, 13 Jan 2021 21:21:40 GMT
# ARGS: KONG_SHA256=306dade5e8c5a8342b2c489a30aa587eacd31be22dff078b787285d301408cd3
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 13 Jan 2021 21:21:40 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 13 Jan 2021 21:21:41 GMT
USER kong
# Wed, 13 Jan 2021 21:21:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Jan 2021 21:21:41 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 13 Jan 2021 21:21:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Jan 2021 21:21:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ee1dcb5626eb3f5d25875679d0f99369984de57183869d464511476fe319c1`  
		Last Modified: Wed, 13 Jan 2021 21:23:55 GMT  
		Size: 51.3 MB (51293039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592aaf7c3c68bd535f7b0a5567fcb75b508ba1f4edb2c29063124c26fd819850`  
		Last Modified: Wed, 13 Jan 2021 21:23:44 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
