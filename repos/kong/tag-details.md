<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.4`](#kong284)
-	[`kong:2.8.4-alpine`](#kong284-alpine)
-	[`kong:2.8.4-ubuntu`](#kong284-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.3`](#kong33)
-	[`kong:3.3-ubuntu`](#kong33-ubuntu)
-	[`kong:3.3.1`](#kong331)
-	[`kong:3.3.1-alpine`](#kong331-alpine)
-	[`kong:3.3.1-ubuntu`](#kong331-ubuntu)
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
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.8`

```console
$ docker pull kong@sha256:beae4144f5beab7a9eecb2633b5311436d8fe2060a817ae5c327619084a06a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

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

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5dd55a3b0c532cbac03084fa97eaebdecad6ae9fb764b3cdc1ac30b6c51a7f92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47435124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87daa865814959d55978568116846b6dca1b7f38203e8630431c692bc4b9ef9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:40:12 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Mar 2024 02:40:13 GMT
ARG ASSET=ce
# Sat, 16 Mar 2024 02:40:13 GMT
ENV ASSET=ce
# Sat, 16 Mar 2024 02:40:13 GMT
ARG EE_PORTS
# Sat, 16 Mar 2024 02:40:13 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 02:40:13 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 16 Mar 2024 02:40:20 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Mar 2024 02:40:21 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Mar 2024 02:40:21 GMT
USER kong
# Sat, 16 Mar 2024 02:40:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:40:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Mar 2024 02:40:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 02:40:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Mar 2024 02:40:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd612e99897c08d13de23a7514b2048d70b0bf41001ef688e6c17584d425d42`  
		Last Modified: Sat, 16 Mar 2024 02:40:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6256dd6da4aa6358e302dd1822bfd16be0e3b83fac10304d3424368649081f`  
		Last Modified: Sat, 16 Mar 2024 02:40:49 GMT  
		Size: 44.1 MB (44100750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2277ed6a7193813f932ed4e6dab978f365e7cf9a8dc1239f4aa9dc0cc30e504`  
		Last Modified: Sat, 16 Mar 2024 02:40:43 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:959c5f1410bdad783bf2bf036c6901bf8d7bea403f40b4c9d7104ec063e692a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c2c8590c37a75fc883baf4e4a652b3c3feed474de36baa9e04912c680fd3ed63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121733563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3f1194632f59221b66fdbdca4b640799d0f472e9a5836c1a77a959fd11836f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:05:07 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:05:07 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:05:07 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:05:08 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:05:08 GMT
ARG KONG_VERSION=2.8.4
# Thu, 25 Apr 2024 23:05:08 GMT
ENV KONG_VERSION=2.8.4
# Thu, 25 Apr 2024 23:05:08 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Thu, 25 Apr 2024 23:05:08 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 25 Apr 2024 23:05:31 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:05:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:05:32 GMT
USER kong
# Thu, 25 Apr 2024 23:05:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:05:32 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:05:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:05:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:05:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f965b9826a7b897a0fa9f7229a9e6e5ff772577c4b449fc2c313da476cd8443`  
		Last Modified: Thu, 25 Apr 2024 23:07:27 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6180e8af049ab9b2ab8842f8efb5e372bda7d3a7ed01f6375a77802f60adbe7d`  
		Last Modified: Thu, 25 Apr 2024 23:07:36 GMT  
		Size: 66.2 MB (66210984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26681bc803a7091fc434e6d57ab6a2328443b7c1fdc6fa32a58512f30736a27b`  
		Last Modified: Thu, 25 Apr 2024 23:07:26 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:70cfde244437af054bf25ca9c062025b042cabebd4ed2802af1308707d1b4bd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113129815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4665267771de296fdff281122935ed446b4ae0e5bb81adcba047e58769dffda4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:26:05 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:26:05 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:26:05 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:26:05 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 02 May 2024 01:26:05 GMT
ARG KONG_VERSION=2.8.4
# Thu, 02 May 2024 01:26:05 GMT
ENV KONG_VERSION=2.8.4
# Thu, 02 May 2024 01:26:05 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Thu, 02 May 2024 01:26:05 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 02 May 2024 01:26:23 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:26:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:26:24 GMT
USER kong
# Thu, 02 May 2024 01:26:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:26:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:26:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400fcf431cdd0a309a97a03537a8e1b880aeca7589ed4e4b33c4f55468086a37`  
		Last Modified: Thu, 02 May 2024 01:28:14 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714329caecbfd80224650bb71a381e9e15659c4990133f85eaf14e320ab0e3f`  
		Last Modified: Thu, 02 May 2024 01:28:20 GMT  
		Size: 59.6 MB (59645795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1ded874f6dfea4f15fbc0c5df30de1302d0e90758763b81a8eaf5bd10c7de5`  
		Last Modified: Thu, 02 May 2024 01:28:12 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4`

```console
$ docker pull kong@sha256:beae4144f5beab7a9eecb2633b5311436d8fe2060a817ae5c327619084a06a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

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

### `kong:2.8.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5dd55a3b0c532cbac03084fa97eaebdecad6ae9fb764b3cdc1ac30b6c51a7f92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47435124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87daa865814959d55978568116846b6dca1b7f38203e8630431c692bc4b9ef9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:40:12 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Mar 2024 02:40:13 GMT
ARG ASSET=ce
# Sat, 16 Mar 2024 02:40:13 GMT
ENV ASSET=ce
# Sat, 16 Mar 2024 02:40:13 GMT
ARG EE_PORTS
# Sat, 16 Mar 2024 02:40:13 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 02:40:13 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 16 Mar 2024 02:40:20 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Mar 2024 02:40:21 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Mar 2024 02:40:21 GMT
USER kong
# Sat, 16 Mar 2024 02:40:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:40:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Mar 2024 02:40:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 02:40:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Mar 2024 02:40:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd612e99897c08d13de23a7514b2048d70b0bf41001ef688e6c17584d425d42`  
		Last Modified: Sat, 16 Mar 2024 02:40:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6256dd6da4aa6358e302dd1822bfd16be0e3b83fac10304d3424368649081f`  
		Last Modified: Sat, 16 Mar 2024 02:40:49 GMT  
		Size: 44.1 MB (44100750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2277ed6a7193813f932ed4e6dab978f365e7cf9a8dc1239f4aa9dc0cc30e504`  
		Last Modified: Sat, 16 Mar 2024 02:40:43 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4-alpine`

```console
$ docker pull kong@sha256:beae4144f5beab7a9eecb2633b5311436d8fe2060a817ae5c327619084a06a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

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

### `kong:2.8.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5dd55a3b0c532cbac03084fa97eaebdecad6ae9fb764b3cdc1ac30b6c51a7f92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47435124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87daa865814959d55978568116846b6dca1b7f38203e8630431c692bc4b9ef9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:40:12 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Mar 2024 02:40:13 GMT
ARG ASSET=ce
# Sat, 16 Mar 2024 02:40:13 GMT
ENV ASSET=ce
# Sat, 16 Mar 2024 02:40:13 GMT
ARG EE_PORTS
# Sat, 16 Mar 2024 02:40:13 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 02:40:13 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 16 Mar 2024 02:40:13 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 16 Mar 2024 02:40:20 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Mar 2024 02:40:21 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Mar 2024 02:40:21 GMT
USER kong
# Sat, 16 Mar 2024 02:40:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 02:40:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Mar 2024 02:40:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 02:40:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Mar 2024 02:40:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd612e99897c08d13de23a7514b2048d70b0bf41001ef688e6c17584d425d42`  
		Last Modified: Sat, 16 Mar 2024 02:40:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6256dd6da4aa6358e302dd1822bfd16be0e3b83fac10304d3424368649081f`  
		Last Modified: Sat, 16 Mar 2024 02:40:49 GMT  
		Size: 44.1 MB (44100750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2277ed6a7193813f932ed4e6dab978f365e7cf9a8dc1239f4aa9dc0cc30e504`  
		Last Modified: Sat, 16 Mar 2024 02:40:43 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4-ubuntu`

```console
$ docker pull kong@sha256:959c5f1410bdad783bf2bf036c6901bf8d7bea403f40b4c9d7104ec063e692a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c2c8590c37a75fc883baf4e4a652b3c3feed474de36baa9e04912c680fd3ed63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121733563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3f1194632f59221b66fdbdca4b640799d0f472e9a5836c1a77a959fd11836f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:05:07 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:05:07 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:05:07 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:05:08 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:05:08 GMT
ARG KONG_VERSION=2.8.4
# Thu, 25 Apr 2024 23:05:08 GMT
ENV KONG_VERSION=2.8.4
# Thu, 25 Apr 2024 23:05:08 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Thu, 25 Apr 2024 23:05:08 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 25 Apr 2024 23:05:31 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:05:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:05:32 GMT
USER kong
# Thu, 25 Apr 2024 23:05:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:05:32 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:05:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:05:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:05:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f965b9826a7b897a0fa9f7229a9e6e5ff772577c4b449fc2c313da476cd8443`  
		Last Modified: Thu, 25 Apr 2024 23:07:27 GMT  
		Size: 25.1 MB (25081969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6180e8af049ab9b2ab8842f8efb5e372bda7d3a7ed01f6375a77802f60adbe7d`  
		Last Modified: Thu, 25 Apr 2024 23:07:36 GMT  
		Size: 66.2 MB (66210984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26681bc803a7091fc434e6d57ab6a2328443b7c1fdc6fa32a58512f30736a27b`  
		Last Modified: Thu, 25 Apr 2024 23:07:26 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:70cfde244437af054bf25ca9c062025b042cabebd4ed2802af1308707d1b4bd6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113129815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4665267771de296fdff281122935ed446b4ae0e5bb81adcba047e58769dffda4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:26:05 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:26:05 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:26:05 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:26:05 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 02 May 2024 01:26:05 GMT
ARG KONG_VERSION=2.8.4
# Thu, 02 May 2024 01:26:05 GMT
ENV KONG_VERSION=2.8.4
# Thu, 02 May 2024 01:26:05 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Thu, 02 May 2024 01:26:05 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 02 May 2024 01:26:23 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:26:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:26:24 GMT
USER kong
# Thu, 02 May 2024 01:26:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:26:25 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:26:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:400fcf431cdd0a309a97a03537a8e1b880aeca7589ed4e4b33c4f55468086a37`  
		Last Modified: Thu, 02 May 2024 01:28:14 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9714329caecbfd80224650bb71a381e9e15659c4990133f85eaf14e320ab0e3f`  
		Last Modified: Thu, 02 May 2024 01:28:20 GMT  
		Size: 59.6 MB (59645795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1ded874f6dfea4f15fbc0c5df30de1302d0e90758763b81a8eaf5bd10c7de5`  
		Last Modified: Thu, 02 May 2024 01:28:12 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:07c81639044917ee739866afe22e81bf5a73944aac1c9eed5a59653146eb0e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:b06c43f067744b3fea17f119dfd8f3cae2fe1585f453e7623fd1fe89dbe86153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98118447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89775cbb43bf90fc2a874f3513cda348f724fbd3bb2d016a5f5ccf12d9b41a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 23:03:22 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:23 GMT
USER kong
# Thu, 25 Apr 2024 23:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:23 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15d038661219aead062cbfe12ef045965ec47a102188bee4f46f8ec24d87bf8`  
		Last Modified: Thu, 25 Apr 2024 23:06:02 GMT  
		Size: 67.7 MB (67677437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30d9e2005833fd965cadbd43571f592dd170fa0304f6343cb6edac6de86e9d1`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3b1179164a713c5773ef13b0e57b6ad9d0ae1da5ac5c84cc84676a0074eb52c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95622839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b33961e8792f987ce3a992e698122ee016b00fd494efe745966668652631b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ENV KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 02 May 2024 01:24:50 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:24:51 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:24:51 GMT
USER kong
# Thu, 02 May 2024 01:24:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:24:52 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:24:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:24:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:24:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edf00e68b1a8acf31910e9ef6fa0430edfcc003b9e4578348c0c13911b5271`  
		Last Modified: Thu, 02 May 2024 01:26:52 GMT  
		Size: 67.2 MB (67220376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b0bbf4529f4a9a4796c92a413eda85fb76d553b20d535d0a9b319e9302f3ec`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3`

```console
$ docker pull kong@sha256:4419d48490a67b86b242f97724ae4a7a11be637fb5fdb1c060c6d28710ed0634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3` - linux; amd64

```console
$ docker pull kong@sha256:d315302fa03e61107a3f8d3ba9b92c1e78361b4bb9fca7f5a6a854ff6914cba0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86518437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95be70df20dc125d789a764d69bc16615cccb8abc7fb283eeaab9123707e7cc9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 23:04:23 GMT
ENV KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 25 Apr 2024 23:04:59 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:05:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:05:00 GMT
USER kong
# Thu, 25 Apr 2024 23:05:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:05:00 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:05:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:05:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:05:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b279498d2bc012390e69ac7da2e72bdca3bd304920ee6c12fc9c8e8b7e26a9d`  
		Last Modified: Thu, 25 Apr 2024 23:07:13 GMT  
		Size: 56.1 MB (56077424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9021e8e5f16ccc4a08f2675ee3c70349fb0c77e918f08bea0270a98b48bb9b`  
		Last Modified: Thu, 25 Apr 2024 23:07:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f91677527f6d8f1fa58b096b8133c09e4a0d7f747e780a04dd6b6b7118d4994e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75764368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f8e97362afe65fd92113b1d956f6e6bb5fff246fdf2df42e9aa64c409309d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_VERSION=3.3.1
# Thu, 02 May 2024 01:25:35 GMT
ENV KONG_VERSION=3.3.1
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 02 May 2024 01:25:59 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:26:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:26:00 GMT
USER kong
# Thu, 02 May 2024 01:26:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:26:00 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:26:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:26:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:26:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605f88e256de790f416dd59e6afa8e723b24b39d74ec4e5d5d41d249bed26c6e`  
		Last Modified: Thu, 02 May 2024 01:27:55 GMT  
		Size: 47.4 MB (47361903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2990338e0b55b3453adea618a47eec3168590c8480ea240ed234e25ca3e78e3e`  
		Last Modified: Thu, 02 May 2024 01:27:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3-ubuntu`

```console
$ docker pull kong@sha256:4419d48490a67b86b242f97724ae4a7a11be637fb5fdb1c060c6d28710ed0634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d315302fa03e61107a3f8d3ba9b92c1e78361b4bb9fca7f5a6a854ff6914cba0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86518437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95be70df20dc125d789a764d69bc16615cccb8abc7fb283eeaab9123707e7cc9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 23:04:23 GMT
ENV KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 25 Apr 2024 23:04:59 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:05:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:05:00 GMT
USER kong
# Thu, 25 Apr 2024 23:05:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:05:00 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:05:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:05:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:05:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b279498d2bc012390e69ac7da2e72bdca3bd304920ee6c12fc9c8e8b7e26a9d`  
		Last Modified: Thu, 25 Apr 2024 23:07:13 GMT  
		Size: 56.1 MB (56077424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9021e8e5f16ccc4a08f2675ee3c70349fb0c77e918f08bea0270a98b48bb9b`  
		Last Modified: Thu, 25 Apr 2024 23:07:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f91677527f6d8f1fa58b096b8133c09e4a0d7f747e780a04dd6b6b7118d4994e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75764368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f8e97362afe65fd92113b1d956f6e6bb5fff246fdf2df42e9aa64c409309d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_VERSION=3.3.1
# Thu, 02 May 2024 01:25:35 GMT
ENV KONG_VERSION=3.3.1
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 02 May 2024 01:25:59 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:26:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:26:00 GMT
USER kong
# Thu, 02 May 2024 01:26:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:26:00 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:26:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:26:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:26:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605f88e256de790f416dd59e6afa8e723b24b39d74ec4e5d5d41d249bed26c6e`  
		Last Modified: Thu, 02 May 2024 01:27:55 GMT  
		Size: 47.4 MB (47361903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2990338e0b55b3453adea618a47eec3168590c8480ea240ed234e25ca3e78e3e`  
		Last Modified: Thu, 02 May 2024 01:27:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1`

```console
$ docker pull kong@sha256:4419d48490a67b86b242f97724ae4a7a11be637fb5fdb1c060c6d28710ed0634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.1` - linux; amd64

```console
$ docker pull kong@sha256:d315302fa03e61107a3f8d3ba9b92c1e78361b4bb9fca7f5a6a854ff6914cba0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86518437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95be70df20dc125d789a764d69bc16615cccb8abc7fb283eeaab9123707e7cc9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 23:04:23 GMT
ENV KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 25 Apr 2024 23:04:59 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:05:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:05:00 GMT
USER kong
# Thu, 25 Apr 2024 23:05:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:05:00 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:05:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:05:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:05:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b279498d2bc012390e69ac7da2e72bdca3bd304920ee6c12fc9c8e8b7e26a9d`  
		Last Modified: Thu, 25 Apr 2024 23:07:13 GMT  
		Size: 56.1 MB (56077424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9021e8e5f16ccc4a08f2675ee3c70349fb0c77e918f08bea0270a98b48bb9b`  
		Last Modified: Thu, 25 Apr 2024 23:07:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f91677527f6d8f1fa58b096b8133c09e4a0d7f747e780a04dd6b6b7118d4994e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75764368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f8e97362afe65fd92113b1d956f6e6bb5fff246fdf2df42e9aa64c409309d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_VERSION=3.3.1
# Thu, 02 May 2024 01:25:35 GMT
ENV KONG_VERSION=3.3.1
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 02 May 2024 01:25:59 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:26:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:26:00 GMT
USER kong
# Thu, 02 May 2024 01:26:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:26:00 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:26:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:26:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:26:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605f88e256de790f416dd59e6afa8e723b24b39d74ec4e5d5d41d249bed26c6e`  
		Last Modified: Thu, 02 May 2024 01:27:55 GMT  
		Size: 47.4 MB (47361903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2990338e0b55b3453adea618a47eec3168590c8480ea240ed234e25ca3e78e3e`  
		Last Modified: Thu, 02 May 2024 01:27:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1-alpine`

```console
$ docker pull kong@sha256:db616c77a845adc44d0d4139b0f665dfee7d0a1106acc0f2e9bef657b6cb8a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:3.3.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:29b3b42cfdd96613c526254ac1f9e7cf148b688fbd68928f2eff4f6cc263e3d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34228489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55eb5e56db73ddd25c6628f90ed7ec93c12b231cf5e889114d44863d4f14848d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:42:07 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Mar 2024 08:42:07 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Mar 2024 08:42:07 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Mar 2024 08:42:07 GMT
ARG KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
# Sat, 16 Mar 2024 08:42:07 GMT
ARG KONG_PREFIX=/usr/local/kong
# Sat, 16 Mar 2024 08:42:07 GMT
ENV KONG_PREFIX=/usr/local/kong
# Sat, 16 Mar 2024 08:42:07 GMT
ARG ASSET=remote
# Sat, 16 Mar 2024 08:42:07 GMT
ARG EE_PORTS
# Sat, 16 Mar 2024 08:42:07 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 16 Mar 2024 08:42:13 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     KONG_SHA256=$KONG_AMD64_SHA ;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 16 Mar 2024 08:42:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Mar 2024 08:42:14 GMT
USER kong
# Sat, 16 Mar 2024 08:42:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:42:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Mar 2024 08:42:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 08:42:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Mar 2024 08:42:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced0f08c887f4c0d12a3033a6face09cdfa8c3c9a8d7ffdf93cad1325b750478`  
		Last Modified: Sat, 16 Mar 2024 08:42:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cf26a8164ca56a1ce1e3df3979ce10cd580120c2198afba909f94657d698c4`  
		Last Modified: Sat, 16 Mar 2024 08:42:56 GMT  
		Size: 30.8 MB (30847796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c95cd6fd96cb98f003a228e64e25e2bfea498848de9317a5b739e02f7fe2e`  
		Last Modified: Sat, 16 Mar 2024 08:42:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1-ubuntu`

```console
$ docker pull kong@sha256:4419d48490a67b86b242f97724ae4a7a11be637fb5fdb1c060c6d28710ed0634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d315302fa03e61107a3f8d3ba9b92c1e78361b4bb9fca7f5a6a854ff6914cba0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86518437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95be70df20dc125d789a764d69bc16615cccb8abc7fb283eeaab9123707e7cc9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 23:04:23 GMT
ENV KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 25 Apr 2024 23:04:23 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 25 Apr 2024 23:04:59 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:05:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:05:00 GMT
USER kong
# Thu, 25 Apr 2024 23:05:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:05:00 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:05:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:05:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:05:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b279498d2bc012390e69ac7da2e72bdca3bd304920ee6c12fc9c8e8b7e26a9d`  
		Last Modified: Thu, 25 Apr 2024 23:07:13 GMT  
		Size: 56.1 MB (56077424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9021e8e5f16ccc4a08f2675ee3c70349fb0c77e918f08bea0270a98b48bb9b`  
		Last Modified: Thu, 25 Apr 2024 23:07:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f91677527f6d8f1fa58b096b8133c09e4a0d7f747e780a04dd6b6b7118d4994e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75764368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f8e97362afe65fd92113b1d956f6e6bb5fff246fdf2df42e9aa64c409309d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_VERSION=3.3.1
# Thu, 02 May 2024 01:25:35 GMT
ENV KONG_VERSION=3.3.1
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 02 May 2024 01:25:35 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 02 May 2024 01:25:59 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:26:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:26:00 GMT
USER kong
# Thu, 02 May 2024 01:26:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:26:00 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:26:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:26:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:26:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605f88e256de790f416dd59e6afa8e723b24b39d74ec4e5d5d41d249bed26c6e`  
		Last Modified: Thu, 02 May 2024 01:27:55 GMT  
		Size: 47.4 MB (47361903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2990338e0b55b3453adea618a47eec3168590c8480ea240ed234e25ca3e78e3e`  
		Last Modified: Thu, 02 May 2024 01:27:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4`

```console
$ docker pull kong@sha256:f0b7b53464a2c76709b235d9d7f2fffa204a338b40be7e3f48111c5cecc279fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:e2417d4f5728e1651af79214ec496fa3a46524d2fb306ecfc4d3ffb1ce07f17f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98352216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8c6dc31ef72b531109097fb04289be7032ff01575f3df9890549f55cc7eaf6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 23:03:51 GMT
ENV KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 25 Apr 2024 23:04:12 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:04:13 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:04:13 GMT
USER kong
# Thu, 25 Apr 2024 23:04:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:04:13 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:04:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:04:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:04:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c1139367eea7e37bf4e6d023906ab515eb286197e2b3d89164a562bc812592`  
		Last Modified: Thu, 25 Apr 2024 23:06:51 GMT  
		Size: 67.9 MB (67911205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958bd61fe446181136e07f7c9adbd6f29f6bb36661020305f92d3a2032603210`  
		Last Modified: Thu, 25 Apr 2024 23:06:42 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:ffe430caaf316cb5c2bb62f1946ab69ba06f711b5fd17cbe4c1338244c0aa310
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89566423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e00605279072c5f793e5eb68048f9a59e43fcc5bfea6069c65b14053894a01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_VERSION=3.4.2
# Thu, 02 May 2024 01:25:15 GMT
ENV KONG_VERSION=3.4.2
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 02 May 2024 01:25:30 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:25:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:25:31 GMT
USER kong
# Thu, 02 May 2024 01:25:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:25:31 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:25:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:25:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:25:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9bad68b40dd15e80cbed4621a6e10d2cbc93a16a959ba30f1925dd6baa2c84`  
		Last Modified: Thu, 02 May 2024 01:27:37 GMT  
		Size: 61.2 MB (61163958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930b75b5dda900d15567bd0f1602f059c57ea2e389b2a1f5fb4f83384f8ef26`  
		Last Modified: Thu, 02 May 2024 01:27:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:f0b7b53464a2c76709b235d9d7f2fffa204a338b40be7e3f48111c5cecc279fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e2417d4f5728e1651af79214ec496fa3a46524d2fb306ecfc4d3ffb1ce07f17f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98352216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8c6dc31ef72b531109097fb04289be7032ff01575f3df9890549f55cc7eaf6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 23:03:51 GMT
ENV KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 25 Apr 2024 23:04:12 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:04:13 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:04:13 GMT
USER kong
# Thu, 25 Apr 2024 23:04:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:04:13 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:04:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:04:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:04:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c1139367eea7e37bf4e6d023906ab515eb286197e2b3d89164a562bc812592`  
		Last Modified: Thu, 25 Apr 2024 23:06:51 GMT  
		Size: 67.9 MB (67911205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958bd61fe446181136e07f7c9adbd6f29f6bb36661020305f92d3a2032603210`  
		Last Modified: Thu, 25 Apr 2024 23:06:42 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:ffe430caaf316cb5c2bb62f1946ab69ba06f711b5fd17cbe4c1338244c0aa310
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89566423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e00605279072c5f793e5eb68048f9a59e43fcc5bfea6069c65b14053894a01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_VERSION=3.4.2
# Thu, 02 May 2024 01:25:15 GMT
ENV KONG_VERSION=3.4.2
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 02 May 2024 01:25:30 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:25:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:25:31 GMT
USER kong
# Thu, 02 May 2024 01:25:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:25:31 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:25:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:25:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:25:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9bad68b40dd15e80cbed4621a6e10d2cbc93a16a959ba30f1925dd6baa2c84`  
		Last Modified: Thu, 02 May 2024 01:27:37 GMT  
		Size: 61.2 MB (61163958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930b75b5dda900d15567bd0f1602f059c57ea2e389b2a1f5fb4f83384f8ef26`  
		Last Modified: Thu, 02 May 2024 01:27:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2`

```console
$ docker pull kong@sha256:f0b7b53464a2c76709b235d9d7f2fffa204a338b40be7e3f48111c5cecc279fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:e2417d4f5728e1651af79214ec496fa3a46524d2fb306ecfc4d3ffb1ce07f17f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98352216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8c6dc31ef72b531109097fb04289be7032ff01575f3df9890549f55cc7eaf6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 23:03:51 GMT
ENV KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 25 Apr 2024 23:04:12 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:04:13 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:04:13 GMT
USER kong
# Thu, 25 Apr 2024 23:04:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:04:13 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:04:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:04:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:04:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c1139367eea7e37bf4e6d023906ab515eb286197e2b3d89164a562bc812592`  
		Last Modified: Thu, 25 Apr 2024 23:06:51 GMT  
		Size: 67.9 MB (67911205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958bd61fe446181136e07f7c9adbd6f29f6bb36661020305f92d3a2032603210`  
		Last Modified: Thu, 25 Apr 2024 23:06:42 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:ffe430caaf316cb5c2bb62f1946ab69ba06f711b5fd17cbe4c1338244c0aa310
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89566423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e00605279072c5f793e5eb68048f9a59e43fcc5bfea6069c65b14053894a01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_VERSION=3.4.2
# Thu, 02 May 2024 01:25:15 GMT
ENV KONG_VERSION=3.4.2
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 02 May 2024 01:25:30 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:25:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:25:31 GMT
USER kong
# Thu, 02 May 2024 01:25:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:25:31 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:25:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:25:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:25:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9bad68b40dd15e80cbed4621a6e10d2cbc93a16a959ba30f1925dd6baa2c84`  
		Last Modified: Thu, 02 May 2024 01:27:37 GMT  
		Size: 61.2 MB (61163958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930b75b5dda900d15567bd0f1602f059c57ea2e389b2a1f5fb4f83384f8ef26`  
		Last Modified: Thu, 02 May 2024 01:27:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:f0b7b53464a2c76709b235d9d7f2fffa204a338b40be7e3f48111c5cecc279fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e2417d4f5728e1651af79214ec496fa3a46524d2fb306ecfc4d3ffb1ce07f17f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98352216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8c6dc31ef72b531109097fb04289be7032ff01575f3df9890549f55cc7eaf6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 23:03:51 GMT
ENV KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 25 Apr 2024 23:03:51 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 25 Apr 2024 23:04:12 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:04:13 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:04:13 GMT
USER kong
# Thu, 25 Apr 2024 23:04:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:04:13 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:04:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:04:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:04:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c1139367eea7e37bf4e6d023906ab515eb286197e2b3d89164a562bc812592`  
		Last Modified: Thu, 25 Apr 2024 23:06:51 GMT  
		Size: 67.9 MB (67911205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958bd61fe446181136e07f7c9adbd6f29f6bb36661020305f92d3a2032603210`  
		Last Modified: Thu, 25 Apr 2024 23:06:42 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:ffe430caaf316cb5c2bb62f1946ab69ba06f711b5fd17cbe4c1338244c0aa310
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89566423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e00605279072c5f793e5eb68048f9a59e43fcc5bfea6069c65b14053894a01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_VERSION=3.4.2
# Thu, 02 May 2024 01:25:15 GMT
ENV KONG_VERSION=3.4.2
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 02 May 2024 01:25:15 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 02 May 2024 01:25:30 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:25:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:25:31 GMT
USER kong
# Thu, 02 May 2024 01:25:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:25:31 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:25:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:25:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:25:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9bad68b40dd15e80cbed4621a6e10d2cbc93a16a959ba30f1925dd6baa2c84`  
		Last Modified: Thu, 02 May 2024 01:27:37 GMT  
		Size: 61.2 MB (61163958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f930b75b5dda900d15567bd0f1602f059c57ea2e389b2a1f5fb4f83384f8ef26`  
		Last Modified: Thu, 02 May 2024 01:27:30 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5`

```console
$ docker pull kong@sha256:62cedb38252e587b8590160ff1c5a87b7b8d124f25ebdbd291ab3124182d3f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5` - linux; amd64

```console
$ docker pull kong@sha256:3c9eb61bd62653587731efb4f7f319896160d412fe4b90b736ef1f2797b49c48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94402700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dcb95b574be1a928d05ef738ae646501417d30d3179aece8706708759f4c87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:03:26 GMT
ARG KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 23:03:27 GMT
ENV KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 23:03:27 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 25 Apr 2024 23:03:27 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 25 Apr 2024 23:03:45 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:46 GMT
USER kong
# Thu, 25 Apr 2024 23:03:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:46 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ae69aa6fc58037b3c8f86414a7dfa712ad20bd289f94bed6ede560be71d43b`  
		Last Modified: Thu, 25 Apr 2024 23:06:30 GMT  
		Size: 64.0 MB (63961689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97385e3d61a5fb0e4ac9a7620237ea35e367b3bb8b2d9a6bf99d4ac1a8a9c045`  
		Last Modified: Thu, 25 Apr 2024 23:06:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9f654e14e0f29e3071771c463c4f5f2535c0d6e9f299c85f6777c0103c3a21c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91889073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bda56f737233e503190cc9f78fc93f91682ecb55adcae80fc8aac1b78ec6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_VERSION=3.5.0
# Thu, 02 May 2024 01:24:55 GMT
ENV KONG_VERSION=3.5.0
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 02 May 2024 01:25:10 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:25:11 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:25:11 GMT
USER kong
# Thu, 02 May 2024 01:25:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:25:11 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:25:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:25:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:25:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e435f0670b37ad1c0e55a485a80390ea761d5cff4bd6315ce45554e86dcfd7f`  
		Last Modified: Thu, 02 May 2024 01:27:19 GMT  
		Size: 63.5 MB (63486607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58ddea5352221d1267daaa84616a3adaf23876ce30b61cd0019406302f0d821`  
		Last Modified: Thu, 02 May 2024 01:27:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5-ubuntu`

```console
$ docker pull kong@sha256:62cedb38252e587b8590160ff1c5a87b7b8d124f25ebdbd291ab3124182d3f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3c9eb61bd62653587731efb4f7f319896160d412fe4b90b736ef1f2797b49c48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94402700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dcb95b574be1a928d05ef738ae646501417d30d3179aece8706708759f4c87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:03:26 GMT
ARG KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 23:03:27 GMT
ENV KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 23:03:27 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 25 Apr 2024 23:03:27 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 25 Apr 2024 23:03:45 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:46 GMT
USER kong
# Thu, 25 Apr 2024 23:03:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:46 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ae69aa6fc58037b3c8f86414a7dfa712ad20bd289f94bed6ede560be71d43b`  
		Last Modified: Thu, 25 Apr 2024 23:06:30 GMT  
		Size: 64.0 MB (63961689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97385e3d61a5fb0e4ac9a7620237ea35e367b3bb8b2d9a6bf99d4ac1a8a9c045`  
		Last Modified: Thu, 25 Apr 2024 23:06:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9f654e14e0f29e3071771c463c4f5f2535c0d6e9f299c85f6777c0103c3a21c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91889073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bda56f737233e503190cc9f78fc93f91682ecb55adcae80fc8aac1b78ec6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_VERSION=3.5.0
# Thu, 02 May 2024 01:24:55 GMT
ENV KONG_VERSION=3.5.0
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 02 May 2024 01:25:10 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:25:11 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:25:11 GMT
USER kong
# Thu, 02 May 2024 01:25:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:25:11 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:25:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:25:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:25:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e435f0670b37ad1c0e55a485a80390ea761d5cff4bd6315ce45554e86dcfd7f`  
		Last Modified: Thu, 02 May 2024 01:27:19 GMT  
		Size: 63.5 MB (63486607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58ddea5352221d1267daaa84616a3adaf23876ce30b61cd0019406302f0d821`  
		Last Modified: Thu, 02 May 2024 01:27:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0`

```console
$ docker pull kong@sha256:62cedb38252e587b8590160ff1c5a87b7b8d124f25ebdbd291ab3124182d3f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0` - linux; amd64

```console
$ docker pull kong@sha256:3c9eb61bd62653587731efb4f7f319896160d412fe4b90b736ef1f2797b49c48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94402700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dcb95b574be1a928d05ef738ae646501417d30d3179aece8706708759f4c87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:03:26 GMT
ARG KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 23:03:27 GMT
ENV KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 23:03:27 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 25 Apr 2024 23:03:27 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 25 Apr 2024 23:03:45 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:46 GMT
USER kong
# Thu, 25 Apr 2024 23:03:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:46 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ae69aa6fc58037b3c8f86414a7dfa712ad20bd289f94bed6ede560be71d43b`  
		Last Modified: Thu, 25 Apr 2024 23:06:30 GMT  
		Size: 64.0 MB (63961689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97385e3d61a5fb0e4ac9a7620237ea35e367b3bb8b2d9a6bf99d4ac1a8a9c045`  
		Last Modified: Thu, 25 Apr 2024 23:06:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9f654e14e0f29e3071771c463c4f5f2535c0d6e9f299c85f6777c0103c3a21c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91889073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bda56f737233e503190cc9f78fc93f91682ecb55adcae80fc8aac1b78ec6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_VERSION=3.5.0
# Thu, 02 May 2024 01:24:55 GMT
ENV KONG_VERSION=3.5.0
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 02 May 2024 01:25:10 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:25:11 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:25:11 GMT
USER kong
# Thu, 02 May 2024 01:25:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:25:11 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:25:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:25:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:25:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e435f0670b37ad1c0e55a485a80390ea761d5cff4bd6315ce45554e86dcfd7f`  
		Last Modified: Thu, 02 May 2024 01:27:19 GMT  
		Size: 63.5 MB (63486607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58ddea5352221d1267daaa84616a3adaf23876ce30b61cd0019406302f0d821`  
		Last Modified: Thu, 02 May 2024 01:27:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0-ubuntu`

```console
$ docker pull kong@sha256:62cedb38252e587b8590160ff1c5a87b7b8d124f25ebdbd291ab3124182d3f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3c9eb61bd62653587731efb4f7f319896160d412fe4b90b736ef1f2797b49c48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94402700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81dcb95b574be1a928d05ef738ae646501417d30d3179aece8706708759f4c87`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:03:26 GMT
ARG KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 23:03:27 GMT
ENV KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 23:03:27 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 25 Apr 2024 23:03:27 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 25 Apr 2024 23:03:45 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:46 GMT
USER kong
# Thu, 25 Apr 2024 23:03:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:46 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ae69aa6fc58037b3c8f86414a7dfa712ad20bd289f94bed6ede560be71d43b`  
		Last Modified: Thu, 25 Apr 2024 23:06:30 GMT  
		Size: 64.0 MB (63961689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97385e3d61a5fb0e4ac9a7620237ea35e367b3bb8b2d9a6bf99d4ac1a8a9c045`  
		Last Modified: Thu, 25 Apr 2024 23:06:20 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9f654e14e0f29e3071771c463c4f5f2535c0d6e9f299c85f6777c0103c3a21c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91889073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bda56f737233e503190cc9f78fc93f91682ecb55adcae80fc8aac1b78ec6d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_VERSION=3.5.0
# Thu, 02 May 2024 01:24:55 GMT
ENV KONG_VERSION=3.5.0
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 02 May 2024 01:24:55 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 02 May 2024 01:25:10 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:25:11 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:25:11 GMT
USER kong
# Thu, 02 May 2024 01:25:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:25:11 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:25:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:25:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:25:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e435f0670b37ad1c0e55a485a80390ea761d5cff4bd6315ce45554e86dcfd7f`  
		Last Modified: Thu, 02 May 2024 01:27:19 GMT  
		Size: 63.5 MB (63486607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58ddea5352221d1267daaa84616a3adaf23876ce30b61cd0019406302f0d821`  
		Last Modified: Thu, 02 May 2024 01:27:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6`

```console
$ docker pull kong@sha256:07c81639044917ee739866afe22e81bf5a73944aac1c9eed5a59653146eb0e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6` - linux; amd64

```console
$ docker pull kong@sha256:b06c43f067744b3fea17f119dfd8f3cae2fe1585f453e7623fd1fe89dbe86153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98118447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89775cbb43bf90fc2a874f3513cda348f724fbd3bb2d016a5f5ccf12d9b41a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 23:03:22 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:23 GMT
USER kong
# Thu, 25 Apr 2024 23:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:23 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15d038661219aead062cbfe12ef045965ec47a102188bee4f46f8ec24d87bf8`  
		Last Modified: Thu, 25 Apr 2024 23:06:02 GMT  
		Size: 67.7 MB (67677437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30d9e2005833fd965cadbd43571f592dd170fa0304f6343cb6edac6de86e9d1`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3b1179164a713c5773ef13b0e57b6ad9d0ae1da5ac5c84cc84676a0074eb52c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95622839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b33961e8792f987ce3a992e698122ee016b00fd494efe745966668652631b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ENV KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 02 May 2024 01:24:50 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:24:51 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:24:51 GMT
USER kong
# Thu, 02 May 2024 01:24:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:24:52 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:24:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:24:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:24:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edf00e68b1a8acf31910e9ef6fa0430edfcc003b9e4578348c0c13911b5271`  
		Last Modified: Thu, 02 May 2024 01:26:52 GMT  
		Size: 67.2 MB (67220376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b0bbf4529f4a9a4796c92a413eda85fb76d553b20d535d0a9b319e9302f3ec`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:07c81639044917ee739866afe22e81bf5a73944aac1c9eed5a59653146eb0e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b06c43f067744b3fea17f119dfd8f3cae2fe1585f453e7623fd1fe89dbe86153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98118447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89775cbb43bf90fc2a874f3513cda348f724fbd3bb2d016a5f5ccf12d9b41a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 23:03:22 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:23 GMT
USER kong
# Thu, 25 Apr 2024 23:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:23 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15d038661219aead062cbfe12ef045965ec47a102188bee4f46f8ec24d87bf8`  
		Last Modified: Thu, 25 Apr 2024 23:06:02 GMT  
		Size: 67.7 MB (67677437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30d9e2005833fd965cadbd43571f592dd170fa0304f6343cb6edac6de86e9d1`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3b1179164a713c5773ef13b0e57b6ad9d0ae1da5ac5c84cc84676a0074eb52c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95622839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b33961e8792f987ce3a992e698122ee016b00fd494efe745966668652631b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ENV KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 02 May 2024 01:24:50 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:24:51 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:24:51 GMT
USER kong
# Thu, 02 May 2024 01:24:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:24:52 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:24:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:24:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:24:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edf00e68b1a8acf31910e9ef6fa0430edfcc003b9e4578348c0c13911b5271`  
		Last Modified: Thu, 02 May 2024 01:26:52 GMT  
		Size: 67.2 MB (67220376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b0bbf4529f4a9a4796c92a413eda85fb76d553b20d535d0a9b319e9302f3ec`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1`

```console
$ docker pull kong@sha256:07c81639044917ee739866afe22e81bf5a73944aac1c9eed5a59653146eb0e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6.1` - linux; amd64

```console
$ docker pull kong@sha256:b06c43f067744b3fea17f119dfd8f3cae2fe1585f453e7623fd1fe89dbe86153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98118447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89775cbb43bf90fc2a874f3513cda348f724fbd3bb2d016a5f5ccf12d9b41a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 23:03:22 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:23 GMT
USER kong
# Thu, 25 Apr 2024 23:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:23 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15d038661219aead062cbfe12ef045965ec47a102188bee4f46f8ec24d87bf8`  
		Last Modified: Thu, 25 Apr 2024 23:06:02 GMT  
		Size: 67.7 MB (67677437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30d9e2005833fd965cadbd43571f592dd170fa0304f6343cb6edac6de86e9d1`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3b1179164a713c5773ef13b0e57b6ad9d0ae1da5ac5c84cc84676a0074eb52c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95622839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b33961e8792f987ce3a992e698122ee016b00fd494efe745966668652631b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ENV KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 02 May 2024 01:24:50 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:24:51 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:24:51 GMT
USER kong
# Thu, 02 May 2024 01:24:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:24:52 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:24:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:24:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:24:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edf00e68b1a8acf31910e9ef6fa0430edfcc003b9e4578348c0c13911b5271`  
		Last Modified: Thu, 02 May 2024 01:26:52 GMT  
		Size: 67.2 MB (67220376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b0bbf4529f4a9a4796c92a413eda85fb76d553b20d535d0a9b319e9302f3ec`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:07c81639044917ee739866afe22e81bf5a73944aac1c9eed5a59653146eb0e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b06c43f067744b3fea17f119dfd8f3cae2fe1585f453e7623fd1fe89dbe86153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98118447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89775cbb43bf90fc2a874f3513cda348f724fbd3bb2d016a5f5ccf12d9b41a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 23:03:22 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:23 GMT
USER kong
# Thu, 25 Apr 2024 23:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:23 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15d038661219aead062cbfe12ef045965ec47a102188bee4f46f8ec24d87bf8`  
		Last Modified: Thu, 25 Apr 2024 23:06:02 GMT  
		Size: 67.7 MB (67677437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30d9e2005833fd965cadbd43571f592dd170fa0304f6343cb6edac6de86e9d1`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3b1179164a713c5773ef13b0e57b6ad9d0ae1da5ac5c84cc84676a0074eb52c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95622839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b33961e8792f987ce3a992e698122ee016b00fd494efe745966668652631b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ENV KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 02 May 2024 01:24:50 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:24:51 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:24:51 GMT
USER kong
# Thu, 02 May 2024 01:24:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:24:52 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:24:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:24:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:24:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edf00e68b1a8acf31910e9ef6fa0430edfcc003b9e4578348c0c13911b5271`  
		Last Modified: Thu, 02 May 2024 01:26:52 GMT  
		Size: 67.2 MB (67220376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b0bbf4529f4a9a4796c92a413eda85fb76d553b20d535d0a9b319e9302f3ec`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:db616c77a845adc44d0d4139b0f665dfee7d0a1106acc0f2e9bef657b6cb8a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:29b3b42cfdd96613c526254ac1f9e7cf148b688fbd68928f2eff4f6cc263e3d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34228489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55eb5e56db73ddd25c6628f90ed7ec93c12b231cf5e889114d44863d4f14848d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:42:07 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Mar 2024 08:42:07 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Mar 2024 08:42:07 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Mar 2024 08:42:07 GMT
ARG KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
# Sat, 16 Mar 2024 08:42:07 GMT
ARG KONG_PREFIX=/usr/local/kong
# Sat, 16 Mar 2024 08:42:07 GMT
ENV KONG_PREFIX=/usr/local/kong
# Sat, 16 Mar 2024 08:42:07 GMT
ARG ASSET=remote
# Sat, 16 Mar 2024 08:42:07 GMT
ARG EE_PORTS
# Sat, 16 Mar 2024 08:42:07 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 16 Mar 2024 08:42:13 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     KONG_SHA256=$KONG_AMD64_SHA ;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 16 Mar 2024 08:42:14 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Mar 2024 08:42:14 GMT
USER kong
# Sat, 16 Mar 2024 08:42:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Mar 2024 08:42:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Mar 2024 08:42:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 08:42:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Mar 2024 08:42:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced0f08c887f4c0d12a3033a6face09cdfa8c3c9a8d7ffdf93cad1325b750478`  
		Last Modified: Sat, 16 Mar 2024 08:42:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cf26a8164ca56a1ce1e3df3979ce10cd580120c2198afba909f94657d698c4`  
		Last Modified: Sat, 16 Mar 2024 08:42:56 GMT  
		Size: 30.8 MB (30847796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d1c95cd6fd96cb98f003a228e64e25e2bfea498848de9317a5b739e02f7fe2e`  
		Last Modified: Sat, 16 Mar 2024 08:42:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:07c81639044917ee739866afe22e81bf5a73944aac1c9eed5a59653146eb0e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:b06c43f067744b3fea17f119dfd8f3cae2fe1585f453e7623fd1fe89dbe86153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98118447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89775cbb43bf90fc2a874f3513cda348f724fbd3bb2d016a5f5ccf12d9b41a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 23:03:22 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:23 GMT
USER kong
# Thu, 25 Apr 2024 23:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:23 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15d038661219aead062cbfe12ef045965ec47a102188bee4f46f8ec24d87bf8`  
		Last Modified: Thu, 25 Apr 2024 23:06:02 GMT  
		Size: 67.7 MB (67677437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30d9e2005833fd965cadbd43571f592dd170fa0304f6343cb6edac6de86e9d1`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3b1179164a713c5773ef13b0e57b6ad9d0ae1da5ac5c84cc84676a0074eb52c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95622839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b33961e8792f987ce3a992e698122ee016b00fd494efe745966668652631b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ENV KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 02 May 2024 01:24:50 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:24:51 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:24:51 GMT
USER kong
# Thu, 02 May 2024 01:24:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:24:52 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:24:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:24:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:24:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edf00e68b1a8acf31910e9ef6fa0430edfcc003b9e4578348c0c13911b5271`  
		Last Modified: Thu, 02 May 2024 01:26:52 GMT  
		Size: 67.2 MB (67220376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b0bbf4529f4a9a4796c92a413eda85fb76d553b20d535d0a9b319e9302f3ec`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:07c81639044917ee739866afe22e81bf5a73944aac1c9eed5a59653146eb0e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b06c43f067744b3fea17f119dfd8f3cae2fe1585f453e7623fd1fe89dbe86153
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98118447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a89775cbb43bf90fc2a874f3513cda348f724fbd3bb2d016a5f5ccf12d9b41a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 23:02:45 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 23:02:45 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 23:02:45 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 23:02:46 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 23:02:46 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 23:02:46 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 23:03:22 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 23:03:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 23:03:23 GMT
USER kong
# Thu, 25 Apr 2024 23:03:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 23:03:23 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 23:03:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 23:03:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 23:03:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ab8f8d0e3a93f6c5a01bcc22af717906fe52c9666bc6f3f3372cb2fa161ca8`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15d038661219aead062cbfe12ef045965ec47a102188bee4f46f8ec24d87bf8`  
		Last Modified: Thu, 25 Apr 2024 23:06:02 GMT  
		Size: 67.7 MB (67677437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30d9e2005833fd965cadbd43571f592dd170fa0304f6343cb6edac6de86e9d1`  
		Last Modified: Thu, 25 Apr 2024 23:05:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b3b1179164a713c5773ef13b0e57b6ad9d0ae1da5ac5c84cc84676a0074eb52c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95622839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b33961e8792f987ce3a992e698122ee016b00fd494efe745966668652631b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Apr 2024 14:32:22 GMT
ARG RELEASE
# Sat, 27 Apr 2024 14:32:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 14:32:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 14:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 14:32:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Sat, 27 Apr 2024 14:32:33 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 01:24:32 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 May 2024 01:24:32 GMT
ARG ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ENV ASSET=ce
# Thu, 02 May 2024 01:24:32 GMT
ARG EE_PORTS
# Thu, 02 May 2024 01:24:32 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ENV KONG_VERSION=3.6.1
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 02 May 2024 01:24:32 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 02 May 2024 01:24:50 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 May 2024 01:24:51 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 02 May 2024 01:24:51 GMT
USER kong
# Thu, 02 May 2024 01:24:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 May 2024 01:24:52 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 May 2024 01:24:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 May 2024 01:24:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 May 2024 01:24:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b076355b79badd38bc5732aebeb48133934a0adae078e4a6bf52c7d9d7a4a82`  
		Last Modified: Sun, 28 Apr 2024 01:56:19 GMT  
		Size: 28.4 MB (28401184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03023e4edb848ce23a04dbdafb917b1fb8b27a7fc00ee3ac62fcf2690e8ee1b4`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edf00e68b1a8acf31910e9ef6fa0430edfcc003b9e4578348c0c13911b5271`  
		Last Modified: Thu, 02 May 2024 01:26:52 GMT  
		Size: 67.2 MB (67220376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b0bbf4529f4a9a4796c92a413eda85fb76d553b20d535d0a9b319e9302f3ec`  
		Last Modified: Thu, 02 May 2024 01:26:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
