<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.4`](#kong284)
-	[`kong:2.8.4-alpine`](#kong284-alpine)
-	[`kong:2.8.4-ubuntu`](#kong284-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.1`](#kong31)
-	[`kong:3.1-ubuntu`](#kong31-ubuntu)
-	[`kong:3.1.1`](#kong311)
-	[`kong:3.1.1-alpine`](#kong311-alpine)
-	[`kong:3.1.1-ubuntu`](#kong311-ubuntu)
-	[`kong:3.2`](#kong32)
-	[`kong:3.2-ubuntu`](#kong32-ubuntu)
-	[`kong:3.2.2`](#kong322)
-	[`kong:3.2.2-alpine`](#kong322-alpine)
-	[`kong:3.2.2-ubuntu`](#kong322-ubuntu)
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
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.8`

```console
$ docker pull kong@sha256:01015f06fadad772b33237cb970604f4a36f4f9637d717732fdfb50da26d0d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:fe949ed350899094244a6b9cfb57dafd2355ba2b71d6a841ad17e1bf970933f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48122804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9017d8a58c08420cf391e93fd2f4bf47a004a1d1f38b798d58869d97d0a70c54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:51:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 27 Jan 2024 03:51:20 GMT
ARG ASSET=ce
# Sat, 27 Jan 2024 03:51:20 GMT
ENV ASSET=ce
# Sat, 27 Jan 2024 03:51:20 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:51:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 03:51:20 GMT
ENV KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 27 Jan 2024 03:51:28 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 27 Jan 2024 03:51:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:51:28 GMT
USER kong
# Sat, 27 Jan 2024 03:51:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:51:29 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:51:29 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:51:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:51:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea7fc85e8e79ea77bacc20c0656df7cefb2748ba5d23b0a804d3aadc927ad6`  
		Last Modified: Sat, 27 Jan 2024 03:52:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bcb12b899d3369175fb817406fefd67b261d879cb75db961af92c2df174c21`  
		Last Modified: Sat, 27 Jan 2024 03:52:53 GMT  
		Size: 44.7 MB (44719248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa1b516145a906af4ec7af39ff885911ad906ec39f7c064d4e2d17acf0f0e8b`  
		Last Modified: Sat, 27 Jan 2024 03:52:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:175ff9f5281d49b86c6f3af22a58f38762d2d544def71a844640f23c84d25998
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47440549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531bcc3c87205b1121431f7fd10f1a59ec8e801b80c11e1d89d55e32777f780`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:19:54 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 27 Jan 2024 09:19:54 GMT
ARG ASSET=ce
# Sat, 27 Jan 2024 09:19:55 GMT
ENV ASSET=ce
# Sat, 27 Jan 2024 09:19:55 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 09:19:55 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 09:19:55 GMT
ENV KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 27 Jan 2024 09:20:02 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 27 Jan 2024 09:20:03 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 09:20:03 GMT
USER kong
# Sat, 27 Jan 2024 09:20:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:20:03 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 09:20:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 09:20:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 09:20:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8518f53a060a7e33424e11203079bf369a3d79256904b46698734f292bc98d2`  
		Last Modified: Sat, 27 Jan 2024 09:20:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f4168b4b82bd934c51a9cfb293b51764b91bbe2dcd45d77e33ea1180ddf25`  
		Last Modified: Sat, 27 Jan 2024 09:20:52 GMT  
		Size: 44.1 MB (44106175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bfe151688fe4d29f912370d2fd1f58edec86d738477ee988a0318c10c1f9c1`  
		Last Modified: Sat, 27 Jan 2024 09:20:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:f94f2e9975972820213724734804c93283619db15a64de1e9aec7e2ec3472ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ad0498480bff07c904cad5bfc07f9fe8cc4f17474a95e5e3a23882b4581f6bee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116553516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8f0c09fecba67f1198185b70e66d495f8d89d12a3064223217d7d666c6ab09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:32:16 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:32:16 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:32:16 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:32:17 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:32:17 GMT
ARG KONG_VERSION=2.8.4
# Fri, 02 Feb 2024 07:32:17 GMT
ENV KONG_VERSION=2.8.4
# Fri, 02 Feb 2024 07:32:17 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Fri, 02 Feb 2024 07:32:17 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 02 Feb 2024 07:32:43 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:32:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:32:44 GMT
USER kong
# Fri, 02 Feb 2024 07:32:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:32:44 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:32:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:32:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:32:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e1b3cb01de03debb5f3857844813ed14c2b18db4ba7bb504cf0d7eb35ce88f`  
		Last Modified: Fri, 02 Feb 2024 07:35:03 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4255bf203982c37146d96d4603c57b1c5da1e5c2b1d27fe3f338b5a20e87f0d`  
		Last Modified: Fri, 02 Feb 2024 07:35:11 GMT  
		Size: 61.0 MB (61022791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e79f1bc87ac99344f89b1bb6a630f6d40550c71147f4698d183b89b557b5dd0`  
		Last Modified: Fri, 02 Feb 2024 07:35:01 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4645a0c4291a597056b899a0ac7f75f24143d09f63beca8e5c46484dfe8f4e94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113127263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab25475b8a4a6ff9583cdc72574db05a1b52a76161ce2264be86acf380a9cbaf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:06:33 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:06:33 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:06:33 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:06:34 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:06:34 GMT
ARG KONG_VERSION=2.8.4
# Fri, 02 Feb 2024 02:06:34 GMT
ENV KONG_VERSION=2.8.4
# Fri, 02 Feb 2024 02:06:34 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Fri, 02 Feb 2024 02:06:34 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 02 Feb 2024 02:06:53 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:06:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:06:54 GMT
USER kong
# Fri, 02 Feb 2024 02:06:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:06:54 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:06:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:06:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:06:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d57a018facd2c519f010c3e34e807214b335dca9f49e7ec7579b8c92794bfda`  
		Last Modified: Fri, 02 Feb 2024 02:09:07 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97f09a955167df5e1984317465c1266382dc1d81c90857f646e252b4fa29c70`  
		Last Modified: Fri, 02 Feb 2024 02:09:13 GMT  
		Size: 59.6 MB (59644318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87915db07a2db67ce9aa2af491c42fb0704e596c87ef062eeba61f14f35a1c5b`  
		Last Modified: Fri, 02 Feb 2024 02:09:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4`

```console
$ docker pull kong@sha256:01015f06fadad772b33237cb970604f4a36f4f9637d717732fdfb50da26d0d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.4` - linux; amd64

```console
$ docker pull kong@sha256:fe949ed350899094244a6b9cfb57dafd2355ba2b71d6a841ad17e1bf970933f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48122804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9017d8a58c08420cf391e93fd2f4bf47a004a1d1f38b798d58869d97d0a70c54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:51:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 27 Jan 2024 03:51:20 GMT
ARG ASSET=ce
# Sat, 27 Jan 2024 03:51:20 GMT
ENV ASSET=ce
# Sat, 27 Jan 2024 03:51:20 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:51:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 03:51:20 GMT
ENV KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 27 Jan 2024 03:51:28 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 27 Jan 2024 03:51:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:51:28 GMT
USER kong
# Sat, 27 Jan 2024 03:51:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:51:29 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:51:29 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:51:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:51:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea7fc85e8e79ea77bacc20c0656df7cefb2748ba5d23b0a804d3aadc927ad6`  
		Last Modified: Sat, 27 Jan 2024 03:52:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bcb12b899d3369175fb817406fefd67b261d879cb75db961af92c2df174c21`  
		Last Modified: Sat, 27 Jan 2024 03:52:53 GMT  
		Size: 44.7 MB (44719248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa1b516145a906af4ec7af39ff885911ad906ec39f7c064d4e2d17acf0f0e8b`  
		Last Modified: Sat, 27 Jan 2024 03:52:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:175ff9f5281d49b86c6f3af22a58f38762d2d544def71a844640f23c84d25998
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47440549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531bcc3c87205b1121431f7fd10f1a59ec8e801b80c11e1d89d55e32777f780`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:19:54 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 27 Jan 2024 09:19:54 GMT
ARG ASSET=ce
# Sat, 27 Jan 2024 09:19:55 GMT
ENV ASSET=ce
# Sat, 27 Jan 2024 09:19:55 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 09:19:55 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 09:19:55 GMT
ENV KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 27 Jan 2024 09:20:02 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 27 Jan 2024 09:20:03 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 09:20:03 GMT
USER kong
# Sat, 27 Jan 2024 09:20:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:20:03 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 09:20:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 09:20:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 09:20:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8518f53a060a7e33424e11203079bf369a3d79256904b46698734f292bc98d2`  
		Last Modified: Sat, 27 Jan 2024 09:20:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f4168b4b82bd934c51a9cfb293b51764b91bbe2dcd45d77e33ea1180ddf25`  
		Last Modified: Sat, 27 Jan 2024 09:20:52 GMT  
		Size: 44.1 MB (44106175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bfe151688fe4d29f912370d2fd1f58edec86d738477ee988a0318c10c1f9c1`  
		Last Modified: Sat, 27 Jan 2024 09:20:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4-alpine`

```console
$ docker pull kong@sha256:01015f06fadad772b33237cb970604f4a36f4f9637d717732fdfb50da26d0d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:fe949ed350899094244a6b9cfb57dafd2355ba2b71d6a841ad17e1bf970933f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48122804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9017d8a58c08420cf391e93fd2f4bf47a004a1d1f38b798d58869d97d0a70c54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:51:19 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 27 Jan 2024 03:51:20 GMT
ARG ASSET=ce
# Sat, 27 Jan 2024 03:51:20 GMT
ENV ASSET=ce
# Sat, 27 Jan 2024 03:51:20 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:51:20 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 03:51:20 GMT
ENV KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 27 Jan 2024 03:51:20 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 27 Jan 2024 03:51:28 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 27 Jan 2024 03:51:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:51:28 GMT
USER kong
# Sat, 27 Jan 2024 03:51:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:51:29 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:51:29 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:51:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:51:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ea7fc85e8e79ea77bacc20c0656df7cefb2748ba5d23b0a804d3aadc927ad6`  
		Last Modified: Sat, 27 Jan 2024 03:52:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bcb12b899d3369175fb817406fefd67b261d879cb75db961af92c2df174c21`  
		Last Modified: Sat, 27 Jan 2024 03:52:53 GMT  
		Size: 44.7 MB (44719248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa1b516145a906af4ec7af39ff885911ad906ec39f7c064d4e2d17acf0f0e8b`  
		Last Modified: Sat, 27 Jan 2024 03:52:45 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:175ff9f5281d49b86c6f3af22a58f38762d2d544def71a844640f23c84d25998
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47440549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531bcc3c87205b1121431f7fd10f1a59ec8e801b80c11e1d89d55e32777f780`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:19:54 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 27 Jan 2024 09:19:54 GMT
ARG ASSET=ce
# Sat, 27 Jan 2024 09:19:55 GMT
ENV ASSET=ce
# Sat, 27 Jan 2024 09:19:55 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 09:19:55 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 09:19:55 GMT
ENV KONG_VERSION=2.8.4
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Sat, 27 Jan 2024 09:19:55 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Sat, 27 Jan 2024 09:20:02 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 27 Jan 2024 09:20:03 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 09:20:03 GMT
USER kong
# Sat, 27 Jan 2024 09:20:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:20:03 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 09:20:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 09:20:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 09:20:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8518f53a060a7e33424e11203079bf369a3d79256904b46698734f292bc98d2`  
		Last Modified: Sat, 27 Jan 2024 09:20:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4f4168b4b82bd934c51a9cfb293b51764b91bbe2dcd45d77e33ea1180ddf25`  
		Last Modified: Sat, 27 Jan 2024 09:20:52 GMT  
		Size: 44.1 MB (44106175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bfe151688fe4d29f912370d2fd1f58edec86d738477ee988a0318c10c1f9c1`  
		Last Modified: Sat, 27 Jan 2024 09:20:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4-ubuntu`

```console
$ docker pull kong@sha256:f94f2e9975972820213724734804c93283619db15a64de1e9aec7e2ec3472ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ad0498480bff07c904cad5bfc07f9fe8cc4f17474a95e5e3a23882b4581f6bee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116553516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8f0c09fecba67f1198185b70e66d495f8d89d12a3064223217d7d666c6ab09`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:32:16 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:32:16 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:32:16 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:32:17 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:32:17 GMT
ARG KONG_VERSION=2.8.4
# Fri, 02 Feb 2024 07:32:17 GMT
ENV KONG_VERSION=2.8.4
# Fri, 02 Feb 2024 07:32:17 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Fri, 02 Feb 2024 07:32:17 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 02 Feb 2024 07:32:43 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:32:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:32:44 GMT
USER kong
# Fri, 02 Feb 2024 07:32:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:32:44 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:32:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:32:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:32:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e1b3cb01de03debb5f3857844813ed14c2b18db4ba7bb504cf0d7eb35ce88f`  
		Last Modified: Fri, 02 Feb 2024 07:35:03 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4255bf203982c37146d96d4603c57b1c5da1e5c2b1d27fe3f338b5a20e87f0d`  
		Last Modified: Fri, 02 Feb 2024 07:35:11 GMT  
		Size: 61.0 MB (61022791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e79f1bc87ac99344f89b1bb6a630f6d40550c71147f4698d183b89b557b5dd0`  
		Last Modified: Fri, 02 Feb 2024 07:35:01 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4645a0c4291a597056b899a0ac7f75f24143d09f63beca8e5c46484dfe8f4e94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113127263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab25475b8a4a6ff9583cdc72574db05a1b52a76161ce2264be86acf380a9cbaf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:06:33 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:06:33 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:06:33 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:06:34 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:06:34 GMT
ARG KONG_VERSION=2.8.4
# Fri, 02 Feb 2024 02:06:34 GMT
ENV KONG_VERSION=2.8.4
# Fri, 02 Feb 2024 02:06:34 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Fri, 02 Feb 2024 02:06:34 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 02 Feb 2024 02:06:53 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:06:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:06:54 GMT
USER kong
# Fri, 02 Feb 2024 02:06:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:06:54 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:06:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:06:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:06:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d57a018facd2c519f010c3e34e807214b335dca9f49e7ec7579b8c92794bfda`  
		Last Modified: Fri, 02 Feb 2024 02:09:07 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97f09a955167df5e1984317465c1266382dc1d81c90857f646e252b4fa29c70`  
		Last Modified: Fri, 02 Feb 2024 02:09:13 GMT  
		Size: 59.6 MB (59644318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87915db07a2db67ce9aa2af491c42fb0704e596c87ef062eeba61f14f35a1c5b`  
		Last Modified: Fri, 02 Feb 2024 02:09:05 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:f49d0a9261a850aa82788ecf0b64474d965fc8baf17cbee68687f21fbcb7f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:ff03eb11f67d73f74747840fb052f2e01b53e560c039b82f78beb256b2497467
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d6d5e8a04fb00f97161dd265608d428df838b8dcb24570650387373ef4422`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 07:29:58 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:29:59 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:29:59 GMT
USER kong
# Fri, 02 Feb 2024 07:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:29:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:29:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:29:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:29:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75647976f218a637e1f8fbf664bf81d67743a41f121b477844760d429c65d303`  
		Last Modified: Fri, 02 Feb 2024 07:33:18 GMT  
		Size: 64.0 MB (63959063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c71490554f68130975444ccc887639f6093bde5617563817ab3b9a7fac5a21`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:641ebb8b331f431f480217585bfd6b4950ef8751b8e0246156051f06d4c9a231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6105956b06bb453e1af507ca0084eccc513ace226b77d8ddef86697d9679066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 02:04:42 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:04:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:04:43 GMT
USER kong
# Fri, 02 Feb 2024 02:04:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:04:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:04:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:04:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7812175ddcfaaa6e1d23578b162b7804abc0028f957d916fb554b30e0b20d275`  
		Last Modified: Fri, 02 Feb 2024 02:07:23 GMT  
		Size: 63.5 MB (63486306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457282a5822c35a448fdf61a792b9cae3d9f593e4a83b3f05dfc337f05836de8`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1`

```console
$ docker pull kong@sha256:b265c81b06ac61cf4457307ba4fd18a6c1fd378eb9e5bf49e2899c9a19db17aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1` - linux; amd64

```console
$ docker pull kong@sha256:dbe5a5d11909a3a95eff75dda98282b61e4bdb383de1caf26abea71294a8e611
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75699930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0977826187c2f8c20f0163968549e4c2e519c21e5f8c459043681cf688130f11`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:51:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 03:51:05 GMT
ENV KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 27 Jan 2024 03:51:05 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 03:51:05 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:51:05 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 03:51:12 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 03:51:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:51:12 GMT
USER kong
# Sat, 27 Jan 2024 03:51:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:51:12 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:51:13 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:51:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:51:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7e2c83861192436c2b92193b6b009511f97e64793d53b31220862107ba4030`  
		Last Modified: Sat, 27 Jan 2024 03:52:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc993f9347c5257302402cecaf18cfb571aeb93e854b6b42a7fbe04fc00ae57`  
		Last Modified: Sat, 27 Jan 2024 03:52:34 GMT  
		Size: 72.9 MB (72891079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6213ae80787849c597e587402003d3a1cbada7220883fa31026f05b98b76da0f`  
		Last Modified: Sat, 27 Jan 2024 03:52:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e558676aa302b7115d8f82a72be4ecee311c17af5113163eee4f9b9b767145ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73716468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc397091ebf77dd35d5aaffc2beb40d48d8d32fd67cfbb9319925794473101eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:19:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 09:19:43 GMT
ARG KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 09:19:43 GMT
ENV KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 09:19:44 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 27 Jan 2024 09:19:44 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 27 Jan 2024 09:19:44 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 09:19:44 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 09:19:44 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 09:19:49 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 09:19:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 09:19:50 GMT
USER kong
# Sat, 27 Jan 2024 09:19:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:19:50 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 09:19:50 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 09:19:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 09:19:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9df6da955aca6e08795cc34d8f1a36c9e7802c9dc1764c648256e0c26e9f26`  
		Last Modified: Sat, 27 Jan 2024 09:20:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2745fcc6a3a0fb60f58e24afb12c414c1ba2d9c9a514b8ad87784bed6d8428a8`  
		Last Modified: Sat, 27 Jan 2024 09:20:35 GMT  
		Size: 71.0 MB (71007169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afbc8bfa7f8ea46f46e7dbb1611ceda9f3a5d7caaf115c4781ec1a866a4a79`  
		Last Modified: Sat, 27 Jan 2024 09:20:28 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1-ubuntu`

```console
$ docker pull kong@sha256:7c87a6055b5bd80b0e8ecd72d4cb84b7ed6ee08970f446094085a6989453a5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:21e93c0e650ed9d3629ef08ff1ac7b526d1a17af84b31383bc1350a9dcdd3b31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101919072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef9e25a07b51def8a679e0deac7b0ba577ca58302b3964fa2cf60cd4ee6aad1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:31:39 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:31:39 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:31:39 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:31:40 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:31:40 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:31:40 GMT
ARG KONG_VERSION=3.1.1
# Fri, 02 Feb 2024 07:31:40 GMT
ENV KONG_VERSION=3.1.1
# Fri, 02 Feb 2024 07:31:40 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Fri, 02 Feb 2024 07:31:40 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Fri, 02 Feb 2024 07:32:05 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:32:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:32:06 GMT
USER kong
# Fri, 02 Feb 2024 07:32:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:32:06 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:32:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:32:06 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:32:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59868e3e33c139839859b72dbaaa269ebcb409bb4ad298714a6ee184c9add37`  
		Last Modified: Fri, 02 Feb 2024 07:34:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df464fdec1b52ba6d33d3d87877e4bf6b5f692fc87f87076808a7a180fabed22`  
		Last Modified: Fri, 02 Feb 2024 07:34:53 GMT  
		Size: 73.3 MB (73333604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805240893333a133df0a94e2635da22bd327a62e73d2919d0f52b881bef3803`  
		Last Modified: Fri, 02 Feb 2024 07:34:41 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8f9413461730df9ffe7658d8dd59046d2d25530ec9874be82094932cbc70109a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99178377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f892aa03a697a59dcec51e9ffc064b9014b31a1f2de9370602e7b3f1f5d5b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:05:58 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:05:58 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:05:58 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:05:58 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:05:58 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:58 GMT
ARG KONG_VERSION=3.1.1
# Fri, 02 Feb 2024 02:05:58 GMT
ENV KONG_VERSION=3.1.1
# Fri, 02 Feb 2024 02:05:58 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Fri, 02 Feb 2024 02:05:58 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Fri, 02 Feb 2024 02:06:27 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:06:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:06:28 GMT
USER kong
# Fri, 02 Feb 2024 02:06:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:06:28 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:06:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:06:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:06:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945c0be80e646727d5d4ba6c543f57c71fd14e633a90f653a2b908a84fc9e966`  
		Last Modified: Fri, 02 Feb 2024 02:08:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2b3e33419c6c925a6a156a558c75b92e165ca5f6559220a7b773f3b0da5172`  
		Last Modified: Fri, 02 Feb 2024 02:08:54 GMT  
		Size: 72.0 MB (71972312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a891f62a4f1177043dc9b1259f11b620a8febcf9d7ec53013da80327ba609`  
		Last Modified: Fri, 02 Feb 2024 02:08:45 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1`

```console
$ docker pull kong@sha256:b265c81b06ac61cf4457307ba4fd18a6c1fd378eb9e5bf49e2899c9a19db17aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1` - linux; amd64

```console
$ docker pull kong@sha256:dbe5a5d11909a3a95eff75dda98282b61e4bdb383de1caf26abea71294a8e611
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75699930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0977826187c2f8c20f0163968549e4c2e519c21e5f8c459043681cf688130f11`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:51:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 03:51:05 GMT
ENV KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 27 Jan 2024 03:51:05 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 03:51:05 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:51:05 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 03:51:12 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 03:51:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:51:12 GMT
USER kong
# Sat, 27 Jan 2024 03:51:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:51:12 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:51:13 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:51:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:51:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7e2c83861192436c2b92193b6b009511f97e64793d53b31220862107ba4030`  
		Last Modified: Sat, 27 Jan 2024 03:52:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc993f9347c5257302402cecaf18cfb571aeb93e854b6b42a7fbe04fc00ae57`  
		Last Modified: Sat, 27 Jan 2024 03:52:34 GMT  
		Size: 72.9 MB (72891079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6213ae80787849c597e587402003d3a1cbada7220883fa31026f05b98b76da0f`  
		Last Modified: Sat, 27 Jan 2024 03:52:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e558676aa302b7115d8f82a72be4ecee311c17af5113163eee4f9b9b767145ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73716468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc397091ebf77dd35d5aaffc2beb40d48d8d32fd67cfbb9319925794473101eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:19:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 09:19:43 GMT
ARG KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 09:19:43 GMT
ENV KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 09:19:44 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 27 Jan 2024 09:19:44 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 27 Jan 2024 09:19:44 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 09:19:44 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 09:19:44 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 09:19:49 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 09:19:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 09:19:50 GMT
USER kong
# Sat, 27 Jan 2024 09:19:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:19:50 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 09:19:50 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 09:19:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 09:19:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9df6da955aca6e08795cc34d8f1a36c9e7802c9dc1764c648256e0c26e9f26`  
		Last Modified: Sat, 27 Jan 2024 09:20:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2745fcc6a3a0fb60f58e24afb12c414c1ba2d9c9a514b8ad87784bed6d8428a8`  
		Last Modified: Sat, 27 Jan 2024 09:20:35 GMT  
		Size: 71.0 MB (71007169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afbc8bfa7f8ea46f46e7dbb1611ceda9f3a5d7caaf115c4781ec1a866a4a79`  
		Last Modified: Sat, 27 Jan 2024 09:20:28 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1-alpine`

```console
$ docker pull kong@sha256:b265c81b06ac61cf4457307ba4fd18a6c1fd378eb9e5bf49e2899c9a19db17aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:dbe5a5d11909a3a95eff75dda98282b61e4bdb383de1caf26abea71294a8e611
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75699930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0977826187c2f8c20f0163968549e4c2e519c21e5f8c459043681cf688130f11`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:51:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 03:51:05 GMT
ENV KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 27 Jan 2024 03:51:05 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 27 Jan 2024 03:51:05 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 03:51:05 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:51:05 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 03:51:12 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 03:51:12 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:51:12 GMT
USER kong
# Sat, 27 Jan 2024 03:51:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:51:12 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:51:13 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:51:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:51:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7e2c83861192436c2b92193b6b009511f97e64793d53b31220862107ba4030`  
		Last Modified: Sat, 27 Jan 2024 03:52:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc993f9347c5257302402cecaf18cfb571aeb93e854b6b42a7fbe04fc00ae57`  
		Last Modified: Sat, 27 Jan 2024 03:52:34 GMT  
		Size: 72.9 MB (72891079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6213ae80787849c597e587402003d3a1cbada7220883fa31026f05b98b76da0f`  
		Last Modified: Sat, 27 Jan 2024 03:52:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e558676aa302b7115d8f82a72be4ecee311c17af5113163eee4f9b9b767145ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73716468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc397091ebf77dd35d5aaffc2beb40d48d8d32fd67cfbb9319925794473101eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 09:19:43 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 09:19:43 GMT
ARG KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 09:19:43 GMT
ENV KONG_VERSION=3.1.1
# Sat, 27 Jan 2024 09:19:44 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Sat, 27 Jan 2024 09:19:44 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Sat, 27 Jan 2024 09:19:44 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 09:19:44 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 09:19:44 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 09:19:49 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 09:19:50 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 09:19:50 GMT
USER kong
# Sat, 27 Jan 2024 09:19:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 09:19:50 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 09:19:50 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 09:19:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 09:19:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9df6da955aca6e08795cc34d8f1a36c9e7802c9dc1764c648256e0c26e9f26`  
		Last Modified: Sat, 27 Jan 2024 09:20:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2745fcc6a3a0fb60f58e24afb12c414c1ba2d9c9a514b8ad87784bed6d8428a8`  
		Last Modified: Sat, 27 Jan 2024 09:20:35 GMT  
		Size: 71.0 MB (71007169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04afbc8bfa7f8ea46f46e7dbb1611ceda9f3a5d7caaf115c4781ec1a866a4a79`  
		Last Modified: Sat, 27 Jan 2024 09:20:28 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1-ubuntu`

```console
$ docker pull kong@sha256:7c87a6055b5bd80b0e8ecd72d4cb84b7ed6ee08970f446094085a6989453a5fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:21e93c0e650ed9d3629ef08ff1ac7b526d1a17af84b31383bc1350a9dcdd3b31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101919072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef9e25a07b51def8a679e0deac7b0ba577ca58302b3964fa2cf60cd4ee6aad1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:31:39 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:31:39 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:31:39 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:31:40 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:31:40 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:31:40 GMT
ARG KONG_VERSION=3.1.1
# Fri, 02 Feb 2024 07:31:40 GMT
ENV KONG_VERSION=3.1.1
# Fri, 02 Feb 2024 07:31:40 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Fri, 02 Feb 2024 07:31:40 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Fri, 02 Feb 2024 07:32:05 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:32:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:32:06 GMT
USER kong
# Fri, 02 Feb 2024 07:32:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:32:06 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:32:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:32:06 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:32:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59868e3e33c139839859b72dbaaa269ebcb409bb4ad298714a6ee184c9add37`  
		Last Modified: Fri, 02 Feb 2024 07:34:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df464fdec1b52ba6d33d3d87877e4bf6b5f692fc87f87076808a7a180fabed22`  
		Last Modified: Fri, 02 Feb 2024 07:34:53 GMT  
		Size: 73.3 MB (73333604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7805240893333a133df0a94e2635da22bd327a62e73d2919d0f52b881bef3803`  
		Last Modified: Fri, 02 Feb 2024 07:34:41 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8f9413461730df9ffe7658d8dd59046d2d25530ec9874be82094932cbc70109a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99178377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f892aa03a697a59dcec51e9ffc064b9014b31a1f2de9370602e7b3f1f5d5b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:05:58 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:05:58 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:05:58 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:05:58 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:05:58 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:58 GMT
ARG KONG_VERSION=3.1.1
# Fri, 02 Feb 2024 02:05:58 GMT
ENV KONG_VERSION=3.1.1
# Fri, 02 Feb 2024 02:05:58 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Fri, 02 Feb 2024 02:05:58 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Fri, 02 Feb 2024 02:06:27 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:06:28 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:06:28 GMT
USER kong
# Fri, 02 Feb 2024 02:06:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:06:28 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:06:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:06:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:06:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:beb9e0b551f10db0eea20b2fc47ad9cb3a7f0f338845eeb162a82fec32843b1a`  
		Last Modified: Wed, 24 Jan 2024 18:44:36 GMT  
		Size: 27.2 MB (27205060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945c0be80e646727d5d4ba6c543f57c71fd14e633a90f653a2b908a84fc9e966`  
		Last Modified: Fri, 02 Feb 2024 02:08:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2b3e33419c6c925a6a156a558c75b92e165ca5f6559220a7b773f3b0da5172`  
		Last Modified: Fri, 02 Feb 2024 02:08:54 GMT  
		Size: 72.0 MB (71972312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a891f62a4f1177043dc9b1259f11b620a8febcf9d7ec53013da80327ba609`  
		Last Modified: Fri, 02 Feb 2024 02:08:45 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2`

```console
$ docker pull kong@sha256:c50b66ff09616505e893d7cd610c9bf7a1462f8ca5e974be2cb5d41d5651e0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2` - linux; amd64

```console
$ docker pull kong@sha256:d2898d0d2761bbcc5f87a5fa7537d7d8140b399fdad5b66e35f2e4de22e26297
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74498840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7aa4dcca561526023167096d96cf6dd1c16be0fa94d12e7c6d98ef0cba1e37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 07:31:13 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Feb 2024 07:31:30 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:31:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:31:31 GMT
USER kong
# Fri, 02 Feb 2024 07:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:31:31 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:31:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:31:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:31:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632bed0c8d0ac4d392f380bb9c086570a5a34a58e577fab51c6da2714b2f4eb1`  
		Last Modified: Fri, 02 Feb 2024 07:34:25 GMT  
		Size: 44.0 MB (44049682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545fc6f5e4f6b91845d362d1fd6d754b1a7f029c8c4579458455f469a095bd89`  
		Last Modified: Fri, 02 Feb 2024 07:34:18 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:258435f249006def686068b0a9f918f06eafde1eeb2af2611de9d72b58580262
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78611826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547e53fdfb8ef9f98ff0573dcdcd23ebf8c07b1d59e5189c20de391e6d7f400`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:36 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 02:05:36 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 02:05:37 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Feb 2024 02:05:37 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Feb 2024 02:05:53 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:54 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:54 GMT
USER kong
# Fri, 02 Feb 2024 02:05:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:54 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68487436458cc3c7bccfba09b0931a8cec5deffaa093f22e5c899254f845ef05`  
		Last Modified: Fri, 02 Feb 2024 02:08:31 GMT  
		Size: 50.2 MB (50210438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d40d18bb4d230ff5bcd21981a91ded4b494a7931651de97c28905e9f1db86b4`  
		Last Modified: Fri, 02 Feb 2024 02:08:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2-ubuntu`

```console
$ docker pull kong@sha256:c50b66ff09616505e893d7cd610c9bf7a1462f8ca5e974be2cb5d41d5651e0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d2898d0d2761bbcc5f87a5fa7537d7d8140b399fdad5b66e35f2e4de22e26297
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74498840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7aa4dcca561526023167096d96cf6dd1c16be0fa94d12e7c6d98ef0cba1e37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 07:31:13 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Feb 2024 07:31:30 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:31:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:31:31 GMT
USER kong
# Fri, 02 Feb 2024 07:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:31:31 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:31:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:31:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:31:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632bed0c8d0ac4d392f380bb9c086570a5a34a58e577fab51c6da2714b2f4eb1`  
		Last Modified: Fri, 02 Feb 2024 07:34:25 GMT  
		Size: 44.0 MB (44049682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545fc6f5e4f6b91845d362d1fd6d754b1a7f029c8c4579458455f469a095bd89`  
		Last Modified: Fri, 02 Feb 2024 07:34:18 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:258435f249006def686068b0a9f918f06eafde1eeb2af2611de9d72b58580262
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78611826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547e53fdfb8ef9f98ff0573dcdcd23ebf8c07b1d59e5189c20de391e6d7f400`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:36 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 02:05:36 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 02:05:37 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Feb 2024 02:05:37 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Feb 2024 02:05:53 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:54 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:54 GMT
USER kong
# Fri, 02 Feb 2024 02:05:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:54 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68487436458cc3c7bccfba09b0931a8cec5deffaa093f22e5c899254f845ef05`  
		Last Modified: Fri, 02 Feb 2024 02:08:31 GMT  
		Size: 50.2 MB (50210438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d40d18bb4d230ff5bcd21981a91ded4b494a7931651de97c28905e9f1db86b4`  
		Last Modified: Fri, 02 Feb 2024 02:08:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2`

```console
$ docker pull kong@sha256:c50b66ff09616505e893d7cd610c9bf7a1462f8ca5e974be2cb5d41d5651e0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2.2` - linux; amd64

```console
$ docker pull kong@sha256:d2898d0d2761bbcc5f87a5fa7537d7d8140b399fdad5b66e35f2e4de22e26297
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74498840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7aa4dcca561526023167096d96cf6dd1c16be0fa94d12e7c6d98ef0cba1e37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 07:31:13 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Feb 2024 07:31:30 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:31:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:31:31 GMT
USER kong
# Fri, 02 Feb 2024 07:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:31:31 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:31:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:31:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:31:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632bed0c8d0ac4d392f380bb9c086570a5a34a58e577fab51c6da2714b2f4eb1`  
		Last Modified: Fri, 02 Feb 2024 07:34:25 GMT  
		Size: 44.0 MB (44049682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545fc6f5e4f6b91845d362d1fd6d754b1a7f029c8c4579458455f469a095bd89`  
		Last Modified: Fri, 02 Feb 2024 07:34:18 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:258435f249006def686068b0a9f918f06eafde1eeb2af2611de9d72b58580262
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78611826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547e53fdfb8ef9f98ff0573dcdcd23ebf8c07b1d59e5189c20de391e6d7f400`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:36 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 02:05:36 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 02:05:37 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Feb 2024 02:05:37 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Feb 2024 02:05:53 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:54 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:54 GMT
USER kong
# Fri, 02 Feb 2024 02:05:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:54 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68487436458cc3c7bccfba09b0931a8cec5deffaa093f22e5c899254f845ef05`  
		Last Modified: Fri, 02 Feb 2024 02:08:31 GMT  
		Size: 50.2 MB (50210438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d40d18bb4d230ff5bcd21981a91ded4b494a7931651de97c28905e9f1db86b4`  
		Last Modified: Fri, 02 Feb 2024 02:08:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2-alpine`

```console
$ docker pull kong@sha256:0988867b9421b42dfa0f4dcb98c4b3541e58e74464c0615ebe656ccf80c75706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:3.2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:b23a9d2fe62702e3828751fee0c1f674514f82e83d275ef9d0539d343179f189
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36931908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c52c5c974fc0e315f85e461961f084f1b787276b5cec40e525f74a3e593070`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:50:39 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 03:50:52 GMT
ARG KONG_VERSION=3.2.2
# Sat, 27 Jan 2024 03:50:52 GMT
ENV KONG_VERSION=3.2.2
# Sat, 27 Jan 2024 03:50:52 GMT
ARG KONG_SHA256=a07c3bc0307e2d8fe33acb8be5fe659f348279540eaa267bc6968005094835ef
# Sat, 27 Jan 2024 03:50:52 GMT
ARG KONG_PREFIX=/usr/local/kong
# Sat, 27 Jan 2024 03:50:52 GMT
ENV KONG_PREFIX=/usr/local/kong
# Sat, 27 Jan 2024 03:50:52 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 03:50:52 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:50:52 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 03:50:58 GMT
# ARGS: ASSET=remote KONG_SHA256=a07c3bc0307e2d8fe33acb8be5fe659f348279540eaa267bc6968005094835ef
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 03:50:59 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:50:59 GMT
USER kong
# Sat, 27 Jan 2024 03:50:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:50:59 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:50:59 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:50:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:50:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee27ec06dee9be3482200f7e344cbe9a42e72820c3dc88b2784ae146276a8071`  
		Last Modified: Sat, 27 Jan 2024 03:52:12 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa106ffb364a695af306bc038a87c19d3a8db853d60f958989ed5a3743ec828`  
		Last Modified: Sat, 27 Jan 2024 03:52:17 GMT  
		Size: 33.6 MB (33551212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733a88957d542bce47d54262dd4d25c542a4446092d97d4a0e8162f8c2518bfc`  
		Last Modified: Sat, 27 Jan 2024 03:52:12 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2-ubuntu`

```console
$ docker pull kong@sha256:c50b66ff09616505e893d7cd610c9bf7a1462f8ca5e974be2cb5d41d5651e0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d2898d0d2761bbcc5f87a5fa7537d7d8140b399fdad5b66e35f2e4de22e26297
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74498840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7aa4dcca561526023167096d96cf6dd1c16be0fa94d12e7c6d98ef0cba1e37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 07:31:13 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Feb 2024 07:31:13 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Feb 2024 07:31:30 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:31:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:31:31 GMT
USER kong
# Fri, 02 Feb 2024 07:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:31:31 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:31:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:31:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:31:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632bed0c8d0ac4d392f380bb9c086570a5a34a58e577fab51c6da2714b2f4eb1`  
		Last Modified: Fri, 02 Feb 2024 07:34:25 GMT  
		Size: 44.0 MB (44049682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545fc6f5e4f6b91845d362d1fd6d754b1a7f029c8c4579458455f469a095bd89`  
		Last Modified: Fri, 02 Feb 2024 07:34:18 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:258435f249006def686068b0a9f918f06eafde1eeb2af2611de9d72b58580262
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78611826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547e53fdfb8ef9f98ff0573dcdcd23ebf8c07b1d59e5189c20de391e6d7f400`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:36 GMT
ARG KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 02:05:36 GMT
ENV KONG_VERSION=3.2.2
# Fri, 02 Feb 2024 02:05:37 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Fri, 02 Feb 2024 02:05:37 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Fri, 02 Feb 2024 02:05:53 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:54 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:54 GMT
USER kong
# Fri, 02 Feb 2024 02:05:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:54 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68487436458cc3c7bccfba09b0931a8cec5deffaa093f22e5c899254f845ef05`  
		Last Modified: Fri, 02 Feb 2024 02:08:31 GMT  
		Size: 50.2 MB (50210438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d40d18bb4d230ff5bcd21981a91ded4b494a7931651de97c28905e9f1db86b4`  
		Last Modified: Fri, 02 Feb 2024 02:08:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3`

```console
$ docker pull kong@sha256:671ada76fdb101343f79271e59df91905ae4726000379a29aa0fd552ae9a8934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3` - linux; amd64

```console
$ docker pull kong@sha256:d92bf1a867d08a59e13a26956706d752f0bdd59bbdb0bd4bdaca8c753fe4657d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81349196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad893bccc7de6249845a5dfc261e4b60f8df94c5809bba58fd8e5f9f253c2a38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 07:30:29 GMT
ENV KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 02 Feb 2024 07:31:01 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:31:02 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:31:02 GMT
USER kong
# Fri, 02 Feb 2024 07:31:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:31:02 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:31:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:31:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:31:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c96f7ddb5eca819e90a0c2f3def53505e1fb83bf91416b1f96efa7191c9b86`  
		Last Modified: Fri, 02 Feb 2024 07:34:06 GMT  
		Size: 50.9 MB (50900036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a3107a4dddf3695946d038ea0b62a1b0afc9146d3e7d348d03939086793774`  
		Last Modified: Fri, 02 Feb 2024 07:33:58 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:612bca9f0e57d35596155baa00ef1c39a06226c395450885c583143f1e352ec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75762516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7812ed217ec2d1781d6bb4573134149932bf04448089ba2940e5a7c8d572c5d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:08 GMT
ARG KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 02:05:08 GMT
ENV KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 02:05:08 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 02 Feb 2024 02:05:09 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 02 Feb 2024 02:05:33 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:34 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:34 GMT
USER kong
# Fri, 02 Feb 2024 02:05:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:34 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05401bc333caa74ae5f51fe81458547154479844a995898f1a6dbb9a5709dcfe`  
		Last Modified: Fri, 02 Feb 2024 02:08:08 GMT  
		Size: 47.4 MB (47361128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79a00afc6ac0819b76cced6d6dfe538adfebad3a24a0a614a8a3cc254773c54`  
		Last Modified: Fri, 02 Feb 2024 02:08:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3-ubuntu`

```console
$ docker pull kong@sha256:671ada76fdb101343f79271e59df91905ae4726000379a29aa0fd552ae9a8934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d92bf1a867d08a59e13a26956706d752f0bdd59bbdb0bd4bdaca8c753fe4657d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81349196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad893bccc7de6249845a5dfc261e4b60f8df94c5809bba58fd8e5f9f253c2a38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 07:30:29 GMT
ENV KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 02 Feb 2024 07:31:01 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:31:02 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:31:02 GMT
USER kong
# Fri, 02 Feb 2024 07:31:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:31:02 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:31:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:31:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:31:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c96f7ddb5eca819e90a0c2f3def53505e1fb83bf91416b1f96efa7191c9b86`  
		Last Modified: Fri, 02 Feb 2024 07:34:06 GMT  
		Size: 50.9 MB (50900036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a3107a4dddf3695946d038ea0b62a1b0afc9146d3e7d348d03939086793774`  
		Last Modified: Fri, 02 Feb 2024 07:33:58 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:612bca9f0e57d35596155baa00ef1c39a06226c395450885c583143f1e352ec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75762516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7812ed217ec2d1781d6bb4573134149932bf04448089ba2940e5a7c8d572c5d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:08 GMT
ARG KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 02:05:08 GMT
ENV KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 02:05:08 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 02 Feb 2024 02:05:09 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 02 Feb 2024 02:05:33 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:34 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:34 GMT
USER kong
# Fri, 02 Feb 2024 02:05:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:34 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05401bc333caa74ae5f51fe81458547154479844a995898f1a6dbb9a5709dcfe`  
		Last Modified: Fri, 02 Feb 2024 02:08:08 GMT  
		Size: 47.4 MB (47361128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79a00afc6ac0819b76cced6d6dfe538adfebad3a24a0a614a8a3cc254773c54`  
		Last Modified: Fri, 02 Feb 2024 02:08:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1`

```console
$ docker pull kong@sha256:671ada76fdb101343f79271e59df91905ae4726000379a29aa0fd552ae9a8934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.1` - linux; amd64

```console
$ docker pull kong@sha256:d92bf1a867d08a59e13a26956706d752f0bdd59bbdb0bd4bdaca8c753fe4657d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81349196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad893bccc7de6249845a5dfc261e4b60f8df94c5809bba58fd8e5f9f253c2a38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 07:30:29 GMT
ENV KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 02 Feb 2024 07:31:01 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:31:02 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:31:02 GMT
USER kong
# Fri, 02 Feb 2024 07:31:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:31:02 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:31:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:31:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:31:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c96f7ddb5eca819e90a0c2f3def53505e1fb83bf91416b1f96efa7191c9b86`  
		Last Modified: Fri, 02 Feb 2024 07:34:06 GMT  
		Size: 50.9 MB (50900036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a3107a4dddf3695946d038ea0b62a1b0afc9146d3e7d348d03939086793774`  
		Last Modified: Fri, 02 Feb 2024 07:33:58 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:612bca9f0e57d35596155baa00ef1c39a06226c395450885c583143f1e352ec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75762516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7812ed217ec2d1781d6bb4573134149932bf04448089ba2940e5a7c8d572c5d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:08 GMT
ARG KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 02:05:08 GMT
ENV KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 02:05:08 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 02 Feb 2024 02:05:09 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 02 Feb 2024 02:05:33 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:34 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:34 GMT
USER kong
# Fri, 02 Feb 2024 02:05:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:34 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05401bc333caa74ae5f51fe81458547154479844a995898f1a6dbb9a5709dcfe`  
		Last Modified: Fri, 02 Feb 2024 02:08:08 GMT  
		Size: 47.4 MB (47361128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79a00afc6ac0819b76cced6d6dfe538adfebad3a24a0a614a8a3cc254773c54`  
		Last Modified: Fri, 02 Feb 2024 02:08:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1-alpine`

```console
$ docker pull kong@sha256:cbb0b61a591c9484cbf2a37b5850057e54d4dc96f8c07c07001cf1e47315829d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:3.3.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:c4a028c24c2e8b5d81d686a7c411ec4c4f80f1dcd495ea6c1026e4b7b8f8ab29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34231634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92def505322dce3d2b96b9ad20c95b6b5cc025658a2fa427c9fd73776c59dc8b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:50:39 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_VERSION=3.3.1
# Sat, 27 Jan 2024 03:50:39 GMT
ENV KONG_VERSION=3.3.1
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_PREFIX=/usr/local/kong
# Sat, 27 Jan 2024 03:50:39 GMT
ENV KONG_PREFIX=/usr/local/kong
# Sat, 27 Jan 2024 03:50:39 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 03:50:39 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:50:39 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 03:50:45 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     KONG_SHA256=$KONG_AMD64_SHA ;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 03:50:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:50:46 GMT
USER kong
# Sat, 27 Jan 2024 03:50:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:50:46 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:50:46 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:50:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:50:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2059c54846f7238a7e9e662c2ddd540de2c4db29fab44c43fbe070b39b8b61`  
		Last Modified: Sat, 27 Jan 2024 03:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50c3036110cfbae400e5b2fd68ce10ecf07c0cad0a9a0754f202ef6114c8a5c`  
		Last Modified: Sat, 27 Jan 2024 03:52:03 GMT  
		Size: 30.9 MB (30850943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713fc864f01da83252ecef138198826f49c9ca9603f4d8cc9a7b2f5e2a8bcd3e`  
		Last Modified: Sat, 27 Jan 2024 03:51:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1-ubuntu`

```console
$ docker pull kong@sha256:671ada76fdb101343f79271e59df91905ae4726000379a29aa0fd552ae9a8934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d92bf1a867d08a59e13a26956706d752f0bdd59bbdb0bd4bdaca8c753fe4657d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81349196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad893bccc7de6249845a5dfc261e4b60f8df94c5809bba58fd8e5f9f253c2a38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 07:30:29 GMT
ENV KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 02 Feb 2024 07:30:29 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 02 Feb 2024 07:31:01 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:31:02 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:31:02 GMT
USER kong
# Fri, 02 Feb 2024 07:31:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:31:02 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:31:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:31:02 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:31:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c96f7ddb5eca819e90a0c2f3def53505e1fb83bf91416b1f96efa7191c9b86`  
		Last Modified: Fri, 02 Feb 2024 07:34:06 GMT  
		Size: 50.9 MB (50900036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a3107a4dddf3695946d038ea0b62a1b0afc9146d3e7d348d03939086793774`  
		Last Modified: Fri, 02 Feb 2024 07:33:58 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:612bca9f0e57d35596155baa00ef1c39a06226c395450885c583143f1e352ec4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75762516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7812ed217ec2d1781d6bb4573134149932bf04448089ba2940e5a7c8d572c5d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:05:08 GMT
ARG KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 02:05:08 GMT
ENV KONG_VERSION=3.3.1
# Fri, 02 Feb 2024 02:05:08 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 02 Feb 2024 02:05:09 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 02 Feb 2024 02:05:33 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:34 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:34 GMT
USER kong
# Fri, 02 Feb 2024 02:05:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:34 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05401bc333caa74ae5f51fe81458547154479844a995898f1a6dbb9a5709dcfe`  
		Last Modified: Fri, 02 Feb 2024 02:08:08 GMT  
		Size: 47.4 MB (47361128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79a00afc6ac0819b76cced6d6dfe538adfebad3a24a0a614a8a3cc254773c54`  
		Last Modified: Fri, 02 Feb 2024 02:08:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4`

```console
$ docker pull kong@sha256:285383f91e00e04b331a245ed5bfefa66ef20e6d851a426ba38424f3fec3a317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:3d03346a97b8b0ec226b33967c500f901305caedb80e1ea24506c702bc792015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93171872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b45f79fd6ffa5419ffeb974b47dac6efda06c2a5d1a95a48b756e7ca71f365`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 07:30:03 GMT
ENV KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 02 Feb 2024 07:30:22 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:30:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:30:23 GMT
USER kong
# Fri, 02 Feb 2024 07:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:30:23 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:30:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:30:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:30:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03bbe1ce30f04e3cc31542d06bae6011dd3ebcc1a4cb473d17498d600813695`  
		Last Modified: Fri, 02 Feb 2024 07:33:45 GMT  
		Size: 62.7 MB (62722712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db12840ce22ef00424ea3ebbca556e35ae53fa157e7ba006d1df4a4c091b70b`  
		Last Modified: Fri, 02 Feb 2024 07:33:35 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:758f6fb72c260efb4dfdc39272b2853feddc40b5606c5678734efcdc8284f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89562230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6d7314ca6fc8075afb98f9508720360db5ea4e3b670892eda314e2483123d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 02:04:49 GMT
ENV KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 02 Feb 2024 02:05:04 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:05 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:05 GMT
USER kong
# Fri, 02 Feb 2024 02:05:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:05 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786b9043f6111226ed6848afee2ab8af00c90dfa9a6a1cf03621f11b1dc509bd`  
		Last Modified: Fri, 02 Feb 2024 02:07:49 GMT  
		Size: 61.2 MB (61160842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee66e10bd3123bdd47ecef975e40469de839a94b6af7c377317e68cdfdd95f`  
		Last Modified: Fri, 02 Feb 2024 02:07:42 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:285383f91e00e04b331a245ed5bfefa66ef20e6d851a426ba38424f3fec3a317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3d03346a97b8b0ec226b33967c500f901305caedb80e1ea24506c702bc792015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93171872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b45f79fd6ffa5419ffeb974b47dac6efda06c2a5d1a95a48b756e7ca71f365`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 07:30:03 GMT
ENV KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 02 Feb 2024 07:30:22 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:30:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:30:23 GMT
USER kong
# Fri, 02 Feb 2024 07:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:30:23 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:30:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:30:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:30:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03bbe1ce30f04e3cc31542d06bae6011dd3ebcc1a4cb473d17498d600813695`  
		Last Modified: Fri, 02 Feb 2024 07:33:45 GMT  
		Size: 62.7 MB (62722712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db12840ce22ef00424ea3ebbca556e35ae53fa157e7ba006d1df4a4c091b70b`  
		Last Modified: Fri, 02 Feb 2024 07:33:35 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:758f6fb72c260efb4dfdc39272b2853feddc40b5606c5678734efcdc8284f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89562230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6d7314ca6fc8075afb98f9508720360db5ea4e3b670892eda314e2483123d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 02:04:49 GMT
ENV KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 02 Feb 2024 02:05:04 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:05 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:05 GMT
USER kong
# Fri, 02 Feb 2024 02:05:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:05 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786b9043f6111226ed6848afee2ab8af00c90dfa9a6a1cf03621f11b1dc509bd`  
		Last Modified: Fri, 02 Feb 2024 02:07:49 GMT  
		Size: 61.2 MB (61160842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee66e10bd3123bdd47ecef975e40469de839a94b6af7c377317e68cdfdd95f`  
		Last Modified: Fri, 02 Feb 2024 02:07:42 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2`

```console
$ docker pull kong@sha256:285383f91e00e04b331a245ed5bfefa66ef20e6d851a426ba38424f3fec3a317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:3d03346a97b8b0ec226b33967c500f901305caedb80e1ea24506c702bc792015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93171872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b45f79fd6ffa5419ffeb974b47dac6efda06c2a5d1a95a48b756e7ca71f365`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 07:30:03 GMT
ENV KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 02 Feb 2024 07:30:22 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:30:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:30:23 GMT
USER kong
# Fri, 02 Feb 2024 07:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:30:23 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:30:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:30:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:30:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03bbe1ce30f04e3cc31542d06bae6011dd3ebcc1a4cb473d17498d600813695`  
		Last Modified: Fri, 02 Feb 2024 07:33:45 GMT  
		Size: 62.7 MB (62722712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db12840ce22ef00424ea3ebbca556e35ae53fa157e7ba006d1df4a4c091b70b`  
		Last Modified: Fri, 02 Feb 2024 07:33:35 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:758f6fb72c260efb4dfdc39272b2853feddc40b5606c5678734efcdc8284f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89562230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6d7314ca6fc8075afb98f9508720360db5ea4e3b670892eda314e2483123d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 02:04:49 GMT
ENV KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 02 Feb 2024 02:05:04 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:05 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:05 GMT
USER kong
# Fri, 02 Feb 2024 02:05:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:05 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786b9043f6111226ed6848afee2ab8af00c90dfa9a6a1cf03621f11b1dc509bd`  
		Last Modified: Fri, 02 Feb 2024 02:07:49 GMT  
		Size: 61.2 MB (61160842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee66e10bd3123bdd47ecef975e40469de839a94b6af7c377317e68cdfdd95f`  
		Last Modified: Fri, 02 Feb 2024 02:07:42 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:285383f91e00e04b331a245ed5bfefa66ef20e6d851a426ba38424f3fec3a317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3d03346a97b8b0ec226b33967c500f901305caedb80e1ea24506c702bc792015
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93171872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b45f79fd6ffa5419ffeb974b47dac6efda06c2a5d1a95a48b756e7ca71f365`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 07:30:03 GMT
ENV KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 02 Feb 2024 07:30:03 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 02 Feb 2024 07:30:22 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:30:23 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:30:23 GMT
USER kong
# Fri, 02 Feb 2024 07:30:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:30:23 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:30:23 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:30:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:30:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03bbe1ce30f04e3cc31542d06bae6011dd3ebcc1a4cb473d17498d600813695`  
		Last Modified: Fri, 02 Feb 2024 07:33:45 GMT  
		Size: 62.7 MB (62722712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db12840ce22ef00424ea3ebbca556e35ae53fa157e7ba006d1df4a4c091b70b`  
		Last Modified: Fri, 02 Feb 2024 07:33:35 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:758f6fb72c260efb4dfdc39272b2853feddc40b5606c5678734efcdc8284f8c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89562230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6d7314ca6fc8075afb98f9508720360db5ea4e3b670892eda314e2483123d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 02:04:49 GMT
ENV KONG_VERSION=3.4.2
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 02 Feb 2024 02:04:49 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 02 Feb 2024 02:05:04 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:05:05 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:05:05 GMT
USER kong
# Fri, 02 Feb 2024 02:05:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:05:05 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:05:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:05:05 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:05:05 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786b9043f6111226ed6848afee2ab8af00c90dfa9a6a1cf03621f11b1dc509bd`  
		Last Modified: Fri, 02 Feb 2024 02:07:49 GMT  
		Size: 61.2 MB (61160842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee66e10bd3123bdd47ecef975e40469de839a94b6af7c377317e68cdfdd95f`  
		Last Modified: Fri, 02 Feb 2024 02:07:42 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5`

```console
$ docker pull kong@sha256:f49d0a9261a850aa82788ecf0b64474d965fc8baf17cbee68687f21fbcb7f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5` - linux; amd64

```console
$ docker pull kong@sha256:ff03eb11f67d73f74747840fb052f2e01b53e560c039b82f78beb256b2497467
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d6d5e8a04fb00f97161dd265608d428df838b8dcb24570650387373ef4422`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 07:29:58 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:29:59 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:29:59 GMT
USER kong
# Fri, 02 Feb 2024 07:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:29:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:29:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:29:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:29:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75647976f218a637e1f8fbf664bf81d67743a41f121b477844760d429c65d303`  
		Last Modified: Fri, 02 Feb 2024 07:33:18 GMT  
		Size: 64.0 MB (63959063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c71490554f68130975444ccc887639f6093bde5617563817ab3b9a7fac5a21`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:641ebb8b331f431f480217585bfd6b4950ef8751b8e0246156051f06d4c9a231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6105956b06bb453e1af507ca0084eccc513ace226b77d8ddef86697d9679066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 02:04:42 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:04:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:04:43 GMT
USER kong
# Fri, 02 Feb 2024 02:04:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:04:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:04:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:04:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7812175ddcfaaa6e1d23578b162b7804abc0028f957d916fb554b30e0b20d275`  
		Last Modified: Fri, 02 Feb 2024 02:07:23 GMT  
		Size: 63.5 MB (63486306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457282a5822c35a448fdf61a792b9cae3d9f593e4a83b3f05dfc337f05836de8`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5-ubuntu`

```console
$ docker pull kong@sha256:f49d0a9261a850aa82788ecf0b64474d965fc8baf17cbee68687f21fbcb7f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ff03eb11f67d73f74747840fb052f2e01b53e560c039b82f78beb256b2497467
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d6d5e8a04fb00f97161dd265608d428df838b8dcb24570650387373ef4422`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 07:29:58 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:29:59 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:29:59 GMT
USER kong
# Fri, 02 Feb 2024 07:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:29:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:29:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:29:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:29:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75647976f218a637e1f8fbf664bf81d67743a41f121b477844760d429c65d303`  
		Last Modified: Fri, 02 Feb 2024 07:33:18 GMT  
		Size: 64.0 MB (63959063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c71490554f68130975444ccc887639f6093bde5617563817ab3b9a7fac5a21`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:641ebb8b331f431f480217585bfd6b4950ef8751b8e0246156051f06d4c9a231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6105956b06bb453e1af507ca0084eccc513ace226b77d8ddef86697d9679066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 02:04:42 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:04:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:04:43 GMT
USER kong
# Fri, 02 Feb 2024 02:04:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:04:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:04:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:04:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7812175ddcfaaa6e1d23578b162b7804abc0028f957d916fb554b30e0b20d275`  
		Last Modified: Fri, 02 Feb 2024 02:07:23 GMT  
		Size: 63.5 MB (63486306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457282a5822c35a448fdf61a792b9cae3d9f593e4a83b3f05dfc337f05836de8`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0`

```console
$ docker pull kong@sha256:f49d0a9261a850aa82788ecf0b64474d965fc8baf17cbee68687f21fbcb7f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0` - linux; amd64

```console
$ docker pull kong@sha256:ff03eb11f67d73f74747840fb052f2e01b53e560c039b82f78beb256b2497467
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d6d5e8a04fb00f97161dd265608d428df838b8dcb24570650387373ef4422`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 07:29:58 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:29:59 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:29:59 GMT
USER kong
# Fri, 02 Feb 2024 07:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:29:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:29:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:29:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:29:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75647976f218a637e1f8fbf664bf81d67743a41f121b477844760d429c65d303`  
		Last Modified: Fri, 02 Feb 2024 07:33:18 GMT  
		Size: 64.0 MB (63959063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c71490554f68130975444ccc887639f6093bde5617563817ab3b9a7fac5a21`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:641ebb8b331f431f480217585bfd6b4950ef8751b8e0246156051f06d4c9a231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6105956b06bb453e1af507ca0084eccc513ace226b77d8ddef86697d9679066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 02:04:42 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:04:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:04:43 GMT
USER kong
# Fri, 02 Feb 2024 02:04:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:04:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:04:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:04:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7812175ddcfaaa6e1d23578b162b7804abc0028f957d916fb554b30e0b20d275`  
		Last Modified: Fri, 02 Feb 2024 02:07:23 GMT  
		Size: 63.5 MB (63486306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457282a5822c35a448fdf61a792b9cae3d9f593e4a83b3f05dfc337f05836de8`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0-ubuntu`

```console
$ docker pull kong@sha256:f49d0a9261a850aa82788ecf0b64474d965fc8baf17cbee68687f21fbcb7f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ff03eb11f67d73f74747840fb052f2e01b53e560c039b82f78beb256b2497467
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d6d5e8a04fb00f97161dd265608d428df838b8dcb24570650387373ef4422`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 07:29:58 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:29:59 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:29:59 GMT
USER kong
# Fri, 02 Feb 2024 07:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:29:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:29:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:29:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:29:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75647976f218a637e1f8fbf664bf81d67743a41f121b477844760d429c65d303`  
		Last Modified: Fri, 02 Feb 2024 07:33:18 GMT  
		Size: 64.0 MB (63959063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c71490554f68130975444ccc887639f6093bde5617563817ab3b9a7fac5a21`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:641ebb8b331f431f480217585bfd6b4950ef8751b8e0246156051f06d4c9a231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6105956b06bb453e1af507ca0084eccc513ace226b77d8ddef86697d9679066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 02:04:42 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:04:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:04:43 GMT
USER kong
# Fri, 02 Feb 2024 02:04:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:04:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:04:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:04:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7812175ddcfaaa6e1d23578b162b7804abc0028f957d916fb554b30e0b20d275`  
		Last Modified: Fri, 02 Feb 2024 02:07:23 GMT  
		Size: 63.5 MB (63486306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457282a5822c35a448fdf61a792b9cae3d9f593e4a83b3f05dfc337f05836de8`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:cbb0b61a591c9484cbf2a37b5850057e54d4dc96f8c07c07001cf1e47315829d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:c4a028c24c2e8b5d81d686a7c411ec4c4f80f1dcd495ea6c1026e4b7b8f8ab29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34231634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92def505322dce3d2b96b9ad20c95b6b5cc025658a2fa427c9fd73776c59dc8b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:02 GMT
ADD file:c44c9bd36ba35cc78fb9396304ea008def9f42a3beef76aa33b2cf1fde1c10b3 in / 
# Sat, 27 Jan 2024 00:31:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:50:39 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_VERSION=3.3.1
# Sat, 27 Jan 2024 03:50:39 GMT
ENV KONG_VERSION=3.3.1
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
# Sat, 27 Jan 2024 03:50:39 GMT
ARG KONG_PREFIX=/usr/local/kong
# Sat, 27 Jan 2024 03:50:39 GMT
ENV KONG_PREFIX=/usr/local/kong
# Sat, 27 Jan 2024 03:50:39 GMT
ARG ASSET=remote
# Sat, 27 Jan 2024 03:50:39 GMT
ARG EE_PORTS
# Sat, 27 Jan 2024 03:50:39 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Sat, 27 Jan 2024 03:50:45 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     KONG_SHA256=$KONG_AMD64_SHA ;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Sat, 27 Jan 2024 03:50:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:50:46 GMT
USER kong
# Sat, 27 Jan 2024 03:50:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:50:46 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 27 Jan 2024 03:50:46 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:50:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Sat, 27 Jan 2024 03:50:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3c854c8cbf469fda815b8f6183300c07cfa2fbb5703859ca79aff93ae934961b`  
		Last Modified: Sat, 27 Jan 2024 00:31:44 GMT  
		Size: 3.4 MB (3379404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2059c54846f7238a7e9e662c2ddd540de2c4db29fab44c43fbe070b39b8b61`  
		Last Modified: Sat, 27 Jan 2024 03:51:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50c3036110cfbae400e5b2fd68ce10ecf07c0cad0a9a0754f202ef6114c8a5c`  
		Last Modified: Sat, 27 Jan 2024 03:52:03 GMT  
		Size: 30.9 MB (30850943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713fc864f01da83252ecef138198826f49c9ca9603f4d8cc9a7b2f5e2a8bcd3e`  
		Last Modified: Sat, 27 Jan 2024 03:51:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:f49d0a9261a850aa82788ecf0b64474d965fc8baf17cbee68687f21fbcb7f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:ff03eb11f67d73f74747840fb052f2e01b53e560c039b82f78beb256b2497467
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d6d5e8a04fb00f97161dd265608d428df838b8dcb24570650387373ef4422`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 07:29:58 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:29:59 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:29:59 GMT
USER kong
# Fri, 02 Feb 2024 07:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:29:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:29:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:29:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:29:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75647976f218a637e1f8fbf664bf81d67743a41f121b477844760d429c65d303`  
		Last Modified: Fri, 02 Feb 2024 07:33:18 GMT  
		Size: 64.0 MB (63959063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c71490554f68130975444ccc887639f6093bde5617563817ab3b9a7fac5a21`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:641ebb8b331f431f480217585bfd6b4950ef8751b8e0246156051f06d4c9a231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6105956b06bb453e1af507ca0084eccc513ace226b77d8ddef86697d9679066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 02:04:42 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:04:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:04:43 GMT
USER kong
# Fri, 02 Feb 2024 02:04:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:04:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:04:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:04:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7812175ddcfaaa6e1d23578b162b7804abc0028f957d916fb554b30e0b20d275`  
		Last Modified: Fri, 02 Feb 2024 02:07:23 GMT  
		Size: 63.5 MB (63486306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457282a5822c35a448fdf61a792b9cae3d9f593e4a83b3f05dfc337f05836de8`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:f49d0a9261a850aa82788ecf0b64474d965fc8baf17cbee68687f21fbcb7f9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ff03eb11f67d73f74747840fb052f2e01b53e560c039b82f78beb256b2497467
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94408225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107d6d5e8a04fb00f97161dd265608d428df838b8dcb24570650387373ef4422`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 07:29:38 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 07:29:38 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 07:29:38 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 07:29:39 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 07:29:39 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 07:29:58 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 07:29:59 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 07:29:59 GMT
USER kong
# Fri, 02 Feb 2024 07:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 07:29:59 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 07:29:59 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 07:29:59 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 07:29:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf9b7e3d930068dfa084509f2f2fb7c4f6c9af37a98d59cb28d7f9cdad416cb`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75647976f218a637e1f8fbf664bf81d67743a41f121b477844760d429c65d303`  
		Last Modified: Fri, 02 Feb 2024 07:33:18 GMT  
		Size: 64.0 MB (63959063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c71490554f68130975444ccc887639f6093bde5617563817ab3b9a7fac5a21`  
		Last Modified: Fri, 02 Feb 2024 07:33:09 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:641ebb8b331f431f480217585bfd6b4950ef8751b8e0246156051f06d4c9a231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6105956b06bb453e1af507ca0084eccc513ace226b77d8ddef86697d9679066`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:04:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 02 Feb 2024 02:04:25 GMT
ARG ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ENV ASSET=ce
# Fri, 02 Feb 2024 02:04:25 GMT
ARG EE_PORTS
# Fri, 02 Feb 2024 02:04:26 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 02 Feb 2024 02:04:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 02 Feb 2024 02:04:42 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 02 Feb 2024 02:04:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 02 Feb 2024 02:04:43 GMT
USER kong
# Fri, 02 Feb 2024 02:04:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 02 Feb 2024 02:04:43 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 02 Feb 2024 02:04:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 02 Feb 2024 02:04:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 02 Feb 2024 02:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e873cdb43385532c313d9bd37127d6a5891742f8f8120743f17911ce0f806b40`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7812175ddcfaaa6e1d23578b162b7804abc0028f957d916fb554b30e0b20d275`  
		Last Modified: Fri, 02 Feb 2024 02:07:23 GMT  
		Size: 63.5 MB (63486306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457282a5822c35a448fdf61a792b9cae3d9f593e4a83b3f05dfc337f05836de8`  
		Last Modified: Fri, 02 Feb 2024 02:07:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
