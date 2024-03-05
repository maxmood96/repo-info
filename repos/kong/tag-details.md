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
$ docker pull kong@sha256:62bfd28edc3c8adb5ff5bc7f8f1d9d6bf6ec977f0bc14648ec3c94133a674157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7f8b7d14c468a2bf39f90a37c68786454b6252d731ffe92641920c9a2565b0dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116577390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57dc52d3e324ded3c6804428d9d8428a02f6f608043b56ca19be77638c0c3630`
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
# Fri, 16 Feb 2024 02:07:25 GMT
ARG ASSET=ce
# Fri, 16 Feb 2024 02:07:25 GMT
ENV ASSET=ce
# Fri, 16 Feb 2024 02:07:25 GMT
ARG EE_PORTS
# Fri, 16 Feb 2024 02:07:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 16 Feb 2024 02:07:26 GMT
ARG KONG_VERSION=2.8.4
# Fri, 16 Feb 2024 02:07:26 GMT
ENV KONG_VERSION=2.8.4
# Fri, 16 Feb 2024 02:07:26 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Fri, 16 Feb 2024 02:07:26 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 16 Feb 2024 02:07:48 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:07:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:07:49 GMT
USER kong
# Fri, 16 Feb 2024 02:07:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:07:49 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:07:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:07:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:07:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7ba36d33aba1e66b291a2a7f942c19f092bdb36d0fea455ec2589aee8133ad`  
		Last Modified: Fri, 16 Feb 2024 02:10:16 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa5c30ba9fcface501fb09c030dffd044cb3fae4403234fa738aa41a53c0415`  
		Last Modified: Fri, 16 Feb 2024 02:10:25 GMT  
		Size: 61.0 MB (61044471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4767181d1a0827dc32b111186737977a9803669b1a9165edf2837775ee5fc35`  
		Last Modified: Fri, 16 Feb 2024 02:10:15 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:dc60456b49fe33717e9fb2194107af6f5073d61168469381bb5a1ec4b29c58f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113148610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bff69a6ae107167bfa6e4f5ac65995e75a9d5e3e99ad2b66d0ba2d113b415a`
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
# Fri, 16 Feb 2024 05:16:39 GMT
ARG ASSET=ce
# Fri, 16 Feb 2024 05:16:39 GMT
ENV ASSET=ce
# Fri, 16 Feb 2024 05:16:39 GMT
ARG EE_PORTS
# Fri, 16 Feb 2024 05:16:39 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 16 Feb 2024 05:16:39 GMT
ARG KONG_VERSION=2.8.4
# Fri, 16 Feb 2024 05:16:40 GMT
ENV KONG_VERSION=2.8.4
# Fri, 16 Feb 2024 05:16:40 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Fri, 16 Feb 2024 05:16:40 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 16 Feb 2024 05:16:59 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:17:00 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:17:00 GMT
USER kong
# Fri, 16 Feb 2024 05:17:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:17:00 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:17:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:17:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:17:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d22b0f8deecddd8b48423d7e92203b7efb162409403b397f608889f4e13495`  
		Last Modified: Fri, 16 Feb 2024 05:19:10 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54df78066adfb2a5505cccdbbca5937eb601f49de1c5e54d32ff6a87cd6cedc`  
		Last Modified: Fri, 16 Feb 2024 05:19:16 GMT  
		Size: 59.7 MB (59665445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d9ec1801c50d0a6b605e79d72b0daea07cbcb493717cb91d6d49ccd96229a3`  
		Last Modified: Fri, 16 Feb 2024 05:19:09 GMT  
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
$ docker pull kong@sha256:62bfd28edc3c8adb5ff5bc7f8f1d9d6bf6ec977f0bc14648ec3c94133a674157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7f8b7d14c468a2bf39f90a37c68786454b6252d731ffe92641920c9a2565b0dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116577390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57dc52d3e324ded3c6804428d9d8428a02f6f608043b56ca19be77638c0c3630`
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
# Fri, 16 Feb 2024 02:07:25 GMT
ARG ASSET=ce
# Fri, 16 Feb 2024 02:07:25 GMT
ENV ASSET=ce
# Fri, 16 Feb 2024 02:07:25 GMT
ARG EE_PORTS
# Fri, 16 Feb 2024 02:07:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 16 Feb 2024 02:07:26 GMT
ARG KONG_VERSION=2.8.4
# Fri, 16 Feb 2024 02:07:26 GMT
ENV KONG_VERSION=2.8.4
# Fri, 16 Feb 2024 02:07:26 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Fri, 16 Feb 2024 02:07:26 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 16 Feb 2024 02:07:48 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:07:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:07:49 GMT
USER kong
# Fri, 16 Feb 2024 02:07:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:07:49 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:07:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:07:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:07:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d66d6a6a368713979f9d00fad193991ae1af18b8efd3abf4d70ade192807c1bd`  
		Last Modified: Tue, 13 Feb 2024 03:03:16 GMT  
		Size: 30.5 MB (30450077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7ba36d33aba1e66b291a2a7f942c19f092bdb36d0fea455ec2589aee8133ad`  
		Last Modified: Fri, 16 Feb 2024 02:10:16 GMT  
		Size: 25.1 MB (25081962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa5c30ba9fcface501fb09c030dffd044cb3fae4403234fa738aa41a53c0415`  
		Last Modified: Fri, 16 Feb 2024 02:10:25 GMT  
		Size: 61.0 MB (61044471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4767181d1a0827dc32b111186737977a9803669b1a9165edf2837775ee5fc35`  
		Last Modified: Fri, 16 Feb 2024 02:10:15 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:dc60456b49fe33717e9fb2194107af6f5073d61168469381bb5a1ec4b29c58f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113148610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bff69a6ae107167bfa6e4f5ac65995e75a9d5e3e99ad2b66d0ba2d113b415a`
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
# Fri, 16 Feb 2024 05:16:39 GMT
ARG ASSET=ce
# Fri, 16 Feb 2024 05:16:39 GMT
ENV ASSET=ce
# Fri, 16 Feb 2024 05:16:39 GMT
ARG EE_PORTS
# Fri, 16 Feb 2024 05:16:39 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 16 Feb 2024 05:16:39 GMT
ARG KONG_VERSION=2.8.4
# Fri, 16 Feb 2024 05:16:40 GMT
ENV KONG_VERSION=2.8.4
# Fri, 16 Feb 2024 05:16:40 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Fri, 16 Feb 2024 05:16:40 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 16 Feb 2024 05:16:59 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:17:00 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:17:00 GMT
USER kong
# Fri, 16 Feb 2024 05:17:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:17:00 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:17:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:17:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:17:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3e5db86eb9ec9d504e578b563fa89da9e71500cd4403efe3f4f9a567bdf34e85`  
		Last Modified: Tue, 13 Feb 2024 17:23:16 GMT  
		Size: 28.4 MB (28400321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d22b0f8deecddd8b48423d7e92203b7efb162409403b397f608889f4e13495`  
		Last Modified: Fri, 16 Feb 2024 05:19:10 GMT  
		Size: 25.1 MB (25081964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54df78066adfb2a5505cccdbbca5937eb601f49de1c5e54d32ff6a87cd6cedc`  
		Last Modified: Fri, 16 Feb 2024 05:19:16 GMT  
		Size: 59.7 MB (59665445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d9ec1801c50d0a6b605e79d72b0daea07cbcb493717cb91d6d49ccd96229a3`  
		Last Modified: Fri, 16 Feb 2024 05:19:09 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:e033ea7352d2f86b7c43fc219582f34a733ddcc72670dadcfebd126aa1632eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3` - linux; amd64

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

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4603899b07eefa2025325e9df46e44ddf92a067122adbf21c62aec26ee034db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95620494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e676baa736ff092e5a2c98460067653a91bb621b67a9be687b51632fe148a1`
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
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ENV KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Tue, 05 Mar 2024 19:45:42 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Mar 2024 19:45:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Tue, 05 Mar 2024 19:45:43 GMT
USER kong
# Tue, 05 Mar 2024 19:45:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Mar 2024 19:45:44 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Mar 2024 19:45:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Mar 2024 19:45:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Mar 2024 19:45:44 GMT
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
	-	`sha256:693a80b4021fcc6f54961dedb26635b75923122a4f5432027515ef7649e34a1e`  
		Last Modified: Tue, 05 Mar 2024 19:46:18 GMT  
		Size: 67.2 MB (67218891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd93d34c6b0c7198610e08a00d4025d87ba24549201edef9a3dbcf1d90be26d`  
		Last Modified: Tue, 05 Mar 2024 19:46:10 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3`

```console
$ docker pull kong@sha256:b7dc498464435317edf467eb87e17e0d58dbbb036d190468b43bc2252b8f410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3` - linux; amd64

```console
$ docker pull kong@sha256:f80f7a8552e61517f13d30a16787dfdbcd8a2f1c045f62deb1e89a0f6265097f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81378069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996e32fb36c72c095923832ed1bba320e132853b00c054891a6b1d744b0a7646`
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
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 02:06:17 GMT
ENV KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 16 Feb 2024 02:06:45 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:06:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:06:46 GMT
USER kong
# Fri, 16 Feb 2024 02:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:06:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:06:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:06:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:06:46 GMT
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
	-	`sha256:874ee52c96e2ee1875a8c43201af9fda7bb8dcdd4426345858e265c20510f076`  
		Last Modified: Fri, 16 Feb 2024 02:09:38 GMT  
		Size: 50.9 MB (50926709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900a279eaf93039867153af6781137e4e8d69d9f08bf710ac2ae2fcd2fc78f5`  
		Last Modified: Fri, 16 Feb 2024 02:09:30 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b9d920c64ea5594d810ad936e447748278dffdff4134fac39515533371303e11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75787580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf01f16e18cd2dad4489be0d5d95f272bdfd3c41a6549ebfbd4b41bcfab90d85`
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
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 05:15:47 GMT
ENV KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 16 Feb 2024 05:16:08 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:16:08 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:16:08 GMT
USER kong
# Fri, 16 Feb 2024 05:16:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:16:08 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:16:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:16:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:16:09 GMT
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
	-	`sha256:8f2cc2ea0545594caf199600f8e268437096dd3fe22e6d51d5fcf74d161f3d59`  
		Last Modified: Fri, 16 Feb 2024 05:18:34 GMT  
		Size: 47.4 MB (47385977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29daedb5de75a2e750743a87f3cba28b295f95d323923e112211db009c84a61`  
		Last Modified: Fri, 16 Feb 2024 05:18:28 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3-ubuntu`

```console
$ docker pull kong@sha256:b7dc498464435317edf467eb87e17e0d58dbbb036d190468b43bc2252b8f410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f80f7a8552e61517f13d30a16787dfdbcd8a2f1c045f62deb1e89a0f6265097f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81378069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996e32fb36c72c095923832ed1bba320e132853b00c054891a6b1d744b0a7646`
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
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 02:06:17 GMT
ENV KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 16 Feb 2024 02:06:45 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:06:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:06:46 GMT
USER kong
# Fri, 16 Feb 2024 02:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:06:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:06:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:06:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:06:46 GMT
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
	-	`sha256:874ee52c96e2ee1875a8c43201af9fda7bb8dcdd4426345858e265c20510f076`  
		Last Modified: Fri, 16 Feb 2024 02:09:38 GMT  
		Size: 50.9 MB (50926709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900a279eaf93039867153af6781137e4e8d69d9f08bf710ac2ae2fcd2fc78f5`  
		Last Modified: Fri, 16 Feb 2024 02:09:30 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b9d920c64ea5594d810ad936e447748278dffdff4134fac39515533371303e11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75787580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf01f16e18cd2dad4489be0d5d95f272bdfd3c41a6549ebfbd4b41bcfab90d85`
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
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 05:15:47 GMT
ENV KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 16 Feb 2024 05:16:08 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:16:08 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:16:08 GMT
USER kong
# Fri, 16 Feb 2024 05:16:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:16:08 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:16:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:16:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:16:09 GMT
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
	-	`sha256:8f2cc2ea0545594caf199600f8e268437096dd3fe22e6d51d5fcf74d161f3d59`  
		Last Modified: Fri, 16 Feb 2024 05:18:34 GMT  
		Size: 47.4 MB (47385977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29daedb5de75a2e750743a87f3cba28b295f95d323923e112211db009c84a61`  
		Last Modified: Fri, 16 Feb 2024 05:18:28 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1`

```console
$ docker pull kong@sha256:b7dc498464435317edf467eb87e17e0d58dbbb036d190468b43bc2252b8f410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.1` - linux; amd64

```console
$ docker pull kong@sha256:f80f7a8552e61517f13d30a16787dfdbcd8a2f1c045f62deb1e89a0f6265097f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81378069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996e32fb36c72c095923832ed1bba320e132853b00c054891a6b1d744b0a7646`
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
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 02:06:17 GMT
ENV KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 16 Feb 2024 02:06:45 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:06:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:06:46 GMT
USER kong
# Fri, 16 Feb 2024 02:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:06:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:06:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:06:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:06:46 GMT
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
	-	`sha256:874ee52c96e2ee1875a8c43201af9fda7bb8dcdd4426345858e265c20510f076`  
		Last Modified: Fri, 16 Feb 2024 02:09:38 GMT  
		Size: 50.9 MB (50926709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900a279eaf93039867153af6781137e4e8d69d9f08bf710ac2ae2fcd2fc78f5`  
		Last Modified: Fri, 16 Feb 2024 02:09:30 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b9d920c64ea5594d810ad936e447748278dffdff4134fac39515533371303e11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75787580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf01f16e18cd2dad4489be0d5d95f272bdfd3c41a6549ebfbd4b41bcfab90d85`
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
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 05:15:47 GMT
ENV KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 16 Feb 2024 05:16:08 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:16:08 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:16:08 GMT
USER kong
# Fri, 16 Feb 2024 05:16:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:16:08 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:16:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:16:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:16:09 GMT
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
	-	`sha256:8f2cc2ea0545594caf199600f8e268437096dd3fe22e6d51d5fcf74d161f3d59`  
		Last Modified: Fri, 16 Feb 2024 05:18:34 GMT  
		Size: 47.4 MB (47385977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29daedb5de75a2e750743a87f3cba28b295f95d323923e112211db009c84a61`  
		Last Modified: Fri, 16 Feb 2024 05:18:28 GMT  
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
$ docker pull kong@sha256:b7dc498464435317edf467eb87e17e0d58dbbb036d190468b43bc2252b8f410e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f80f7a8552e61517f13d30a16787dfdbcd8a2f1c045f62deb1e89a0f6265097f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81378069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996e32fb36c72c095923832ed1bba320e132853b00c054891a6b1d744b0a7646`
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
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 02:06:17 GMT
ENV KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 16 Feb 2024 02:06:17 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 16 Feb 2024 02:06:45 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:06:46 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:06:46 GMT
USER kong
# Fri, 16 Feb 2024 02:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:06:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:06:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:06:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:06:46 GMT
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
	-	`sha256:874ee52c96e2ee1875a8c43201af9fda7bb8dcdd4426345858e265c20510f076`  
		Last Modified: Fri, 16 Feb 2024 02:09:38 GMT  
		Size: 50.9 MB (50926709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900a279eaf93039867153af6781137e4e8d69d9f08bf710ac2ae2fcd2fc78f5`  
		Last Modified: Fri, 16 Feb 2024 02:09:30 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b9d920c64ea5594d810ad936e447748278dffdff4134fac39515533371303e11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75787580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf01f16e18cd2dad4489be0d5d95f272bdfd3c41a6549ebfbd4b41bcfab90d85`
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
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 05:15:47 GMT
ENV KONG_VERSION=3.3.1
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Fri, 16 Feb 2024 05:15:47 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Fri, 16 Feb 2024 05:16:08 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:16:08 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:16:08 GMT
USER kong
# Fri, 16 Feb 2024 05:16:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:16:08 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:16:09 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:16:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:16:09 GMT
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
	-	`sha256:8f2cc2ea0545594caf199600f8e268437096dd3fe22e6d51d5fcf74d161f3d59`  
		Last Modified: Fri, 16 Feb 2024 05:18:34 GMT  
		Size: 47.4 MB (47385977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29daedb5de75a2e750743a87f3cba28b295f95d323923e112211db009c84a61`  
		Last Modified: Fri, 16 Feb 2024 05:18:28 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4`

```console
$ docker pull kong@sha256:9f8a09a1f924233ada6ce092b27d30dc0e7b497565f1b7aa87113ccdc7c9913f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:7fd672ca66ef6c3e12c6f6a1127058288f6c5beae7fb290f5da6048cea3ec363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93195821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff01c31e338aa8dc782ace36d10171a9fa7a85ea3f187f998cb8c6aa09d1abe`
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
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 02:05:50 GMT
ENV KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 16 Feb 2024 02:06:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:06:10 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:06:10 GMT
USER kong
# Fri, 16 Feb 2024 02:06:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:06:10 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:06:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:06:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:06:10 GMT
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
	-	`sha256:7f34ed4d1da81934f87503b19ec4714f4909235ab3aadc6d3c059473af1b524e`  
		Last Modified: Fri, 16 Feb 2024 02:09:17 GMT  
		Size: 62.7 MB (62744462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a757e2956bf0b06f8ff3c465a23bfe4d03cfc46afe82629f251a90eba05807a`  
		Last Modified: Fri, 16 Feb 2024 02:09:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3aff9e5b1e3ce9c6ce032bf53b387ab79cae7b6d66b9ee445e7154f12dcd0e00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89582308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76a04fb16cb3a3d84f611ca5fd3376b57e7353a2a4dda5d590064eaea9aaea6`
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
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 05:15:27 GMT
ENV KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 16 Feb 2024 05:15:43 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:44 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:44 GMT
USER kong
# Fri, 16 Feb 2024 05:15:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:44 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:44 GMT
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
	-	`sha256:c0b83d3a9d6857c63c96b0eec73feba7f94d5722275733ede0d3b18d26f44df2`  
		Last Modified: Fri, 16 Feb 2024 05:18:16 GMT  
		Size: 61.2 MB (61180704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb62699f99cff9f9c5dd0daa610e3811beb173c6e16719b8e3d598afca6ebe9`  
		Last Modified: Fri, 16 Feb 2024 05:18:09 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:9f8a09a1f924233ada6ce092b27d30dc0e7b497565f1b7aa87113ccdc7c9913f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7fd672ca66ef6c3e12c6f6a1127058288f6c5beae7fb290f5da6048cea3ec363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93195821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff01c31e338aa8dc782ace36d10171a9fa7a85ea3f187f998cb8c6aa09d1abe`
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
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 02:05:50 GMT
ENV KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 16 Feb 2024 02:06:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:06:10 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:06:10 GMT
USER kong
# Fri, 16 Feb 2024 02:06:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:06:10 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:06:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:06:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:06:10 GMT
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
	-	`sha256:7f34ed4d1da81934f87503b19ec4714f4909235ab3aadc6d3c059473af1b524e`  
		Last Modified: Fri, 16 Feb 2024 02:09:17 GMT  
		Size: 62.7 MB (62744462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a757e2956bf0b06f8ff3c465a23bfe4d03cfc46afe82629f251a90eba05807a`  
		Last Modified: Fri, 16 Feb 2024 02:09:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3aff9e5b1e3ce9c6ce032bf53b387ab79cae7b6d66b9ee445e7154f12dcd0e00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89582308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76a04fb16cb3a3d84f611ca5fd3376b57e7353a2a4dda5d590064eaea9aaea6`
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
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 05:15:27 GMT
ENV KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 16 Feb 2024 05:15:43 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:44 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:44 GMT
USER kong
# Fri, 16 Feb 2024 05:15:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:44 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:44 GMT
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
	-	`sha256:c0b83d3a9d6857c63c96b0eec73feba7f94d5722275733ede0d3b18d26f44df2`  
		Last Modified: Fri, 16 Feb 2024 05:18:16 GMT  
		Size: 61.2 MB (61180704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb62699f99cff9f9c5dd0daa610e3811beb173c6e16719b8e3d598afca6ebe9`  
		Last Modified: Fri, 16 Feb 2024 05:18:09 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2`

```console
$ docker pull kong@sha256:9f8a09a1f924233ada6ce092b27d30dc0e7b497565f1b7aa87113ccdc7c9913f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:7fd672ca66ef6c3e12c6f6a1127058288f6c5beae7fb290f5da6048cea3ec363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93195821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff01c31e338aa8dc782ace36d10171a9fa7a85ea3f187f998cb8c6aa09d1abe`
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
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 02:05:50 GMT
ENV KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 16 Feb 2024 02:06:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:06:10 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:06:10 GMT
USER kong
# Fri, 16 Feb 2024 02:06:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:06:10 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:06:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:06:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:06:10 GMT
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
	-	`sha256:7f34ed4d1da81934f87503b19ec4714f4909235ab3aadc6d3c059473af1b524e`  
		Last Modified: Fri, 16 Feb 2024 02:09:17 GMT  
		Size: 62.7 MB (62744462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a757e2956bf0b06f8ff3c465a23bfe4d03cfc46afe82629f251a90eba05807a`  
		Last Modified: Fri, 16 Feb 2024 02:09:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3aff9e5b1e3ce9c6ce032bf53b387ab79cae7b6d66b9ee445e7154f12dcd0e00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89582308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76a04fb16cb3a3d84f611ca5fd3376b57e7353a2a4dda5d590064eaea9aaea6`
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
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 05:15:27 GMT
ENV KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 16 Feb 2024 05:15:43 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:44 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:44 GMT
USER kong
# Fri, 16 Feb 2024 05:15:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:44 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:44 GMT
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
	-	`sha256:c0b83d3a9d6857c63c96b0eec73feba7f94d5722275733ede0d3b18d26f44df2`  
		Last Modified: Fri, 16 Feb 2024 05:18:16 GMT  
		Size: 61.2 MB (61180704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb62699f99cff9f9c5dd0daa610e3811beb173c6e16719b8e3d598afca6ebe9`  
		Last Modified: Fri, 16 Feb 2024 05:18:09 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:9f8a09a1f924233ada6ce092b27d30dc0e7b497565f1b7aa87113ccdc7c9913f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7fd672ca66ef6c3e12c6f6a1127058288f6c5beae7fb290f5da6048cea3ec363
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93195821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff01c31e338aa8dc782ace36d10171a9fa7a85ea3f187f998cb8c6aa09d1abe`
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
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 02:05:50 GMT
ENV KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 16 Feb 2024 02:05:50 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 16 Feb 2024 02:06:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:06:10 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:06:10 GMT
USER kong
# Fri, 16 Feb 2024 02:06:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:06:10 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:06:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:06:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:06:10 GMT
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
	-	`sha256:7f34ed4d1da81934f87503b19ec4714f4909235ab3aadc6d3c059473af1b524e`  
		Last Modified: Fri, 16 Feb 2024 02:09:17 GMT  
		Size: 62.7 MB (62744462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a757e2956bf0b06f8ff3c465a23bfe4d03cfc46afe82629f251a90eba05807a`  
		Last Modified: Fri, 16 Feb 2024 02:09:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3aff9e5b1e3ce9c6ce032bf53b387ab79cae7b6d66b9ee445e7154f12dcd0e00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89582308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76a04fb16cb3a3d84f611ca5fd3376b57e7353a2a4dda5d590064eaea9aaea6`
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
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 05:15:27 GMT
ENV KONG_VERSION=3.4.2
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 16 Feb 2024 05:15:27 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 16 Feb 2024 05:15:43 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:44 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:44 GMT
USER kong
# Fri, 16 Feb 2024 05:15:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:44 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:44 GMT
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
	-	`sha256:c0b83d3a9d6857c63c96b0eec73feba7f94d5722275733ede0d3b18d26f44df2`  
		Last Modified: Fri, 16 Feb 2024 05:18:16 GMT  
		Size: 61.2 MB (61180704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb62699f99cff9f9c5dd0daa610e3811beb173c6e16719b8e3d598afca6ebe9`  
		Last Modified: Fri, 16 Feb 2024 05:18:09 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5`

```console
$ docker pull kong@sha256:ba218fe5832d5fd2c2d915df9016d59e17af1ef58dcd7edbf4744cc480c55793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5` - linux; amd64

```console
$ docker pull kong@sha256:8e7bf8f916f2b97433086a7bd0634949bf8985a154c2e7aee0527e264072afe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94410626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9086c81fab97d183242ebb695cc03cb7752316349a50f26f3ea8f6525ba295`
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
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 02:05:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 16 Feb 2024 02:05:45 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:05:45 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:05:45 GMT
USER kong
# Fri, 16 Feb 2024 02:05:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:05:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:05:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:05:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:05:46 GMT
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
	-	`sha256:a1987899b311e95245b1abbd74f688362f3617e237f31643e8a1f0147fb2b727`  
		Last Modified: Fri, 16 Feb 2024 02:08:54 GMT  
		Size: 64.0 MB (63959266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d99abe6a16b1943f92c4154d08d767a5b063f11098cb03c9b63ee3ca9242d`  
		Last Modified: Fri, 16 Feb 2024 02:08:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fc70eae062f655daca5715857dca8b30ebc69265dcebfbc7512aacfb7f5fba12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d029fb3245e115ac45091815f9234ff5d26e38c377a4d080058852cecfb315df`
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
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 05:15:08 GMT
ENV KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 16 Feb 2024 05:15:23 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:24 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:24 GMT
USER kong
# Fri, 16 Feb 2024 05:15:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:24 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:24 GMT
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
	-	`sha256:f046a0daa1bfd6a47d6120cb9823a641963d2b659505ad39e804314ef919b217`  
		Last Modified: Fri, 16 Feb 2024 05:17:57 GMT  
		Size: 63.5 MB (63486175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdd86c66e85953ec55e08eabc2349491bf46e7f97e8c408cc7e7780b0698492`  
		Last Modified: Fri, 16 Feb 2024 05:17:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5-ubuntu`

```console
$ docker pull kong@sha256:ba218fe5832d5fd2c2d915df9016d59e17af1ef58dcd7edbf4744cc480c55793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8e7bf8f916f2b97433086a7bd0634949bf8985a154c2e7aee0527e264072afe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94410626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9086c81fab97d183242ebb695cc03cb7752316349a50f26f3ea8f6525ba295`
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
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 02:05:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 16 Feb 2024 02:05:45 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:05:45 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:05:45 GMT
USER kong
# Fri, 16 Feb 2024 02:05:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:05:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:05:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:05:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:05:46 GMT
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
	-	`sha256:a1987899b311e95245b1abbd74f688362f3617e237f31643e8a1f0147fb2b727`  
		Last Modified: Fri, 16 Feb 2024 02:08:54 GMT  
		Size: 64.0 MB (63959266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d99abe6a16b1943f92c4154d08d767a5b063f11098cb03c9b63ee3ca9242d`  
		Last Modified: Fri, 16 Feb 2024 02:08:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fc70eae062f655daca5715857dca8b30ebc69265dcebfbc7512aacfb7f5fba12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d029fb3245e115ac45091815f9234ff5d26e38c377a4d080058852cecfb315df`
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
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 05:15:08 GMT
ENV KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 16 Feb 2024 05:15:23 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:24 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:24 GMT
USER kong
# Fri, 16 Feb 2024 05:15:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:24 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:24 GMT
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
	-	`sha256:f046a0daa1bfd6a47d6120cb9823a641963d2b659505ad39e804314ef919b217`  
		Last Modified: Fri, 16 Feb 2024 05:17:57 GMT  
		Size: 63.5 MB (63486175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdd86c66e85953ec55e08eabc2349491bf46e7f97e8c408cc7e7780b0698492`  
		Last Modified: Fri, 16 Feb 2024 05:17:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0`

```console
$ docker pull kong@sha256:ba218fe5832d5fd2c2d915df9016d59e17af1ef58dcd7edbf4744cc480c55793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0` - linux; amd64

```console
$ docker pull kong@sha256:8e7bf8f916f2b97433086a7bd0634949bf8985a154c2e7aee0527e264072afe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94410626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9086c81fab97d183242ebb695cc03cb7752316349a50f26f3ea8f6525ba295`
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
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 02:05:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 16 Feb 2024 02:05:45 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:05:45 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:05:45 GMT
USER kong
# Fri, 16 Feb 2024 02:05:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:05:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:05:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:05:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:05:46 GMT
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
	-	`sha256:a1987899b311e95245b1abbd74f688362f3617e237f31643e8a1f0147fb2b727`  
		Last Modified: Fri, 16 Feb 2024 02:08:54 GMT  
		Size: 64.0 MB (63959266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d99abe6a16b1943f92c4154d08d767a5b063f11098cb03c9b63ee3ca9242d`  
		Last Modified: Fri, 16 Feb 2024 02:08:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fc70eae062f655daca5715857dca8b30ebc69265dcebfbc7512aacfb7f5fba12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d029fb3245e115ac45091815f9234ff5d26e38c377a4d080058852cecfb315df`
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
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 05:15:08 GMT
ENV KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 16 Feb 2024 05:15:23 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:24 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:24 GMT
USER kong
# Fri, 16 Feb 2024 05:15:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:24 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:24 GMT
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
	-	`sha256:f046a0daa1bfd6a47d6120cb9823a641963d2b659505ad39e804314ef919b217`  
		Last Modified: Fri, 16 Feb 2024 05:17:57 GMT  
		Size: 63.5 MB (63486175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdd86c66e85953ec55e08eabc2349491bf46e7f97e8c408cc7e7780b0698492`  
		Last Modified: Fri, 16 Feb 2024 05:17:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0-ubuntu`

```console
$ docker pull kong@sha256:ba218fe5832d5fd2c2d915df9016d59e17af1ef58dcd7edbf4744cc480c55793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8e7bf8f916f2b97433086a7bd0634949bf8985a154c2e7aee0527e264072afe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94410626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9086c81fab97d183242ebb695cc03cb7752316349a50f26f3ea8f6525ba295`
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
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 02:05:26 GMT
ENV KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 16 Feb 2024 02:05:26 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 16 Feb 2024 02:05:45 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 02:05:45 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 02:05:45 GMT
USER kong
# Fri, 16 Feb 2024 02:05:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 02:05:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 02:05:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 02:05:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 02:05:46 GMT
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
	-	`sha256:a1987899b311e95245b1abbd74f688362f3617e237f31643e8a1f0147fb2b727`  
		Last Modified: Fri, 16 Feb 2024 02:08:54 GMT  
		Size: 64.0 MB (63959266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6d99abe6a16b1943f92c4154d08d767a5b063f11098cb03c9b63ee3ca9242d`  
		Last Modified: Fri, 16 Feb 2024 02:08:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fc70eae062f655daca5715857dca8b30ebc69265dcebfbc7512aacfb7f5fba12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d029fb3245e115ac45091815f9234ff5d26e38c377a4d080058852cecfb315df`
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
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 05:15:08 GMT
ENV KONG_VERSION=3.5.0
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 16 Feb 2024 05:15:08 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 16 Feb 2024 05:15:23 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 16 Feb 2024 05:15:24 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 16 Feb 2024 05:15:24 GMT
USER kong
# Fri, 16 Feb 2024 05:15:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 16 Feb 2024 05:15:24 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 16 Feb 2024 05:15:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 05:15:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 16 Feb 2024 05:15:24 GMT
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
	-	`sha256:f046a0daa1bfd6a47d6120cb9823a641963d2b659505ad39e804314ef919b217`  
		Last Modified: Fri, 16 Feb 2024 05:17:57 GMT  
		Size: 63.5 MB (63486175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdd86c66e85953ec55e08eabc2349491bf46e7f97e8c408cc7e7780b0698492`  
		Last Modified: Fri, 16 Feb 2024 05:17:49 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6`

```console
$ docker pull kong@sha256:e033ea7352d2f86b7c43fc219582f34a733ddcc72670dadcfebd126aa1632eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6` - linux; amd64

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

### `kong:3.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4603899b07eefa2025325e9df46e44ddf92a067122adbf21c62aec26ee034db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95620494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e676baa736ff092e5a2c98460067653a91bb621b67a9be687b51632fe148a1`
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
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ENV KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Tue, 05 Mar 2024 19:45:42 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Mar 2024 19:45:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Tue, 05 Mar 2024 19:45:43 GMT
USER kong
# Tue, 05 Mar 2024 19:45:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Mar 2024 19:45:44 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Mar 2024 19:45:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Mar 2024 19:45:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Mar 2024 19:45:44 GMT
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
	-	`sha256:693a80b4021fcc6f54961dedb26635b75923122a4f5432027515ef7649e34a1e`  
		Last Modified: Tue, 05 Mar 2024 19:46:18 GMT  
		Size: 67.2 MB (67218891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd93d34c6b0c7198610e08a00d4025d87ba24549201edef9a3dbcf1d90be26d`  
		Last Modified: Tue, 05 Mar 2024 19:46:10 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:e033ea7352d2f86b7c43fc219582f34a733ddcc72670dadcfebd126aa1632eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6-ubuntu` - linux; amd64

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

### `kong:3.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4603899b07eefa2025325e9df46e44ddf92a067122adbf21c62aec26ee034db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95620494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e676baa736ff092e5a2c98460067653a91bb621b67a9be687b51632fe148a1`
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
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ENV KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Tue, 05 Mar 2024 19:45:42 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Mar 2024 19:45:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Tue, 05 Mar 2024 19:45:43 GMT
USER kong
# Tue, 05 Mar 2024 19:45:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Mar 2024 19:45:44 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Mar 2024 19:45:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Mar 2024 19:45:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Mar 2024 19:45:44 GMT
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
	-	`sha256:693a80b4021fcc6f54961dedb26635b75923122a4f5432027515ef7649e34a1e`  
		Last Modified: Tue, 05 Mar 2024 19:46:18 GMT  
		Size: 67.2 MB (67218891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd93d34c6b0c7198610e08a00d4025d87ba24549201edef9a3dbcf1d90be26d`  
		Last Modified: Tue, 05 Mar 2024 19:46:10 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1`

```console
$ docker pull kong@sha256:e1c01f5410562328e4969b43b9ad303976f8a60e9e5e122e2c60719ebafc60ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `kong:3.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4603899b07eefa2025325e9df46e44ddf92a067122adbf21c62aec26ee034db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95620494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e676baa736ff092e5a2c98460067653a91bb621b67a9be687b51632fe148a1`
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
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ENV KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Tue, 05 Mar 2024 19:45:42 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Mar 2024 19:45:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Tue, 05 Mar 2024 19:45:43 GMT
USER kong
# Tue, 05 Mar 2024 19:45:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Mar 2024 19:45:44 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Mar 2024 19:45:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Mar 2024 19:45:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Mar 2024 19:45:44 GMT
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
	-	`sha256:693a80b4021fcc6f54961dedb26635b75923122a4f5432027515ef7649e34a1e`  
		Last Modified: Tue, 05 Mar 2024 19:46:18 GMT  
		Size: 67.2 MB (67218891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd93d34c6b0c7198610e08a00d4025d87ba24549201edef9a3dbcf1d90be26d`  
		Last Modified: Tue, 05 Mar 2024 19:46:10 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:e1c01f5410562328e4969b43b9ad303976f8a60e9e5e122e2c60719ebafc60ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `kong:3.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4603899b07eefa2025325e9df46e44ddf92a067122adbf21c62aec26ee034db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95620494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e676baa736ff092e5a2c98460067653a91bb621b67a9be687b51632fe148a1`
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
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ENV KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Tue, 05 Mar 2024 19:45:42 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Mar 2024 19:45:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Tue, 05 Mar 2024 19:45:43 GMT
USER kong
# Tue, 05 Mar 2024 19:45:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Mar 2024 19:45:44 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Mar 2024 19:45:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Mar 2024 19:45:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Mar 2024 19:45:44 GMT
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
	-	`sha256:693a80b4021fcc6f54961dedb26635b75923122a4f5432027515ef7649e34a1e`  
		Last Modified: Tue, 05 Mar 2024 19:46:18 GMT  
		Size: 67.2 MB (67218891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd93d34c6b0c7198610e08a00d4025d87ba24549201edef9a3dbcf1d90be26d`  
		Last Modified: Tue, 05 Mar 2024 19:46:10 GMT  
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
$ docker pull kong@sha256:e033ea7352d2f86b7c43fc219582f34a733ddcc72670dadcfebd126aa1632eb8
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
$ docker pull kong@sha256:4603899b07eefa2025325e9df46e44ddf92a067122adbf21c62aec26ee034db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95620494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e676baa736ff092e5a2c98460067653a91bb621b67a9be687b51632fe148a1`
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
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ENV KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Tue, 05 Mar 2024 19:45:42 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Mar 2024 19:45:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Tue, 05 Mar 2024 19:45:43 GMT
USER kong
# Tue, 05 Mar 2024 19:45:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Mar 2024 19:45:44 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Mar 2024 19:45:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Mar 2024 19:45:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Mar 2024 19:45:44 GMT
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
	-	`sha256:693a80b4021fcc6f54961dedb26635b75923122a4f5432027515ef7649e34a1e`  
		Last Modified: Tue, 05 Mar 2024 19:46:18 GMT  
		Size: 67.2 MB (67218891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd93d34c6b0c7198610e08a00d4025d87ba24549201edef9a3dbcf1d90be26d`  
		Last Modified: Tue, 05 Mar 2024 19:46:10 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:e033ea7352d2f86b7c43fc219582f34a733ddcc72670dadcfebd126aa1632eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

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

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4603899b07eefa2025325e9df46e44ddf92a067122adbf21c62aec26ee034db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95620494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e676baa736ff092e5a2c98460067653a91bb621b67a9be687b51632fe148a1`
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
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ENV KONG_VERSION=3.6.1
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Tue, 05 Mar 2024 19:45:07 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Tue, 05 Mar 2024 19:45:42 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Mar 2024 19:45:43 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Tue, 05 Mar 2024 19:45:43 GMT
USER kong
# Tue, 05 Mar 2024 19:45:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Mar 2024 19:45:44 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Mar 2024 19:45:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Mar 2024 19:45:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Mar 2024 19:45:44 GMT
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
	-	`sha256:693a80b4021fcc6f54961dedb26635b75923122a4f5432027515ef7649e34a1e`  
		Last Modified: Tue, 05 Mar 2024 19:46:18 GMT  
		Size: 67.2 MB (67218891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd93d34c6b0c7198610e08a00d4025d87ba24549201edef9a3dbcf1d90be26d`  
		Last Modified: Tue, 05 Mar 2024 19:46:10 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
