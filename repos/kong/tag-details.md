<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.4`](#kong284)
-	[`kong:2.8.4-alpine`](#kong284-alpine)
-	[`kong:2.8.4-ubuntu`](#kong284-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.4`](#kong34)
-	[`kong:3.4-ubuntu`](#kong34-ubuntu)
-	[`kong:3.4.2`](#kong342)
-	[`kong:3.4.2-ubuntu`](#kong342-ubuntu)
-	[`kong:3.5`](#kong35)
-	[`kong:3.5-ubuntu`](#kong35-ubuntu)
-	[`kong:3.5.0`](#kong350)
-	[`kong:3.5.0-ubuntu`](#kong350-ubuntu)
-	[`kong:3.6`](#kong36)
-	[`kong:3.6-ubuntu`](#kong36-ubuntu)
-	[`kong:3.6.1`](#kong361)
-	[`kong:3.6.1-ubuntu`](#kong361-ubuntu)
-	[`kong:3.7`](#kong37)
-	[`kong:3.7-ubuntu`](#kong37-ubuntu)
-	[`kong:3.7.0`](#kong370)
-	[`kong:3.7.0-ubuntu`](#kong370-ubuntu)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.8`

```console
$ docker pull kong@sha256:6dd27da5c4ef60b7dd8041474636dd4b16ca0619926886d7268e0cb737eaa6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:eabe04c11acecb5a45ed2d2e235e133b8cce4b57eb274766ea35bf6f15533aee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b647b495d1191b1c6660bfafc5fc121f5868115f27d5a2b1dde7b986e01f015`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:42:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Mar 2024 08:42:20 GMT
ARG ASSET=ce
# Sat, 16 Mar 2024 08:42:20 GMT
ENV ASSET=ce
# Sat, 16 Mar 2024 08:42:20 GMT
ARG EE_PORTS
# Sat, 16 Mar 2024 08:42:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 08:42:20 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 16 Mar 2024 08:42:28 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Mar 2024 08:42:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Mar 2024 08:42:28 GMT
USER kong
# Sat, 16 Mar 2024 08:42:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:42:28 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Mar 2024 08:42:29 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 08:42:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Mar 2024 08:42:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473c07a218a4949e46dab18b8e41402a9330a692cfaeae43f320bfd607707009`  
		Last Modified: Sat, 16 Mar 2024 08:43:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218b46ec42b4988ef080ec0eed5ad36371aa259ef900eefa8f01309d03449d84`  
		Last Modified: Sat, 16 Mar 2024 08:43:11 GMT  
		Size: 44.7 MB (44716900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902d83c366d3225163eec0a9ad89a1841fd4791ece418094c908ff1f1badf853`  
		Last Modified: Sat, 16 Mar 2024 08:43:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:cbb4ef7bc95c9f497341d2c4fb99bf7450d5e283c87e6fe7389a48919b514f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:efcf9c410ff84a727f8e0a796d09b19e4b45bbfe20e9795e68f8d0aac9b6ca9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116549388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc55722a4595026505e6c990c2429c6f67f77fda76ab41895b2ad5fb3193d46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:31:10 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:31:10 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:31:10 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:31:10 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:31:10 GMT
ARG KONG_VERSION=2.8.4
# Wed, 05 Jun 2024 07:31:10 GMT
ENV KONG_VERSION=2.8.4
# Wed, 05 Jun 2024 07:31:11 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Wed, 05 Jun 2024 07:31:11 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Wed, 05 Jun 2024 07:31:39 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:31:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:31:40 GMT
USER kong
# Wed, 05 Jun 2024 07:31:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:31:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:31:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:31:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:31:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e7c2ea5c74c56b2204aa68af2405c00aff3f9ebd18fedf2592e897777c48a7`  
		Last Modified: Wed, 05 Jun 2024 07:33:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d41bde6bb16c1c697fcd2be7adb5a880a6b4064d1f604dbe753c5af23c3fd3`  
		Last Modified: Wed, 05 Jun 2024 07:33:36 GMT  
		Size: 61.0 MB (61027273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f7c3c9272055868997065e093a269efd8498d6e7eaf430dc65ef92d38eacd9`  
		Last Modified: Wed, 05 Jun 2024 07:33:26 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4`

```console
$ docker pull kong@sha256:6dd27da5c4ef60b7dd8041474636dd4b16ca0619926886d7268e0cb737eaa6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.4` - linux; amd64

```console
$ docker pull kong@sha256:eabe04c11acecb5a45ed2d2e235e133b8cce4b57eb274766ea35bf6f15533aee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b647b495d1191b1c6660bfafc5fc121f5868115f27d5a2b1dde7b986e01f015`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:42:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Mar 2024 08:42:20 GMT
ARG ASSET=ce
# Sat, 16 Mar 2024 08:42:20 GMT
ENV ASSET=ce
# Sat, 16 Mar 2024 08:42:20 GMT
ARG EE_PORTS
# Sat, 16 Mar 2024 08:42:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 08:42:20 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 16 Mar 2024 08:42:28 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Mar 2024 08:42:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Mar 2024 08:42:28 GMT
USER kong
# Sat, 16 Mar 2024 08:42:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:42:28 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Mar 2024 08:42:29 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 08:42:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Mar 2024 08:42:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473c07a218a4949e46dab18b8e41402a9330a692cfaeae43f320bfd607707009`  
		Last Modified: Sat, 16 Mar 2024 08:43:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218b46ec42b4988ef080ec0eed5ad36371aa259ef900eefa8f01309d03449d84`  
		Last Modified: Sat, 16 Mar 2024 08:43:11 GMT  
		Size: 44.7 MB (44716900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902d83c366d3225163eec0a9ad89a1841fd4791ece418094c908ff1f1badf853`  
		Last Modified: Sat, 16 Mar 2024 08:43:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4-alpine`

```console
$ docker pull kong@sha256:6dd27da5c4ef60b7dd8041474636dd4b16ca0619926886d7268e0cb737eaa6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:eabe04c11acecb5a45ed2d2e235e133b8cce4b57eb274766ea35bf6f15533aee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48120451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b647b495d1191b1c6660bfafc5fc121f5868115f27d5a2b1dde7b986e01f015`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:42:20 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Mar 2024 08:42:20 GMT
ARG ASSET=ce
# Sat, 16 Mar 2024 08:42:20 GMT
ENV ASSET=ce
# Sat, 16 Mar 2024 08:42:20 GMT
ARG EE_PORTS
# Sat, 16 Mar 2024 08:42:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 08:42:20 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 16 Mar 2024 08:42:20 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 16 Mar 2024 08:42:28 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Mar 2024 08:42:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Mar 2024 08:42:28 GMT
USER kong
# Sat, 16 Mar 2024 08:42:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:42:28 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Mar 2024 08:42:29 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 08:42:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Mar 2024 08:42:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473c07a218a4949e46dab18b8e41402a9330a692cfaeae43f320bfd607707009`  
		Last Modified: Sat, 16 Mar 2024 08:43:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218b46ec42b4988ef080ec0eed5ad36371aa259ef900eefa8f01309d03449d84`  
		Last Modified: Sat, 16 Mar 2024 08:43:11 GMT  
		Size: 44.7 MB (44716900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902d83c366d3225163eec0a9ad89a1841fd4791ece418094c908ff1f1badf853`  
		Last Modified: Sat, 16 Mar 2024 08:43:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4-ubuntu`

```console
$ docker pull kong@sha256:cbb4ef7bc95c9f497341d2c4fb99bf7450d5e283c87e6fe7389a48919b514f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:efcf9c410ff84a727f8e0a796d09b19e4b45bbfe20e9795e68f8d0aac9b6ca9f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116549388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc55722a4595026505e6c990c2429c6f67f77fda76ab41895b2ad5fb3193d46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:31:10 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:31:10 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:31:10 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:31:10 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:31:10 GMT
ARG KONG_VERSION=2.8.4
# Wed, 05 Jun 2024 07:31:10 GMT
ENV KONG_VERSION=2.8.4
# Wed, 05 Jun 2024 07:31:11 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Wed, 05 Jun 2024 07:31:11 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Wed, 05 Jun 2024 07:31:39 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:31:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:31:40 GMT
USER kong
# Wed, 05 Jun 2024 07:31:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:31:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:31:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:31:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:31:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e7c2ea5c74c56b2204aa68af2405c00aff3f9ebd18fedf2592e897777c48a7`  
		Last Modified: Wed, 05 Jun 2024 07:33:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d41bde6bb16c1c697fcd2be7adb5a880a6b4064d1f604dbe753c5af23c3fd3`  
		Last Modified: Wed, 05 Jun 2024 07:33:36 GMT  
		Size: 61.0 MB (61027273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f7c3c9272055868997065e093a269efd8498d6e7eaf430dc65ef92d38eacd9`  
		Last Modified: Wed, 05 Jun 2024 07:33:26 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:97d11d733e672f595741c8fc960f14a39dd3b13fdaad265de08d652f88eb5bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:3f28edf0884ce7546b4ed94ddc08afc6eb3c2efa20ca5986c1ccd2452c9c71ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98167820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af51126fa339261f64d1ea93f52437c5ceb167bf5d0468fcaba770e566f58f12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:29:38 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:29:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:29:39 GMT
USER kong
# Wed, 05 Jun 2024 07:29:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:29:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:29:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:29:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:29:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcffa07bff0143c0d9ad661c0f5226ac86a339a5f39c5c603e5ce6ac78de2ec`  
		Last Modified: Wed, 05 Jun 2024 07:32:08 GMT  
		Size: 67.7 MB (67727251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52858b68207de97916df9417ba48dc4dcf30d50281a04bb5b1167d5ed15d4a4f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fce47e2300795cc221b7240e45636bda073bcd5d4d86a8caaa82ae665cb79e62
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96059455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e4192e756aceefd1145e195e472b6ca5b3b0a444ece3fa5b2c187c4c76247`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:09:13 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:09:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:09:14 GMT
USER kong
# Wed, 05 Jun 2024 07:09:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:09:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:09:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:09:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:09:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4420256d090d6d8707889b04ce276526622caac72ba31ad93132bd61bed57`  
		Last Modified: Wed, 05 Jun 2024 07:11:45 GMT  
		Size: 67.7 MB (67655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a41a1d7a093c16efdfe0884d405ec2facb9c315388d52aceca99a4d068b9f39`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4`

```console
$ docker pull kong@sha256:70f98f0d048c9d5f98c43c5fe4d2b916be27d774a0443b9e701c646dcb3ca4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:5f968967b941c60ef3143910ef26f78811fdbc79f19c7b10ee418d760ffd29e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794afc90787cfc3dad640b2a5b8f85b1835dd3f1649fca3e16aae0b99be9b123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:22:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:22:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:22:09 GMT
USER kong
# Sat, 15 Jun 2024 00:22:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:22:10 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a347fe47d68ffa81beab3d274caae8aab610627f58a546a75198efb9c11e070`  
		Last Modified: Sat, 15 Jun 2024 00:23:27 GMT  
		Size: 62.7 MB (62748133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61b3f40e2db198262e6bb9c1c6173fba253605c983cfa6dbbfd6285c26ac7b`  
		Last Modified: Sat, 15 Jun 2024 00:23:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bc2432c1fc70478be156c49eb2f3af1d6b686023e16e572056a6189ccf1d5abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89575599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c6f42ebe0af9280ccbda442f8ee1b6292c1766bcaedd4380d74732b567a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:41:14 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:41:15 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:41:15 GMT
USER kong
# Sat, 15 Jun 2024 00:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:41:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:41:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:41:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:41:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb5026d472701f71e6f3fb94dfb5d03622f307df72949ebd53d94984938e856`  
		Last Modified: Sat, 15 Jun 2024 00:42:18 GMT  
		Size: 61.2 MB (61172007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb5dd4a808f942e8072e8be104ee1a94133b3f1d4c667a1386f558b8a6ddd4`  
		Last Modified: Sat, 15 Jun 2024 00:42:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:70f98f0d048c9d5f98c43c5fe4d2b916be27d774a0443b9e701c646dcb3ca4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5f968967b941c60ef3143910ef26f78811fdbc79f19c7b10ee418d760ffd29e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794afc90787cfc3dad640b2a5b8f85b1835dd3f1649fca3e16aae0b99be9b123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:22:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:22:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:22:09 GMT
USER kong
# Sat, 15 Jun 2024 00:22:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:22:10 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a347fe47d68ffa81beab3d274caae8aab610627f58a546a75198efb9c11e070`  
		Last Modified: Sat, 15 Jun 2024 00:23:27 GMT  
		Size: 62.7 MB (62748133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61b3f40e2db198262e6bb9c1c6173fba253605c983cfa6dbbfd6285c26ac7b`  
		Last Modified: Sat, 15 Jun 2024 00:23:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bc2432c1fc70478be156c49eb2f3af1d6b686023e16e572056a6189ccf1d5abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89575599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c6f42ebe0af9280ccbda442f8ee1b6292c1766bcaedd4380d74732b567a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:41:14 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:41:15 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:41:15 GMT
USER kong
# Sat, 15 Jun 2024 00:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:41:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:41:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:41:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:41:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb5026d472701f71e6f3fb94dfb5d03622f307df72949ebd53d94984938e856`  
		Last Modified: Sat, 15 Jun 2024 00:42:18 GMT  
		Size: 61.2 MB (61172007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb5dd4a808f942e8072e8be104ee1a94133b3f1d4c667a1386f558b8a6ddd4`  
		Last Modified: Sat, 15 Jun 2024 00:42:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2`

```console
$ docker pull kong@sha256:70f98f0d048c9d5f98c43c5fe4d2b916be27d774a0443b9e701c646dcb3ca4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:5f968967b941c60ef3143910ef26f78811fdbc79f19c7b10ee418d760ffd29e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794afc90787cfc3dad640b2a5b8f85b1835dd3f1649fca3e16aae0b99be9b123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:22:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:22:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:22:09 GMT
USER kong
# Sat, 15 Jun 2024 00:22:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:22:10 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a347fe47d68ffa81beab3d274caae8aab610627f58a546a75198efb9c11e070`  
		Last Modified: Sat, 15 Jun 2024 00:23:27 GMT  
		Size: 62.7 MB (62748133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61b3f40e2db198262e6bb9c1c6173fba253605c983cfa6dbbfd6285c26ac7b`  
		Last Modified: Sat, 15 Jun 2024 00:23:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bc2432c1fc70478be156c49eb2f3af1d6b686023e16e572056a6189ccf1d5abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89575599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c6f42ebe0af9280ccbda442f8ee1b6292c1766bcaedd4380d74732b567a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:41:14 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:41:15 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:41:15 GMT
USER kong
# Sat, 15 Jun 2024 00:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:41:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:41:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:41:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:41:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb5026d472701f71e6f3fb94dfb5d03622f307df72949ebd53d94984938e856`  
		Last Modified: Sat, 15 Jun 2024 00:42:18 GMT  
		Size: 61.2 MB (61172007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb5dd4a808f942e8072e8be104ee1a94133b3f1d4c667a1386f558b8a6ddd4`  
		Last Modified: Sat, 15 Jun 2024 00:42:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:70f98f0d048c9d5f98c43c5fe4d2b916be27d774a0443b9e701c646dcb3ca4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5f968967b941c60ef3143910ef26f78811fdbc79f19c7b10ee418d760ffd29e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794afc90787cfc3dad640b2a5b8f85b1835dd3f1649fca3e16aae0b99be9b123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:22:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:22:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:22:09 GMT
USER kong
# Sat, 15 Jun 2024 00:22:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:22:10 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a347fe47d68ffa81beab3d274caae8aab610627f58a546a75198efb9c11e070`  
		Last Modified: Sat, 15 Jun 2024 00:23:27 GMT  
		Size: 62.7 MB (62748133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61b3f40e2db198262e6bb9c1c6173fba253605c983cfa6dbbfd6285c26ac7b`  
		Last Modified: Sat, 15 Jun 2024 00:23:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bc2432c1fc70478be156c49eb2f3af1d6b686023e16e572056a6189ccf1d5abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89575599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c6f42ebe0af9280ccbda442f8ee1b6292c1766bcaedd4380d74732b567a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:41:14 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:41:15 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:41:15 GMT
USER kong
# Sat, 15 Jun 2024 00:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:41:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:41:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:41:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:41:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb5026d472701f71e6f3fb94dfb5d03622f307df72949ebd53d94984938e856`  
		Last Modified: Sat, 15 Jun 2024 00:42:18 GMT  
		Size: 61.2 MB (61172007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb5dd4a808f942e8072e8be104ee1a94133b3f1d4c667a1386f558b8a6ddd4`  
		Last Modified: Sat, 15 Jun 2024 00:42:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5`

```console
$ docker pull kong@sha256:80695162a49f52a7f3284e11c86226b966c627c979b966ad4d12abad46efcb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5` - linux; amd64

```console
$ docker pull kong@sha256:9411fd86123391795f79d80f37dda9b14e769fd2800e9dc72d98359a3d66f9c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b605def7c3fee50f8798d6ad6d7bd1e852c0232a1eff8ca2249be020714a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:21:41 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:41 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:42 GMT
USER kong
# Sat, 15 Jun 2024 00:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:42 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8916e7036bb7e051f8b6c6f87ea74e5047cad1d9ca82626533470537f807cc8`  
		Last Modified: Sat, 15 Jun 2024 00:23:07 GMT  
		Size: 64.0 MB (63964608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9249b03ce187d409b282fd06a99e1a0eb8eea969209b029d5d9240c42228102c`  
		Last Modified: Sat, 15 Jun 2024 00:22:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e5e5b678f64a3dd2e8d10244195adaa1237b46b8a07f6bc133ae358539572d4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7271c81a1a45e919c608e0de23466b110af5284cf913d31a7b6fc71dc6854b7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:40:47 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:48 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:48 GMT
USER kong
# Sat, 15 Jun 2024 00:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:48 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f60e3de80db16b864444f80b19cc87ca2470443506ed93968cc66678762d2d`  
		Last Modified: Sat, 15 Jun 2024 00:41:59 GMT  
		Size: 63.5 MB (63484296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed3435482ab32691718553e82af2f33d52a726bb73bd0ba6f5eff665364ed2`  
		Last Modified: Sat, 15 Jun 2024 00:41:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5-ubuntu`

```console
$ docker pull kong@sha256:80695162a49f52a7f3284e11c86226b966c627c979b966ad4d12abad46efcb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9411fd86123391795f79d80f37dda9b14e769fd2800e9dc72d98359a3d66f9c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b605def7c3fee50f8798d6ad6d7bd1e852c0232a1eff8ca2249be020714a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:21:41 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:41 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:42 GMT
USER kong
# Sat, 15 Jun 2024 00:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:42 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8916e7036bb7e051f8b6c6f87ea74e5047cad1d9ca82626533470537f807cc8`  
		Last Modified: Sat, 15 Jun 2024 00:23:07 GMT  
		Size: 64.0 MB (63964608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9249b03ce187d409b282fd06a99e1a0eb8eea969209b029d5d9240c42228102c`  
		Last Modified: Sat, 15 Jun 2024 00:22:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e5e5b678f64a3dd2e8d10244195adaa1237b46b8a07f6bc133ae358539572d4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7271c81a1a45e919c608e0de23466b110af5284cf913d31a7b6fc71dc6854b7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:40:47 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:48 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:48 GMT
USER kong
# Sat, 15 Jun 2024 00:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:48 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f60e3de80db16b864444f80b19cc87ca2470443506ed93968cc66678762d2d`  
		Last Modified: Sat, 15 Jun 2024 00:41:59 GMT  
		Size: 63.5 MB (63484296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed3435482ab32691718553e82af2f33d52a726bb73bd0ba6f5eff665364ed2`  
		Last Modified: Sat, 15 Jun 2024 00:41:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0`

```console
$ docker pull kong@sha256:80695162a49f52a7f3284e11c86226b966c627c979b966ad4d12abad46efcb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0` - linux; amd64

```console
$ docker pull kong@sha256:9411fd86123391795f79d80f37dda9b14e769fd2800e9dc72d98359a3d66f9c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b605def7c3fee50f8798d6ad6d7bd1e852c0232a1eff8ca2249be020714a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:21:41 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:41 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:42 GMT
USER kong
# Sat, 15 Jun 2024 00:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:42 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8916e7036bb7e051f8b6c6f87ea74e5047cad1d9ca82626533470537f807cc8`  
		Last Modified: Sat, 15 Jun 2024 00:23:07 GMT  
		Size: 64.0 MB (63964608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9249b03ce187d409b282fd06a99e1a0eb8eea969209b029d5d9240c42228102c`  
		Last Modified: Sat, 15 Jun 2024 00:22:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e5e5b678f64a3dd2e8d10244195adaa1237b46b8a07f6bc133ae358539572d4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7271c81a1a45e919c608e0de23466b110af5284cf913d31a7b6fc71dc6854b7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:40:47 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:48 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:48 GMT
USER kong
# Sat, 15 Jun 2024 00:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:48 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f60e3de80db16b864444f80b19cc87ca2470443506ed93968cc66678762d2d`  
		Last Modified: Sat, 15 Jun 2024 00:41:59 GMT  
		Size: 63.5 MB (63484296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed3435482ab32691718553e82af2f33d52a726bb73bd0ba6f5eff665364ed2`  
		Last Modified: Sat, 15 Jun 2024 00:41:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0-ubuntu`

```console
$ docker pull kong@sha256:80695162a49f52a7f3284e11c86226b966c627c979b966ad4d12abad46efcb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9411fd86123391795f79d80f37dda9b14e769fd2800e9dc72d98359a3d66f9c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b605def7c3fee50f8798d6ad6d7bd1e852c0232a1eff8ca2249be020714a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:21:41 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:41 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:42 GMT
USER kong
# Sat, 15 Jun 2024 00:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:42 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8916e7036bb7e051f8b6c6f87ea74e5047cad1d9ca82626533470537f807cc8`  
		Last Modified: Sat, 15 Jun 2024 00:23:07 GMT  
		Size: 64.0 MB (63964608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9249b03ce187d409b282fd06a99e1a0eb8eea969209b029d5d9240c42228102c`  
		Last Modified: Sat, 15 Jun 2024 00:22:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e5e5b678f64a3dd2e8d10244195adaa1237b46b8a07f6bc133ae358539572d4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7271c81a1a45e919c608e0de23466b110af5284cf913d31a7b6fc71dc6854b7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:40:47 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:48 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:48 GMT
USER kong
# Sat, 15 Jun 2024 00:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:48 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f60e3de80db16b864444f80b19cc87ca2470443506ed93968cc66678762d2d`  
		Last Modified: Sat, 15 Jun 2024 00:41:59 GMT  
		Size: 63.5 MB (63484296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed3435482ab32691718553e82af2f33d52a726bb73bd0ba6f5eff665364ed2`  
		Last Modified: Sat, 15 Jun 2024 00:41:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6`

```console
$ docker pull kong@sha256:a3d2c8699f5e864c916187424153b93135c2b4add8548e7675432bc53fd61807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6` - linux; amd64

```console
$ docker pull kong@sha256:aefc3b35390452620d257ac2dfa0a81133ae6d0f4c5abfc5df9cefe2417b1245
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b61bee6996c212d86bec55a46011d8dcd051c98ede6d5b64e8e17be28ab0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:21:16 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:17 GMT
USER kong
# Sat, 15 Jun 2024 00:21:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9750302f66dbbd904d68dc009bd096ae1e295fbcc60c062fca374ea83cb8d`  
		Last Modified: Sat, 15 Jun 2024 00:22:47 GMT  
		Size: 67.7 MB (67676065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395a55bfda51337af1c0622d33c891e9903f19de2dc2f4e50a960d5ce097fa`  
		Last Modified: Sat, 15 Jun 2024 00:22:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e388fdd07ab562a159e861687e7b61a2bf312175fd97cd9787070bf59808efee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95633709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77420d480b60404df779c63c7a33f101b72698933492269a17ec75717a5e0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:40:17 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:19 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:19 GMT
USER kong
# Sat, 15 Jun 2024 00:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:19 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f099f0061884274828d95293909d9c908211fbd97b94ca687f3311c80d0a59`  
		Last Modified: Sat, 15 Jun 2024 00:41:40 GMT  
		Size: 67.2 MB (67230117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdd9430c73a732aa248c466dff075f60e0673d76b5a7af2e7675c1f3a90669`  
		Last Modified: Sat, 15 Jun 2024 00:41:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:a3d2c8699f5e864c916187424153b93135c2b4add8548e7675432bc53fd61807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:aefc3b35390452620d257ac2dfa0a81133ae6d0f4c5abfc5df9cefe2417b1245
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b61bee6996c212d86bec55a46011d8dcd051c98ede6d5b64e8e17be28ab0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:21:16 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:17 GMT
USER kong
# Sat, 15 Jun 2024 00:21:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9750302f66dbbd904d68dc009bd096ae1e295fbcc60c062fca374ea83cb8d`  
		Last Modified: Sat, 15 Jun 2024 00:22:47 GMT  
		Size: 67.7 MB (67676065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395a55bfda51337af1c0622d33c891e9903f19de2dc2f4e50a960d5ce097fa`  
		Last Modified: Sat, 15 Jun 2024 00:22:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e388fdd07ab562a159e861687e7b61a2bf312175fd97cd9787070bf59808efee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95633709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77420d480b60404df779c63c7a33f101b72698933492269a17ec75717a5e0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:40:17 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:19 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:19 GMT
USER kong
# Sat, 15 Jun 2024 00:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:19 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f099f0061884274828d95293909d9c908211fbd97b94ca687f3311c80d0a59`  
		Last Modified: Sat, 15 Jun 2024 00:41:40 GMT  
		Size: 67.2 MB (67230117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdd9430c73a732aa248c466dff075f60e0673d76b5a7af2e7675c1f3a90669`  
		Last Modified: Sat, 15 Jun 2024 00:41:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1`

```console
$ docker pull kong@sha256:a3d2c8699f5e864c916187424153b93135c2b4add8548e7675432bc53fd61807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6.1` - linux; amd64

```console
$ docker pull kong@sha256:aefc3b35390452620d257ac2dfa0a81133ae6d0f4c5abfc5df9cefe2417b1245
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b61bee6996c212d86bec55a46011d8dcd051c98ede6d5b64e8e17be28ab0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:21:16 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:17 GMT
USER kong
# Sat, 15 Jun 2024 00:21:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9750302f66dbbd904d68dc009bd096ae1e295fbcc60c062fca374ea83cb8d`  
		Last Modified: Sat, 15 Jun 2024 00:22:47 GMT  
		Size: 67.7 MB (67676065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395a55bfda51337af1c0622d33c891e9903f19de2dc2f4e50a960d5ce097fa`  
		Last Modified: Sat, 15 Jun 2024 00:22:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e388fdd07ab562a159e861687e7b61a2bf312175fd97cd9787070bf59808efee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95633709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77420d480b60404df779c63c7a33f101b72698933492269a17ec75717a5e0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:40:17 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:19 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:19 GMT
USER kong
# Sat, 15 Jun 2024 00:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:19 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f099f0061884274828d95293909d9c908211fbd97b94ca687f3311c80d0a59`  
		Last Modified: Sat, 15 Jun 2024 00:41:40 GMT  
		Size: 67.2 MB (67230117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdd9430c73a732aa248c466dff075f60e0673d76b5a7af2e7675c1f3a90669`  
		Last Modified: Sat, 15 Jun 2024 00:41:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:a3d2c8699f5e864c916187424153b93135c2b4add8548e7675432bc53fd61807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:aefc3b35390452620d257ac2dfa0a81133ae6d0f4c5abfc5df9cefe2417b1245
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b61bee6996c212d86bec55a46011d8dcd051c98ede6d5b64e8e17be28ab0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:21:16 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:17 GMT
USER kong
# Sat, 15 Jun 2024 00:21:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9750302f66dbbd904d68dc009bd096ae1e295fbcc60c062fca374ea83cb8d`  
		Last Modified: Sat, 15 Jun 2024 00:22:47 GMT  
		Size: 67.7 MB (67676065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395a55bfda51337af1c0622d33c891e9903f19de2dc2f4e50a960d5ce097fa`  
		Last Modified: Sat, 15 Jun 2024 00:22:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e388fdd07ab562a159e861687e7b61a2bf312175fd97cd9787070bf59808efee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95633709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77420d480b60404df779c63c7a33f101b72698933492269a17ec75717a5e0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:40:17 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:19 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:19 GMT
USER kong
# Sat, 15 Jun 2024 00:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:19 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f099f0061884274828d95293909d9c908211fbd97b94ca687f3311c80d0a59`  
		Last Modified: Sat, 15 Jun 2024 00:41:40 GMT  
		Size: 67.2 MB (67230117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdd9430c73a732aa248c466dff075f60e0673d76b5a7af2e7675c1f3a90669`  
		Last Modified: Sat, 15 Jun 2024 00:41:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.7`

```console
$ docker pull kong@sha256:97d11d733e672f595741c8fc960f14a39dd3b13fdaad265de08d652f88eb5bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.7` - linux; amd64

```console
$ docker pull kong@sha256:3f28edf0884ce7546b4ed94ddc08afc6eb3c2efa20ca5986c1ccd2452c9c71ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98167820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af51126fa339261f64d1ea93f52437c5ceb167bf5d0468fcaba770e566f58f12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:29:38 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:29:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:29:39 GMT
USER kong
# Wed, 05 Jun 2024 07:29:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:29:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:29:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:29:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:29:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcffa07bff0143c0d9ad661c0f5226ac86a339a5f39c5c603e5ce6ac78de2ec`  
		Last Modified: Wed, 05 Jun 2024 07:32:08 GMT  
		Size: 67.7 MB (67727251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52858b68207de97916df9417ba48dc4dcf30d50281a04bb5b1167d5ed15d4a4f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fce47e2300795cc221b7240e45636bda073bcd5d4d86a8caaa82ae665cb79e62
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96059455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e4192e756aceefd1145e195e472b6ca5b3b0a444ece3fa5b2c187c4c76247`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:09:13 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:09:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:09:14 GMT
USER kong
# Wed, 05 Jun 2024 07:09:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:09:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:09:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:09:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:09:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4420256d090d6d8707889b04ce276526622caac72ba31ad93132bd61bed57`  
		Last Modified: Wed, 05 Jun 2024 07:11:45 GMT  
		Size: 67.7 MB (67655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a41a1d7a093c16efdfe0884d405ec2facb9c315388d52aceca99a4d068b9f39`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.7-ubuntu`

```console
$ docker pull kong@sha256:97d11d733e672f595741c8fc960f14a39dd3b13fdaad265de08d652f88eb5bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3f28edf0884ce7546b4ed94ddc08afc6eb3c2efa20ca5986c1ccd2452c9c71ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98167820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af51126fa339261f64d1ea93f52437c5ceb167bf5d0468fcaba770e566f58f12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:29:38 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:29:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:29:39 GMT
USER kong
# Wed, 05 Jun 2024 07:29:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:29:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:29:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:29:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:29:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcffa07bff0143c0d9ad661c0f5226ac86a339a5f39c5c603e5ce6ac78de2ec`  
		Last Modified: Wed, 05 Jun 2024 07:32:08 GMT  
		Size: 67.7 MB (67727251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52858b68207de97916df9417ba48dc4dcf30d50281a04bb5b1167d5ed15d4a4f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fce47e2300795cc221b7240e45636bda073bcd5d4d86a8caaa82ae665cb79e62
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96059455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e4192e756aceefd1145e195e472b6ca5b3b0a444ece3fa5b2c187c4c76247`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:09:13 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:09:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:09:14 GMT
USER kong
# Wed, 05 Jun 2024 07:09:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:09:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:09:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:09:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:09:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4420256d090d6d8707889b04ce276526622caac72ba31ad93132bd61bed57`  
		Last Modified: Wed, 05 Jun 2024 07:11:45 GMT  
		Size: 67.7 MB (67655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a41a1d7a093c16efdfe0884d405ec2facb9c315388d52aceca99a4d068b9f39`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.7.0`

```console
$ docker pull kong@sha256:97d11d733e672f595741c8fc960f14a39dd3b13fdaad265de08d652f88eb5bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.7.0` - linux; amd64

```console
$ docker pull kong@sha256:3f28edf0884ce7546b4ed94ddc08afc6eb3c2efa20ca5986c1ccd2452c9c71ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98167820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af51126fa339261f64d1ea93f52437c5ceb167bf5d0468fcaba770e566f58f12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:29:38 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:29:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:29:39 GMT
USER kong
# Wed, 05 Jun 2024 07:29:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:29:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:29:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:29:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:29:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcffa07bff0143c0d9ad661c0f5226ac86a339a5f39c5c603e5ce6ac78de2ec`  
		Last Modified: Wed, 05 Jun 2024 07:32:08 GMT  
		Size: 67.7 MB (67727251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52858b68207de97916df9417ba48dc4dcf30d50281a04bb5b1167d5ed15d4a4f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.7.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fce47e2300795cc221b7240e45636bda073bcd5d4d86a8caaa82ae665cb79e62
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96059455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e4192e756aceefd1145e195e472b6ca5b3b0a444ece3fa5b2c187c4c76247`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:09:13 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:09:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:09:14 GMT
USER kong
# Wed, 05 Jun 2024 07:09:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:09:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:09:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:09:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:09:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4420256d090d6d8707889b04ce276526622caac72ba31ad93132bd61bed57`  
		Last Modified: Wed, 05 Jun 2024 07:11:45 GMT  
		Size: 67.7 MB (67655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a41a1d7a093c16efdfe0884d405ec2facb9c315388d52aceca99a4d068b9f39`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.7.0-ubuntu`

```console
$ docker pull kong@sha256:97d11d733e672f595741c8fc960f14a39dd3b13fdaad265de08d652f88eb5bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.7.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3f28edf0884ce7546b4ed94ddc08afc6eb3c2efa20ca5986c1ccd2452c9c71ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98167820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af51126fa339261f64d1ea93f52437c5ceb167bf5d0468fcaba770e566f58f12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:29:38 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:29:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:29:39 GMT
USER kong
# Wed, 05 Jun 2024 07:29:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:29:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:29:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:29:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:29:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcffa07bff0143c0d9ad661c0f5226ac86a339a5f39c5c603e5ce6ac78de2ec`  
		Last Modified: Wed, 05 Jun 2024 07:32:08 GMT  
		Size: 67.7 MB (67727251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52858b68207de97916df9417ba48dc4dcf30d50281a04bb5b1167d5ed15d4a4f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.7.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fce47e2300795cc221b7240e45636bda073bcd5d4d86a8caaa82ae665cb79e62
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96059455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e4192e756aceefd1145e195e472b6ca5b3b0a444ece3fa5b2c187c4c76247`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:09:13 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:09:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:09:14 GMT
USER kong
# Wed, 05 Jun 2024 07:09:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:09:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:09:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:09:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:09:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4420256d090d6d8707889b04ce276526622caac72ba31ad93132bd61bed57`  
		Last Modified: Wed, 05 Jun 2024 07:11:45 GMT  
		Size: 67.7 MB (67655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a41a1d7a093c16efdfe0884d405ec2facb9c315388d52aceca99a4d068b9f39`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:97d11d733e672f595741c8fc960f14a39dd3b13fdaad265de08d652f88eb5bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:3f28edf0884ce7546b4ed94ddc08afc6eb3c2efa20ca5986c1ccd2452c9c71ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98167820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af51126fa339261f64d1ea93f52437c5ceb167bf5d0468fcaba770e566f58f12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:29:38 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:29:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:29:39 GMT
USER kong
# Wed, 05 Jun 2024 07:29:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:29:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:29:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:29:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:29:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcffa07bff0143c0d9ad661c0f5226ac86a339a5f39c5c603e5ce6ac78de2ec`  
		Last Modified: Wed, 05 Jun 2024 07:32:08 GMT  
		Size: 67.7 MB (67727251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52858b68207de97916df9417ba48dc4dcf30d50281a04bb5b1167d5ed15d4a4f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fce47e2300795cc221b7240e45636bda073bcd5d4d86a8caaa82ae665cb79e62
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96059455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e4192e756aceefd1145e195e472b6ca5b3b0a444ece3fa5b2c187c4c76247`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:09:13 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:09:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:09:14 GMT
USER kong
# Wed, 05 Jun 2024 07:09:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:09:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:09:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:09:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:09:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4420256d090d6d8707889b04ce276526622caac72ba31ad93132bd61bed57`  
		Last Modified: Wed, 05 Jun 2024 07:11:45 GMT  
		Size: 67.7 MB (67655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a41a1d7a093c16efdfe0884d405ec2facb9c315388d52aceca99a4d068b9f39`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:97d11d733e672f595741c8fc960f14a39dd3b13fdaad265de08d652f88eb5bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3f28edf0884ce7546b4ed94ddc08afc6eb3c2efa20ca5986c1ccd2452c9c71ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98167820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af51126fa339261f64d1ea93f52437c5ceb167bf5d0468fcaba770e566f58f12`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:29:00 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:29:38 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:29:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:29:39 GMT
USER kong
# Wed, 05 Jun 2024 07:29:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:29:39 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:29:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:29:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:29:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcffa07bff0143c0d9ad661c0f5226ac86a339a5f39c5c603e5ce6ac78de2ec`  
		Last Modified: Wed, 05 Jun 2024 07:32:08 GMT  
		Size: 67.7 MB (67727251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52858b68207de97916df9417ba48dc4dcf30d50281a04bb5b1167d5ed15d4a4f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fce47e2300795cc221b7240e45636bda073bcd5d4d86a8caaa82ae665cb79e62
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96059455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18e4192e756aceefd1145e195e472b6ca5b3b0a444ece3fa5b2c187c4c76247`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ENV KONG_VERSION=3.7.0
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Wed, 05 Jun 2024 07:08:20 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Wed, 05 Jun 2024 07:09:13 GMT
# ARGS: KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 05 Jun 2024 07:09:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Wed, 05 Jun 2024 07:09:14 GMT
USER kong
# Wed, 05 Jun 2024 07:09:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Jun 2024 07:09:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 05 Jun 2024 07:09:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Jun 2024 07:09:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 05 Jun 2024 07:09:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf4420256d090d6d8707889b04ce276526622caac72ba31ad93132bd61bed57`  
		Last Modified: Wed, 05 Jun 2024 07:11:45 GMT  
		Size: 67.7 MB (67655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a41a1d7a093c16efdfe0884d405ec2facb9c315388d52aceca99a4d068b9f39`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
