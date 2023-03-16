## `kong:ubuntu`

```console
$ docker pull kong@sha256:975961b67d0fbc8c196a6b5793a6dd37c31bc178ab6203f1c6f904b9607e8e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8ed9bd110f3da4288bdbeea1e304bad5871743e77bb8c64c47a3e61672777ee0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101726780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33890cc7473f3e37ff7fca779b2a0f56eeba8c5dc3fe6f0262e000b3c57eb911`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:41:26 GMT
ADD file:20f2ff22b9a8ca9bec5178036c9ebc525a12cd4312daf5d14a9a631a30be20e1 in / 
# Wed, 08 Mar 2023 04:41:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 04:52:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 16 Mar 2023 04:52:49 GMT
ARG ASSET=ce
# Thu, 16 Mar 2023 04:52:49 GMT
ENV ASSET=ce
# Thu, 16 Mar 2023 04:52:49 GMT
ARG EE_PORTS
# Thu, 16 Mar 2023 04:52:49 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 16 Mar 2023 04:52:49 GMT
ARG KONG_VERSION=3.1.1
# Thu, 16 Mar 2023 04:52:50 GMT
ENV KONG_VERSION=3.1.1
# Thu, 16 Mar 2023 04:52:50 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 16 Mar 2023 04:52:50 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 16 Mar 2023 04:53:44 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 16 Mar 2023 04:53:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 16 Mar 2023 04:53:45 GMT
USER kong
# Thu, 16 Mar 2023 04:53:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:53:45 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 16 Mar 2023 04:53:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Mar 2023 04:53:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 16 Mar 2023 04:53:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:5544ebdc0c7b82aa6901eae124b1d220914d2629a9bde25396d7ee9cfd273a8f`  
		Last Modified: Wed, 08 Mar 2023 09:02:58 GMT  
		Size: 28.6 MB (28578068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0310ac76a75b3413c8efa68949fbf815db82ac8624b9d1ca500280c0722969f`  
		Last Modified: Thu, 16 Mar 2023 04:56:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7f03c733975322bd977f20abb1e6abb79a4c3d9b211be3afa32f6e14d522ac`  
		Last Modified: Thu, 16 Mar 2023 04:56:13 GMT  
		Size: 73.1 MB (73147706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31059c935546737773cd25b29801a0113c45428a34a09cc5676aa03f11aeff8f`  
		Last Modified: Thu, 16 Mar 2023 04:56:02 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9f9955f0bdc78ba76c52a2eba62efede56b47fb645ec01b4356579f5eddfeb51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98966357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ae7460b241a3710fe8abe5f21fea1620f771abbed7d26aeaef4b916de33c55`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:32:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 16 Mar 2023 02:32:55 GMT
ARG ASSET=ce
# Thu, 16 Mar 2023 02:32:55 GMT
ENV ASSET=ce
# Thu, 16 Mar 2023 02:32:55 GMT
ARG EE_PORTS
# Thu, 16 Mar 2023 02:32:56 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 16 Mar 2023 02:32:56 GMT
ARG KONG_VERSION=3.1.1
# Thu, 16 Mar 2023 02:32:56 GMT
ENV KONG_VERSION=3.1.1
# Thu, 16 Mar 2023 02:32:56 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 16 Mar 2023 02:32:56 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 16 Mar 2023 02:33:24 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 16 Mar 2023 02:33:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 16 Mar 2023 02:33:25 GMT
USER kong
# Thu, 16 Mar 2023 02:33:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 16 Mar 2023 02:33:26 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 16 Mar 2023 02:33:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Mar 2023 02:33:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 16 Mar 2023 02:33:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e58bbdc23e3f7ce51624faf13094ccd5a8b2bc147310d449308170aaea47858`  
		Last Modified: Thu, 16 Mar 2023 02:34:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e646675e52dfdb0a044814d6b6639b18f1ca2b8c611012f3505e0d58e12d98da`  
		Last Modified: Thu, 16 Mar 2023 02:35:07 GMT  
		Size: 71.8 MB (71769188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4789db6cc6108aa4834e2b9b21406a3dcba608a8dd70f6868fb008f1882368`  
		Last Modified: Thu, 16 Mar 2023 02:34:59 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
