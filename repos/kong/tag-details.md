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
$ docker pull kong@sha256:f33cb30d6c78c39b7e0e38615618452a0d33d3ec7f47813cd9aec22066b4c08d
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
$ docker pull kong@sha256:6f1cb2410babae2d350a98d8638e558a74c5158b5da554e9d881b25a72c2b794
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117234039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b30956a70b5e3b3ad79e59df26f8e53d883dafb4a0985e22e1f6f56956f0dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:06:42 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:06:43 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:06:43 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:06:43 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:06:43 GMT
ARG KONG_VERSION=2.8.4
# Thu, 25 Apr 2024 22:06:43 GMT
ENV KONG_VERSION=2.8.4
# Thu, 25 Apr 2024 22:06:43 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Thu, 25 Apr 2024 22:06:43 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 25 Apr 2024 22:07:03 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:07:04 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:07:04 GMT
USER kong
# Thu, 25 Apr 2024 22:07:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:07:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:07:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:07:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:07:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5043c1277e7042f7b4e77c4e541f9cc36a21c178ccc317eacf213acfcb23c2`  
		Last Modified: Thu, 25 Apr 2024 22:08:52 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e5819b82b96bba0af71dc0ab051b042a955af996137bfd3fc80fe31625adff`  
		Last Modified: Thu, 25 Apr 2024 22:08:58 GMT  
		Size: 63.8 MB (63750193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8f7ae75db18f4fb2dcaccf80aedff3f85e85d271f2c72556d68064d7e9ffb0`  
		Last Modified: Thu, 25 Apr 2024 22:08:50 GMT  
		Size: 881.0 B  
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
$ docker pull kong@sha256:f33cb30d6c78c39b7e0e38615618452a0d33d3ec7f47813cd9aec22066b4c08d
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
$ docker pull kong@sha256:6f1cb2410babae2d350a98d8638e558a74c5158b5da554e9d881b25a72c2b794
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.2 MB (117234039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b30956a70b5e3b3ad79e59df26f8e53d883dafb4a0985e22e1f6f56956f0dc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:06:42 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:06:43 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:06:43 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:06:43 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:06:43 GMT
ARG KONG_VERSION=2.8.4
# Thu, 25 Apr 2024 22:06:43 GMT
ENV KONG_VERSION=2.8.4
# Thu, 25 Apr 2024 22:06:43 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Thu, 25 Apr 2024 22:06:43 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 25 Apr 2024 22:07:03 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:07:04 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:07:04 GMT
USER kong
# Thu, 25 Apr 2024 22:07:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:07:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:07:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:07:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:07:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5043c1277e7042f7b4e77c4e541f9cc36a21c178ccc317eacf213acfcb23c2`  
		Last Modified: Thu, 25 Apr 2024 22:08:52 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e5819b82b96bba0af71dc0ab051b042a955af996137bfd3fc80fe31625adff`  
		Last Modified: Thu, 25 Apr 2024 22:08:58 GMT  
		Size: 63.8 MB (63750193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8f7ae75db18f4fb2dcaccf80aedff3f85e85d271f2c72556d68064d7e9ffb0`  
		Last Modified: Thu, 25 Apr 2024 22:08:50 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:d93136eb665e6cae0848725311ae1f8a32d2bba87e873df358832c0a7575143c
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
$ docker pull kong@sha256:bde77f329464540d7d83614f575fc65ab79d76572a7034552c1b6605511794f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95623784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1935fd8575244cdbd2c0d79cef46d5df6cd4ff5880741ff773fa1a3c2637fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 22:04:34 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 22:05:03 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:04 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:04 GMT
USER kong
# Thu, 25 Apr 2024 22:05:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7ade7f4505271144d656830c1831023ee3c295d52ccb442c1816dd9c1b134`  
		Last Modified: Thu, 25 Apr 2024 22:07:34 GMT  
		Size: 67.2 MB (67221503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a52a7825f533f4aa4a7b064393af483ff5555fefacc3e39199e89b288c454`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3`

```console
$ docker pull kong@sha256:d82474200f91217a4371b5c82306172f1a4e562ae416e5957e8cf3f5f8f9c3d4
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
$ docker pull kong@sha256:cf96d1d1e387709a28043447010e86309b153bbefef287d1b95cacd3f8dd1a95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79865971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38635d628b1b377ff69b33da1461e4e45c8d546572391c7d13d7c29e65327956`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:06:00 GMT
ARG KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 22:06:00 GMT
ENV KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 22:06:00 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 25 Apr 2024 22:06:01 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 25 Apr 2024 22:06:37 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:06:38 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:06:38 GMT
USER kong
# Thu, 25 Apr 2024 22:06:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:06:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:06:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:06:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:06:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1707ad38da38d676ed2aa049b0abbe6f41097dffad909b246259d3ed8ece710`  
		Last Modified: Thu, 25 Apr 2024 22:08:36 GMT  
		Size: 51.5 MB (51463689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26a616b9618d4354c932d4b3141ccc10215bac059a92aa2de8d9fa39402a9b`  
		Last Modified: Thu, 25 Apr 2024 22:08:30 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3-ubuntu`

```console
$ docker pull kong@sha256:d82474200f91217a4371b5c82306172f1a4e562ae416e5957e8cf3f5f8f9c3d4
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
$ docker pull kong@sha256:cf96d1d1e387709a28043447010e86309b153bbefef287d1b95cacd3f8dd1a95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79865971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38635d628b1b377ff69b33da1461e4e45c8d546572391c7d13d7c29e65327956`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:06:00 GMT
ARG KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 22:06:00 GMT
ENV KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 22:06:00 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 25 Apr 2024 22:06:01 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 25 Apr 2024 22:06:37 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:06:38 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:06:38 GMT
USER kong
# Thu, 25 Apr 2024 22:06:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:06:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:06:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:06:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:06:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1707ad38da38d676ed2aa049b0abbe6f41097dffad909b246259d3ed8ece710`  
		Last Modified: Thu, 25 Apr 2024 22:08:36 GMT  
		Size: 51.5 MB (51463689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26a616b9618d4354c932d4b3141ccc10215bac059a92aa2de8d9fa39402a9b`  
		Last Modified: Thu, 25 Apr 2024 22:08:30 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1`

```console
$ docker pull kong@sha256:d82474200f91217a4371b5c82306172f1a4e562ae416e5957e8cf3f5f8f9c3d4
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
$ docker pull kong@sha256:cf96d1d1e387709a28043447010e86309b153bbefef287d1b95cacd3f8dd1a95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79865971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38635d628b1b377ff69b33da1461e4e45c8d546572391c7d13d7c29e65327956`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:06:00 GMT
ARG KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 22:06:00 GMT
ENV KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 22:06:00 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 25 Apr 2024 22:06:01 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 25 Apr 2024 22:06:37 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:06:38 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:06:38 GMT
USER kong
# Thu, 25 Apr 2024 22:06:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:06:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:06:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:06:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:06:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1707ad38da38d676ed2aa049b0abbe6f41097dffad909b246259d3ed8ece710`  
		Last Modified: Thu, 25 Apr 2024 22:08:36 GMT  
		Size: 51.5 MB (51463689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26a616b9618d4354c932d4b3141ccc10215bac059a92aa2de8d9fa39402a9b`  
		Last Modified: Thu, 25 Apr 2024 22:08:30 GMT  
		Size: 1.2 KB (1155 bytes)  
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
$ docker pull kong@sha256:d82474200f91217a4371b5c82306172f1a4e562ae416e5957e8cf3f5f8f9c3d4
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
$ docker pull kong@sha256:cf96d1d1e387709a28043447010e86309b153bbefef287d1b95cacd3f8dd1a95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79865971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38635d628b1b377ff69b33da1461e4e45c8d546572391c7d13d7c29e65327956`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:06:00 GMT
ARG KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 22:06:00 GMT
ENV KONG_VERSION=3.3.1
# Thu, 25 Apr 2024 22:06:00 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Thu, 25 Apr 2024 22:06:01 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Thu, 25 Apr 2024 22:06:37 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:06:38 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:06:38 GMT
USER kong
# Thu, 25 Apr 2024 22:06:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:06:38 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:06:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:06:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:06:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1707ad38da38d676ed2aa049b0abbe6f41097dffad909b246259d3ed8ece710`  
		Last Modified: Thu, 25 Apr 2024 22:08:36 GMT  
		Size: 51.5 MB (51463689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a26a616b9618d4354c932d4b3141ccc10215bac059a92aa2de8d9fa39402a9b`  
		Last Modified: Thu, 25 Apr 2024 22:08:30 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4`

```console
$ docker pull kong@sha256:ac986b8471cb6d9a5a57cb640290aca63006877401a49e17812392e1d72a9414
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
$ docker pull kong@sha256:56e13044e4397576dc0f05f30b43ee8c26fc8f32190eedad4dfb32d9f87a4a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93649509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437374102e21a8c992ef86e6cd4c43b16e81270c5362e30d7664ecbdf3923b8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 22:05:27 GMT
ENV KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 25 Apr 2024 22:05:52 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:53 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:53 GMT
USER kong
# Thu, 25 Apr 2024 22:05:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:53 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2970dda2e1569112e63eff99ff72fe621a73728041e6719b24d2270c5d0a9d5`  
		Last Modified: Thu, 25 Apr 2024 22:08:18 GMT  
		Size: 65.2 MB (65247226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc9d7ef3132d84514c83ea00be65de8a3cfadd1625effa1ceef50e16543668b`  
		Last Modified: Thu, 25 Apr 2024 22:08:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:ac986b8471cb6d9a5a57cb640290aca63006877401a49e17812392e1d72a9414
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
$ docker pull kong@sha256:56e13044e4397576dc0f05f30b43ee8c26fc8f32190eedad4dfb32d9f87a4a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93649509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437374102e21a8c992ef86e6cd4c43b16e81270c5362e30d7664ecbdf3923b8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 22:05:27 GMT
ENV KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 25 Apr 2024 22:05:52 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:53 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:53 GMT
USER kong
# Thu, 25 Apr 2024 22:05:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:53 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2970dda2e1569112e63eff99ff72fe621a73728041e6719b24d2270c5d0a9d5`  
		Last Modified: Thu, 25 Apr 2024 22:08:18 GMT  
		Size: 65.2 MB (65247226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc9d7ef3132d84514c83ea00be65de8a3cfadd1625effa1ceef50e16543668b`  
		Last Modified: Thu, 25 Apr 2024 22:08:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2`

```console
$ docker pull kong@sha256:ac986b8471cb6d9a5a57cb640290aca63006877401a49e17812392e1d72a9414
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
$ docker pull kong@sha256:56e13044e4397576dc0f05f30b43ee8c26fc8f32190eedad4dfb32d9f87a4a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93649509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437374102e21a8c992ef86e6cd4c43b16e81270c5362e30d7664ecbdf3923b8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 22:05:27 GMT
ENV KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 25 Apr 2024 22:05:52 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:53 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:53 GMT
USER kong
# Thu, 25 Apr 2024 22:05:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:53 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2970dda2e1569112e63eff99ff72fe621a73728041e6719b24d2270c5d0a9d5`  
		Last Modified: Thu, 25 Apr 2024 22:08:18 GMT  
		Size: 65.2 MB (65247226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc9d7ef3132d84514c83ea00be65de8a3cfadd1625effa1ceef50e16543668b`  
		Last Modified: Thu, 25 Apr 2024 22:08:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:ac986b8471cb6d9a5a57cb640290aca63006877401a49e17812392e1d72a9414
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
$ docker pull kong@sha256:56e13044e4397576dc0f05f30b43ee8c26fc8f32190eedad4dfb32d9f87a4a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93649509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437374102e21a8c992ef86e6cd4c43b16e81270c5362e30d7664ecbdf3923b8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 22:05:27 GMT
ENV KONG_VERSION=3.4.2
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 25 Apr 2024 22:05:27 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 25 Apr 2024 22:05:52 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:53 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:53 GMT
USER kong
# Thu, 25 Apr 2024 22:05:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:53 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2970dda2e1569112e63eff99ff72fe621a73728041e6719b24d2270c5d0a9d5`  
		Last Modified: Thu, 25 Apr 2024 22:08:18 GMT  
		Size: 65.2 MB (65247226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc9d7ef3132d84514c83ea00be65de8a3cfadd1625effa1ceef50e16543668b`  
		Last Modified: Thu, 25 Apr 2024 22:08:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5`

```console
$ docker pull kong@sha256:84049830316240fc4343228ca564f7acea6b1861c9f4163102dfac35fbd2471b
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
$ docker pull kong@sha256:9a8e5d2c481a6c304044b247588335d0e78f9619c8cad0649b8bda1b9954e79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91890676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00016e5f28c39d1c94d39989efd1d344d2ea5a8c5ba7f1f5205d194101cf6510`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 22:05:07 GMT
ENV KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 25 Apr 2024 22:05:23 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:24 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:24 GMT
USER kong
# Thu, 25 Apr 2024 22:05:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6e6a8fd717bf6ffeaa9fcd06ab8f6991d46b0a235408d239ae2fdd9aa8bba2`  
		Last Modified: Thu, 25 Apr 2024 22:07:59 GMT  
		Size: 63.5 MB (63488393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8ec77f4b512afd48e76bc43bddb09cabc8a205c522d89477b915c4a9fcf23c`  
		Last Modified: Thu, 25 Apr 2024 22:07:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5-ubuntu`

```console
$ docker pull kong@sha256:84049830316240fc4343228ca564f7acea6b1861c9f4163102dfac35fbd2471b
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
$ docker pull kong@sha256:9a8e5d2c481a6c304044b247588335d0e78f9619c8cad0649b8bda1b9954e79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91890676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00016e5f28c39d1c94d39989efd1d344d2ea5a8c5ba7f1f5205d194101cf6510`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 22:05:07 GMT
ENV KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 25 Apr 2024 22:05:23 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:24 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:24 GMT
USER kong
# Thu, 25 Apr 2024 22:05:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6e6a8fd717bf6ffeaa9fcd06ab8f6991d46b0a235408d239ae2fdd9aa8bba2`  
		Last Modified: Thu, 25 Apr 2024 22:07:59 GMT  
		Size: 63.5 MB (63488393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8ec77f4b512afd48e76bc43bddb09cabc8a205c522d89477b915c4a9fcf23c`  
		Last Modified: Thu, 25 Apr 2024 22:07:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0`

```console
$ docker pull kong@sha256:84049830316240fc4343228ca564f7acea6b1861c9f4163102dfac35fbd2471b
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
$ docker pull kong@sha256:9a8e5d2c481a6c304044b247588335d0e78f9619c8cad0649b8bda1b9954e79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91890676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00016e5f28c39d1c94d39989efd1d344d2ea5a8c5ba7f1f5205d194101cf6510`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 22:05:07 GMT
ENV KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 25 Apr 2024 22:05:23 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:24 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:24 GMT
USER kong
# Thu, 25 Apr 2024 22:05:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6e6a8fd717bf6ffeaa9fcd06ab8f6991d46b0a235408d239ae2fdd9aa8bba2`  
		Last Modified: Thu, 25 Apr 2024 22:07:59 GMT  
		Size: 63.5 MB (63488393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8ec77f4b512afd48e76bc43bddb09cabc8a205c522d89477b915c4a9fcf23c`  
		Last Modified: Thu, 25 Apr 2024 22:07:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0-ubuntu`

```console
$ docker pull kong@sha256:84049830316240fc4343228ca564f7acea6b1861c9f4163102dfac35fbd2471b
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
$ docker pull kong@sha256:9a8e5d2c481a6c304044b247588335d0e78f9619c8cad0649b8bda1b9954e79a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91890676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00016e5f28c39d1c94d39989efd1d344d2ea5a8c5ba7f1f5205d194101cf6510`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 22:05:07 GMT
ENV KONG_VERSION=3.5.0
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Thu, 25 Apr 2024 22:05:07 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Thu, 25 Apr 2024 22:05:23 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:24 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:24 GMT
USER kong
# Thu, 25 Apr 2024 22:05:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:24 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6e6a8fd717bf6ffeaa9fcd06ab8f6991d46b0a235408d239ae2fdd9aa8bba2`  
		Last Modified: Thu, 25 Apr 2024 22:07:59 GMT  
		Size: 63.5 MB (63488393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8ec77f4b512afd48e76bc43bddb09cabc8a205c522d89477b915c4a9fcf23c`  
		Last Modified: Thu, 25 Apr 2024 22:07:51 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6`

```console
$ docker pull kong@sha256:d93136eb665e6cae0848725311ae1f8a32d2bba87e873df358832c0a7575143c
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
$ docker pull kong@sha256:bde77f329464540d7d83614f575fc65ab79d76572a7034552c1b6605511794f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95623784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1935fd8575244cdbd2c0d79cef46d5df6cd4ff5880741ff773fa1a3c2637fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 22:04:34 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 22:05:03 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:04 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:04 GMT
USER kong
# Thu, 25 Apr 2024 22:05:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7ade7f4505271144d656830c1831023ee3c295d52ccb442c1816dd9c1b134`  
		Last Modified: Thu, 25 Apr 2024 22:07:34 GMT  
		Size: 67.2 MB (67221503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a52a7825f533f4aa4a7b064393af483ff5555fefacc3e39199e89b288c454`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:d93136eb665e6cae0848725311ae1f8a32d2bba87e873df358832c0a7575143c
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
$ docker pull kong@sha256:bde77f329464540d7d83614f575fc65ab79d76572a7034552c1b6605511794f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95623784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1935fd8575244cdbd2c0d79cef46d5df6cd4ff5880741ff773fa1a3c2637fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 22:04:34 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 22:05:03 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:04 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:04 GMT
USER kong
# Thu, 25 Apr 2024 22:05:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7ade7f4505271144d656830c1831023ee3c295d52ccb442c1816dd9c1b134`  
		Last Modified: Thu, 25 Apr 2024 22:07:34 GMT  
		Size: 67.2 MB (67221503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a52a7825f533f4aa4a7b064393af483ff5555fefacc3e39199e89b288c454`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1`

```console
$ docker pull kong@sha256:d93136eb665e6cae0848725311ae1f8a32d2bba87e873df358832c0a7575143c
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
$ docker pull kong@sha256:bde77f329464540d7d83614f575fc65ab79d76572a7034552c1b6605511794f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95623784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1935fd8575244cdbd2c0d79cef46d5df6cd4ff5880741ff773fa1a3c2637fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 22:04:34 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 22:05:03 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:04 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:04 GMT
USER kong
# Thu, 25 Apr 2024 22:05:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7ade7f4505271144d656830c1831023ee3c295d52ccb442c1816dd9c1b134`  
		Last Modified: Thu, 25 Apr 2024 22:07:34 GMT  
		Size: 67.2 MB (67221503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a52a7825f533f4aa4a7b064393af483ff5555fefacc3e39199e89b288c454`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:d93136eb665e6cae0848725311ae1f8a32d2bba87e873df358832c0a7575143c
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
$ docker pull kong@sha256:bde77f329464540d7d83614f575fc65ab79d76572a7034552c1b6605511794f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95623784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1935fd8575244cdbd2c0d79cef46d5df6cd4ff5880741ff773fa1a3c2637fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 22:04:34 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 22:05:03 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:04 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:04 GMT
USER kong
# Thu, 25 Apr 2024 22:05:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7ade7f4505271144d656830c1831023ee3c295d52ccb442c1816dd9c1b134`  
		Last Modified: Thu, 25 Apr 2024 22:07:34 GMT  
		Size: 67.2 MB (67221503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a52a7825f533f4aa4a7b064393af483ff5555fefacc3e39199e89b288c454`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
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
$ docker pull kong@sha256:d93136eb665e6cae0848725311ae1f8a32d2bba87e873df358832c0a7575143c
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
$ docker pull kong@sha256:bde77f329464540d7d83614f575fc65ab79d76572a7034552c1b6605511794f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95623784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1935fd8575244cdbd2c0d79cef46d5df6cd4ff5880741ff773fa1a3c2637fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 22:04:34 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 22:05:03 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:04 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:04 GMT
USER kong
# Thu, 25 Apr 2024 22:05:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7ade7f4505271144d656830c1831023ee3c295d52ccb442c1816dd9c1b134`  
		Last Modified: Thu, 25 Apr 2024 22:07:34 GMT  
		Size: 67.2 MB (67221503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a52a7825f533f4aa4a7b064393af483ff5555fefacc3e39199e89b288c454`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:d93136eb665e6cae0848725311ae1f8a32d2bba87e873df358832c0a7575143c
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
$ docker pull kong@sha256:bde77f329464540d7d83614f575fc65ab79d76572a7034552c1b6605511794f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95623784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1935fd8575244cdbd2c0d79cef46d5df6cd4ff5880741ff773fa1a3c2637fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 22:04:33 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 25 Apr 2024 22:04:33 GMT
ARG ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ENV ASSET=ce
# Thu, 25 Apr 2024 22:04:33 GMT
ARG EE_PORTS
# Thu, 25 Apr 2024 22:04:33 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ENV KONG_VERSION=3.6.1
# Thu, 25 Apr 2024 22:04:33 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Thu, 25 Apr 2024 22:04:34 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Thu, 25 Apr 2024 22:05:03 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 25 Apr 2024 22:05:04 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Thu, 25 Apr 2024 22:05:04 GMT
USER kong
# Thu, 25 Apr 2024 22:05:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 25 Apr 2024 22:05:04 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 25 Apr 2024 22:05:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Apr 2024 22:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 25 Apr 2024 22:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd72b9800809f383cecac03ea943ff4d8918a71655fdaa8bfa1319466d4a481`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a7ade7f4505271144d656830c1831023ee3c295d52ccb442c1816dd9c1b134`  
		Last Modified: Thu, 25 Apr 2024 22:07:34 GMT  
		Size: 67.2 MB (67221503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476a52a7825f533f4aa4a7b064393af483ff5555fefacc3e39199e89b288c454`  
		Last Modified: Thu, 25 Apr 2024 22:07:26 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
