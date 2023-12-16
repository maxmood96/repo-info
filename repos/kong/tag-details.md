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
$ docker pull kong@sha256:ec90ef624f2c35fd47b3fa9512c074bd4a10288147661de8ffc3cb2c9265e62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:32b4e4f073babe2e4d9cac98036ae1333fb6cee3fa553892ce0a2324b4aba53f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48118502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3c4fcf23846f9a5759e3d1f6adad39cc2703d220861e07ba8d357e366a6d7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:07:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 01 Dec 2023 07:07:21 GMT
ARG ASSET=ce
# Fri, 01 Dec 2023 07:07:21 GMT
ENV ASSET=ce
# Fri, 01 Dec 2023 07:07:21 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:07:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 07:07:22 GMT
ENV KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Fri, 01 Dec 2023 07:07:32 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 01 Dec 2023 07:07:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:07:32 GMT
USER kong
# Fri, 01 Dec 2023 07:07:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:07:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:07:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:07:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:07:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4e11641bb63841f6f8dd5690779d150a2459c70246625205e6a9bdf5de0b99`  
		Last Modified: Fri, 01 Dec 2023 07:09:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876f1cc886148eaffa5b54f67a24648854f72c85cc6cd629ca6475a83c41b80a`  
		Last Modified: Fri, 01 Dec 2023 07:09:13 GMT  
		Size: 44.7 MB (44715070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6a95b00aecd339a135f747cd35c069f2c0b8cc82d08bdbc51573bb3101a5ec`  
		Last Modified: Fri, 01 Dec 2023 07:09:06 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:69d9c9da292fc40935705bb37908562d83c8cd30f2874ea162a136f86c7d9a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47439098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8922d011a424550df7e41250f20d1d0fd623acf9fb8e8f8fef343cfe181f4664`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:24:15 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 01 Dec 2023 03:24:15 GMT
ARG ASSET=ce
# Fri, 01 Dec 2023 03:24:15 GMT
ENV ASSET=ce
# Fri, 01 Dec 2023 03:24:15 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 03:24:15 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 03:24:15 GMT
ENV KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Fri, 01 Dec 2023 03:24:24 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 01 Dec 2023 03:24:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 03:24:25 GMT
USER kong
# Fri, 01 Dec 2023 03:24:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 03:24:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 03:24:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 03:24:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 03:24:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4dd0a85670f5229f054f48797559e0876e3527a04c7d07f92bfc86aa42ffb8a`  
		Last Modified: Fri, 01 Dec 2023 03:25:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9de9e084432bea9a90140a1df5a0c74701c3b3a5b42f5c4aa70b5af305e03d`  
		Last Modified: Fri, 01 Dec 2023 03:25:45 GMT  
		Size: 44.1 MB (44105057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678a920393647691b83afb6c453ea5768cb45def55361aba76fc9d66e85d95f`  
		Last Modified: Fri, 01 Dec 2023 03:25:39 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:fe011057d7bd8daf4d1f0151dc4a8f60602a54dcf4a5d7a008a29a71f58bf16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:932adfd01a4f54d8bbe04a179ed87e70087dcffc51fbfc1b944d934aacf342b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116553793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf9f17bb69fa0d5ea709c21fa1be6b4280c2382c7bd3622464efc272109899`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 12:00:48 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 12:00:48 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 12:00:48 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 12:00:48 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Dec 2023 12:00:48 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Dec 2023 12:00:48 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Dec 2023 12:00:49 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Sat, 16 Dec 2023 12:00:49 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Sat, 16 Dec 2023 12:01:16 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 12:01:17 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 12:01:17 GMT
USER kong
# Sat, 16 Dec 2023 12:01:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 12:01:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 12:01:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 12:01:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 12:01:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0681d4dec191b21e0d9333e4a8616a8aaf4eda0d0cb0fae80078579595deff33`  
		Last Modified: Sat, 16 Dec 2023 12:03:27 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e14a22e4cd6280f951aefbb1cff85d1040eb68b9e7a15dba261e2cdcdb53f7a`  
		Last Modified: Sat, 16 Dec 2023 12:03:35 GMT  
		Size: 61.0 MB (61024382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfced4fd40a400130725c6595bc02fdffb7d78ae3538042541309756497018bb`  
		Last Modified: Sat, 16 Dec 2023 12:03:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b05cd7529519a64f2a9c8400c2f9e532cf838b8fbb18322e2fbde0aeecd8b2ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113127919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52cf57885ebf3909f58429db33c957e1812a211e1b9e5e038e1768acf20313d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:46:26 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:46:26 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:46:26 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:46:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:46:26 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Dec 2023 10:46:26 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Dec 2023 10:46:26 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Sat, 16 Dec 2023 10:46:26 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Sat, 16 Dec 2023 10:46:44 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:46:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:46:45 GMT
