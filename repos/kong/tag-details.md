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
$ docker pull kong@sha256:ba39c041aad1bddd5cab6ea1137a875d15ac57b532a0e5f6794bcae7d0b2c8a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:4252ac9254855225aeba185ab3cf7fa1891af5d37ab322cdeafa1527d323dfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48136355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8037f40dd4b90c1a579b7ad23d3171522a097b00323c7a5845778b78816642a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 04 Oct 2023 00:24:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 00:24:10 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 04 Oct 2023 00:24:10 GMT
ARG ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ENV ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ARG EE_PORTS
# Wed, 04 Oct 2023 00:24:10 GMT
COPY kong.tar.gz /tmp/kong.tar.gz # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ENV KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Wed, 04 Oct 2023 00:24:10 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.4 KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
USER kong
# Wed, 04 Oct 2023 00:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Oct 2023 00:24:10 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 04 Oct 2023 00:24:10 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Oct 2023 00:24:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81995acde77c32cd0dda6aa6faf8d1058ffecc035df910d47543fe2206d6b70`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbbb6648541fd885efe231db8c876784892234968a94a140abfbe9dcc74a43`  
		Last Modified: Fri, 21 Jun 2024 01:02:43 GMT  
		Size: 44.7 MB (44721448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1795355319c3f6714b8a6eecac9948d0f48fca20e21316c5f3881a4ad6791c`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8` - unknown; unknown

```console
$ docker pull kong@sha256:47b415407a511369247571010551aa6c30ee3c052cc63dde0312e4d9980ecde5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bcdf6bab9a319c2ac589eafdd0af009254a1f0a31a199a9c3440af68e9604f`

```dockerfile
```

-	Layers:
	-	`sha256:994d1ecf008a3f4ac12fb23dc95d07acd03dd175effd209de0eb51cb6658620b`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 2.0 MB (1959467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b8b04919b2a59a6c6b38e518220d7631dd87ffd3f66c676539bc40b0a92981`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 14.9 KB (14895 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:c50f65bd030346ebc2a2a9883c7392ae32d7f1df36d665ebfcef295c1a3e101d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d191f963fa26468dc42f3cdc8cecc336333db3691dc0b334677b077d59bf4420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115643745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1953ff32d1e788fb275046185f66c9598595351e670a5caf5227ffb25867b4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 04 Oct 2023 00:24:10 GMT
ARG RELEASE
# Wed, 04 Oct 2023 00:24:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 00:24:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 00:24:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 04 Oct 2023 00:24:10 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["/bin/bash"]
# Wed, 04 Oct 2023 00:24:10 GMT
ARG ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ENV ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ARG EE_PORTS
# Wed, 04 Oct 2023 00:24:10 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ENV KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Wed, 04 Oct 2023 00:24:10 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.4 KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
USER kong
# Wed, 04 Oct 2023 00:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Oct 2023 00:24:10 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 04 Oct 2023 00:24:10 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Oct 2023 00:24:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6747641a56053f84cf5115a2c61a09af97a8603789d6d1ebc53f5080dd057fef`  
		Last Modified: Fri, 21 Jun 2024 01:03:01 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ecfca9f9cfc5213dc8cf0853f852ee35750ba976cf612fed17d2a0d4f6b0b2`  
		Last Modified: Fri, 21 Jun 2024 01:03:01 GMT  
		Size: 61.0 MB (61027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4697170bbdc2fe2a7dc81313754e44cbffb9473ade09c8e006a3ed865ed3d3`  
		Last Modified: Fri, 21 Jun 2024 01:03:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5272881cae742aaf46bb986eb33f3919438c9eabdf7d34eb62d9fc4090db5a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6116506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f5f08abc2f50971f3bbedf3c6fab855153cc97c7b36fc964e2057da469f44`

```dockerfile
```

-	Layers:
	-	`sha256:332c5abc605549f47c6cd73f8e624d225575924c296ea138db847c3ee23eef8b`  
		Last Modified: Fri, 21 Jun 2024 01:03:00 GMT  
		Size: 6.1 MB (6102306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59eba6e1d0f158c4e0faf895a4481f8731c9ec7b80102affb6ec49ffc038b212`  
		Last Modified: Fri, 21 Jun 2024 01:03:00 GMT  
		Size: 14.2 KB (14200 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.4`

```console
$ docker pull kong@sha256:ba39c041aad1bddd5cab6ea1137a875d15ac57b532a0e5f6794bcae7d0b2c8a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.4` - linux; amd64

```console
$ docker pull kong@sha256:4252ac9254855225aeba185ab3cf7fa1891af5d37ab322cdeafa1527d323dfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48136355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8037f40dd4b90c1a579b7ad23d3171522a097b00323c7a5845778b78816642a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 04 Oct 2023 00:24:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 00:24:10 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 04 Oct 2023 00:24:10 GMT
ARG ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ENV ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ARG EE_PORTS
# Wed, 04 Oct 2023 00:24:10 GMT
COPY kong.tar.gz /tmp/kong.tar.gz # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ENV KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Wed, 04 Oct 2023 00:24:10 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.4 KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
USER kong
# Wed, 04 Oct 2023 00:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Oct 2023 00:24:10 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 04 Oct 2023 00:24:10 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Oct 2023 00:24:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81995acde77c32cd0dda6aa6faf8d1058ffecc035df910d47543fe2206d6b70`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbbb6648541fd885efe231db8c876784892234968a94a140abfbe9dcc74a43`  
		Last Modified: Fri, 21 Jun 2024 01:02:43 GMT  
		Size: 44.7 MB (44721448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1795355319c3f6714b8a6eecac9948d0f48fca20e21316c5f3881a4ad6791c`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.4` - unknown; unknown

```console
$ docker pull kong@sha256:47b415407a511369247571010551aa6c30ee3c052cc63dde0312e4d9980ecde5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bcdf6bab9a319c2ac589eafdd0af009254a1f0a31a199a9c3440af68e9604f`

```dockerfile
```

-	Layers:
	-	`sha256:994d1ecf008a3f4ac12fb23dc95d07acd03dd175effd209de0eb51cb6658620b`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 2.0 MB (1959467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b8b04919b2a59a6c6b38e518220d7631dd87ffd3f66c676539bc40b0a92981`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 14.9 KB (14895 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.4-alpine`

```console
$ docker pull kong@sha256:ba39c041aad1bddd5cab6ea1137a875d15ac57b532a0e5f6794bcae7d0b2c8a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:4252ac9254855225aeba185ab3cf7fa1891af5d37ab322cdeafa1527d323dfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48136355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8037f40dd4b90c1a579b7ad23d3171522a097b00323c7a5845778b78816642a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 04 Oct 2023 00:24:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["/bin/sh"]
# Wed, 04 Oct 2023 00:24:10 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 04 Oct 2023 00:24:10 GMT
ARG ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ENV ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ARG EE_PORTS
# Wed, 04 Oct 2023 00:24:10 GMT
COPY kong.tar.gz /tmp/kong.tar.gz # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ENV KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
# Wed, 04 Oct 2023 00:24:10 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.4 KONG_AMD64_SHA=930b3b933b6c3f0393700433a919745900485d19e0cd8aba2d70aa066ccd10d2 KONG_ARM64_SHA=9027da2a4df477b462f34da9450412012ffdc0f9019e33ed7ff8e88f3df062c6
RUN set -eux;     arch="$(apk --print-arch)";     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       x86_64) KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/raw/names/kong-${arch}/versions/${KONG_VERSION}/kong-${KONG_VERSION}.${arch}.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi     && mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
USER kong
# Wed, 04 Oct 2023 00:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Oct 2023 00:24:10 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 04 Oct 2023 00:24:10 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Oct 2023 00:24:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81995acde77c32cd0dda6aa6faf8d1058ffecc035df910d47543fe2206d6b70`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbdbbb6648541fd885efe231db8c876784892234968a94a140abfbe9dcc74a43`  
		Last Modified: Fri, 21 Jun 2024 01:02:43 GMT  
		Size: 44.7 MB (44721448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1795355319c3f6714b8a6eecac9948d0f48fca20e21316c5f3881a4ad6791c`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.4-alpine` - unknown; unknown

```console
$ docker pull kong@sha256:47b415407a511369247571010551aa6c30ee3c052cc63dde0312e4d9980ecde5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (1974362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7bcdf6bab9a319c2ac589eafdd0af009254a1f0a31a199a9c3440af68e9604f`

```dockerfile
```

-	Layers:
	-	`sha256:994d1ecf008a3f4ac12fb23dc95d07acd03dd175effd209de0eb51cb6658620b`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 2.0 MB (1959467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b8b04919b2a59a6c6b38e518220d7631dd87ffd3f66c676539bc40b0a92981`  
		Last Modified: Fri, 21 Jun 2024 01:02:42 GMT  
		Size: 14.9 KB (14895 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.4-ubuntu`

```console
$ docker pull kong@sha256:c50f65bd030346ebc2a2a9883c7392ae32d7f1df36d665ebfcef295c1a3e101d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d191f963fa26468dc42f3cdc8cecc336333db3691dc0b334677b077d59bf4420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115643745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1953ff32d1e788fb275046185f66c9598595351e670a5caf5227ffb25867b4d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 04 Oct 2023 00:24:10 GMT
ARG RELEASE
# Wed, 04 Oct 2023 00:24:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 04 Oct 2023 00:24:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 04 Oct 2023 00:24:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 04 Oct 2023 00:24:10 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["/bin/bash"]
# Wed, 04 Oct 2023 00:24:10 GMT
ARG ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ENV ASSET=ce
# Wed, 04 Oct 2023 00:24:10 GMT
ARG EE_PORTS
# Wed, 04 Oct 2023 00:24:10 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ENV KONG_VERSION=2.8.4
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534
# Wed, 04 Oct 2023 00:24:10 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Wed, 04 Oct 2023 00:24:10 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.4 KONG_AMD64_SHA=e4bc62c80f717114cc486776ee453931c5de0e8eaf0901ac11dbb4b2bae14534 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 04 Oct 2023 00:24:10 GMT
USER kong
# Wed, 04 Oct 2023 00:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Oct 2023 00:24:10 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 04 Oct 2023 00:24:10 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Oct 2023 00:24:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 04 Oct 2023 00:24:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6747641a56053f84cf5115a2c61a09af97a8603789d6d1ebc53f5080dd057fef`  
		Last Modified: Fri, 21 Jun 2024 01:03:01 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ecfca9f9cfc5213dc8cf0853f852ee35750ba976cf612fed17d2a0d4f6b0b2`  
		Last Modified: Fri, 21 Jun 2024 01:03:01 GMT  
		Size: 61.0 MB (61027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4697170bbdc2fe2a7dc81313754e44cbffb9473ade09c8e006a3ed865ed3d3`  
		Last Modified: Fri, 21 Jun 2024 01:03:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5272881cae742aaf46bb986eb33f3919438c9eabdf7d34eb62d9fc4090db5a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6116506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756f5f08abc2f50971f3bbedf3c6fab855153cc97c7b36fc964e2057da469f44`

```dockerfile
```

-	Layers:
	-	`sha256:332c5abc605549f47c6cd73f8e624d225575924c296ea138db847c3ee23eef8b`  
		Last Modified: Fri, 21 Jun 2024 01:03:00 GMT  
		Size: 6.1 MB (6102306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59eba6e1d0f158c4e0faf895a4481f8731c9ec7b80102affb6ec49ffc038b212`  
		Last Modified: Fri, 21 Jun 2024 01:03:00 GMT  
		Size: 14.2 KB (14200 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:254854ee311c41d1cf04acff81df78c68934248ade7969cd719248a0ad0b034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:3d160b49452beb9284be4f1d477fcfeb3c2bb938b0e47db1738769651ec42459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97258319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d967392a66d1b2d3bd77ae7cfd8f13d3ef5303681af1098ba138d5b3cd498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9bfb45b48b84ffaf80f514b095a52620db20a68aad8177ed5b1720983d59d`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09c4454980010c5ff3a760e258d5f9a304a4110f3da0b2e1c49a86e881a0ef`  
		Last Modified: Fri, 21 Jun 2024 01:02:59 GMT  
		Size: 67.7 MB (67723278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953588e058a11320cf42aa340409ecae24ebd41b95c258cc589311d93669ce61`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:af216d3f0bf5e3dd365dc710f68a4da486b092ad579477c65f19bc4453ae1769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6135abeb1eca91fb62495568d1b0e1560449b30ae7731204b43da81568a38`

```dockerfile
```

-	Layers:
	-	`sha256:90ac06d912cdf589576194d617980493ed4df294d4077509ea41c08fe08c7c7c`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8715170f7dfec8f3646afaeeedc9969d83ad4c3458b2c464edfbadf905c95bc1`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b61fab45757711a87939a6e3986bf3e2641b8781f4075522410828cf47e0243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc29e518570edb281a05d56c8d69c68a528e97339267e7403060c82a5dc2ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf263a0587898ab134d4ed7a960807491e94fbf767972d9aeabc4b91bc4a887`  
		Last Modified: Fri, 21 Jun 2024 07:30:48 GMT  
		Size: 67.7 MB (67652504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b51104d51e336231d061ecf51bca3f358b715f35c7da45185e4b06b2354b`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:99bd4decdaf336b039a2ddfa543163cebb5460dbbb1eb840a51a79e8d30bfd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0212bbcbc131caa0ebd62e5e08c2df8205be68a52302a81c676b8827406ead0`

```dockerfile
```

-	Layers:
	-	`sha256:e869b3e21facfc9f3dea3a749fb31e978763ed65978187c8744ce7dc50af8c9f`  
		Last Modified: Fri, 21 Jun 2024 07:30:46 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae146ca14b8e9b20fa69def157dbe274214ef7cfca26c45563ae5e40f13b3ee`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull kong@sha256:254854ee311c41d1cf04acff81df78c68934248ade7969cd719248a0ad0b034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7` - linux; amd64

```console
$ docker pull kong@sha256:3d160b49452beb9284be4f1d477fcfeb3c2bb938b0e47db1738769651ec42459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97258319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d967392a66d1b2d3bd77ae7cfd8f13d3ef5303681af1098ba138d5b3cd498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9bfb45b48b84ffaf80f514b095a52620db20a68aad8177ed5b1720983d59d`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09c4454980010c5ff3a760e258d5f9a304a4110f3da0b2e1c49a86e881a0ef`  
		Last Modified: Fri, 21 Jun 2024 01:02:59 GMT  
		Size: 67.7 MB (67723278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953588e058a11320cf42aa340409ecae24ebd41b95c258cc589311d93669ce61`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:af216d3f0bf5e3dd365dc710f68a4da486b092ad579477c65f19bc4453ae1769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6135abeb1eca91fb62495568d1b0e1560449b30ae7731204b43da81568a38`

```dockerfile
```

-	Layers:
	-	`sha256:90ac06d912cdf589576194d617980493ed4df294d4077509ea41c08fe08c7c7c`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8715170f7dfec8f3646afaeeedc9969d83ad4c3458b2c464edfbadf905c95bc1`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b61fab45757711a87939a6e3986bf3e2641b8781f4075522410828cf47e0243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc29e518570edb281a05d56c8d69c68a528e97339267e7403060c82a5dc2ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf263a0587898ab134d4ed7a960807491e94fbf767972d9aeabc4b91bc4a887`  
		Last Modified: Fri, 21 Jun 2024 07:30:48 GMT  
		Size: 67.7 MB (67652504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b51104d51e336231d061ecf51bca3f358b715f35c7da45185e4b06b2354b`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:99bd4decdaf336b039a2ddfa543163cebb5460dbbb1eb840a51a79e8d30bfd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0212bbcbc131caa0ebd62e5e08c2df8205be68a52302a81c676b8827406ead0`

```dockerfile
```

-	Layers:
	-	`sha256:e869b3e21facfc9f3dea3a749fb31e978763ed65978187c8744ce7dc50af8c9f`  
		Last Modified: Fri, 21 Jun 2024 07:30:46 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae146ca14b8e9b20fa69def157dbe274214ef7cfca26c45563ae5e40f13b3ee`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7-ubuntu`

```console
$ docker pull kong@sha256:254854ee311c41d1cf04acff81df78c68934248ade7969cd719248a0ad0b034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3d160b49452beb9284be4f1d477fcfeb3c2bb938b0e47db1738769651ec42459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97258319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d967392a66d1b2d3bd77ae7cfd8f13d3ef5303681af1098ba138d5b3cd498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9bfb45b48b84ffaf80f514b095a52620db20a68aad8177ed5b1720983d59d`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09c4454980010c5ff3a760e258d5f9a304a4110f3da0b2e1c49a86e881a0ef`  
		Last Modified: Fri, 21 Jun 2024 01:02:59 GMT  
		Size: 67.7 MB (67723278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953588e058a11320cf42aa340409ecae24ebd41b95c258cc589311d93669ce61`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:af216d3f0bf5e3dd365dc710f68a4da486b092ad579477c65f19bc4453ae1769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6135abeb1eca91fb62495568d1b0e1560449b30ae7731204b43da81568a38`

```dockerfile
```

-	Layers:
	-	`sha256:90ac06d912cdf589576194d617980493ed4df294d4077509ea41c08fe08c7c7c`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8715170f7dfec8f3646afaeeedc9969d83ad4c3458b2c464edfbadf905c95bc1`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b61fab45757711a87939a6e3986bf3e2641b8781f4075522410828cf47e0243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc29e518570edb281a05d56c8d69c68a528e97339267e7403060c82a5dc2ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf263a0587898ab134d4ed7a960807491e94fbf767972d9aeabc4b91bc4a887`  
		Last Modified: Fri, 21 Jun 2024 07:30:48 GMT  
		Size: 67.7 MB (67652504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b51104d51e336231d061ecf51bca3f358b715f35c7da45185e4b06b2354b`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:99bd4decdaf336b039a2ddfa543163cebb5460dbbb1eb840a51a79e8d30bfd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0212bbcbc131caa0ebd62e5e08c2df8205be68a52302a81c676b8827406ead0`

```dockerfile
```

-	Layers:
	-	`sha256:e869b3e21facfc9f3dea3a749fb31e978763ed65978187c8744ce7dc50af8c9f`  
		Last Modified: Fri, 21 Jun 2024 07:30:46 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae146ca14b8e9b20fa69def157dbe274214ef7cfca26c45563ae5e40f13b3ee`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.0`

```console
$ docker pull kong@sha256:254854ee311c41d1cf04acff81df78c68934248ade7969cd719248a0ad0b034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.0` - linux; amd64

```console
$ docker pull kong@sha256:3d160b49452beb9284be4f1d477fcfeb3c2bb938b0e47db1738769651ec42459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97258319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d967392a66d1b2d3bd77ae7cfd8f13d3ef5303681af1098ba138d5b3cd498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9bfb45b48b84ffaf80f514b095a52620db20a68aad8177ed5b1720983d59d`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09c4454980010c5ff3a760e258d5f9a304a4110f3da0b2e1c49a86e881a0ef`  
		Last Modified: Fri, 21 Jun 2024 01:02:59 GMT  
		Size: 67.7 MB (67723278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953588e058a11320cf42aa340409ecae24ebd41b95c258cc589311d93669ce61`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.0` - unknown; unknown

```console
$ docker pull kong@sha256:af216d3f0bf5e3dd365dc710f68a4da486b092ad579477c65f19bc4453ae1769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6135abeb1eca91fb62495568d1b0e1560449b30ae7731204b43da81568a38`

```dockerfile
```

-	Layers:
	-	`sha256:90ac06d912cdf589576194d617980493ed4df294d4077509ea41c08fe08c7c7c`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8715170f7dfec8f3646afaeeedc9969d83ad4c3458b2c464edfbadf905c95bc1`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b61fab45757711a87939a6e3986bf3e2641b8781f4075522410828cf47e0243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc29e518570edb281a05d56c8d69c68a528e97339267e7403060c82a5dc2ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf263a0587898ab134d4ed7a960807491e94fbf767972d9aeabc4b91bc4a887`  
		Last Modified: Fri, 21 Jun 2024 07:30:48 GMT  
		Size: 67.7 MB (67652504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b51104d51e336231d061ecf51bca3f358b715f35c7da45185e4b06b2354b`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.0` - unknown; unknown

```console
$ docker pull kong@sha256:99bd4decdaf336b039a2ddfa543163cebb5460dbbb1eb840a51a79e8d30bfd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0212bbcbc131caa0ebd62e5e08c2df8205be68a52302a81c676b8827406ead0`

```dockerfile
```

-	Layers:
	-	`sha256:e869b3e21facfc9f3dea3a749fb31e978763ed65978187c8744ce7dc50af8c9f`  
		Last Modified: Fri, 21 Jun 2024 07:30:46 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae146ca14b8e9b20fa69def157dbe274214ef7cfca26c45563ae5e40f13b3ee`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.0-ubuntu`

```console
$ docker pull kong@sha256:254854ee311c41d1cf04acff81df78c68934248ade7969cd719248a0ad0b034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3d160b49452beb9284be4f1d477fcfeb3c2bb938b0e47db1738769651ec42459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97258319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d967392a66d1b2d3bd77ae7cfd8f13d3ef5303681af1098ba138d5b3cd498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9bfb45b48b84ffaf80f514b095a52620db20a68aad8177ed5b1720983d59d`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09c4454980010c5ff3a760e258d5f9a304a4110f3da0b2e1c49a86e881a0ef`  
		Last Modified: Fri, 21 Jun 2024 01:02:59 GMT  
		Size: 67.7 MB (67723278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953588e058a11320cf42aa340409ecae24ebd41b95c258cc589311d93669ce61`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:af216d3f0bf5e3dd365dc710f68a4da486b092ad579477c65f19bc4453ae1769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6135abeb1eca91fb62495568d1b0e1560449b30ae7731204b43da81568a38`

```dockerfile
```

-	Layers:
	-	`sha256:90ac06d912cdf589576194d617980493ed4df294d4077509ea41c08fe08c7c7c`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8715170f7dfec8f3646afaeeedc9969d83ad4c3458b2c464edfbadf905c95bc1`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b61fab45757711a87939a6e3986bf3e2641b8781f4075522410828cf47e0243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc29e518570edb281a05d56c8d69c68a528e97339267e7403060c82a5dc2ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf263a0587898ab134d4ed7a960807491e94fbf767972d9aeabc4b91bc4a887`  
		Last Modified: Fri, 21 Jun 2024 07:30:48 GMT  
		Size: 67.7 MB (67652504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b51104d51e336231d061ecf51bca3f358b715f35c7da45185e4b06b2354b`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:99bd4decdaf336b039a2ddfa543163cebb5460dbbb1eb840a51a79e8d30bfd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0212bbcbc131caa0ebd62e5e08c2df8205be68a52302a81c676b8827406ead0`

```dockerfile
```

-	Layers:
	-	`sha256:e869b3e21facfc9f3dea3a749fb31e978763ed65978187c8744ce7dc50af8c9f`  
		Last Modified: Fri, 21 Jun 2024 07:30:46 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae146ca14b8e9b20fa69def157dbe274214ef7cfca26c45563ae5e40f13b3ee`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:254854ee311c41d1cf04acff81df78c68934248ade7969cd719248a0ad0b034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:3d160b49452beb9284be4f1d477fcfeb3c2bb938b0e47db1738769651ec42459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97258319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d967392a66d1b2d3bd77ae7cfd8f13d3ef5303681af1098ba138d5b3cd498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9bfb45b48b84ffaf80f514b095a52620db20a68aad8177ed5b1720983d59d`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09c4454980010c5ff3a760e258d5f9a304a4110f3da0b2e1c49a86e881a0ef`  
		Last Modified: Fri, 21 Jun 2024 01:02:59 GMT  
		Size: 67.7 MB (67723278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953588e058a11320cf42aa340409ecae24ebd41b95c258cc589311d93669ce61`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:af216d3f0bf5e3dd365dc710f68a4da486b092ad579477c65f19bc4453ae1769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6135abeb1eca91fb62495568d1b0e1560449b30ae7731204b43da81568a38`

```dockerfile
```

-	Layers:
	-	`sha256:90ac06d912cdf589576194d617980493ed4df294d4077509ea41c08fe08c7c7c`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8715170f7dfec8f3646afaeeedc9969d83ad4c3458b2c464edfbadf905c95bc1`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b61fab45757711a87939a6e3986bf3e2641b8781f4075522410828cf47e0243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc29e518570edb281a05d56c8d69c68a528e97339267e7403060c82a5dc2ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf263a0587898ab134d4ed7a960807491e94fbf767972d9aeabc4b91bc4a887`  
		Last Modified: Fri, 21 Jun 2024 07:30:48 GMT  
		Size: 67.7 MB (67652504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b51104d51e336231d061ecf51bca3f358b715f35c7da45185e4b06b2354b`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:99bd4decdaf336b039a2ddfa543163cebb5460dbbb1eb840a51a79e8d30bfd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0212bbcbc131caa0ebd62e5e08c2df8205be68a52302a81c676b8827406ead0`

```dockerfile
```

-	Layers:
	-	`sha256:e869b3e21facfc9f3dea3a749fb31e978763ed65978187c8744ce7dc50af8c9f`  
		Last Modified: Fri, 21 Jun 2024 07:30:46 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae146ca14b8e9b20fa69def157dbe274214ef7cfca26c45563ae5e40f13b3ee`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:254854ee311c41d1cf04acff81df78c68934248ade7969cd719248a0ad0b034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3d160b49452beb9284be4f1d477fcfeb3c2bb938b0e47db1738769651ec42459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97258319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32d967392a66d1b2d3bd77ae7cfd8f13d3ef5303681af1098ba138d5b3cd498`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a9bfb45b48b84ffaf80f514b095a52620db20a68aad8177ed5b1720983d59d`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09c4454980010c5ff3a760e258d5f9a304a4110f3da0b2e1c49a86e881a0ef`  
		Last Modified: Fri, 21 Jun 2024 01:02:59 GMT  
		Size: 67.7 MB (67723278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953588e058a11320cf42aa340409ecae24ebd41b95c258cc589311d93669ce61`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:af216d3f0bf5e3dd365dc710f68a4da486b092ad579477c65f19bc4453ae1769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0d6135abeb1eca91fb62495568d1b0e1560449b30ae7731204b43da81568a38`

```dockerfile
```

-	Layers:
	-	`sha256:90ac06d912cdf589576194d617980493ed4df294d4077509ea41c08fe08c7c7c`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8715170f7dfec8f3646afaeeedc9969d83ad4c3458b2c464edfbadf905c95bc1`  
		Last Modified: Fri, 21 Jun 2024 01:02:58 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b61fab45757711a87939a6e3986bf3e2641b8781f4075522410828cf47e0243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc29e518570edb281a05d56c8d69c68a528e97339267e7403060c82a5dc2ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 03:39:31 GMT
ARG RELEASE
# Mon, 03 Jun 2024 03:39:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 03:39:31 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["/bin/bash"]
# Mon, 03 Jun 2024 03:39:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Mon, 03 Jun 2024 03:39:31 GMT
ARG ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ENV ASSET=ce
# Mon, 03 Jun 2024 03:39:31 GMT
ARG EE_PORTS
# Mon, 03 Jun 2024 03:39:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ENV KONG_VERSION=3.7.0
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4
# Mon, 03 Jun 2024 03:39:31 GMT
ARG KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
# Mon, 03 Jun 2024 03:39:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.0 KONG_AMD64_SHA=71b946cac188653eb29714f21b98eb146cec536e05a5818a49007f9211e572d4 KONG_ARM64_SHA=fb01282dfe9bf42ba27df30c2bc269aadac3ae3f298ba535f77b15a7bff2f6df
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 03 Jun 2024 03:39:31 GMT
USER kong
# Mon, 03 Jun 2024 03:39:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 03 Jun 2024 03:39:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 03 Jun 2024 03:39:31 GMT
STOPSIGNAL SIGQUIT
# Mon, 03 Jun 2024 03:39:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Mon, 03 Jun 2024 03:39:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf263a0587898ab134d4ed7a960807491e94fbf767972d9aeabc4b91bc4a887`  
		Last Modified: Fri, 21 Jun 2024 07:30:48 GMT  
		Size: 67.7 MB (67652504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e1b51104d51e336231d061ecf51bca3f358b715f35c7da45185e4b06b2354b`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:99bd4decdaf336b039a2ddfa543163cebb5460dbbb1eb840a51a79e8d30bfd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0212bbcbc131caa0ebd62e5e08c2df8205be68a52302a81c676b8827406ead0`

```dockerfile
```

-	Layers:
	-	`sha256:e869b3e21facfc9f3dea3a749fb31e978763ed65978187c8744ce7dc50af8c9f`  
		Last Modified: Fri, 21 Jun 2024 07:30:46 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae146ca14b8e9b20fa69def157dbe274214ef7cfca26c45563ae5e40f13b3ee`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
