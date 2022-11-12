## `kong:latest`

```console
$ docker pull kong@sha256:c0a209738d32222e035ba499645c1fc97af0359f44ff03f9f11f9525d1cbb885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:c0d9a1d8769f68be88cfd37215cd783d6a99220ab38217cd901fff9ea026e755
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75537736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f94128c143e46d5866905344d31b50f1a6173e7a017e380113c1ca0d1e7b438`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:00:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 10 Nov 2022 21:46:01 GMT
ARG KONG_VERSION=3.0.1
# Thu, 10 Nov 2022 21:46:02 GMT
ENV KONG_VERSION=3.0.1
# Thu, 10 Nov 2022 21:46:02 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Thu, 10 Nov 2022 21:46:02 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Thu, 10 Nov 2022 21:46:02 GMT
ARG ASSET=remote
# Thu, 10 Nov 2022 21:46:02 GMT
ARG EE_PORTS
# Thu, 10 Nov 2022 21:46:02 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Thu, 10 Nov 2022 21:46:10 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Thu, 10 Nov 2022 21:46:11 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 10 Nov 2022 21:46:11 GMT
USER kong
# Thu, 10 Nov 2022 21:46:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Nov 2022 21:46:11 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 10 Nov 2022 21:46:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 10 Nov 2022 21:46:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 10 Nov 2022 21:46:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518bc7b676db80fbdd22f09188bf7ea2270f6b1ee4a49b546c65f615abdb470a`  
		Last Modified: Thu, 10 Nov 2022 21:47:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d000063fd2260f7f5c777d18b185489c38b4d566e5358906aa5d2ec7a5481a39`  
		Last Modified: Thu, 10 Nov 2022 21:48:06 GMT  
		Size: 72.7 MB (72730665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669a3f691a57cf72226582b124a176485a9ad85eb0892d79479b8280f3a29c99`  
		Last Modified: Thu, 10 Nov 2022 21:47:58 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:25b187fcd9ecac9db05adabe438d68d09d430854241f54fbd4849a19f6f90f4a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73537168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ce94b18c8a72fedb2b055cbbc84e2c6b84f8204f4086efcd65921826786b8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:27:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 12 Nov 2022 04:27:43 GMT
ARG KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:43 GMT
ENV KONG_VERSION=3.0.1
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901
# Sat, 12 Nov 2022 04:27:44 GMT
ARG KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
# Sat, 12 Nov 2022 04:27:44 GMT
ARG ASSET=remote
# Sat, 12 Nov 2022 04:27:44 GMT
ARG EE_PORTS
# Sat, 12 Nov 2022 04:27:44 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 12 Nov 2022 04:27:51 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=1bca2660d7200cb9e2c1f9ec73ddec967c5934e1494d62123c7d036e98743901 KONG_ARM64_SHA=853f53b447d5971c8eed02355aa718fb09fa91693f54ba417366f70d9dd4a932
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 12 Nov 2022 04:27:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 12 Nov 2022 04:27:52 GMT
USER kong
# Sat, 12 Nov 2022 04:27:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 12 Nov 2022 04:27:52 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 12 Nov 2022 04:27:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 12 Nov 2022 04:27:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 12 Nov 2022 04:27:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e04f8e193571681898f535d00719ae347a2ee8873a72a6520167dc9c128091`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad12cb9acc717d4960140d35382d1f782ce2e51aacc2f6ad3101bc6106db6c5`  
		Last Modified: Sat, 12 Nov 2022 04:30:21 GMT  
		Size: 70.8 MB (70828396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276145d452351533920e24f4a22aca2f2d76f8ebbca1bef83b44ca5578386672`  
		Last Modified: Sat, 12 Nov 2022 04:30:13 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