USER kong
# Sat, 16 Dec 2023 10:46:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:46:45 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:46:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:46:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:46:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6fd3aef902da3190df0df6171b4539a5542282a3bf218b38242585db8b9bf3`  
		Last Modified: Sat, 16 Dec 2023 10:48:45 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fc7c31562a6f34770360baeffe5eebaf929dcce6c106cc91067a5f38c93d2c`  
		Last Modified: Sat, 16 Dec 2023 10:48:52 GMT  
		Size: 59.6 MB (59644793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395d5e99e69c2d674c740443ef63bb81398c80bd72ce99238a622451f75728f0`  
		Last Modified: Sat, 16 Dec 2023 10:48:44 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4`

```console
$ docker pull kong@sha256:ec90ef624f2c35fd47b3fa9512c074bd4a10288147661de8ffc3cb2c9265e62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.4` - linux; amd64

```console
$ docker pull kong@sha256:32b4e4f073babe2e4d9cac98036ae1333fb6cee3fa553892ce0a2324b4aba53f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48118502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3c4fcf23846f9a5759e3d1f6adad39cc2703d220861e07ba8d357e366a6d7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:07:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 01 Dec 2023 07:07:21 GMT
ARG ASSET=ce
# Fri, 01 Dec 2023 07:07:21 GMT
ENV ASSET=ce
# Fri, 01 Dec 2023 07:07:21 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:07:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 07:07:22 GMT
ENV KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Fri, 01 Dec 2023 07:07:32 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 01 Dec 2023 07:07:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:07:32 GMT
USER kong
# Fri, 01 Dec 2023 07:07:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:07:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:07:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:07:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:07:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4e11641bb63841f6f8dd5690779d150a2459c70246625205e6a9bdf5de0b99`  
		Last Modified: Fri, 01 Dec 2023 07:09:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876f1cc886148eaffa5b54f67a24648854f72c85cc6cd629ca6475a83c41b80a`  
		Last Modified: Fri, 01 Dec 2023 07:09:13 GMT  
		Size: 44.7 MB (44715070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6a95b00aecd339a135f747cd35c069f2c0b8cc82d08bdbc51573bb3101a5ec`  
		Last Modified: Fri, 01 Dec 2023 07:09:06 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:69d9c9da292fc40935705bb37908562d83c8cd30f2874ea162a136f86c7d9a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47439098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8922d011a424550df7e41250f20d1d0fd623acf9fb8e8f8fef343cfe181f4664`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:24:15 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 01 Dec 2023 03:24:15 GMT
ARG ASSET=ce
# Fri, 01 Dec 2023 03:24:15 GMT
ENV ASSET=ce
# Fri, 01 Dec 2023 03:24:15 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 03:24:15 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 03:24:15 GMT
ENV KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Fri, 01 Dec 2023 03:24:24 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 01 Dec 2023 03:24:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 03:24:25 GMT
USER kong
# Fri, 01 Dec 2023 03:24:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 03:24:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 03:24:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 03:24:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 03:24:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4dd0a85670f5229f054f48797559e0876e3527a04c7d07f92bfc86aa42ffb8a`  
		Last Modified: Fri, 01 Dec 2023 03:25:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9de9e084432bea9a90140a1df5a0c74701c3b3a5b42f5c4aa70b5af305e03d`  
		Last Modified: Fri, 01 Dec 2023 03:25:45 GMT  
		Size: 44.1 MB (44105057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678a920393647691b83afb6c453ea5768cb45def55361aba76fc9d66e85d95f`  
		Last Modified: Fri, 01 Dec 2023 03:25:39 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4-alpine`

```console
$ docker pull kong@sha256:ec90ef624f2c35fd47b3fa9512c074bd4a10288147661de8ffc3cb2c9265e62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:32b4e4f073babe2e4d9cac98036ae1333fb6cee3fa553892ce0a2324b4aba53f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48118502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3c4fcf23846f9a5759e3d1f6adad39cc2703d220861e07ba8d357e366a6d7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:07:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 01 Dec 2023 07:07:21 GMT
ARG ASSET=ce
# Fri, 01 Dec 2023 07:07:21 GMT
ENV ASSET=ce
# Fri, 01 Dec 2023 07:07:21 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:07:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 07:07:22 GMT
ENV KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Fri, 01 Dec 2023 07:07:22 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Fri, 01 Dec 2023 07:07:32 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 01 Dec 2023 07:07:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:07:32 GMT
USER kong
# Fri, 01 Dec 2023 07:07:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:07:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:07:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:07:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:07:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4e11641bb63841f6f8dd5690779d150a2459c70246625205e6a9bdf5de0b99`  
		Last Modified: Fri, 01 Dec 2023 07:09:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876f1cc886148eaffa5b54f67a24648854f72c85cc6cd629ca6475a83c41b80a`  
		Last Modified: Fri, 01 Dec 2023 07:09:13 GMT  
		Size: 44.7 MB (44715070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6a95b00aecd339a135f747cd35c069f2c0b8cc82d08bdbc51573bb3101a5ec`  
		Last Modified: Fri, 01 Dec 2023 07:09:06 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:69d9c9da292fc40935705bb37908562d83c8cd30f2874ea162a136f86c7d9a6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47439098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8922d011a424550df7e41250f20d1d0fd623acf9fb8e8f8fef343cfe181f4664`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:24:15 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 01 Dec 2023 03:24:15 GMT
ARG ASSET=ce
# Fri, 01 Dec 2023 03:24:15 GMT
ENV ASSET=ce
# Fri, 01 Dec 2023 03:24:15 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 03:24:15 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 03:24:15 GMT
ENV KONG_VERSION=2.8.4
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Fri, 01 Dec 2023 03:24:15 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Fri, 01 Dec 2023 03:24:24 GMT
# ARGS: KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Fri, 01 Dec 2023 03:24:25 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 03:24:25 GMT
USER kong
# Fri, 01 Dec 2023 03:24:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 03:24:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 03:24:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 03:24:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 03:24:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4dd0a85670f5229f054f48797559e0876e3527a04c7d07f92bfc86aa42ffb8a`  
		Last Modified: Fri, 01 Dec 2023 03:25:39 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9de9e084432bea9a90140a1df5a0c74701c3b3a5b42f5c4aa70b5af305e03d`  
		Last Modified: Fri, 01 Dec 2023 03:25:45 GMT  
		Size: 44.1 MB (44105057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4678a920393647691b83afb6c453ea5768cb45def55361aba76fc9d66e85d95f`  
		Last Modified: Fri, 01 Dec 2023 03:25:39 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.4-ubuntu`

```console
$ docker pull kong@sha256:fe011057d7bd8daf4d1f0151dc4a8f60602a54dcf4a5d7a008a29a71f58bf16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:932adfd01a4f54d8bbe04a179ed87e70087dcffc51fbfc1b944d934aacf342b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116553793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf9f17bb69fa0d5ea709c21fa1be6b4280c2382c7bd3622464efc272109899`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 12:00:48 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 12:00:48 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 12:00:48 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 12:00:48 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Dec 2023 12:00:48 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Dec 2023 12:00:48 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Dec 2023 12:00:49 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Sat, 16 Dec 2023 12:00:49 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Sat, 16 Dec 2023 12:01:16 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 12:01:17 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 12:01:17 GMT
USER kong
# Sat, 16 Dec 2023 12:01:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 12:01:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 12:01:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 12:01:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 12:01:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0681d4dec191b21e0d9333e4a8616a8aaf4eda0d0cb0fae80078579595deff33`  
		Last Modified: Sat, 16 Dec 2023 12:03:27 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e14a22e4cd6280f951aefbb1cff85d1040eb68b9e7a15dba261e2cdcdb53f7a`  
		Last Modified: Sat, 16 Dec 2023 12:03:35 GMT  
		Size: 61.0 MB (61024382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfced4fd40a400130725c6595bc02fdffb7d78ae3538042541309756497018bb`  
		Last Modified: Sat, 16 Dec 2023 12:03:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b05cd7529519a64f2a9c8400c2f9e532cf838b8fbb18322e2fbde0aeecd8b2ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.1 MB (113127919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52cf57885ebf3909f58429db33c957e1812a211e1b9e5e038e1768acf20313d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:46:26 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:46:26 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:46:26 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:46:26 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:46:26 GMT
ARG KONG_VERSION=2.8.4
# Sat, 16 Dec 2023 10:46:26 GMT
ENV KONG_VERSION=2.8.4
# Sat, 16 Dec 2023 10:46:26 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Sat, 16 Dec 2023 10:46:26 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Sat, 16 Dec 2023 10:46:44 GMT
# ARGS: KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:46:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:46:45 GMT
USER kong
# Sat, 16 Dec 2023 10:46:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:46:45 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:46:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:46:45 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:46:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6fd3aef902da3190df0df6171b4539a5542282a3bf218b38242585db8b9bf3`  
		Last Modified: Sat, 16 Dec 2023 10:48:45 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fc7c31562a6f34770360baeffe5eebaf929dcce6c106cc91067a5f38c93d2c`  
		Last Modified: Sat, 16 Dec 2023 10:48:52 GMT  
		Size: 59.6 MB (59644793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395d5e99e69c2d674c740443ef63bb81398c80bd72ce99238a622451f75728f0`  
		Last Modified: Sat, 16 Dec 2023 10:48:44 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3`

```console
$ docker pull kong@sha256:e8d0c74da65ba6b624203f8f825ba19be0ce2fa233324153c65182f6add22c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:e5d979f74ee2b865582d8cefce70846f2f4e21608d35c7231fe05e1e6282736d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94409505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaf3dd270ac7abeda9304bb58e18e5be0fb01d57600354e59d1a5d70a233f10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 11:58:35 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:58:36 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:58:36 GMT
USER kong
# Sat, 16 Dec 2023 11:58:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:58:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:58:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:58:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:58:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d362b85c03043e5663d1252149889eec4c21d5bde9c89a09ff2b0670e95f4b`  
		Last Modified: Sat, 16 Dec 2023 12:01:48 GMT  
		Size: 64.0 MB (63961643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec47c99d768e1edb15d1098095f264e239ad9f05df6888420f3f416437831c0`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a42e3c863da10dba85b3ec17122fab30152a4336787114d3131ff98a02d44841
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91884840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083db3718895ee84dbc1f4773b7fd32c6fc4f6427d583e73f05005b9a3863817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 10:44:34 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:35 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:35 GMT
USER kong
# Sat, 16 Dec 2023 10:44:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:35 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:35 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361c5af99b74dbd43e763c35e9a7a948bd5f696ebe6812a05c90c30bc63ec1be`  
		Last Modified: Sat, 16 Dec 2023 10:47:15 GMT  
		Size: 63.5 MB (63483276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2420a704579187d9c2b7bb05302437a5ef4643e457fca280041f715872ab95`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1`

```console
$ docker pull kong@sha256:79da7f8540d793791190125555ed98f3408c9c117e8a8764ac436aec7c1228ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1` - linux; amd64

```console
$ docker pull kong@sha256:9a05d373b5f7cecf3fbbd93884c87a993117a3007e405b6908b49ee7051de081
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75698851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb054f1e3450ec32edfd9a293d10b75b606f4f88e7ded7ed561ccac71e3ebc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:06:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 07:06:52 GMT
ARG KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 07:06:52 GMT
ENV KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 07:06:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 01 Dec 2023 07:06:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 01 Dec 2023 07:06:53 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 07:06:53 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:06:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 07:07:00 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 07:07:00 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:07:01 GMT
USER kong
# Fri, 01 Dec 2023 07:07:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:07:01 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:07:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:07:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:07:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e9021df6031eb64be930d68ff29e956b7d725dd25fce948dc2824c55c83f26`  
		Last Modified: Fri, 01 Dec 2023 07:08:28 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856c7a5686e63bfd6825a996153a7babdf73b1a8f0aa600dbdef57370ba41a6e`  
		Last Modified: Fri, 01 Dec 2023 07:08:36 GMT  
		Size: 72.9 MB (72890055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c337fda3a5dc972ce857e4e87e415241bc5c35a6200d9fdd950507954b0873`  
		Last Modified: Fri, 01 Dec 2023 07:08:28 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:645d2382467d88a823145b3779eac5c8a2343f0663584b9e828a33167aa52791
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73715883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb85c79d57a86aef06f0f2f486f23e7eb3e676d3ac9e689f3af639644ec2455a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:23:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 03:23:49 GMT
ENV KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 01 Dec 2023 03:23:49 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 03:23:49 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 03:23:49 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 03:23:56 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 03:23:57 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 03:23:57 GMT
USER kong
# Fri, 01 Dec 2023 03:23:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 03:23:57 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 03:23:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 03:23:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 03:23:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72688af05eae29ca058143f0a22e7039329aac2b19f97587834e76630a72a10a`  
		Last Modified: Fri, 01 Dec 2023 03:24:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cbc734061a38d2f224881be088784a3dc7c1ebfe636c720d9d795cdee931b6`  
		Last Modified: Fri, 01 Dec 2023 03:25:07 GMT  
		Size: 71.0 MB (71006574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c701e0ca678821c763dd0852ddd97ecef05ea0c407eb963ba5d7f5d449276f`  
		Last Modified: Fri, 01 Dec 2023 03:24:59 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1-ubuntu`

```console
$ docker pull kong@sha256:1d706fcff29d997097ca17a5b0534676fbd466bbb3986183510010370f775e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:efe3d06405741cc939ceb38a2274b70cd3e0528a29bcd4920061874e435f2219
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101921259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b32410f88239332f82b9dc443d997e45d224276079f3ed56eb6a2b7742efb4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 12:00:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 12:00:04 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 12:00:04 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 12:00:04 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 12:00:05 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 12:00:05 GMT
ARG KONG_VERSION=3.1.1
# Sat, 16 Dec 2023 12:00:05 GMT
ENV KONG_VERSION=3.1.1
# Sat, 16 Dec 2023 12:00:05 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Sat, 16 Dec 2023 12:00:05 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Sat, 16 Dec 2023 12:00:38 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 12:00:39 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 12:00:39 GMT
USER kong
# Sat, 16 Dec 2023 12:00:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 12:00:39 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 12:00:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 12:00:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 12:00:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d46a6b5c80ff5b7a59ce9fb43ccf1c5eceb449af762f48a01b2a1036703fccd`  
		Last Modified: Sat, 16 Dec 2023 12:03:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5311c26634d757c09fad5a6fe1d7130c9862b66c54a569b061fc0bbceb770fbd`  
		Last Modified: Sat, 16 Dec 2023 12:03:16 GMT  
		Size: 73.3 MB (73336228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b67ad7b32c7b8f2080dffd7e46c182b30134b2a684bfd5c07b03cdc6b91c9`  
		Last Modified: Sat, 16 Dec 2023 12:03:05 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:09916eb483bbd7300a98ccc2446f88ed7911a82889373ad432d079b7414c1dcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99174546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27d2c73cffe3b4fa4b37d14b8ef4f0a92fbfcf73540344b3eb3ebc728543fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:45:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:45:44 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:45:44 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:45:44 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:45:44 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:44 GMT
ARG KONG_VERSION=3.1.1
# Sat, 16 Dec 2023 10:45:44 GMT
ENV KONG_VERSION=3.1.1
# Sat, 16 Dec 2023 10:45:44 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Sat, 16 Dec 2023 10:45:44 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Sat, 16 Dec 2023 10:46:20 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:46:21 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:46:21 GMT
USER kong
# Sat, 16 Dec 2023 10:46:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:46:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:46:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:46:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:46:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9d99a856c893c8b0e671634ebc0eca450fdddaa19bc5ab6b47b3ccdd7cbe25`  
		Last Modified: Sat, 16 Dec 2023 10:48:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99dce8d9e63ecd65306f1ccc6994146b366bf4badd7e5ac09f9d6e712c92416`  
		Last Modified: Sat, 16 Dec 2023 10:48:35 GMT  
		Size: 72.0 MB (71970395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a00e40128e9ad0f06ff523372abacf0848f336e4ba64d49b9b846157539941`  
		Last Modified: Sat, 16 Dec 2023 10:48:26 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1`

```console
$ docker pull kong@sha256:79da7f8540d793791190125555ed98f3408c9c117e8a8764ac436aec7c1228ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1` - linux; amd64

```console
$ docker pull kong@sha256:9a05d373b5f7cecf3fbbd93884c87a993117a3007e405b6908b49ee7051de081
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75698851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb054f1e3450ec32edfd9a293d10b75b606f4f88e7ded7ed561ccac71e3ebc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:06:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 07:06:52 GMT
ARG KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 07:06:52 GMT
ENV KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 07:06:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 01 Dec 2023 07:06:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 01 Dec 2023 07:06:53 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 07:06:53 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:06:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 07:07:00 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 07:07:00 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:07:01 GMT
USER kong
# Fri, 01 Dec 2023 07:07:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:07:01 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:07:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:07:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:07:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e9021df6031eb64be930d68ff29e956b7d725dd25fce948dc2824c55c83f26`  
		Last Modified: Fri, 01 Dec 2023 07:08:28 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856c7a5686e63bfd6825a996153a7babdf73b1a8f0aa600dbdef57370ba41a6e`  
		Last Modified: Fri, 01 Dec 2023 07:08:36 GMT  
		Size: 72.9 MB (72890055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c337fda3a5dc972ce857e4e87e415241bc5c35a6200d9fdd950507954b0873`  
		Last Modified: Fri, 01 Dec 2023 07:08:28 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:645d2382467d88a823145b3779eac5c8a2343f0663584b9e828a33167aa52791
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73715883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb85c79d57a86aef06f0f2f486f23e7eb3e676d3ac9e689f3af639644ec2455a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:23:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 03:23:49 GMT
ENV KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 01 Dec 2023 03:23:49 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 03:23:49 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 03:23:49 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 03:23:56 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 03:23:57 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 03:23:57 GMT
USER kong
# Fri, 01 Dec 2023 03:23:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 03:23:57 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 03:23:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 03:23:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 03:23:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72688af05eae29ca058143f0a22e7039329aac2b19f97587834e76630a72a10a`  
		Last Modified: Fri, 01 Dec 2023 03:24:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cbc734061a38d2f224881be088784a3dc7c1ebfe636c720d9d795cdee931b6`  
		Last Modified: Fri, 01 Dec 2023 03:25:07 GMT  
		Size: 71.0 MB (71006574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c701e0ca678821c763dd0852ddd97ecef05ea0c407eb963ba5d7f5d449276f`  
		Last Modified: Fri, 01 Dec 2023 03:24:59 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1-alpine`

```console
$ docker pull kong@sha256:79da7f8540d793791190125555ed98f3408c9c117e8a8764ac436aec7c1228ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:9a05d373b5f7cecf3fbbd93884c87a993117a3007e405b6908b49ee7051de081
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75698851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4eb054f1e3450ec32edfd9a293d10b75b606f4f88e7ded7ed561ccac71e3ebc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:05 GMT
ADD file:282274bb02b29182f35c732f021f3dab6de9f16a1ae24460061ad1abdca6444a in / 
# Thu, 30 Nov 2023 23:23:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:06:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 07:06:52 GMT
ARG KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 07:06:52 GMT
ENV KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 07:06:53 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 01 Dec 2023 07:06:53 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 01 Dec 2023 07:06:53 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 07:06:53 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:06:53 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 07:07:00 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 07:07:00 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:07:01 GMT
USER kong
# Fri, 01 Dec 2023 07:07:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:07:01 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:07:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:07:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:07:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:070eb51debd997eca763a31532c01e2579afe94e43b110d84282a81cb576e342`  
		Last Modified: Thu, 30 Nov 2023 23:23:49 GMT  
		Size: 2.8 MB (2807782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e9021df6031eb64be930d68ff29e956b7d725dd25fce948dc2824c55c83f26`  
		Last Modified: Fri, 01 Dec 2023 07:08:28 GMT  
		Size: 136.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856c7a5686e63bfd6825a996153a7babdf73b1a8f0aa600dbdef57370ba41a6e`  
		Last Modified: Fri, 01 Dec 2023 07:08:36 GMT  
		Size: 72.9 MB (72890055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c337fda3a5dc972ce857e4e87e415241bc5c35a6200d9fdd950507954b0873`  
		Last Modified: Fri, 01 Dec 2023 07:08:28 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:645d2382467d88a823145b3779eac5c8a2343f0663584b9e828a33167aa52791
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73715883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb85c79d57a86aef06f0f2f486f23e7eb3e676d3ac9e689f3af639644ec2455a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:11 GMT
ADD file:1efd26ad638f3c262f37eb81a32e3f026121dcd60479e91c42097bfc8329ed3b in / 
# Thu, 30 Nov 2023 23:11:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 03:23:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 03:23:49 GMT
ENV KONG_VERSION=3.1.1
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c
# Fri, 01 Dec 2023 03:23:49 GMT
ARG KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
# Fri, 01 Dec 2023 03:23:49 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 03:23:49 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 03:23:49 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 03:23:56 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=9194977814e91b6997ce4795957d9b4bcec9d220667e01a08ade7ac64704f57c KONG_ARM64_SHA=92d98307a3193602bbe4dbed2d099cde5404a8acd09d53f0b9a9f2bcf6038500
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) export ARCH='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) export ARCH='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc pcre perl tzdata libcap zlib zlib-dev bash     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 03:23:57 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 03:23:57 GMT
USER kong
# Fri, 01 Dec 2023 03:23:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 03:23:57 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 03:23:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 03:23:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 03:23:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:5362b5901f8a9898f2bcc8eb6c3e6990364aa058617afaae388bdb9f437d3d7e`  
		Last Modified: Thu, 30 Nov 2023 23:11:54 GMT  
		Size: 2.7 MB (2708293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72688af05eae29ca058143f0a22e7039329aac2b19f97587834e76630a72a10a`  
		Last Modified: Fri, 01 Dec 2023 03:24:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cbc734061a38d2f224881be088784a3dc7c1ebfe636c720d9d795cdee931b6`  
		Last Modified: Fri, 01 Dec 2023 03:25:07 GMT  
		Size: 71.0 MB (71006574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c701e0ca678821c763dd0852ddd97ecef05ea0c407eb963ba5d7f5d449276f`  
		Last Modified: Fri, 01 Dec 2023 03:24:59 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.1.1-ubuntu`

```console
$ docker pull kong@sha256:1d706fcff29d997097ca17a5b0534676fbd466bbb3986183510010370f775e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.1.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:efe3d06405741cc939ceb38a2274b70cd3e0528a29bcd4920061874e435f2219
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101921259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b32410f88239332f82b9dc443d997e45d224276079f3ed56eb6a2b7742efb4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 12:00:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 12:00:04 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 12:00:04 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 12:00:04 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 12:00:05 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 12:00:05 GMT
ARG KONG_VERSION=3.1.1
# Sat, 16 Dec 2023 12:00:05 GMT
ENV KONG_VERSION=3.1.1
# Sat, 16 Dec 2023 12:00:05 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Sat, 16 Dec 2023 12:00:05 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Sat, 16 Dec 2023 12:00:38 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 12:00:39 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 12:00:39 GMT
USER kong
# Sat, 16 Dec 2023 12:00:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 12:00:39 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 12:00:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 12:00:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 12:00:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d46a6b5c80ff5b7a59ce9fb43ccf1c5eceb449af762f48a01b2a1036703fccd`  
		Last Modified: Sat, 16 Dec 2023 12:03:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5311c26634d757c09fad5a6fe1d7130c9862b66c54a569b061fc0bbceb770fbd`  
		Last Modified: Sat, 16 Dec 2023 12:03:16 GMT  
		Size: 73.3 MB (73336228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809b67ad7b32c7b8f2080dffd7e46c182b30134b2a684bfd5c07b03cdc6b91c9`  
		Last Modified: Sat, 16 Dec 2023 12:03:05 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.1.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:09916eb483bbd7300a98ccc2446f88ed7911a82889373ad432d079b7414c1dcf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99174546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a27d2c73cffe3b4fa4b37d14b8ef4f0a92fbfcf73540344b3eb3ebc728543fd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:45:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:45:44 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:45:44 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:45:44 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:45:44 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:44 GMT
ARG KONG_VERSION=3.1.1
# Sat, 16 Dec 2023 10:45:44 GMT
ENV KONG_VERSION=3.1.1
# Sat, 16 Dec 2023 10:45:44 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Sat, 16 Dec 2023 10:45:44 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Sat, 16 Dec 2023 10:46:20 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:46:21 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:46:21 GMT
USER kong
# Sat, 16 Dec 2023 10:46:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:46:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:46:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:46:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:46:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9d99a856c893c8b0e671634ebc0eca450fdddaa19bc5ab6b47b3ccdd7cbe25`  
		Last Modified: Sat, 16 Dec 2023 10:48:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99dce8d9e63ecd65306f1ccc6994146b366bf4badd7e5ac09f9d6e712c92416`  
		Last Modified: Sat, 16 Dec 2023 10:48:35 GMT  
		Size: 72.0 MB (71970395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a00e40128e9ad0f06ff523372abacf0848f336e4ba64d49b9b846157539941`  
		Last Modified: Sat, 16 Dec 2023 10:48:26 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2`

```console
$ docker pull kong@sha256:c85e1d5a58157a8b5416c15c977175fa3537a7d2e6c7f8a9b232e86f21e6aaf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2` - linux; amd64

```console
$ docker pull kong@sha256:8757062ab7ef6e1f8f2c1576786d551d3b7e75fe3d5aed346cf5c8200456f0e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74497250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca4dc474d7b60a5d1be48fc63f1cedc6fd5ad597f7bf4af439808f05e46acb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 11:59:38 GMT
ENV KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 16 Dec 2023 11:59:56 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:56 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:57 GMT
USER kong
# Sat, 16 Dec 2023 11:59:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:57 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:57 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5524f48582e03215b82ccb58d322b94d4703971b7547ac2e8aca4fc1374c1be`  
		Last Modified: Sat, 16 Dec 2023 12:02:53 GMT  
		Size: 44.0 MB (44049387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070b553eabeb28aed8e4de6a9156675208009ef887e724c27b29793d4c8f95b`  
		Last Modified: Sat, 16 Dec 2023 12:02:46 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b024c132f8037119445a031b02c1cbc66415c8d6f98abf81cf943f84a8d7cefb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78620721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ce3c47a0f02e52c391d6f83ce72e18a32da6717fb66fc31ae3c97f8e603581`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 10:45:23 GMT
ENV KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 16 Dec 2023 10:45:38 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:45:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:45:39 GMT
USER kong
# Sat, 16 Dec 2023 10:45:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:45:39 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:45:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:45:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:45:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1da74dd98d3deecce0e5e754ca31a561ae61813602b13cf308bf891ebf6c19`  
		Last Modified: Sat, 16 Dec 2023 10:48:14 GMT  
		Size: 50.2 MB (50219158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d03ebdb1e914a012455c6bf86a9c863673937d41b7521ede4f302b48eeaa3`  
		Last Modified: Sat, 16 Dec 2023 10:48:07 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2-ubuntu`

```console
$ docker pull kong@sha256:c85e1d5a58157a8b5416c15c977175fa3537a7d2e6c7f8a9b232e86f21e6aaf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8757062ab7ef6e1f8f2c1576786d551d3b7e75fe3d5aed346cf5c8200456f0e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74497250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca4dc474d7b60a5d1be48fc63f1cedc6fd5ad597f7bf4af439808f05e46acb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 11:59:38 GMT
ENV KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 16 Dec 2023 11:59:56 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:56 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:57 GMT
USER kong
# Sat, 16 Dec 2023 11:59:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:57 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:57 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5524f48582e03215b82ccb58d322b94d4703971b7547ac2e8aca4fc1374c1be`  
		Last Modified: Sat, 16 Dec 2023 12:02:53 GMT  
		Size: 44.0 MB (44049387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070b553eabeb28aed8e4de6a9156675208009ef887e724c27b29793d4c8f95b`  
		Last Modified: Sat, 16 Dec 2023 12:02:46 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b024c132f8037119445a031b02c1cbc66415c8d6f98abf81cf943f84a8d7cefb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78620721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ce3c47a0f02e52c391d6f83ce72e18a32da6717fb66fc31ae3c97f8e603581`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 10:45:23 GMT
ENV KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 16 Dec 2023 10:45:38 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:45:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:45:39 GMT
USER kong
# Sat, 16 Dec 2023 10:45:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:45:39 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:45:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:45:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:45:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1da74dd98d3deecce0e5e754ca31a561ae61813602b13cf308bf891ebf6c19`  
		Last Modified: Sat, 16 Dec 2023 10:48:14 GMT  
		Size: 50.2 MB (50219158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d03ebdb1e914a012455c6bf86a9c863673937d41b7521ede4f302b48eeaa3`  
		Last Modified: Sat, 16 Dec 2023 10:48:07 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2`

```console
$ docker pull kong@sha256:c85e1d5a58157a8b5416c15c977175fa3537a7d2e6c7f8a9b232e86f21e6aaf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2.2` - linux; amd64

```console
$ docker pull kong@sha256:8757062ab7ef6e1f8f2c1576786d551d3b7e75fe3d5aed346cf5c8200456f0e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74497250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca4dc474d7b60a5d1be48fc63f1cedc6fd5ad597f7bf4af439808f05e46acb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 11:59:38 GMT
ENV KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 16 Dec 2023 11:59:56 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:56 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:57 GMT
USER kong
# Sat, 16 Dec 2023 11:59:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:57 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:57 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5524f48582e03215b82ccb58d322b94d4703971b7547ac2e8aca4fc1374c1be`  
		Last Modified: Sat, 16 Dec 2023 12:02:53 GMT  
		Size: 44.0 MB (44049387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070b553eabeb28aed8e4de6a9156675208009ef887e724c27b29793d4c8f95b`  
		Last Modified: Sat, 16 Dec 2023 12:02:46 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b024c132f8037119445a031b02c1cbc66415c8d6f98abf81cf943f84a8d7cefb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78620721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ce3c47a0f02e52c391d6f83ce72e18a32da6717fb66fc31ae3c97f8e603581`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 10:45:23 GMT
ENV KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 16 Dec 2023 10:45:38 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:45:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:45:39 GMT
USER kong
# Sat, 16 Dec 2023 10:45:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:45:39 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:45:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:45:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:45:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1da74dd98d3deecce0e5e754ca31a561ae61813602b13cf308bf891ebf6c19`  
		Last Modified: Sat, 16 Dec 2023 10:48:14 GMT  
		Size: 50.2 MB (50219158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d03ebdb1e914a012455c6bf86a9c863673937d41b7521ede4f302b48eeaa3`  
		Last Modified: Sat, 16 Dec 2023 10:48:07 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2-alpine`

```console
$ docker pull kong@sha256:8f877e1c34c3ff35e3d11c65aeb9fe7220e30e5ff34aec54d52500a1b6280b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:3.2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:0b74d6878c7a32e608ae2ba4390c3a589eb32244dcdeffe3820615ecb1623678
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36930156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305b2398aefa39fd80d7d16ffd590bb4fadc175fd9e9e81bc6081280a1547b96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:06:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 07:06:38 GMT
ARG KONG_VERSION=3.2.2
# Fri, 01 Dec 2023 07:06:38 GMT
ENV KONG_VERSION=3.2.2
# Fri, 01 Dec 2023 07:06:38 GMT
ARG KONG_SHA256=a07c3bc0307e2d8fe33acb8be5fe659f348279540eaa267bc6968005094835ef
# Fri, 01 Dec 2023 07:06:38 GMT
ARG KONG_PREFIX=/usr/local/kong
# Fri, 01 Dec 2023 07:06:38 GMT
ENV KONG_PREFIX=/usr/local/kong
# Fri, 01 Dec 2023 07:06:38 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 07:06:38 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:06:38 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 07:06:45 GMT
# ARGS: ASSET=remote KONG_SHA256=a07c3bc0307e2d8fe33acb8be5fe659f348279540eaa267bc6968005094835ef
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 07:06:45 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:06:45 GMT
USER kong
# Fri, 01 Dec 2023 07:06:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:06:46 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:06:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:06:46 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:06:46 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e04843b882f7e87fd4d7694d63670fc991522c9b10a14eb8c32f4f13e8a38f`  
		Last Modified: Fri, 01 Dec 2023 07:08:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605a0b4ddd821259cf3d40e26507851c37449ef591ab0bb8efa312164758d2cf`  
		Last Modified: Fri, 01 Dec 2023 07:08:20 GMT  
		Size: 33.5 MB (33549547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9f4cf9fc4607281710f8d4208822a822dec9ec96d47d8df6a5be34b17b30d4`  
		Last Modified: Fri, 01 Dec 2023 07:08:15 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.2.2-ubuntu`

```console
$ docker pull kong@sha256:c85e1d5a58157a8b5416c15c977175fa3537a7d2e6c7f8a9b232e86f21e6aaf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8757062ab7ef6e1f8f2c1576786d551d3b7e75fe3d5aed346cf5c8200456f0e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74497250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ca4dc474d7b60a5d1be48fc63f1cedc6fd5ad597f7bf4af439808f05e46acb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 11:59:38 GMT
ENV KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 16 Dec 2023 11:59:38 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 16 Dec 2023 11:59:56 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:56 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:57 GMT
USER kong
# Sat, 16 Dec 2023 11:59:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:57 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:57 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5524f48582e03215b82ccb58d322b94d4703971b7547ac2e8aca4fc1374c1be`  
		Last Modified: Sat, 16 Dec 2023 12:02:53 GMT  
		Size: 44.0 MB (44049387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8070b553eabeb28aed8e4de6a9156675208009ef887e724c27b29793d4c8f95b`  
		Last Modified: Sat, 16 Dec 2023 12:02:46 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b024c132f8037119445a031b02c1cbc66415c8d6f98abf81cf943f84a8d7cefb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78620721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ce3c47a0f02e52c391d6f83ce72e18a32da6717fb66fc31ae3c97f8e603581`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 10:45:23 GMT
ENV KONG_VERSION=3.2.2
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540
# Sat, 16 Dec 2023 10:45:23 GMT
ARG KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
# Sat, 16 Dec 2023 10:45:38 GMT
# ARGS: KONG_AMD64_SHA=bfb905c69950386397e8a975358324ec3e2c8fd6dd0425e4a5c2a4c80add4540 KONG_ARM64_SHA=676335fefeb77eff168b27161678615575f3d573a62b19a5a86a5c8bba2c492a
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:45:39 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:45:39 GMT
USER kong
# Sat, 16 Dec 2023 10:45:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:45:39 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:45:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:45:39 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:45:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1da74dd98d3deecce0e5e754ca31a561ae61813602b13cf308bf891ebf6c19`  
		Last Modified: Sat, 16 Dec 2023 10:48:14 GMT  
		Size: 50.2 MB (50219158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d03ebdb1e914a012455c6bf86a9c863673937d41b7521ede4f302b48eeaa3`  
		Last Modified: Sat, 16 Dec 2023 10:48:07 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3`

```console
$ docker pull kong@sha256:a65278709f02008e59f0ec381c879e02b7c9b59082661d213397bcb909371d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3` - linux; amd64

```console
$ docker pull kong@sha256:99e3ef60ed89206a3ffa131a78c64d564a853229413917fda2d7729a31cd0568
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81347557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3a2bf17e60a20911a2d1000b269c465720a1b4b35c2759be29998bab0ff647`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 11:59:07 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Sat, 16 Dec 2023 11:59:30 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:31 GMT
USER kong
# Sat, 16 Dec 2023 11:59:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:31 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fef9332a350665cfa4c6c89202c84a97b6270c74eedf1bbebf8cc74ace7977`  
		Last Modified: Sat, 16 Dec 2023 12:02:34 GMT  
		Size: 50.9 MB (50899695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325319f428d883030566f413839acafeb3c491039e9b6e0538be48672c4d63ac`  
		Last Modified: Sat, 16 Dec 2023 12:02:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0708a9792599f44a43ac5154f4e33fa3b7787ca1d2d0cd509d3bc635eabedd6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75768012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55857341703ffde41832a852f494888cdbcd044df933b98a1d5a62ca4648d997`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 10:45:00 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Sat, 16 Dec 2023 10:45:20 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:45:20 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:45:20 GMT
USER kong
# Sat, 16 Dec 2023 10:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:45:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:45:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:45:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:45:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be04eaba12a7e4e492a72e41aa949e957d6d1bb11550cbe9bbece631ce02760`  
		Last Modified: Sat, 16 Dec 2023 10:47:56 GMT  
		Size: 47.4 MB (47366448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67343f06862b919bb36a3fc0b862b1360d867ff7743365e0b3ff70d6142eb509`  
		Last Modified: Sat, 16 Dec 2023 10:47:50 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3-ubuntu`

```console
$ docker pull kong@sha256:a65278709f02008e59f0ec381c879e02b7c9b59082661d213397bcb909371d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:99e3ef60ed89206a3ffa131a78c64d564a853229413917fda2d7729a31cd0568
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81347557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3a2bf17e60a20911a2d1000b269c465720a1b4b35c2759be29998bab0ff647`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 11:59:07 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Sat, 16 Dec 2023 11:59:30 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:31 GMT
USER kong
# Sat, 16 Dec 2023 11:59:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:31 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fef9332a350665cfa4c6c89202c84a97b6270c74eedf1bbebf8cc74ace7977`  
		Last Modified: Sat, 16 Dec 2023 12:02:34 GMT  
		Size: 50.9 MB (50899695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325319f428d883030566f413839acafeb3c491039e9b6e0538be48672c4d63ac`  
		Last Modified: Sat, 16 Dec 2023 12:02:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0708a9792599f44a43ac5154f4e33fa3b7787ca1d2d0cd509d3bc635eabedd6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75768012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55857341703ffde41832a852f494888cdbcd044df933b98a1d5a62ca4648d997`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 10:45:00 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Sat, 16 Dec 2023 10:45:20 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:45:20 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:45:20 GMT
USER kong
# Sat, 16 Dec 2023 10:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:45:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:45:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:45:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:45:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be04eaba12a7e4e492a72e41aa949e957d6d1bb11550cbe9bbece631ce02760`  
		Last Modified: Sat, 16 Dec 2023 10:47:56 GMT  
		Size: 47.4 MB (47366448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67343f06862b919bb36a3fc0b862b1360d867ff7743365e0b3ff70d6142eb509`  
		Last Modified: Sat, 16 Dec 2023 10:47:50 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1`

```console
$ docker pull kong@sha256:a65278709f02008e59f0ec381c879e02b7c9b59082661d213397bcb909371d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.1` - linux; amd64

```console
$ docker pull kong@sha256:99e3ef60ed89206a3ffa131a78c64d564a853229413917fda2d7729a31cd0568
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81347557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3a2bf17e60a20911a2d1000b269c465720a1b4b35c2759be29998bab0ff647`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 11:59:07 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Sat, 16 Dec 2023 11:59:30 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:31 GMT
USER kong
# Sat, 16 Dec 2023 11:59:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:31 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fef9332a350665cfa4c6c89202c84a97b6270c74eedf1bbebf8cc74ace7977`  
		Last Modified: Sat, 16 Dec 2023 12:02:34 GMT  
		Size: 50.9 MB (50899695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325319f428d883030566f413839acafeb3c491039e9b6e0538be48672c4d63ac`  
		Last Modified: Sat, 16 Dec 2023 12:02:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0708a9792599f44a43ac5154f4e33fa3b7787ca1d2d0cd509d3bc635eabedd6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75768012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55857341703ffde41832a852f494888cdbcd044df933b98a1d5a62ca4648d997`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 10:45:00 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Sat, 16 Dec 2023 10:45:20 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:45:20 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:45:20 GMT
USER kong
# Sat, 16 Dec 2023 10:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:45:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:45:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:45:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:45:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be04eaba12a7e4e492a72e41aa949e957d6d1bb11550cbe9bbece631ce02760`  
		Last Modified: Sat, 16 Dec 2023 10:47:56 GMT  
		Size: 47.4 MB (47366448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67343f06862b919bb36a3fc0b862b1360d867ff7743365e0b3ff70d6142eb509`  
		Last Modified: Sat, 16 Dec 2023 10:47:50 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1-alpine`

```console
$ docker pull kong@sha256:92e301995c504133e4ba0b69f6260b389553a5821a8c6e491feac3df5f859ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:3.3.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:52d5380e2779819916b1c1b9afe3c6aa733baaab12a4dc2e7064a492081d1330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34229592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82061e7453178852640fa6f05498b98433f4fcf1c58ee9e6dd1b4e510d7e8683`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:06:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 07:06:25 GMT
ARG KONG_VERSION=3.3.1
# Fri, 01 Dec 2023 07:06:25 GMT
ENV KONG_VERSION=3.3.1
# Fri, 01 Dec 2023 07:06:25 GMT
ARG KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
# Fri, 01 Dec 2023 07:06:25 GMT
ARG KONG_PREFIX=/usr/local/kong
# Fri, 01 Dec 2023 07:06:26 GMT
ENV KONG_PREFIX=/usr/local/kong
# Fri, 01 Dec 2023 07:06:26 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 07:06:26 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:06:26 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 07:06:32 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     KONG_SHA256=$KONG_AMD64_SHA ;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 07:06:32 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:06:32 GMT
USER kong
# Fri, 01 Dec 2023 07:06:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:06:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:06:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:06:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:06:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d217203619b7312ed56103e24c86c8b8873e22d87b2a033b3be222af47d6972`  
		Last Modified: Fri, 01 Dec 2023 07:08:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64e0a7832a6342ab148a3b79c7b887ae24ebd4add4bcdcbfed8dd029f411cac`  
		Last Modified: Fri, 01 Dec 2023 07:08:07 GMT  
		Size: 30.8 MB (30848978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f17c6af677aeefc80cff56534ddea0225138f58d242dc53cadb06dde1f373a7`  
		Last Modified: Fri, 01 Dec 2023 07:08:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.3.1-ubuntu`

```console
$ docker pull kong@sha256:a65278709f02008e59f0ec381c879e02b7c9b59082661d213397bcb909371d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.3.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:99e3ef60ed89206a3ffa131a78c64d564a853229413917fda2d7729a31cd0568
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81347557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3a2bf17e60a20911a2d1000b269c465720a1b4b35c2759be29998bab0ff647`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 11:59:07 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Sat, 16 Dec 2023 11:59:07 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Sat, 16 Dec 2023 11:59:30 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:31 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:31 GMT
USER kong
# Sat, 16 Dec 2023 11:59:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:31 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29fef9332a350665cfa4c6c89202c84a97b6270c74eedf1bbebf8cc74ace7977`  
		Last Modified: Sat, 16 Dec 2023 12:02:34 GMT  
		Size: 50.9 MB (50899695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325319f428d883030566f413839acafeb3c491039e9b6e0538be48672c4d63ac`  
		Last Modified: Sat, 16 Dec 2023 12:02:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.3.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0708a9792599f44a43ac5154f4e33fa3b7787ca1d2d0cd509d3bc635eabedd6e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75768012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55857341703ffde41832a852f494888cdbcd044df933b98a1d5a62ca4648d997`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 10:45:00 GMT
ENV KONG_VERSION=3.3.1
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20
# Sat, 16 Dec 2023 10:45:00 GMT
ARG KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
# Sat, 16 Dec 2023 10:45:20 GMT
# ARGS: KONG_AMD64_SHA=3aa6625933b60c8a4669a3623bcd3a3d736dfd807bbc314ea8989cd63c117a20 KONG_ARM64_SHA=3fd20cd0e45e81d858b54d3e40992d73ac9d7d11e398c0d02854ff69988657dd
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:45:20 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:45:20 GMT
USER kong
# Sat, 16 Dec 2023 10:45:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:45:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:45:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:45:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:45:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be04eaba12a7e4e492a72e41aa949e957d6d1bb11550cbe9bbece631ce02760`  
		Last Modified: Sat, 16 Dec 2023 10:47:56 GMT  
		Size: 47.4 MB (47366448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67343f06862b919bb36a3fc0b862b1360d867ff7743365e0b3ff70d6142eb509`  
		Last Modified: Sat, 16 Dec 2023 10:47:50 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4`

```console
$ docker pull kong@sha256:94c5977e8cf6c523522b2fb2065a43dee275bc61fac8495e336c4ea9501d0c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:5ebae6d82867d483323e9b94afa2c16320f67defbd6deb1c779f43a094e5d483
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93176840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1af3e874339d41dadfa6067a64191eb19b1f7b847f589f63994113e53cd527e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 11:58:40 GMT
ENV KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 16 Dec 2023 11:58:59 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:00 GMT
USER kong
# Sat, 16 Dec 2023 11:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:00 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad67bf8a12760b2dde172d4d1588e5194e6b7d3ec3b7df6b3cba3ebe70aa1770`  
		Last Modified: Sat, 16 Dec 2023 12:02:14 GMT  
		Size: 62.7 MB (62728977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61648a16f8302198b16329e458e71b1a0dacd18c635781c985ee815bca93184`  
		Last Modified: Sat, 16 Dec 2023 12:02:04 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:100b580025d060b208f4d70cde09a8cd613902af99f7351beedee2f283481fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89564029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa91496d32b306e6772fa95f1767ae042c0a9320e60c9d5d0789a612b9b89d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 10:44:40 GMT
ENV KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 16 Dec 2023 10:44:55 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:56 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:56 GMT
USER kong
# Sat, 16 Dec 2023 10:44:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:56 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:56 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437cd7243bf19e3ddaf26cd91043001da81451f15a8656e28dc70523f8846066`  
		Last Modified: Sat, 16 Dec 2023 10:47:39 GMT  
		Size: 61.2 MB (61162465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b3f7db895910317703cd6867110ec13c8c1e8be7022a9f588f215fbfa284ac`  
		Last Modified: Sat, 16 Dec 2023 10:47:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:94c5977e8cf6c523522b2fb2065a43dee275bc61fac8495e336c4ea9501d0c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5ebae6d82867d483323e9b94afa2c16320f67defbd6deb1c779f43a094e5d483
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93176840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1af3e874339d41dadfa6067a64191eb19b1f7b847f589f63994113e53cd527e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 11:58:40 GMT
ENV KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 16 Dec 2023 11:58:59 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:00 GMT
USER kong
# Sat, 16 Dec 2023 11:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:00 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad67bf8a12760b2dde172d4d1588e5194e6b7d3ec3b7df6b3cba3ebe70aa1770`  
		Last Modified: Sat, 16 Dec 2023 12:02:14 GMT  
		Size: 62.7 MB (62728977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61648a16f8302198b16329e458e71b1a0dacd18c635781c985ee815bca93184`  
		Last Modified: Sat, 16 Dec 2023 12:02:04 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:100b580025d060b208f4d70cde09a8cd613902af99f7351beedee2f283481fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89564029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa91496d32b306e6772fa95f1767ae042c0a9320e60c9d5d0789a612b9b89d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 10:44:40 GMT
ENV KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 16 Dec 2023 10:44:55 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:56 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:56 GMT
USER kong
# Sat, 16 Dec 2023 10:44:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:56 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:56 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437cd7243bf19e3ddaf26cd91043001da81451f15a8656e28dc70523f8846066`  
		Last Modified: Sat, 16 Dec 2023 10:47:39 GMT  
		Size: 61.2 MB (61162465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b3f7db895910317703cd6867110ec13c8c1e8be7022a9f588f215fbfa284ac`  
		Last Modified: Sat, 16 Dec 2023 10:47:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2`

```console
$ docker pull kong@sha256:94c5977e8cf6c523522b2fb2065a43dee275bc61fac8495e336c4ea9501d0c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:5ebae6d82867d483323e9b94afa2c16320f67defbd6deb1c779f43a094e5d483
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93176840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1af3e874339d41dadfa6067a64191eb19b1f7b847f589f63994113e53cd527e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 11:58:40 GMT
ENV KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 16 Dec 2023 11:58:59 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:00 GMT
USER kong
# Sat, 16 Dec 2023 11:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:00 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad67bf8a12760b2dde172d4d1588e5194e6b7d3ec3b7df6b3cba3ebe70aa1770`  
		Last Modified: Sat, 16 Dec 2023 12:02:14 GMT  
		Size: 62.7 MB (62728977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61648a16f8302198b16329e458e71b1a0dacd18c635781c985ee815bca93184`  
		Last Modified: Sat, 16 Dec 2023 12:02:04 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:100b580025d060b208f4d70cde09a8cd613902af99f7351beedee2f283481fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89564029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa91496d32b306e6772fa95f1767ae042c0a9320e60c9d5d0789a612b9b89d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 10:44:40 GMT
ENV KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 16 Dec 2023 10:44:55 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:56 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:56 GMT
USER kong
# Sat, 16 Dec 2023 10:44:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:56 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:56 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437cd7243bf19e3ddaf26cd91043001da81451f15a8656e28dc70523f8846066`  
		Last Modified: Sat, 16 Dec 2023 10:47:39 GMT  
		Size: 61.2 MB (61162465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b3f7db895910317703cd6867110ec13c8c1e8be7022a9f588f215fbfa284ac`  
		Last Modified: Sat, 16 Dec 2023 10:47:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:94c5977e8cf6c523522b2fb2065a43dee275bc61fac8495e336c4ea9501d0c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5ebae6d82867d483323e9b94afa2c16320f67defbd6deb1c779f43a094e5d483
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93176840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1af3e874339d41dadfa6067a64191eb19b1f7b847f589f63994113e53cd527e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 11:58:40 GMT
ENV KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Sat, 16 Dec 2023 11:58:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 16 Dec 2023 11:58:59 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:59:00 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:59:00 GMT
USER kong
# Sat, 16 Dec 2023 11:59:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:59:00 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:59:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:59:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:59:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad67bf8a12760b2dde172d4d1588e5194e6b7d3ec3b7df6b3cba3ebe70aa1770`  
		Last Modified: Sat, 16 Dec 2023 12:02:14 GMT  
		Size: 62.7 MB (62728977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61648a16f8302198b16329e458e71b1a0dacd18c635781c985ee815bca93184`  
		Last Modified: Sat, 16 Dec 2023 12:02:04 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:100b580025d060b208f4d70cde09a8cd613902af99f7351beedee2f283481fdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89564029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa91496d32b306e6772fa95f1767ae042c0a9320e60c9d5d0789a612b9b89d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 10:44:40 GMT
ENV KONG_VERSION=3.4.2
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Sat, 16 Dec 2023 10:44:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 16 Dec 2023 10:44:55 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:56 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:56 GMT
USER kong
# Sat, 16 Dec 2023 10:44:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:56 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:56 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437cd7243bf19e3ddaf26cd91043001da81451f15a8656e28dc70523f8846066`  
		Last Modified: Sat, 16 Dec 2023 10:47:39 GMT  
		Size: 61.2 MB (61162465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b3f7db895910317703cd6867110ec13c8c1e8be7022a9f588f215fbfa284ac`  
		Last Modified: Sat, 16 Dec 2023 10:47:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5`

```console
$ docker pull kong@sha256:e8d0c74da65ba6b624203f8f825ba19be0ce2fa233324153c65182f6add22c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5` - linux; amd64

```console
$ docker pull kong@sha256:e5d979f74ee2b865582d8cefce70846f2f4e21608d35c7231fe05e1e6282736d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94409505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaf3dd270ac7abeda9304bb58e18e5be0fb01d57600354e59d1a5d70a233f10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 11:58:35 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:58:36 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:58:36 GMT
USER kong
# Sat, 16 Dec 2023 11:58:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:58:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:58:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:58:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:58:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d362b85c03043e5663d1252149889eec4c21d5bde9c89a09ff2b0670e95f4b`  
		Last Modified: Sat, 16 Dec 2023 12:01:48 GMT  
		Size: 64.0 MB (63961643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec47c99d768e1edb15d1098095f264e239ad9f05df6888420f3f416437831c0`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a42e3c863da10dba85b3ec17122fab30152a4336787114d3131ff98a02d44841
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91884840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083db3718895ee84dbc1f4773b7fd32c6fc4f6427d583e73f05005b9a3863817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 10:44:34 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:35 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:35 GMT
USER kong
# Sat, 16 Dec 2023 10:44:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:35 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:35 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361c5af99b74dbd43e763c35e9a7a948bd5f696ebe6812a05c90c30bc63ec1be`  
		Last Modified: Sat, 16 Dec 2023 10:47:15 GMT  
		Size: 63.5 MB (63483276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2420a704579187d9c2b7bb05302437a5ef4643e457fca280041f715872ab95`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5-ubuntu`

```console
$ docker pull kong@sha256:e8d0c74da65ba6b624203f8f825ba19be0ce2fa233324153c65182f6add22c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e5d979f74ee2b865582d8cefce70846f2f4e21608d35c7231fe05e1e6282736d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94409505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaf3dd270ac7abeda9304bb58e18e5be0fb01d57600354e59d1a5d70a233f10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 11:58:35 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:58:36 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:58:36 GMT
USER kong
# Sat, 16 Dec 2023 11:58:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:58:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:58:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:58:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:58:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d362b85c03043e5663d1252149889eec4c21d5bde9c89a09ff2b0670e95f4b`  
		Last Modified: Sat, 16 Dec 2023 12:01:48 GMT  
		Size: 64.0 MB (63961643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec47c99d768e1edb15d1098095f264e239ad9f05df6888420f3f416437831c0`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a42e3c863da10dba85b3ec17122fab30152a4336787114d3131ff98a02d44841
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91884840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083db3718895ee84dbc1f4773b7fd32c6fc4f6427d583e73f05005b9a3863817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 10:44:34 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:35 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:35 GMT
USER kong
# Sat, 16 Dec 2023 10:44:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:35 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:35 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361c5af99b74dbd43e763c35e9a7a948bd5f696ebe6812a05c90c30bc63ec1be`  
		Last Modified: Sat, 16 Dec 2023 10:47:15 GMT  
		Size: 63.5 MB (63483276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2420a704579187d9c2b7bb05302437a5ef4643e457fca280041f715872ab95`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0`

```console
$ docker pull kong@sha256:e8d0c74da65ba6b624203f8f825ba19be0ce2fa233324153c65182f6add22c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0` - linux; amd64

```console
$ docker pull kong@sha256:e5d979f74ee2b865582d8cefce70846f2f4e21608d35c7231fe05e1e6282736d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94409505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaf3dd270ac7abeda9304bb58e18e5be0fb01d57600354e59d1a5d70a233f10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 11:58:35 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:58:36 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:58:36 GMT
USER kong
# Sat, 16 Dec 2023 11:58:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:58:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:58:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:58:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:58:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d362b85c03043e5663d1252149889eec4c21d5bde9c89a09ff2b0670e95f4b`  
		Last Modified: Sat, 16 Dec 2023 12:01:48 GMT  
		Size: 64.0 MB (63961643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec47c99d768e1edb15d1098095f264e239ad9f05df6888420f3f416437831c0`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a42e3c863da10dba85b3ec17122fab30152a4336787114d3131ff98a02d44841
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91884840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083db3718895ee84dbc1f4773b7fd32c6fc4f6427d583e73f05005b9a3863817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 10:44:34 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:35 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:35 GMT
USER kong
# Sat, 16 Dec 2023 10:44:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:35 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:35 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361c5af99b74dbd43e763c35e9a7a948bd5f696ebe6812a05c90c30bc63ec1be`  
		Last Modified: Sat, 16 Dec 2023 10:47:15 GMT  
		Size: 63.5 MB (63483276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2420a704579187d9c2b7bb05302437a5ef4643e457fca280041f715872ab95`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0-ubuntu`

```console
$ docker pull kong@sha256:e8d0c74da65ba6b624203f8f825ba19be0ce2fa233324153c65182f6add22c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e5d979f74ee2b865582d8cefce70846f2f4e21608d35c7231fe05e1e6282736d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94409505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaf3dd270ac7abeda9304bb58e18e5be0fb01d57600354e59d1a5d70a233f10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 11:58:35 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:58:36 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:58:36 GMT
USER kong
# Sat, 16 Dec 2023 11:58:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:58:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:58:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:58:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:58:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d362b85c03043e5663d1252149889eec4c21d5bde9c89a09ff2b0670e95f4b`  
		Last Modified: Sat, 16 Dec 2023 12:01:48 GMT  
		Size: 64.0 MB (63961643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec47c99d768e1edb15d1098095f264e239ad9f05df6888420f3f416437831c0`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a42e3c863da10dba85b3ec17122fab30152a4336787114d3131ff98a02d44841
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91884840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083db3718895ee84dbc1f4773b7fd32c6fc4f6427d583e73f05005b9a3863817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 10:44:34 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:35 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:35 GMT
USER kong
# Sat, 16 Dec 2023 10:44:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:35 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:35 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361c5af99b74dbd43e763c35e9a7a948bd5f696ebe6812a05c90c30bc63ec1be`  
		Last Modified: Sat, 16 Dec 2023 10:47:15 GMT  
		Size: 63.5 MB (63483276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2420a704579187d9c2b7bb05302437a5ef4643e457fca280041f715872ab95`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:92e301995c504133e4ba0b69f6260b389553a5821a8c6e491feac3df5f859ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:52d5380e2779819916b1c1b9afe3c6aa733baaab12a4dc2e7064a492081d1330
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34229592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82061e7453178852640fa6f05498b98433f4fcf1c58ee9e6dd1b4e510d7e8683`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:06:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 01 Dec 2023 07:06:25 GMT
ARG KONG_VERSION=3.3.1
# Fri, 01 Dec 2023 07:06:25 GMT
ENV KONG_VERSION=3.3.1
# Fri, 01 Dec 2023 07:06:25 GMT
ARG KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
# Fri, 01 Dec 2023 07:06:25 GMT
ARG KONG_PREFIX=/usr/local/kong
# Fri, 01 Dec 2023 07:06:26 GMT
ENV KONG_PREFIX=/usr/local/kong
# Fri, 01 Dec 2023 07:06:26 GMT
ARG ASSET=remote
# Fri, 01 Dec 2023 07:06:26 GMT
ARG EE_PORTS
# Fri, 01 Dec 2023 07:06:26 GMT
COPY file:7815b5fca0a34ed4a30931ccd9d4786733aecc9e9b2d4c363dee07e4a5c9b32f in /tmp/kong.apk.tar.gz 
# Fri, 01 Dec 2023 07:06:32 GMT
# ARGS: ASSET=remote KONG_AMD64_SHA=b544aa8d23b544b7ec48e943e3525f6c1f33b202522020eedf91784c87de1a3d
RUN set -ex;     apk add --virtual .build-deps curl tar gzip ca-certificates;     export ARCH='amd64';     KONG_SHA256=$KONG_AMD64_SHA ;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-${KONG_VERSION}.${ARCH}.apk.tar.gz" -o /tmp/kong.apk.tar.gz       && echo "$KONG_SHA256  /tmp/kong.apk.tar.gz" | sha256sum -c -;     fi     && tar -C / -xzf /tmp/kong.apk.tar.gz     && apk add --no-cache libstdc++ libgcc perl tzdata libcap zlib zlib-dev bash yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.apk.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && apk del .build-deps     && kong version
# Fri, 01 Dec 2023 07:06:32 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 01 Dec 2023 07:06:32 GMT
USER kong
# Fri, 01 Dec 2023 07:06:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 07:06:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 01 Dec 2023 07:06:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 07:06:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong-health"] "1m0s" "10s" "0s" '\n'}
# Fri, 01 Dec 2023 07:06:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d217203619b7312ed56103e24c86c8b8873e22d87b2a033b3be222af47d6972`  
		Last Modified: Fri, 01 Dec 2023 07:08:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64e0a7832a6342ab148a3b79c7b887ae24ebd4add4bcdcbfed8dd029f411cac`  
		Last Modified: Fri, 01 Dec 2023 07:08:07 GMT  
		Size: 30.8 MB (30848978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f17c6af677aeefc80cff56534ddea0225138f58d242dc53cadb06dde1f373a7`  
		Last Modified: Fri, 01 Dec 2023 07:08:02 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:e8d0c74da65ba6b624203f8f825ba19be0ce2fa233324153c65182f6add22c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:e5d979f74ee2b865582d8cefce70846f2f4e21608d35c7231fe05e1e6282736d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94409505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaf3dd270ac7abeda9304bb58e18e5be0fb01d57600354e59d1a5d70a233f10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 11:58:35 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:58:36 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:58:36 GMT
USER kong
# Sat, 16 Dec 2023 11:58:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:58:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:58:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:58:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:58:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d362b85c03043e5663d1252149889eec4c21d5bde9c89a09ff2b0670e95f4b`  
		Last Modified: Sat, 16 Dec 2023 12:01:48 GMT  
		Size: 64.0 MB (63961643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec47c99d768e1edb15d1098095f264e239ad9f05df6888420f3f416437831c0`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a42e3c863da10dba85b3ec17122fab30152a4336787114d3131ff98a02d44841
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91884840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083db3718895ee84dbc1f4773b7fd32c6fc4f6427d583e73f05005b9a3863817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 10:44:34 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:35 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:35 GMT
USER kong
# Sat, 16 Dec 2023 10:44:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:35 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:35 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361c5af99b74dbd43e763c35e9a7a948bd5f696ebe6812a05c90c30bc63ec1be`  
		Last Modified: Sat, 16 Dec 2023 10:47:15 GMT  
		Size: 63.5 MB (63483276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2420a704579187d9c2b7bb05302437a5ef4643e457fca280041f715872ab95`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:e8d0c74da65ba6b624203f8f825ba19be0ce2fa233324153c65182f6add22c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e5d979f74ee2b865582d8cefce70846f2f4e21608d35c7231fe05e1e6282736d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94409505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbaf3dd270ac7abeda9304bb58e18e5be0fb01d57600354e59d1a5d70a233f10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 11:58:11 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 11:58:11 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 11:58:12 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 11:58:12 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 11:58:12 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 11:58:35 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 11:58:36 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 11:58:36 GMT
USER kong
# Sat, 16 Dec 2023 11:58:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 11:58:36 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 11:58:36 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 11:58:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 11:58:36 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80225c4ddb482d68ad56d9e62473b3aaf71e6b3cc5047dc79804c87f8d166405`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d362b85c03043e5663d1252149889eec4c21d5bde9c89a09ff2b0670e95f4b`  
		Last Modified: Sat, 16 Dec 2023 12:01:48 GMT  
		Size: 64.0 MB (63961643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec47c99d768e1edb15d1098095f264e239ad9f05df6888420f3f416437831c0`  
		Last Modified: Sat, 16 Dec 2023 12:01:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a42e3c863da10dba85b3ec17122fab30152a4336787114d3131ff98a02d44841
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91884840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083db3718895ee84dbc1f4773b7fd32c6fc4f6427d583e73f05005b9a3863817`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:44:17 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Sat, 16 Dec 2023 10:44:17 GMT
ARG ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ENV ASSET=ce
# Sat, 16 Dec 2023 10:44:17 GMT
ARG EE_PORTS
# Sat, 16 Dec 2023 10:44:17 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ENV KONG_VERSION=3.5.0
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Sat, 16 Dec 2023 10:44:17 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 16 Dec 2023 10:44:34 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Dec 2023 10:44:35 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 16 Dec 2023 10:44:35 GMT
USER kong
# Sat, 16 Dec 2023 10:44:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:44:35 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Dec 2023 10:44:35 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Dec 2023 10:44:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Dec 2023 10:44:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e44ff616d94c3651e47073a4174c5491897fb794b29bd964a91489138c716a`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361c5af99b74dbd43e763c35e9a7a948bd5f696ebe6812a05c90c30bc63ec1be`  
		Last Modified: Sat, 16 Dec 2023 10:47:15 GMT  
		Size: 63.5 MB (63483276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2420a704579187d9c2b7bb05302437a5ef4643e457fca280041f715872ab95`  
		Last Modified: Sat, 16 Dec 2023 10:47:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
