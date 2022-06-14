<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.5`](#kong25)
-	[`kong:2.5-ubuntu`](#kong25-ubuntu)
-	[`kong:2.5.2`](#kong252)
-	[`kong:2.5.2-alpine`](#kong252-alpine)
-	[`kong:2.5.2-ubuntu`](#kong252-ubuntu)
-	[`kong:2.6`](#kong26)
-	[`kong:2.6-ubuntu`](#kong26-ubuntu)
-	[`kong:2.6.1`](#kong261)
-	[`kong:2.6.1-alpine`](#kong261-alpine)
-	[`kong:2.6.1-ubuntu`](#kong261-ubuntu)
-	[`kong:2.7`](#kong27)
-	[`kong:2.7-ubuntu`](#kong27-ubuntu)
-	[`kong:2.7.2`](#kong272)
-	[`kong:2.7.2-alpine`](#kong272-alpine)
-	[`kong:2.7.2-ubuntu`](#kong272-ubuntu)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.1`](#kong281)
-	[`kong:2.8.1-alpine`](#kong281-alpine)
-	[`kong:2.8.1-ubuntu`](#kong281-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:41e3edb43d99e58372ad516d02d7723dd4addfbb058cb0bc6f6f7ad224d4f383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:154142e5fd657d9db0e53d9c2f2bb9d3f8690754117153217c7e2c26daec1633
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4df8ab4c6b478a834567e91b0c4afaa8f612d2dd2ad82ef1638dffa8a1791`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:52 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:53 GMT
USER kong
# Tue, 05 Apr 2022 07:18:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e19ff8ee1a3d712fb5a9b15e5dc3975135eabb0db2bdc9d86987b1dc0ab312`  
		Last Modified: Tue, 05 Apr 2022 07:20:38 GMT  
		Size: 47.0 MB (47006838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca93a317bbe9559f2a86be6eb2d745765ebaf28fb2f60aa5c32f0fb28634f5`  
		Last Modified: Tue, 05 Apr 2022 07:20:30 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40bc1b80631be6572ebdd0b3297cf1b405d96eb55605a2843f7395d4c07bd914
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ef302d4e9c486b95849bf1d9380438c9704379c74b16ab5a1a2d9f26b4df54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:28:09 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:10 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:11 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:12 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:13 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:14 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:23 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:28:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:28:24 GMT
USER kong
# Tue, 05 Apr 2022 14:28:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:28:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:28:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:28:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:28:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099f94dcde963cbb40fd4c0b539ebda765c2a4ee6973d14bb0528df4fa3835`  
		Last Modified: Tue, 05 Apr 2022 14:32:09 GMT  
		Size: 46.5 MB (46519329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406022bc9bda03a0ac64449c49805df757f7800fc95c620c9ecc541d65b30820`  
		Last Modified: Tue, 05 Apr 2022 14:32:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:510bc535d6907f88e2af363a61113ce0703533711afd88c1a433842c242f974d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:11f841d34c9cb0fd4c85d88ac37ad439e774d2c70655b4a31d56b37bae558424
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128048586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d977f40343e420dc59b181497d486a56084f348bcaf4b37e625c5de4e3fef8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:28:41 GMT
ARG KONG_VERSION=2.5.1
# Tue, 07 Jun 2022 00:28:41 GMT
ENV KONG_VERSION=2.5.1
# Tue, 07 Jun 2022 00:29:01 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 07 Jun 2022 00:29:02 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 07 Jun 2022 00:29:02 GMT
USER kong
# Tue, 07 Jun 2022 00:29:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:29:02 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jun 2022 00:29:02 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jun 2022 00:29:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 07 Jun 2022 00:29:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db15db8740ebbbbeff9a2457e528bdec9fa3e083aa8d7aa0471c2878f2a2c38a`  
		Last Modified: Tue, 07 Jun 2022 00:32:03 GMT  
		Size: 74.4 MB (74393110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3b72977f8db0bd6f2a315d31d5a93a689e503207df719bf1826485c40e7e01`  
		Last Modified: Tue, 07 Jun 2022 00:31:51 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2`

**does not exist** (yet?)

## `kong:2.5.2-alpine`

**does not exist** (yet?)

## `kong:2.5.2-ubuntu`

**does not exist** (yet?)

## `kong:2.6`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:b29e4bf0c09ae2fffddf1e31ea24db35fefc43719bb8845de65e1c98855ef864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c6ccc7146a15a1e3bfccc1856eebd3536ca30368d75484bba17a0a38c9c8fd51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128173926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bac136e69fb550dcb5dd4bdd4456cf0bb9e4a33358b750d4ae7b1b13156c686`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:27:51 GMT
ARG KONG_VERSION=2.6.1
# Tue, 07 Jun 2022 00:27:51 GMT
ENV KONG_VERSION=2.6.1
# Tue, 07 Jun 2022 00:27:51 GMT
ARG KONG_SHA256=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 07 Jun 2022 00:28:11 GMT
# ARGS: KONG_SHA256=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 07 Jun 2022 00:28:11 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 07 Jun 2022 00:28:11 GMT
USER kong
# Tue, 07 Jun 2022 00:28:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:28:12 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jun 2022 00:28:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jun 2022 00:28:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 07 Jun 2022 00:28:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986dc6dc9495a56a782fc4cc0839d8ab40802e0bdf4f83800fc4bd9b3a69bdc4`  
		Last Modified: Tue, 07 Jun 2022 00:31:20 GMT  
		Size: 74.5 MB (74518449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb31489b3bb16bb4d3055ae778be493714a9dd273c28eb8a788517f40de87d3`  
		Last Modified: Tue, 07 Jun 2022 00:31:07 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-alpine`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-ubuntu`

```console
$ docker pull kong@sha256:b29e4bf0c09ae2fffddf1e31ea24db35fefc43719bb8845de65e1c98855ef864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c6ccc7146a15a1e3bfccc1856eebd3536ca30368d75484bba17a0a38c9c8fd51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128173926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bac136e69fb550dcb5dd4bdd4456cf0bb9e4a33358b750d4ae7b1b13156c686`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:27:51 GMT
ARG KONG_VERSION=2.6.1
# Tue, 07 Jun 2022 00:27:51 GMT
ENV KONG_VERSION=2.6.1
# Tue, 07 Jun 2022 00:27:51 GMT
ARG KONG_SHA256=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 07 Jun 2022 00:28:11 GMT
# ARGS: KONG_SHA256=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 07 Jun 2022 00:28:11 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 07 Jun 2022 00:28:11 GMT
USER kong
# Tue, 07 Jun 2022 00:28:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:28:12 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jun 2022 00:28:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jun 2022 00:28:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 07 Jun 2022 00:28:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986dc6dc9495a56a782fc4cc0839d8ab40802e0bdf4f83800fc4bd9b3a69bdc4`  
		Last Modified: Tue, 07 Jun 2022 00:31:20 GMT  
		Size: 74.5 MB (74518449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb31489b3bb16bb4d3055ae778be493714a9dd273c28eb8a788517f40de87d3`  
		Last Modified: Tue, 07 Jun 2022 00:31:07 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:5608014b1142d8deaa812334ec724d6b8a55399ef5daa8cd155798e552f075d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:82a38b5861eb54d84399bc733e8c69739b7b22a052e1197b0e63324091f907a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128083052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee35070bb5998b52dbcabfe8d254bdd7da95353ccf872a5a8af3a424d623bf1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:26:55 GMT
ARG KONG_VERSION=2.7.2
# Tue, 07 Jun 2022 00:26:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 07 Jun 2022 00:26:55 GMT
ARG KONG_SHA256=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 07 Jun 2022 00:27:15 GMT
# ARGS: KONG_SHA256=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 07 Jun 2022 00:27:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 07 Jun 2022 00:27:16 GMT
USER kong
# Tue, 07 Jun 2022 00:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:27:16 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jun 2022 00:27:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jun 2022 00:27:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 07 Jun 2022 00:27:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7391058a82af98cb96cbef218ca71c1efef96b6b1fb170417b6fdc8ae78d372b`  
		Last Modified: Tue, 07 Jun 2022 00:30:36 GMT  
		Size: 74.4 MB (74427577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2949730535707664ffb857e7c9aa0c1a71c94cf075576ef18a76373c1703e07d`  
		Last Modified: Tue, 07 Jun 2022 00:30:23 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-alpine`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-ubuntu`

```console
$ docker pull kong@sha256:5608014b1142d8deaa812334ec724d6b8a55399ef5daa8cd155798e552f075d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:82a38b5861eb54d84399bc733e8c69739b7b22a052e1197b0e63324091f907a2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128083052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee35070bb5998b52dbcabfe8d254bdd7da95353ccf872a5a8af3a424d623bf1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:26:55 GMT
ARG KONG_VERSION=2.7.2
# Tue, 07 Jun 2022 00:26:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 07 Jun 2022 00:26:55 GMT
ARG KONG_SHA256=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 07 Jun 2022 00:27:15 GMT
# ARGS: KONG_SHA256=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 07 Jun 2022 00:27:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 07 Jun 2022 00:27:16 GMT
USER kong
# Tue, 07 Jun 2022 00:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:27:16 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jun 2022 00:27:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jun 2022 00:27:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 07 Jun 2022 00:27:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7391058a82af98cb96cbef218ca71c1efef96b6b1fb170417b6fdc8ae78d372b`  
		Last Modified: Tue, 07 Jun 2022 00:30:36 GMT  
		Size: 74.4 MB (74427577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2949730535707664ffb857e7c9aa0c1a71c94cf075576ef18a76373c1703e07d`  
		Last Modified: Tue, 07 Jun 2022 00:30:23 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:e7f75a2e891f86caf9a70483ad7cbde119d7594149517fafe619b27bee61d349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49125256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8301ad2c6ccefa9744c675de2e3776def471cb145084c87faa69b863bde93cd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:31:04 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:04 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:31:13 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:31:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:31:13 GMT
USER kong
# Tue, 12 Apr 2022 19:31:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:31:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:31:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:31:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:31:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389c4f1235973b918da1c03c0ab36b3fe30f024ed66d40c2704a5e0759137272`  
		Last Modified: Tue, 12 Apr 2022 19:34:09 GMT  
		Size: 46.3 MB (46309685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd99fa0f49fc3b1008ca9553bff84563001d150bed9eec2cc9df121d5db0927b`  
		Last Modified: Tue, 12 Apr 2022 19:34:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b5dd30242a9c70c3f3fe1f1eed665d3f1f3280dd167fe339ff8c991c93b1a129
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48318586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21617654cc9d61550449c01006c561ca0c6bb1f7212bb27a056dc85184de9341`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:57:42 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:43 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:44 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:57:45 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:57:54 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:57:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:57:55 GMT
USER kong
# Tue, 12 Apr 2022 19:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:57:57 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:57:58 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:57:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:58:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1ac9a25b76951006c1ab965d664048643344f28e6224df493b5ed8f25c2627`  
		Last Modified: Tue, 12 Apr 2022 20:11:06 GMT  
		Size: 45.6 MB (45601096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8881b423857a7b53f2a070f5501cfaf8f63792c1f400fc72ec6cb31aaf6b52f0`  
		Last Modified: Tue, 12 Apr 2022 20:10:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:fd8e7897ce63a854c9f2f3d3927a8d587360b80ef0f9def3f1b27117c7d8786f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:50fefa51ccc5909f3e57a7279dd153fbf425bc7704c2f93e777d388ea7f821a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121218928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264d4a75521d2cf61d05595aecf21d93c401834764b9362beb5da91415753d9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 07 Jun 2022 00:26:15 GMT
# ARGS: KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 07 Jun 2022 00:26:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 07 Jun 2022 00:26:16 GMT
USER kong
# Tue, 07 Jun 2022 00:26:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:26:16 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jun 2022 00:26:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jun 2022 00:26:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 07 Jun 2022 00:26:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e76228566c8ec01fe53691dd208967675ceacf38c8ddf4910d1833f8c8741a`  
		Last Modified: Tue, 07 Jun 2022 00:29:51 GMT  
		Size: 67.6 MB (67563452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09188cfbfd1ecaeeb940114cdb434e05b83811c8ae776255cc4cda0ff722221`  
		Last Modified: Tue, 07 Jun 2022 00:29:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1` - linux; amd64

```console
$ docker pull kong@sha256:e7f75a2e891f86caf9a70483ad7cbde119d7594149517fafe619b27bee61d349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49125256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8301ad2c6ccefa9744c675de2e3776def471cb145084c87faa69b863bde93cd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:31:04 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:04 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:31:13 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:31:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:31:13 GMT
USER kong
# Tue, 12 Apr 2022 19:31:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:31:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:31:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:31:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:31:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389c4f1235973b918da1c03c0ab36b3fe30f024ed66d40c2704a5e0759137272`  
		Last Modified: Tue, 12 Apr 2022 19:34:09 GMT  
		Size: 46.3 MB (46309685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd99fa0f49fc3b1008ca9553bff84563001d150bed9eec2cc9df121d5db0927b`  
		Last Modified: Tue, 12 Apr 2022 19:34:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b5dd30242a9c70c3f3fe1f1eed665d3f1f3280dd167fe339ff8c991c93b1a129
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48318586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21617654cc9d61550449c01006c561ca0c6bb1f7212bb27a056dc85184de9341`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:57:42 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:43 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:44 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:57:45 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:57:54 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:57:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:57:55 GMT
USER kong
# Tue, 12 Apr 2022 19:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:57:57 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:57:58 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:57:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:58:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1ac9a25b76951006c1ab965d664048643344f28e6224df493b5ed8f25c2627`  
		Last Modified: Tue, 12 Apr 2022 20:11:06 GMT  
		Size: 45.6 MB (45601096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8881b423857a7b53f2a070f5501cfaf8f63792c1f400fc72ec6cb31aaf6b52f0`  
		Last Modified: Tue, 12 Apr 2022 20:10:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-alpine`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:e7f75a2e891f86caf9a70483ad7cbde119d7594149517fafe619b27bee61d349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49125256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8301ad2c6ccefa9744c675de2e3776def471cb145084c87faa69b863bde93cd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:31:04 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:04 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:31:13 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:31:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:31:13 GMT
USER kong
# Tue, 12 Apr 2022 19:31:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:31:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:31:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:31:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:31:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389c4f1235973b918da1c03c0ab36b3fe30f024ed66d40c2704a5e0759137272`  
		Last Modified: Tue, 12 Apr 2022 19:34:09 GMT  
		Size: 46.3 MB (46309685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd99fa0f49fc3b1008ca9553bff84563001d150bed9eec2cc9df121d5db0927b`  
		Last Modified: Tue, 12 Apr 2022 19:34:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b5dd30242a9c70c3f3fe1f1eed665d3f1f3280dd167fe339ff8c991c93b1a129
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48318586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21617654cc9d61550449c01006c561ca0c6bb1f7212bb27a056dc85184de9341`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:57:42 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:43 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:44 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:57:45 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:57:54 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:57:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:57:55 GMT
USER kong
# Tue, 12 Apr 2022 19:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:57:57 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:57:58 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:57:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:58:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1ac9a25b76951006c1ab965d664048643344f28e6224df493b5ed8f25c2627`  
		Last Modified: Tue, 12 Apr 2022 20:11:06 GMT  
		Size: 45.6 MB (45601096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8881b423857a7b53f2a070f5501cfaf8f63792c1f400fc72ec6cb31aaf6b52f0`  
		Last Modified: Tue, 12 Apr 2022 20:10:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-ubuntu`

```console
$ docker pull kong@sha256:fd8e7897ce63a854c9f2f3d3927a8d587360b80ef0f9def3f1b27117c7d8786f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:50fefa51ccc5909f3e57a7279dd153fbf425bc7704c2f93e777d388ea7f821a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121218928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264d4a75521d2cf61d05595aecf21d93c401834764b9362beb5da91415753d9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 07 Jun 2022 00:26:15 GMT
# ARGS: KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 07 Jun 2022 00:26:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 07 Jun 2022 00:26:16 GMT
USER kong
# Tue, 07 Jun 2022 00:26:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:26:16 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jun 2022 00:26:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jun 2022 00:26:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 07 Jun 2022 00:26:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e76228566c8ec01fe53691dd208967675ceacf38c8ddf4910d1833f8c8741a`  
		Last Modified: Tue, 07 Jun 2022 00:29:51 GMT  
		Size: 67.6 MB (67563452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09188cfbfd1ecaeeb940114cdb434e05b83811c8ae776255cc4cda0ff722221`  
		Last Modified: Tue, 07 Jun 2022 00:29:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:e7f75a2e891f86caf9a70483ad7cbde119d7594149517fafe619b27bee61d349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49125256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8301ad2c6ccefa9744c675de2e3776def471cb145084c87faa69b863bde93cd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:31:04 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:04 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:31:13 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:31:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:31:13 GMT
USER kong
# Tue, 12 Apr 2022 19:31:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:31:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:31:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:31:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:31:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389c4f1235973b918da1c03c0ab36b3fe30f024ed66d40c2704a5e0759137272`  
		Last Modified: Tue, 12 Apr 2022 19:34:09 GMT  
		Size: 46.3 MB (46309685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd99fa0f49fc3b1008ca9553bff84563001d150bed9eec2cc9df121d5db0927b`  
		Last Modified: Tue, 12 Apr 2022 19:34:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b5dd30242a9c70c3f3fe1f1eed665d3f1f3280dd167fe339ff8c991c93b1a129
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48318586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21617654cc9d61550449c01006c561ca0c6bb1f7212bb27a056dc85184de9341`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:57:42 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:43 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:44 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:57:45 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:57:54 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:57:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:57:55 GMT
USER kong
# Tue, 12 Apr 2022 19:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:57:57 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:57:58 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:57:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:58:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1ac9a25b76951006c1ab965d664048643344f28e6224df493b5ed8f25c2627`  
		Last Modified: Tue, 12 Apr 2022 20:11:06 GMT  
		Size: 45.6 MB (45601096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8881b423857a7b53f2a070f5501cfaf8f63792c1f400fc72ec6cb31aaf6b52f0`  
		Last Modified: Tue, 12 Apr 2022 20:10:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:612de7e2260e52063d8afaed6037c8a831781d7ef4354c3fb199c7a88964d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:e7f75a2e891f86caf9a70483ad7cbde119d7594149517fafe619b27bee61d349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49125256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8301ad2c6ccefa9744c675de2e3776def471cb145084c87faa69b863bde93cd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:31:04 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:04 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:31:05 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:31:13 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:31:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:31:13 GMT
USER kong
# Tue, 12 Apr 2022 19:31:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:31:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:31:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:31:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:31:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389c4f1235973b918da1c03c0ab36b3fe30f024ed66d40c2704a5e0759137272`  
		Last Modified: Tue, 12 Apr 2022 19:34:09 GMT  
		Size: 46.3 MB (46309685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd99fa0f49fc3b1008ca9553bff84563001d150bed9eec2cc9df121d5db0927b`  
		Last Modified: Tue, 12 Apr 2022 19:34:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b5dd30242a9c70c3f3fe1f1eed665d3f1f3280dd167fe339ff8c991c93b1a129
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48318586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21617654cc9d61550449c01006c561ca0c6bb1f7212bb27a056dc85184de9341`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:57:42 GMT
ARG KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:43 GMT
ENV KONG_VERSION=2.8.1
# Tue, 12 Apr 2022 19:57:44 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 12 Apr 2022 19:57:45 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 12 Apr 2022 19:57:54 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:57:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:57:55 GMT
USER kong
# Tue, 12 Apr 2022 19:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:57:57 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:57:58 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:57:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:58:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1ac9a25b76951006c1ab965d664048643344f28e6224df493b5ed8f25c2627`  
		Last Modified: Tue, 12 Apr 2022 20:11:06 GMT  
		Size: 45.6 MB (45601096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8881b423857a7b53f2a070f5501cfaf8f63792c1f400fc72ec6cb31aaf6b52f0`  
		Last Modified: Tue, 12 Apr 2022 20:10:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:fd8e7897ce63a854c9f2f3d3927a8d587360b80ef0f9def3f1b27117c7d8786f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:50fefa51ccc5909f3e57a7279dd153fbf425bc7704c2f93e777d388ea7f821a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121218928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264d4a75521d2cf61d05595aecf21d93c401834764b9362beb5da91415753d9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 07 Jun 2022 00:26:15 GMT
# ARGS: KONG_SHA256=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 07 Jun 2022 00:26:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 07 Jun 2022 00:26:16 GMT
USER kong
# Tue, 07 Jun 2022 00:26:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 07 Jun 2022 00:26:16 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 07 Jun 2022 00:26:16 GMT
STOPSIGNAL SIGQUIT
# Tue, 07 Jun 2022 00:26:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 07 Jun 2022 00:26:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e76228566c8ec01fe53691dd208967675ceacf38c8ddf4910d1833f8c8741a`  
		Last Modified: Tue, 07 Jun 2022 00:29:51 GMT  
		Size: 67.6 MB (67563452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09188cfbfd1ecaeeb940114cdb434e05b83811c8ae776255cc4cda0ff722221`  
		Last Modified: Tue, 07 Jun 2022 00:29:39 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
