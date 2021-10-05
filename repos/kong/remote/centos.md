## `kong:centos`

```console
$ docker pull kong@sha256:03453c57b918faa98be9faf2ee7b91239c4a4030a5478b750712408b4104b6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:27efe9259a4da91b92a42030be7bec0d4d3e09b6483ac9473dd4996037c84d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160965349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d952d7b8eb428c80083082cfea96234e5a263dea8f0a1ef32882fbcec5920`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 23:21:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 23:21:23 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 23:21:23 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 23:21:24 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 23:21:24 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Tue, 05 Oct 2021 17:43:00 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Oct 2021 17:43:00 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Oct 2021 17:43:01 GMT
ARG KONG_SHA256=f83a1030b01aa3deb4535394b550228f4804a6fd35a4ea4b11e12dcbcacdadc0
# Tue, 05 Oct 2021 17:43:40 GMT
# ARGS: KONG_SHA256=f83a1030b01aa3deb4535394b550228f4804a6fd35a4ea4b11e12dcbcacdadc0
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then       curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm       && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils git     && yum clean all -q     && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki     && yum install -y /tmp/kong.rpm     && yum clean all     && rm /tmp/kong.rpm     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Oct 2021 17:43:41 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Oct 2021 17:43:41 GMT
USER kong
# Tue, 05 Oct 2021 17:43:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:43:42 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Oct 2021 17:43:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Oct 2021 17:43:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Oct 2021 17:43:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb8a137fa2b84d66997b2207a6880267b365a0a2d08a22a00c4965ecbec7f93`  
		Last Modified: Wed, 15 Sep 2021 23:23:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3563bfe40d23f8dbed26358d7c01a711109642f9d164dacf921387cfe9d5ca`  
		Last Modified: Tue, 05 Oct 2021 17:45:39 GMT  
		Size: 77.4 MB (77446253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b3206af33126cd570c9aa494380def6d75f1e4cdde13c3ea55ccedd8641c93`  
		Last Modified: Tue, 05 Oct 2021 17:45:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
