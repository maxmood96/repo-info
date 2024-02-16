## `kong:latest`

```console
$ docker pull kong@sha256:2f2832a751eee25b4cb643a9b8b14df602a88c249c2baba46e3e7b51df2bb78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:e9e3372e7969efb3dc5745dcc692c697c8f7e59cd4e7e716f9ccafbaad2bbfa2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98126553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef97f00b58b7f117b32dc520e84bb6163ed71513f36d4a443dd7121ad163ceb0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 13 Feb 2024 10:06:26 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:06:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:06:26 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:06:28 GMT
ADD file:7f9a3c5a4231ed19174c21d17ce05d84d568cff6d3a0c2a1d7c3a9be5e45c02c in / 
# Tue, 13 Feb 2024 10:06:28 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 02:05:01 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 16 Feb 2024 02:05:01 GMT
ARG ASSET=ce
# Fri, 16 Feb 2024 02:05:01 GMT
ENV ASSET=ce
# Fri, 16 Feb 2024 02:05:02 GMT
ARG EE_PORTS
# Fri, 16 Feb 2024 02:05:02 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 16 Feb 2024 02:05:02 GMT
ARG KONG_VERSION=3.6.0
# Fri, 16 Feb 2024 02:05:02 GMT
ENV KONG_VERSION=3.6.0
# Fri, 16 Feb 2024 02:05:02 GMT
ARG KONG_AMD64_SHA=73baee93639c774f3932e270f2ef9021ee638bff3b301a94bfb6003aaaa8b5e1
# Fri, 16 Feb 2024 02:05:02 GMT
ARG KONG_ARM64_SHA=c7cc33ccfad303c18d83db0d7262be77fce7ec702c49f096ab201a9c5e1ff0be
# Fri, 16 Feb 2024 02:05:21 GMT
# ARGS: KONG_AMD64_SHA=73baee93639c774f3932e270f2ef9021ee638bff3b301a94bfb6003aaaa8b5e1 KONG_ARM64_SHA=c7cc33ccfad303c18d83db0d7262be77fce7ec702c49f096ab201a9c5e1ff0be
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:05:22 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:05:22 GMT
USER kong
# Fri, 16 Feb 2024 02:05:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:05:22 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:05:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:05:22 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:05:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbaaaf731cf9f53a759457afc1217ff264f6487efe92f19ca7024487d8c1c98`  
		Last Modified: Fri, 16 Feb 2024 02:08:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66ae0b9e5b587cf9eaf0ab116ed8977d9c4d0f07f742ee5a4306abf4e4218f7`  
		Last Modified: Fri, 16 Feb 2024 02:08:26 GMT  
		Size: 67.7 MB (67675195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abccdbcbe9b6bde613b6493c27fd48ee3f71dc385b4c113c18f1a907ddfedeb0`  
		Last Modified: Fri, 16 Feb 2024 02:08:15 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f0a23c56a53c10d010927b01a783857a4377ec0940e3fc4433b25b3ce70aba10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95619098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84509ccc6beb753d5c11ec4dd82335026dd379323c8680868ef5869915409ca6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 13 Feb 2024 10:08:34 GMT
ARG RELEASE
# Tue, 13 Feb 2024 10:08:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Feb 2024 10:08:34 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 13 Feb 2024 10:08:48 GMT
ADD file:8d91b8bd386e0cc3407396da8cb35fad29dc5025c641db58739e8c0b3fd77ef0 in / 
# Tue, 13 Feb 2024 10:08:49 GMT
CMD ["/bin/bash"]
# Fri, 16 Feb 2024 05:14:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 16 Feb 2024 05:14:44 GMT
ARG ASSET=ce
# Fri, 16 Feb 2024 05:14:44 GMT
ENV ASSET=ce
# Fri, 16 Feb 2024 05:14:44 GMT
ARG EE_PORTS
# Fri, 16 Feb 2024 05:14:44 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 16 Feb 2024 05:14:44 GMT
ARG KONG_VERSION=3.6.0
# Fri, 16 Feb 2024 05:14:45 GMT
ENV KONG_VERSION=3.6.0
# Fri, 16 Feb 2024 05:14:45 GMT
ARG KONG_AMD64_SHA=73baee93639c774f3932e270f2ef9021ee638bff3b301a94bfb6003aaaa8b5e1
# Fri, 16 Feb 2024 05:14:45 GMT
ARG KONG_ARM64_SHA=c7cc33ccfad303c18d83db0d7262be77fce7ec702c49f096ab201a9c5e1ff0be
# Fri, 16 Feb 2024 05:15:01 GMT
# ARGS: KONG_AMD64_SHA=73baee93639c774f3932e270f2ef9021ee638bff3b301a94bfb6003aaaa8b5e1 KONG_ARM64_SHA=c7cc33ccfad303c18d83db0d7262be77fce7ec702c49f096ab201a9c5e1ff0be
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:03 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:03 GMT
USER kong
# Fri, 16 Feb 2024 05:15:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:03 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:03 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08565b9b970ce2ee9c59c98b4fe1160dd51718e32b803bccaa3c03b2223f3e1a`  
		Last Modified: Fri, 16 Feb 2024 05:17:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54dfd018f922672b74f65a3a94fa1a94d1b5ba45c2a1c60c8a32e202848dac53`  
		Last Modified: Fri, 16 Feb 2024 05:17:32 GMT  
		Size: 67.2 MB (67217495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8b052c898777961fe47aaa773b77db91db18a35d3c055526b0efc9466bdebb`  
		Last Modified: Fri, 16 Feb 2024 05:17:23 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
