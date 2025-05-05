<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2`](#kong2)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-alpine`](#kong28-alpine)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.5`](#kong285)
-	[`kong:2.8.5-alpine`](#kong285-alpine)
-	[`kong:2.8.5-ubuntu`](#kong285-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.4`](#kong34)
-	[`kong:3.4-ubuntu`](#kong34-ubuntu)
-	[`kong:3.4.2`](#kong342)
-	[`kong:3.4.2-ubuntu`](#kong342-ubuntu)
-	[`kong:3.6`](#kong36)
-	[`kong:3.6-ubuntu`](#kong36-ubuntu)
-	[`kong:3.6.1`](#kong361)
-	[`kong:3.6.1-ubuntu`](#kong361-ubuntu)
-	[`kong:3.7`](#kong37)
-	[`kong:3.7-ubuntu`](#kong37-ubuntu)
-	[`kong:3.7.1`](#kong371)
-	[`kong:3.7.1-ubuntu`](#kong371-ubuntu)
-	[`kong:3.8`](#kong38)
-	[`kong:3.8-ubuntu`](#kong38-ubuntu)
-	[`kong:3.8.0`](#kong380)
-	[`kong:3.8.0-ubuntu`](#kong380-ubuntu)
-	[`kong:3.9`](#kong39)
-	[`kong:3.9-ubuntu`](#kong39-ubuntu)
-	[`kong:3.9.0`](#kong390)
-	[`kong:3.9.0-ubuntu`](#kong390-ubuntu)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2`

```console
$ docker pull kong@sha256:34bbeaf6ee4c2db5f5c33ecf4793f29155753e2191b121eb25ffb6d8f151b37b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:da4b2c2fa9506d147db9143ddfc1fe964a1c0c9941e24e6dd40a4e9ac8e24092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34510255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9d4739f5626bd3f11c53e55b9064b02436a260054d817343b7eb7927699464`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=remote
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.tar.gz /tmp/kong.tar.gz # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: KONG_VERSION=2.8.5 KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332 KONG_PREFIX=/usr/local/kong ASSET=remote EE_PORTS=
RUN set -ex;     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     KONG_SHA256=$KONG_AMD64_SHA ;     apk add --no-cache curl bash ca-certificates;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/alpine/any-version/main/x86_64/kong-${KONG_VERSION}.apk" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;     fi     && apk add --no-cache --virtual .build-deps tar gzip     && tar -C / -xzf /tmp/kong.tar.gz     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zlib zlib-dev bash luarocks yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && ln -sf /usr/local/lib/luarocks/*/luarocks/*/bin/luarocks-admin /usr/local/bin/luarocks-admin     && apk del .build-deps     && kong version # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9851a7d64f2f33b458ca3f24efe10b9058a265c533955fa3424537aef8b42d81`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eea477ea8d85533fb0a730d13829624f62f32239573de255b64ae0a7e865412`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 31.1 MB (31090831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab4817db5a08b6f1059277fd270c6a6ecfe0051048197eec6cd9a8a8a9f7b65`  
		Last Modified: Fri, 14 Feb 2025 19:13:10 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2` - unknown; unknown

```console
$ docker pull kong@sha256:fe1a1eabdb85dc0651b3f9d0bffd515ffd84b9766029c25e1bbc4efd5b460558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7aea4c4e212045ce2dad76d214dbd1d7004250c78f7ea1d9f831a49a065ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:4c1b61d9afe9c611bf9c223814d034e7baee9006f327e304db8f3b7459518f3d`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 1.9 MB (1920833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7530a20bce4bcbbe433d0bf410ef53adda7687befb49d63b6c9bffd258bb5ac9`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8`

```console
$ docker pull kong@sha256:34bbeaf6ee4c2db5f5c33ecf4793f29155753e2191b121eb25ffb6d8f151b37b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:da4b2c2fa9506d147db9143ddfc1fe964a1c0c9941e24e6dd40a4e9ac8e24092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34510255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9d4739f5626bd3f11c53e55b9064b02436a260054d817343b7eb7927699464`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=remote
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.tar.gz /tmp/kong.tar.gz # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: KONG_VERSION=2.8.5 KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332 KONG_PREFIX=/usr/local/kong ASSET=remote EE_PORTS=
RUN set -ex;     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     KONG_SHA256=$KONG_AMD64_SHA ;     apk add --no-cache curl bash ca-certificates;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/alpine/any-version/main/x86_64/kong-${KONG_VERSION}.apk" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;     fi     && apk add --no-cache --virtual .build-deps tar gzip     && tar -C / -xzf /tmp/kong.tar.gz     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zlib zlib-dev bash luarocks yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && ln -sf /usr/local/lib/luarocks/*/luarocks/*/bin/luarocks-admin /usr/local/bin/luarocks-admin     && apk del .build-deps     && kong version # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9851a7d64f2f33b458ca3f24efe10b9058a265c533955fa3424537aef8b42d81`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eea477ea8d85533fb0a730d13829624f62f32239573de255b64ae0a7e865412`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 31.1 MB (31090831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab4817db5a08b6f1059277fd270c6a6ecfe0051048197eec6cd9a8a8a9f7b65`  
		Last Modified: Fri, 14 Feb 2025 19:13:10 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8` - unknown; unknown

```console
$ docker pull kong@sha256:fe1a1eabdb85dc0651b3f9d0bffd515ffd84b9766029c25e1bbc4efd5b460558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7aea4c4e212045ce2dad76d214dbd1d7004250c78f7ea1d9f831a49a065ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:4c1b61d9afe9c611bf9c223814d034e7baee9006f327e304db8f3b7459518f3d`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 1.9 MB (1920833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7530a20bce4bcbbe433d0bf410ef53adda7687befb49d63b6c9bffd258bb5ac9`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8-alpine`

```console
$ docker pull kong@sha256:34bbeaf6ee4c2db5f5c33ecf4793f29155753e2191b121eb25ffb6d8f151b37b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-alpine` - linux; amd64

```console
$ docker pull kong@sha256:da4b2c2fa9506d147db9143ddfc1fe964a1c0c9941e24e6dd40a4e9ac8e24092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34510255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9d4739f5626bd3f11c53e55b9064b02436a260054d817343b7eb7927699464`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=remote
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.tar.gz /tmp/kong.tar.gz # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: KONG_VERSION=2.8.5 KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332 KONG_PREFIX=/usr/local/kong ASSET=remote EE_PORTS=
RUN set -ex;     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     KONG_SHA256=$KONG_AMD64_SHA ;     apk add --no-cache curl bash ca-certificates;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/alpine/any-version/main/x86_64/kong-${KONG_VERSION}.apk" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;     fi     && apk add --no-cache --virtual .build-deps tar gzip     && tar -C / -xzf /tmp/kong.tar.gz     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zlib zlib-dev bash luarocks yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && ln -sf /usr/local/lib/luarocks/*/luarocks/*/bin/luarocks-admin /usr/local/bin/luarocks-admin     && apk del .build-deps     && kong version # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9851a7d64f2f33b458ca3f24efe10b9058a265c533955fa3424537aef8b42d81`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eea477ea8d85533fb0a730d13829624f62f32239573de255b64ae0a7e865412`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 31.1 MB (31090831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab4817db5a08b6f1059277fd270c6a6ecfe0051048197eec6cd9a8a8a9f7b65`  
		Last Modified: Fri, 14 Feb 2025 19:13:10 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-alpine` - unknown; unknown

```console
$ docker pull kong@sha256:fe1a1eabdb85dc0651b3f9d0bffd515ffd84b9766029c25e1bbc4efd5b460558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7aea4c4e212045ce2dad76d214dbd1d7004250c78f7ea1d9f831a49a065ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:4c1b61d9afe9c611bf9c223814d034e7baee9006f327e304db8f3b7459518f3d`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 1.9 MB (1920833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7530a20bce4bcbbe433d0bf410ef53adda7687befb49d63b6c9bffd258bb5ac9`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:9f93c62fb145e65edcb1a94db68c7aa71dba5b970468e689509b9eacf9fb0631
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:a1048cc109adab36f85aeecc09e0bd503b363766a2616f15a6f365c11a9c8b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185218496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f024d139147b98cb293d7a050a6edab8a574687f47e17b7dcc338549ce8363a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ARG RELEASE
# Mon, 01 Jul 2024 13:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 01 Jul 2024 13:31:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 01 Jul 2024 13:31:38 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 01 Jul 2024 13:31:38 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/bash"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=ce
# Mon, 01 Jul 2024 13:31:38 GMT
ENV ASSET=ce
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8675294cd7d9c15cea0d6d4b15fcb2ed512c9c1773fd52b92233be77e14ff6c7`  
		Last Modified: Mon, 05 May 2025 16:36:21 GMT  
		Size: 25.1 MB (25081958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8a6bf1c19bc39746707169d01f507cdaa1340132e7ae1f8b9acdd4895f83fa`  
		Last Modified: Mon, 05 May 2025 16:36:24 GMT  
		Size: 130.6 MB (130603042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce28407a371606ab56bcf390d7b2c26dd21e11b2bab5148a11753ad44850e14`  
		Last Modified: Mon, 05 May 2025 16:36:20 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:7c56bc9211ea1b95b4a8ba67f291fdbb19db3b6087a82df6eed3153d6cc2946d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7147409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef147c9dc8186eb3dcc13cbb561dc87df95b3013cd0a4d1e324a5b3148bc4df`

```dockerfile
```

-	Layers:
	-	`sha256:4ff9bce42ac5ce4aa47383f94f0f9142ed6b7d35c82a976a9527b721fa3b3ad0`  
		Last Modified: Mon, 05 May 2025 16:36:20 GMT  
		Size: 7.1 MB (7132923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477a14cc21205045b0ab52024034386f67a3155fbd3e10ee9932bacd7e2237b4`  
		Last Modified: Mon, 05 May 2025 16:36:20 GMT  
		Size: 14.5 KB (14486 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5`

```console
$ docker pull kong@sha256:34bbeaf6ee4c2db5f5c33ecf4793f29155753e2191b121eb25ffb6d8f151b37b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5` - linux; amd64

```console
$ docker pull kong@sha256:da4b2c2fa9506d147db9143ddfc1fe964a1c0c9941e24e6dd40a4e9ac8e24092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34510255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9d4739f5626bd3f11c53e55b9064b02436a260054d817343b7eb7927699464`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=remote
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.tar.gz /tmp/kong.tar.gz # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: KONG_VERSION=2.8.5 KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332 KONG_PREFIX=/usr/local/kong ASSET=remote EE_PORTS=
RUN set -ex;     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     KONG_SHA256=$KONG_AMD64_SHA ;     apk add --no-cache curl bash ca-certificates;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/alpine/any-version/main/x86_64/kong-${KONG_VERSION}.apk" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;     fi     && apk add --no-cache --virtual .build-deps tar gzip     && tar -C / -xzf /tmp/kong.tar.gz     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zlib zlib-dev bash luarocks yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && ln -sf /usr/local/lib/luarocks/*/luarocks/*/bin/luarocks-admin /usr/local/bin/luarocks-admin     && apk del .build-deps     && kong version # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9851a7d64f2f33b458ca3f24efe10b9058a265c533955fa3424537aef8b42d81`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eea477ea8d85533fb0a730d13829624f62f32239573de255b64ae0a7e865412`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 31.1 MB (31090831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab4817db5a08b6f1059277fd270c6a6ecfe0051048197eec6cd9a8a8a9f7b65`  
		Last Modified: Fri, 14 Feb 2025 19:13:10 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5` - unknown; unknown

```console
$ docker pull kong@sha256:fe1a1eabdb85dc0651b3f9d0bffd515ffd84b9766029c25e1bbc4efd5b460558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7aea4c4e212045ce2dad76d214dbd1d7004250c78f7ea1d9f831a49a065ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:4c1b61d9afe9c611bf9c223814d034e7baee9006f327e304db8f3b7459518f3d`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 1.9 MB (1920833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7530a20bce4bcbbe433d0bf410ef53adda7687befb49d63b6c9bffd258bb5ac9`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-alpine`

```console
$ docker pull kong@sha256:34bbeaf6ee4c2db5f5c33ecf4793f29155753e2191b121eb25ffb6d8f151b37b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-alpine` - linux; amd64

```console
$ docker pull kong@sha256:da4b2c2fa9506d147db9143ddfc1fe964a1c0c9941e24e6dd40a4e9ac8e24092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 MB (34510255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9d4739f5626bd3f11c53e55b9064b02436a260054d817343b7eb7927699464`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_PREFIX=/usr/local/kong
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=remote
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.tar.gz /tmp/kong.tar.gz # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: KONG_VERSION=2.8.5 KONG_AMD64_SHA=22a5cd7c981ec15b34db105aabac7815bd589380a8d27d0c9e138657a9da6332 KONG_PREFIX=/usr/local/kong ASSET=remote EE_PORTS=
RUN set -ex;     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     KONG_SHA256=$KONG_AMD64_SHA ;     apk add --no-cache curl bash ca-certificates;     if [ "$ASSET" = "remote" ] ; then       curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/alpine/any-version/main/x86_64/kong-${KONG_VERSION}.apk" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;     fi     && apk add --no-cache --virtual .build-deps tar gzip     && tar -C / -xzf /tmp/kong.tar.gz     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zlib zlib-dev bash luarocks yaml     && adduser -S kong     && addgroup -S kong     && mkdir -p "${KONG_PREFIX}"     && chown -R kong:0 ${KONG_PREFIX}     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u ${KONG_PREFIX}     && rm -rf /tmp/kong.tar.gz     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && ln -sf /usr/local/lib/luarocks/*/luarocks/*/bin/luarocks-admin /usr/local/bin/luarocks-admin     && apk del .build-deps     && kong version # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9851a7d64f2f33b458ca3f24efe10b9058a265c533955fa3424537aef8b42d81`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eea477ea8d85533fb0a730d13829624f62f32239573de255b64ae0a7e865412`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 31.1 MB (31090831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab4817db5a08b6f1059277fd270c6a6ecfe0051048197eec6cd9a8a8a9f7b65`  
		Last Modified: Fri, 14 Feb 2025 19:13:10 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-alpine` - unknown; unknown

```console
$ docker pull kong@sha256:fe1a1eabdb85dc0651b3f9d0bffd515ffd84b9766029c25e1bbc4efd5b460558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7aea4c4e212045ce2dad76d214dbd1d7004250c78f7ea1d9f831a49a065ab5f`

```dockerfile
```

-	Layers:
	-	`sha256:4c1b61d9afe9c611bf9c223814d034e7baee9006f327e304db8f3b7459518f3d`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 1.9 MB (1920833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7530a20bce4bcbbe433d0bf410ef53adda7687befb49d63b6c9bffd258bb5ac9`  
		Last Modified: Fri, 14 Feb 2025 19:13:11 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:9f93c62fb145e65edcb1a94db68c7aa71dba5b970468e689509b9eacf9fb0631
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:a1048cc109adab36f85aeecc09e0bd503b363766a2616f15a6f365c11a9c8b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185218496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f024d139147b98cb293d7a050a6edab8a574687f47e17b7dcc338549ce8363a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ARG RELEASE
# Mon, 01 Jul 2024 13:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 01 Jul 2024 13:31:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 01 Jul 2024 13:31:38 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 01 Jul 2024 13:31:38 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/bash"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=ce
# Mon, 01 Jul 2024 13:31:38 GMT
ENV ASSET=ce
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8675294cd7d9c15cea0d6d4b15fcb2ed512c9c1773fd52b92233be77e14ff6c7`  
		Last Modified: Mon, 05 May 2025 16:36:21 GMT  
		Size: 25.1 MB (25081958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8a6bf1c19bc39746707169d01f507cdaa1340132e7ae1f8b9acdd4895f83fa`  
		Last Modified: Mon, 05 May 2025 16:36:24 GMT  
		Size: 130.6 MB (130603042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce28407a371606ab56bcf390d7b2c26dd21e11b2bab5148a11753ad44850e14`  
		Last Modified: Mon, 05 May 2025 16:36:20 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:7c56bc9211ea1b95b4a8ba67f291fdbb19db3b6087a82df6eed3153d6cc2946d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7147409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef147c9dc8186eb3dcc13cbb561dc87df95b3013cd0a4d1e324a5b3148bc4df`

```dockerfile
```

-	Layers:
	-	`sha256:4ff9bce42ac5ce4aa47383f94f0f9142ed6b7d35c82a976a9527b721fa3b3ad0`  
		Last Modified: Mon, 05 May 2025 16:36:20 GMT  
		Size: 7.1 MB (7132923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477a14cc21205045b0ab52024034386f67a3155fbd3e10ee9932bacd7e2237b4`  
		Last Modified: Mon, 05 May 2025 16:36:20 GMT  
		Size: 14.5 KB (14486 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:81cb84a14ece9369a93b62ab055dec078efd6744c393d8c78ad49a681f26ff79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:64b511bd7904fb453b67a7546412f9fa90023fb0bc894b175c50c0738cad7bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120292359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29dee4714e746c926a4b043ffedfa7e53b2309d09049452a31e7d670e8ada6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33641554fa01162df8a1f58e295f7cd7500ea15d3384f0039376ca23ee59283b`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 90.6 MB (90573542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75156dcff079865c8eb035aefc6fee2747da1c5eebf4b4f27f159fb6c94ffec3`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:c640d31d180ef175d0ab0cbd49a316eae008b20b11a165557a47d84923da3307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71885738b53967ede0279526d34f0873f2b1b92fd10988fac560d143bc8efb3a`

```dockerfile
```

-	Layers:
	-	`sha256:f086e76b248ffde645e0977b09c477ba1b048dea0b3f840700a6ce629c55f832`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 5.3 MB (5289699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e7fb4268f68b7e8a15927e77eeb71bec82746caf10c48199b44fab0c9e9862`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fadcac914015602c659e84eaeb5a613bce26d8802e552e430d0e8081d611e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118733966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376ab1d5d1f06c7709e2de91c67eb7f9e679e5c1531839b901cff68e0430b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fb2e4918d8e46e87cafdab9800e8200b013313dea30d1e371b6b5a638c93f8`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e66824736c60174bbd80ffb5c8cc7936ce492d205165f933ad218f673d635`  
		Last Modified: Wed, 09 Apr 2025 08:20:06 GMT  
		Size: 89.9 MB (89885725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7d4eff5302e5c62b203443077f3c29e98b8a8d701b949f4368a40829b7054`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:d1137d667449bf4b6e3aa084601bd079d3f14ecd5ef371789763224d794a068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70af9163360fb26ba3244de5487a4c612789c16b7384a10ba213d688809113fc`

```dockerfile
```

-	Layers:
	-	`sha256:0ba117d7e761e4a87609c63563f83f6c34e132a843aa5b23cc5b5e71f4c90fa8`  
		Last Modified: Wed, 09 Apr 2025 08:20:04 GMT  
		Size: 5.3 MB (5296858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f99a09021aa6d5a1d4f1409373eb74121649f1bcc1ae8d0b428bb425f0c575`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:550c5b6c7e6711d41f2fd106f2e7e2dd0cbc08f218ae57d1cb1049e494fe696b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:03c0560c259bd43ab2cfafb65daa4566369e28657b4dee1eb17538f298fd57f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92246411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5a1d0ded28c8802ccd059c25ee7ec2748b151b018aaaa97068ad867bd20bd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:47 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:47 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:47 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ENV KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 14 Jun 2024 20:58:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
USER kong
# Fri, 14 Jun 2024 20:58:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d0b44ace46418c68cce30bd9a30fb1169ca51d944f3119e822e55aa1d87bd`  
		Last Modified: Mon, 05 May 2025 16:35:54 GMT  
		Size: 62.7 MB (62712515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5bb632ea7418833d8a765520cc8284d9919cf4f96a5482547b1c586a7d981`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:bdd62e750816592d7e0a00d5e6a86c3c2df4dff29fcecb4013f0935fc88a64cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae9e5cf7289b8dc01878752334d248a1402b547c58188fe8f2adc047d361270`

```dockerfile
```

-	Layers:
	-	`sha256:94d220fb1fe008811f2adb0afde87dbf2db2a0f8a0baa290eebdd1a590af7a07`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 5.9 MB (5920970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6b95d4c4ff6f560bbba03031b4d60f366e3acb883547c1eaeae27712272e00`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7adb5f70fa01dc2a9cec093de1366dc96aef221430e19792330709158e1b4a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88527321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f661eca62c761f5a5969e07581b2b4af18c7934896c2d3b8ac331f4bd0d3d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:47 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:47 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:47 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ENV KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 14 Jun 2024 20:58:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
USER kong
# Fri, 14 Jun 2024 20:58:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b810ebf0ac95666201d639bcd8cfcc768af87f5a9acfa18ca6047b3436b9fa2`  
		Last Modified: Wed, 09 Apr 2025 08:23:09 GMT  
		Size: 61.2 MB (61171811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b8745359a7bd94737ba90b46b63346adb4dca9d9d990f9630f71de3b2b095`  
		Last Modified: Wed, 09 Apr 2025 08:23:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:aa4789e6ee8d7078136ffa491ce5ba7fa2deff755f47615db13481dd4d38d6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5326c66c1ecfa16d62d09e3b868c0801405355aab79de56ea0bd0b3f1e6f287`

```dockerfile
```

-	Layers:
	-	`sha256:4ed24048628ec657ee74b1ed5e362a18b78939b7224ed318118ad8d99ab13502`  
		Last Modified: Wed, 09 Apr 2025 08:23:08 GMT  
		Size: 5.9 MB (5899049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1aa1f989eb04d050d30d82e3dcd2f426767543a6a49871b6751b83d35bca53`  
		Last Modified: Wed, 09 Apr 2025 08:23:07 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:550c5b6c7e6711d41f2fd106f2e7e2dd0cbc08f218ae57d1cb1049e494fe696b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:03c0560c259bd43ab2cfafb65daa4566369e28657b4dee1eb17538f298fd57f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92246411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5a1d0ded28c8802ccd059c25ee7ec2748b151b018aaaa97068ad867bd20bd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:47 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:47 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:47 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ENV KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 14 Jun 2024 20:58:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
USER kong
# Fri, 14 Jun 2024 20:58:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d0b44ace46418c68cce30bd9a30fb1169ca51d944f3119e822e55aa1d87bd`  
		Last Modified: Mon, 05 May 2025 16:35:54 GMT  
		Size: 62.7 MB (62712515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5bb632ea7418833d8a765520cc8284d9919cf4f96a5482547b1c586a7d981`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:bdd62e750816592d7e0a00d5e6a86c3c2df4dff29fcecb4013f0935fc88a64cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae9e5cf7289b8dc01878752334d248a1402b547c58188fe8f2adc047d361270`

```dockerfile
```

-	Layers:
	-	`sha256:94d220fb1fe008811f2adb0afde87dbf2db2a0f8a0baa290eebdd1a590af7a07`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 5.9 MB (5920970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6b95d4c4ff6f560bbba03031b4d60f366e3acb883547c1eaeae27712272e00`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7adb5f70fa01dc2a9cec093de1366dc96aef221430e19792330709158e1b4a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88527321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f661eca62c761f5a5969e07581b2b4af18c7934896c2d3b8ac331f4bd0d3d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:47 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:47 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:47 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ENV KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 14 Jun 2024 20:58:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
USER kong
# Fri, 14 Jun 2024 20:58:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b810ebf0ac95666201d639bcd8cfcc768af87f5a9acfa18ca6047b3436b9fa2`  
		Last Modified: Wed, 09 Apr 2025 08:23:09 GMT  
		Size: 61.2 MB (61171811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b8745359a7bd94737ba90b46b63346adb4dca9d9d990f9630f71de3b2b095`  
		Last Modified: Wed, 09 Apr 2025 08:23:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:aa4789e6ee8d7078136ffa491ce5ba7fa2deff755f47615db13481dd4d38d6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5326c66c1ecfa16d62d09e3b868c0801405355aab79de56ea0bd0b3f1e6f287`

```dockerfile
```

-	Layers:
	-	`sha256:4ed24048628ec657ee74b1ed5e362a18b78939b7224ed318118ad8d99ab13502`  
		Last Modified: Wed, 09 Apr 2025 08:23:08 GMT  
		Size: 5.9 MB (5899049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1aa1f989eb04d050d30d82e3dcd2f426767543a6a49871b6751b83d35bca53`  
		Last Modified: Wed, 09 Apr 2025 08:23:07 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:550c5b6c7e6711d41f2fd106f2e7e2dd0cbc08f218ae57d1cb1049e494fe696b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:03c0560c259bd43ab2cfafb65daa4566369e28657b4dee1eb17538f298fd57f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92246411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5a1d0ded28c8802ccd059c25ee7ec2748b151b018aaaa97068ad867bd20bd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:47 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:47 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:47 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ENV KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 14 Jun 2024 20:58:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
USER kong
# Fri, 14 Jun 2024 20:58:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d0b44ace46418c68cce30bd9a30fb1169ca51d944f3119e822e55aa1d87bd`  
		Last Modified: Mon, 05 May 2025 16:35:54 GMT  
		Size: 62.7 MB (62712515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5bb632ea7418833d8a765520cc8284d9919cf4f96a5482547b1c586a7d981`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:bdd62e750816592d7e0a00d5e6a86c3c2df4dff29fcecb4013f0935fc88a64cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae9e5cf7289b8dc01878752334d248a1402b547c58188fe8f2adc047d361270`

```dockerfile
```

-	Layers:
	-	`sha256:94d220fb1fe008811f2adb0afde87dbf2db2a0f8a0baa290eebdd1a590af7a07`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 5.9 MB (5920970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6b95d4c4ff6f560bbba03031b4d60f366e3acb883547c1eaeae27712272e00`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7adb5f70fa01dc2a9cec093de1366dc96aef221430e19792330709158e1b4a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88527321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f661eca62c761f5a5969e07581b2b4af18c7934896c2d3b8ac331f4bd0d3d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:47 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:47 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:47 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ENV KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 14 Jun 2024 20:58:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
USER kong
# Fri, 14 Jun 2024 20:58:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b810ebf0ac95666201d639bcd8cfcc768af87f5a9acfa18ca6047b3436b9fa2`  
		Last Modified: Wed, 09 Apr 2025 08:23:09 GMT  
		Size: 61.2 MB (61171811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b8745359a7bd94737ba90b46b63346adb4dca9d9d990f9630f71de3b2b095`  
		Last Modified: Wed, 09 Apr 2025 08:23:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:aa4789e6ee8d7078136ffa491ce5ba7fa2deff755f47615db13481dd4d38d6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5326c66c1ecfa16d62d09e3b868c0801405355aab79de56ea0bd0b3f1e6f287`

```dockerfile
```

-	Layers:
	-	`sha256:4ed24048628ec657ee74b1ed5e362a18b78939b7224ed318118ad8d99ab13502`  
		Last Modified: Wed, 09 Apr 2025 08:23:08 GMT  
		Size: 5.9 MB (5899049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1aa1f989eb04d050d30d82e3dcd2f426767543a6a49871b6751b83d35bca53`  
		Last Modified: Wed, 09 Apr 2025 08:23:07 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:550c5b6c7e6711d41f2fd106f2e7e2dd0cbc08f218ae57d1cb1049e494fe696b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:03c0560c259bd43ab2cfafb65daa4566369e28657b4dee1eb17538f298fd57f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92246411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5a1d0ded28c8802ccd059c25ee7ec2748b151b018aaaa97068ad867bd20bd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:47 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:47 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:47 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ENV KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 14 Jun 2024 20:58:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
USER kong
# Fri, 14 Jun 2024 20:58:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2d0b44ace46418c68cce30bd9a30fb1169ca51d944f3119e822e55aa1d87bd`  
		Last Modified: Mon, 05 May 2025 16:35:54 GMT  
		Size: 62.7 MB (62712515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5bb632ea7418833d8a765520cc8284d9919cf4f96a5482547b1c586a7d981`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:bdd62e750816592d7e0a00d5e6a86c3c2df4dff29fcecb4013f0935fc88a64cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae9e5cf7289b8dc01878752334d248a1402b547c58188fe8f2adc047d361270`

```dockerfile
```

-	Layers:
	-	`sha256:94d220fb1fe008811f2adb0afde87dbf2db2a0f8a0baa290eebdd1a590af7a07`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 5.9 MB (5920970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6b95d4c4ff6f560bbba03031b4d60f366e3acb883547c1eaeae27712272e00`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7adb5f70fa01dc2a9cec093de1366dc96aef221430e19792330709158e1b4a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88527321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f661eca62c761f5a5969e07581b2b4af18c7934896c2d3b8ac331f4bd0d3d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:47 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:47 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:47 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:47 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ENV KONG_VERSION=3.4.2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 14 Jun 2024 20:58:47 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 14 Jun 2024 20:58:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:47 GMT
USER kong
# Fri, 14 Jun 2024 20:58:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b810ebf0ac95666201d639bcd8cfcc768af87f5a9acfa18ca6047b3436b9fa2`  
		Last Modified: Wed, 09 Apr 2025 08:23:09 GMT  
		Size: 61.2 MB (61171811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b8745359a7bd94737ba90b46b63346adb4dca9d9d990f9630f71de3b2b095`  
		Last Modified: Wed, 09 Apr 2025 08:23:07 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:aa4789e6ee8d7078136ffa491ce5ba7fa2deff755f47615db13481dd4d38d6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5326c66c1ecfa16d62d09e3b868c0801405355aab79de56ea0bd0b3f1e6f287`

```dockerfile
```

-	Layers:
	-	`sha256:4ed24048628ec657ee74b1ed5e362a18b78939b7224ed318118ad8d99ab13502`  
		Last Modified: Wed, 09 Apr 2025 08:23:08 GMT  
		Size: 5.9 MB (5899049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1aa1f989eb04d050d30d82e3dcd2f426767543a6a49871b6751b83d35bca53`  
		Last Modified: Wed, 09 Apr 2025 08:23:07 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6`

```console
$ docker pull kong@sha256:63ef844bc592b50740c7b08ee244abb18031ff733190dd4ab800624704fb3985
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6` - linux; amd64

```console
$ docker pull kong@sha256:014603faf29581a0bf560eaef560563e7053436578997fad04f64d79742f41de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97235331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da12367c0b1308fbe0e01be26e0c81350d7216dca543a4b404963f9538328ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ece0567bb19ac52daaa5ca12b2a163a8df02a702baba36bd2f64de3ec8f226`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d300642c086b279dd557c04314a984724091be7926cb1fc6c1aacc256dd592e`  
		Last Modified: Mon, 05 May 2025 16:35:56 GMT  
		Size: 67.7 MB (67701432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d89f1a9c469a18ee9860e8e33779f216e4714152922d9325049905dee678e`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:df49f6f2ba51340cb7031e2ac2077e3fecc96b070530006ecb3e3d731d007e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ba53d859c1e30e4e5c538950d77fb33e5409bf49eff01a42336413f2ae676f`

```dockerfile
```

-	Layers:
	-	`sha256:067a88175c0b72e05093997a1e02c28dce0ca9a19a3e09d8af8d33fea5fcb881`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 5.0 MB (4952059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da60bc42f174169345188c979c80a2a6cc9a72d6dda6efb509dc4b1e4090a1a`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:84cd5335095b60bb8fda3f2a2ffcc2a0e2f78b9e200fb149acc7b05271b54109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94590405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e46d80312c8d16fafcb7da3781631c178d3738dedd7b44af48fab6448c98ca5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61320807ca769c606ad907e9b0abe2b36162a9f69e2a82885f4c386450dc04d7`  
		Last Modified: Wed, 09 Apr 2025 08:22:28 GMT  
		Size: 67.2 MB (67234893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239422441c82783436cdc8613fe877d81875005a4d1bf5aa6e88f11a16531024`  
		Last Modified: Wed, 09 Apr 2025 08:22:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:0504d4870ed8cecbfda042cf69bd7a51e96fe7117330a95ae4cb46a5c9269a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fc862dbd68c4929b75ec0177dfca4b6adab6979f39007d63f3f32f5ae95932`

```dockerfile
```

-	Layers:
	-	`sha256:dee46a8d0a9bb722fd96556caf4e6bb8e821381569c82c54db3411aec8d8ec0a`  
		Last Modified: Wed, 09 Apr 2025 08:22:26 GMT  
		Size: 5.0 MB (4958385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d20898c7daf3b801f50aacec646ce0b995db2505ad324de5d600dc7a6eec0b6`  
		Last Modified: Wed, 09 Apr 2025 08:22:25 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:63ef844bc592b50740c7b08ee244abb18031ff733190dd4ab800624704fb3985
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:014603faf29581a0bf560eaef560563e7053436578997fad04f64d79742f41de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97235331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da12367c0b1308fbe0e01be26e0c81350d7216dca543a4b404963f9538328ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ece0567bb19ac52daaa5ca12b2a163a8df02a702baba36bd2f64de3ec8f226`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d300642c086b279dd557c04314a984724091be7926cb1fc6c1aacc256dd592e`  
		Last Modified: Mon, 05 May 2025 16:35:56 GMT  
		Size: 67.7 MB (67701432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d89f1a9c469a18ee9860e8e33779f216e4714152922d9325049905dee678e`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:df49f6f2ba51340cb7031e2ac2077e3fecc96b070530006ecb3e3d731d007e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ba53d859c1e30e4e5c538950d77fb33e5409bf49eff01a42336413f2ae676f`

```dockerfile
```

-	Layers:
	-	`sha256:067a88175c0b72e05093997a1e02c28dce0ca9a19a3e09d8af8d33fea5fcb881`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 5.0 MB (4952059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da60bc42f174169345188c979c80a2a6cc9a72d6dda6efb509dc4b1e4090a1a`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:84cd5335095b60bb8fda3f2a2ffcc2a0e2f78b9e200fb149acc7b05271b54109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94590405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e46d80312c8d16fafcb7da3781631c178d3738dedd7b44af48fab6448c98ca5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61320807ca769c606ad907e9b0abe2b36162a9f69e2a82885f4c386450dc04d7`  
		Last Modified: Wed, 09 Apr 2025 08:22:28 GMT  
		Size: 67.2 MB (67234893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239422441c82783436cdc8613fe877d81875005a4d1bf5aa6e88f11a16531024`  
		Last Modified: Wed, 09 Apr 2025 08:22:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:0504d4870ed8cecbfda042cf69bd7a51e96fe7117330a95ae4cb46a5c9269a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fc862dbd68c4929b75ec0177dfca4b6adab6979f39007d63f3f32f5ae95932`

```dockerfile
```

-	Layers:
	-	`sha256:dee46a8d0a9bb722fd96556caf4e6bb8e821381569c82c54db3411aec8d8ec0a`  
		Last Modified: Wed, 09 Apr 2025 08:22:26 GMT  
		Size: 5.0 MB (4958385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d20898c7daf3b801f50aacec646ce0b995db2505ad324de5d600dc7a6eec0b6`  
		Last Modified: Wed, 09 Apr 2025 08:22:25 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6.1`

```console
$ docker pull kong@sha256:63ef844bc592b50740c7b08ee244abb18031ff733190dd4ab800624704fb3985
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1` - linux; amd64

```console
$ docker pull kong@sha256:014603faf29581a0bf560eaef560563e7053436578997fad04f64d79742f41de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97235331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da12367c0b1308fbe0e01be26e0c81350d7216dca543a4b404963f9538328ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ece0567bb19ac52daaa5ca12b2a163a8df02a702baba36bd2f64de3ec8f226`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d300642c086b279dd557c04314a984724091be7926cb1fc6c1aacc256dd592e`  
		Last Modified: Mon, 05 May 2025 16:35:56 GMT  
		Size: 67.7 MB (67701432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d89f1a9c469a18ee9860e8e33779f216e4714152922d9325049905dee678e`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:df49f6f2ba51340cb7031e2ac2077e3fecc96b070530006ecb3e3d731d007e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ba53d859c1e30e4e5c538950d77fb33e5409bf49eff01a42336413f2ae676f`

```dockerfile
```

-	Layers:
	-	`sha256:067a88175c0b72e05093997a1e02c28dce0ca9a19a3e09d8af8d33fea5fcb881`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 5.0 MB (4952059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da60bc42f174169345188c979c80a2a6cc9a72d6dda6efb509dc4b1e4090a1a`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:84cd5335095b60bb8fda3f2a2ffcc2a0e2f78b9e200fb149acc7b05271b54109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94590405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e46d80312c8d16fafcb7da3781631c178d3738dedd7b44af48fab6448c98ca5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61320807ca769c606ad907e9b0abe2b36162a9f69e2a82885f4c386450dc04d7`  
		Last Modified: Wed, 09 Apr 2025 08:22:28 GMT  
		Size: 67.2 MB (67234893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239422441c82783436cdc8613fe877d81875005a4d1bf5aa6e88f11a16531024`  
		Last Modified: Wed, 09 Apr 2025 08:22:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:0504d4870ed8cecbfda042cf69bd7a51e96fe7117330a95ae4cb46a5c9269a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fc862dbd68c4929b75ec0177dfca4b6adab6979f39007d63f3f32f5ae95932`

```dockerfile
```

-	Layers:
	-	`sha256:dee46a8d0a9bb722fd96556caf4e6bb8e821381569c82c54db3411aec8d8ec0a`  
		Last Modified: Wed, 09 Apr 2025 08:22:26 GMT  
		Size: 5.0 MB (4958385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d20898c7daf3b801f50aacec646ce0b995db2505ad324de5d600dc7a6eec0b6`  
		Last Modified: Wed, 09 Apr 2025 08:22:25 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:63ef844bc592b50740c7b08ee244abb18031ff733190dd4ab800624704fb3985
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:014603faf29581a0bf560eaef560563e7053436578997fad04f64d79742f41de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97235331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da12367c0b1308fbe0e01be26e0c81350d7216dca543a4b404963f9538328ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ece0567bb19ac52daaa5ca12b2a163a8df02a702baba36bd2f64de3ec8f226`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d300642c086b279dd557c04314a984724091be7926cb1fc6c1aacc256dd592e`  
		Last Modified: Mon, 05 May 2025 16:35:56 GMT  
		Size: 67.7 MB (67701432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d89f1a9c469a18ee9860e8e33779f216e4714152922d9325049905dee678e`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:df49f6f2ba51340cb7031e2ac2077e3fecc96b070530006ecb3e3d731d007e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ba53d859c1e30e4e5c538950d77fb33e5409bf49eff01a42336413f2ae676f`

```dockerfile
```

-	Layers:
	-	`sha256:067a88175c0b72e05093997a1e02c28dce0ca9a19a3e09d8af8d33fea5fcb881`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 5.0 MB (4952059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0da60bc42f174169345188c979c80a2a6cc9a72d6dda6efb509dc4b1e4090a1a`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:84cd5335095b60bb8fda3f2a2ffcc2a0e2f78b9e200fb149acc7b05271b54109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94590405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e46d80312c8d16fafcb7da3781631c178d3738dedd7b44af48fab6448c98ca5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61320807ca769c606ad907e9b0abe2b36162a9f69e2a82885f4c386450dc04d7`  
		Last Modified: Wed, 09 Apr 2025 08:22:28 GMT  
		Size: 67.2 MB (67234893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239422441c82783436cdc8613fe877d81875005a4d1bf5aa6e88f11a16531024`  
		Last Modified: Wed, 09 Apr 2025 08:22:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:0504d4870ed8cecbfda042cf69bd7a51e96fe7117330a95ae4cb46a5c9269a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fc862dbd68c4929b75ec0177dfca4b6adab6979f39007d63f3f32f5ae95932`

```dockerfile
```

-	Layers:
	-	`sha256:dee46a8d0a9bb722fd96556caf4e6bb8e821381569c82c54db3411aec8d8ec0a`  
		Last Modified: Wed, 09 Apr 2025 08:22:26 GMT  
		Size: 5.0 MB (4958385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d20898c7daf3b801f50aacec646ce0b995db2505ad324de5d600dc7a6eec0b6`  
		Last Modified: Wed, 09 Apr 2025 08:22:25 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7`

```console
$ docker pull kong@sha256:72de6e1d36d3e3ac8662b0b1d2ae32ed6f6ad8bdfacd86d48027dcb9d9304524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7` - linux; amd64

```console
$ docker pull kong@sha256:88ed483015a07e23014999b30560839d0c2fb971647af2c5417cf855483457d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97276083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70bf6eb2711468224fb7719a213dbe1bb7b0d6ad3550bcecf76e58f354f24b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 21 Jun 2024 16:03:55 GMT
ARG ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ENV ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ARG EE_PORTS
# Fri, 21 Jun 2024 16:03:55 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ENV KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
# Fri, 21 Jun 2024 16:03:55 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.1 KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
USER kong
# Fri, 21 Jun 2024 16:03:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 16:03:55 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 21 Jun 2024 16:03:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 16:03:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2655616898df00f543a58b637ff9e6315f29f26f0f70198714a90776b5b5892f`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27bced3fdfaca2c141abff1f47a7e27c90c5ef43d3309abee4525b5fcc15e64`  
		Last Modified: Mon, 05 May 2025 16:35:47 GMT  
		Size: 67.7 MB (67742186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c504d4da77ba3a84964fd09d644aaee3412fdee6b2825c10e08a9452f1c2f`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:82bd75c8a537330133bc488ccaf7fe379d7d167b667a4d0aabd80f2411a39608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd04dc8d2ba8ca5215d891707b42ddeb4f1dced17051d1c4a726fba2e5c7173`

```dockerfile
```

-	Layers:
	-	`sha256:4aa7aae7bfe7f125223e70b76a58c08b01f841f4b48a7d0b3276e57be6f169fe`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 5.0 MB (5030507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd6149202fa6b24d4625941c5f91eb72d957bb9cac2aac0fd512d1e7401b4c8`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:669b3f27849c2e7267b87e8a69f3b61bd84f60b33813dce59b793bfdbf53883a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95016335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873bcd75d878044117b71b4cd846b3c80edb2203872217375342416561d8d818`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 21 Jun 2024 16:03:55 GMT
ARG ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ENV ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ARG EE_PORTS
# Fri, 21 Jun 2024 16:03:55 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ENV KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
# Fri, 21 Jun 2024 16:03:55 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.1 KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
USER kong
# Fri, 21 Jun 2024 16:03:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 16:03:55 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 21 Jun 2024 16:03:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 16:03:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01634c9fd3192e8a7da95731163912dc9e5e5dcae03379ed926f5a99c830a301`  
		Last Modified: Wed, 09 Apr 2025 08:21:47 GMT  
		Size: 67.7 MB (67660822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c151430c30ce9ed13780f5447abb627c018089207d3167742f4122a384a2a8`  
		Last Modified: Wed, 09 Apr 2025 08:21:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:13c00250e06f93c43ca9efdae03fd9236d390d6bbf9e1580a78f0928a8f791c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5052326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e87a3d3b70ed3392056cca190016785e3869fcb724f849ee4913b3dbeb18dc`

```dockerfile
```

-	Layers:
	-	`sha256:263694bc3ea2c6d4a402de964ebdb1c759eeccd248db0ab0f237a0e4d9619f88`  
		Last Modified: Wed, 09 Apr 2025 08:21:45 GMT  
		Size: 5.0 MB (5036833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7474320b4e83e990b4998fae43b94ff63cfe303c7075ce68787f472327b547d1`  
		Last Modified: Wed, 09 Apr 2025 08:21:44 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7-ubuntu`

```console
$ docker pull kong@sha256:72de6e1d36d3e3ac8662b0b1d2ae32ed6f6ad8bdfacd86d48027dcb9d9304524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:88ed483015a07e23014999b30560839d0c2fb971647af2c5417cf855483457d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97276083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70bf6eb2711468224fb7719a213dbe1bb7b0d6ad3550bcecf76e58f354f24b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 21 Jun 2024 16:03:55 GMT
ARG ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ENV ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ARG EE_PORTS
# Fri, 21 Jun 2024 16:03:55 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ENV KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
# Fri, 21 Jun 2024 16:03:55 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.1 KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
USER kong
# Fri, 21 Jun 2024 16:03:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 16:03:55 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 21 Jun 2024 16:03:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 16:03:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2655616898df00f543a58b637ff9e6315f29f26f0f70198714a90776b5b5892f`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27bced3fdfaca2c141abff1f47a7e27c90c5ef43d3309abee4525b5fcc15e64`  
		Last Modified: Mon, 05 May 2025 16:35:47 GMT  
		Size: 67.7 MB (67742186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c504d4da77ba3a84964fd09d644aaee3412fdee6b2825c10e08a9452f1c2f`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:82bd75c8a537330133bc488ccaf7fe379d7d167b667a4d0aabd80f2411a39608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd04dc8d2ba8ca5215d891707b42ddeb4f1dced17051d1c4a726fba2e5c7173`

```dockerfile
```

-	Layers:
	-	`sha256:4aa7aae7bfe7f125223e70b76a58c08b01f841f4b48a7d0b3276e57be6f169fe`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 5.0 MB (5030507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd6149202fa6b24d4625941c5f91eb72d957bb9cac2aac0fd512d1e7401b4c8`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:669b3f27849c2e7267b87e8a69f3b61bd84f60b33813dce59b793bfdbf53883a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95016335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873bcd75d878044117b71b4cd846b3c80edb2203872217375342416561d8d818`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 21 Jun 2024 16:03:55 GMT
ARG ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ENV ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ARG EE_PORTS
# Fri, 21 Jun 2024 16:03:55 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ENV KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
# Fri, 21 Jun 2024 16:03:55 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.1 KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
USER kong
# Fri, 21 Jun 2024 16:03:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 16:03:55 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 21 Jun 2024 16:03:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 16:03:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01634c9fd3192e8a7da95731163912dc9e5e5dcae03379ed926f5a99c830a301`  
		Last Modified: Wed, 09 Apr 2025 08:21:47 GMT  
		Size: 67.7 MB (67660822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c151430c30ce9ed13780f5447abb627c018089207d3167742f4122a384a2a8`  
		Last Modified: Wed, 09 Apr 2025 08:21:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:13c00250e06f93c43ca9efdae03fd9236d390d6bbf9e1580a78f0928a8f791c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5052326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e87a3d3b70ed3392056cca190016785e3869fcb724f849ee4913b3dbeb18dc`

```dockerfile
```

-	Layers:
	-	`sha256:263694bc3ea2c6d4a402de964ebdb1c759eeccd248db0ab0f237a0e4d9619f88`  
		Last Modified: Wed, 09 Apr 2025 08:21:45 GMT  
		Size: 5.0 MB (5036833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7474320b4e83e990b4998fae43b94ff63cfe303c7075ce68787f472327b547d1`  
		Last Modified: Wed, 09 Apr 2025 08:21:44 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.1`

```console
$ docker pull kong@sha256:72de6e1d36d3e3ac8662b0b1d2ae32ed6f6ad8bdfacd86d48027dcb9d9304524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1` - linux; amd64

```console
$ docker pull kong@sha256:88ed483015a07e23014999b30560839d0c2fb971647af2c5417cf855483457d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97276083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70bf6eb2711468224fb7719a213dbe1bb7b0d6ad3550bcecf76e58f354f24b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 21 Jun 2024 16:03:55 GMT
ARG ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ENV ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ARG EE_PORTS
# Fri, 21 Jun 2024 16:03:55 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ENV KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
# Fri, 21 Jun 2024 16:03:55 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.1 KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
USER kong
# Fri, 21 Jun 2024 16:03:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 16:03:55 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 21 Jun 2024 16:03:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 16:03:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2655616898df00f543a58b637ff9e6315f29f26f0f70198714a90776b5b5892f`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27bced3fdfaca2c141abff1f47a7e27c90c5ef43d3309abee4525b5fcc15e64`  
		Last Modified: Mon, 05 May 2025 16:35:47 GMT  
		Size: 67.7 MB (67742186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c504d4da77ba3a84964fd09d644aaee3412fdee6b2825c10e08a9452f1c2f`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:82bd75c8a537330133bc488ccaf7fe379d7d167b667a4d0aabd80f2411a39608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd04dc8d2ba8ca5215d891707b42ddeb4f1dced17051d1c4a726fba2e5c7173`

```dockerfile
```

-	Layers:
	-	`sha256:4aa7aae7bfe7f125223e70b76a58c08b01f841f4b48a7d0b3276e57be6f169fe`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 5.0 MB (5030507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd6149202fa6b24d4625941c5f91eb72d957bb9cac2aac0fd512d1e7401b4c8`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:669b3f27849c2e7267b87e8a69f3b61bd84f60b33813dce59b793bfdbf53883a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95016335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873bcd75d878044117b71b4cd846b3c80edb2203872217375342416561d8d818`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 21 Jun 2024 16:03:55 GMT
ARG ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ENV ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ARG EE_PORTS
# Fri, 21 Jun 2024 16:03:55 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ENV KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
# Fri, 21 Jun 2024 16:03:55 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.1 KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
USER kong
# Fri, 21 Jun 2024 16:03:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 16:03:55 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 21 Jun 2024 16:03:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 16:03:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01634c9fd3192e8a7da95731163912dc9e5e5dcae03379ed926f5a99c830a301`  
		Last Modified: Wed, 09 Apr 2025 08:21:47 GMT  
		Size: 67.7 MB (67660822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c151430c30ce9ed13780f5447abb627c018089207d3167742f4122a384a2a8`  
		Last Modified: Wed, 09 Apr 2025 08:21:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:13c00250e06f93c43ca9efdae03fd9236d390d6bbf9e1580a78f0928a8f791c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5052326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e87a3d3b70ed3392056cca190016785e3869fcb724f849ee4913b3dbeb18dc`

```dockerfile
```

-	Layers:
	-	`sha256:263694bc3ea2c6d4a402de964ebdb1c759eeccd248db0ab0f237a0e4d9619f88`  
		Last Modified: Wed, 09 Apr 2025 08:21:45 GMT  
		Size: 5.0 MB (5036833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7474320b4e83e990b4998fae43b94ff63cfe303c7075ce68787f472327b547d1`  
		Last Modified: Wed, 09 Apr 2025 08:21:44 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.1-ubuntu`

```console
$ docker pull kong@sha256:72de6e1d36d3e3ac8662b0b1d2ae32ed6f6ad8bdfacd86d48027dcb9d9304524
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:88ed483015a07e23014999b30560839d0c2fb971647af2c5417cf855483457d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97276083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70bf6eb2711468224fb7719a213dbe1bb7b0d6ad3550bcecf76e58f354f24b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 21 Jun 2024 16:03:55 GMT
ARG ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ENV ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ARG EE_PORTS
# Fri, 21 Jun 2024 16:03:55 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ENV KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
# Fri, 21 Jun 2024 16:03:55 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.1 KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
USER kong
# Fri, 21 Jun 2024 16:03:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 16:03:55 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 21 Jun 2024 16:03:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 16:03:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2655616898df00f543a58b637ff9e6315f29f26f0f70198714a90776b5b5892f`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27bced3fdfaca2c141abff1f47a7e27c90c5ef43d3309abee4525b5fcc15e64`  
		Last Modified: Mon, 05 May 2025 16:35:47 GMT  
		Size: 67.7 MB (67742186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64c504d4da77ba3a84964fd09d644aaee3412fdee6b2825c10e08a9452f1c2f`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:82bd75c8a537330133bc488ccaf7fe379d7d167b667a4d0aabd80f2411a39608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd04dc8d2ba8ca5215d891707b42ddeb4f1dced17051d1c4a726fba2e5c7173`

```dockerfile
```

-	Layers:
	-	`sha256:4aa7aae7bfe7f125223e70b76a58c08b01f841f4b48a7d0b3276e57be6f169fe`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 5.0 MB (5030507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd6149202fa6b24d4625941c5f91eb72d957bb9cac2aac0fd512d1e7401b4c8`  
		Last Modified: Mon, 05 May 2025 16:35:46 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:669b3f27849c2e7267b87e8a69f3b61bd84f60b33813dce59b793bfdbf53883a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95016335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873bcd75d878044117b71b4cd846b3c80edb2203872217375342416561d8d818`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 21 Jun 2024 16:03:55 GMT
ARG ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ENV ASSET=ce
# Fri, 21 Jun 2024 16:03:55 GMT
ARG EE_PORTS
# Fri, 21 Jun 2024 16:03:55 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ENV KONG_VERSION=3.7.1
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec
# Fri, 21 Jun 2024 16:03:55 GMT
ARG KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
# Fri, 21 Jun 2024 16:03:55 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.7.1 KONG_AMD64_SHA=58e380961fc90c6b4dfd62f4ee596ab053afe5ae72a93445c4356f496f2dc9ec KONG_ARM64_SHA=602a68cf3a09bbea26106d4bd4041c242d7913e40582d18cac0f6958aad78f72
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 21 Jun 2024 16:03:55 GMT
USER kong
# Fri, 21 Jun 2024 16:03:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 16:03:55 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 21 Jun 2024 16:03:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 16:03:55 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 21 Jun 2024 16:03:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01634c9fd3192e8a7da95731163912dc9e5e5dcae03379ed926f5a99c830a301`  
		Last Modified: Wed, 09 Apr 2025 08:21:47 GMT  
		Size: 67.7 MB (67660822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c151430c30ce9ed13780f5447abb627c018089207d3167742f4122a384a2a8`  
		Last Modified: Wed, 09 Apr 2025 08:21:44 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:13c00250e06f93c43ca9efdae03fd9236d390d6bbf9e1580a78f0928a8f791c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5052326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e87a3d3b70ed3392056cca190016785e3869fcb724f849ee4913b3dbeb18dc`

```dockerfile
```

-	Layers:
	-	`sha256:263694bc3ea2c6d4a402de964ebdb1c759eeccd248db0ab0f237a0e4d9619f88`  
		Last Modified: Wed, 09 Apr 2025 08:21:45 GMT  
		Size: 5.0 MB (5036833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7474320b4e83e990b4998fae43b94ff63cfe303c7075ce68787f472327b547d1`  
		Last Modified: Wed, 09 Apr 2025 08:21:44 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:d7c2ce3a315dc2cb8c2f8fbc77bcdb114e7eed734e5e2fbd3f28a6e5d0560571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:9467b3977e0e9dc17df19a4680cd42595f555c17eb62b9ace0962526d4bef8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d503bfc17d654969b0a73037cd5689b0e9dc8e288caec382ca3196d9942c3b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa262f908b62de8e4bc68d19bb86861048f0dc293b35cf5ee463afa82b2dc8c`  
		Last Modified: Mon, 05 May 2025 16:36:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3556a2141fd7ddd6f1ca613f45c9910967df0a0dce156c64a8bf8aca613308ed`  
		Last Modified: Mon, 05 May 2025 16:36:10 GMT  
		Size: 88.0 MB (88001378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d89f1a9c469a18ee9860e8e33779f216e4714152922d9325049905dee678e`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:c49333e5b3764451c9a045b1aea615006667e0af6effe78ddd4300645a795ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74694eee6af01b81437105d9f60caba1c61216990d7d3831459d2d14dad53daf`

```dockerfile
```

-	Layers:
	-	`sha256:95c78b1deef0dc54f7356abbc7a705e53694f2657d9ab55941808d46874d9dae`  
		Last Modified: Mon, 05 May 2025 16:36:08 GMT  
		Size: 5.2 MB (5224350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d3b843c6e5b09ff2a1c30733c60b9194033de23162251e8dc8010d2c126d8`  
		Last Modified: Mon, 05 May 2025 16:36:07 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:80c27682256f3e4fcfea8261f6c3f81d7bffb009e25d4712cc0cc4371c548ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114639082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0d34bf852cb210d8974ff9c7a0c57b49f116e93fb4a9d63ae8ee70158a3d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bcf3c21481e53716fa9a3662000d527ea14a33bbe4340524a5d6cb9f6c8732`  
		Last Modified: Wed, 09 Apr 2025 08:21:05 GMT  
		Size: 87.3 MB (87283569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8625c0832bbea8472720f18c0197fb1011b03d836210c1a2cb4f7e37339dc`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:e20de0b31af9d076509247d7c8bbad67e00c4e8d87d6f4919340522f872001d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208c216c335e5718536792fe9fa8ad6e2e5c0a119961f1bde3a4c43aed94746d`

```dockerfile
```

-	Layers:
	-	`sha256:ad7e94740d3f36834d5e62ccd8a6e4e992d145988e9c0dc7c700ec5e26701dd4`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 5.2 MB (5230676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f72a519d54e71cffbe64db28f74d9846c13414da85cd8a3393cb657b20ddf40`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:d7c2ce3a315dc2cb8c2f8fbc77bcdb114e7eed734e5e2fbd3f28a6e5d0560571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9467b3977e0e9dc17df19a4680cd42595f555c17eb62b9ace0962526d4bef8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d503bfc17d654969b0a73037cd5689b0e9dc8e288caec382ca3196d9942c3b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa262f908b62de8e4bc68d19bb86861048f0dc293b35cf5ee463afa82b2dc8c`  
		Last Modified: Mon, 05 May 2025 16:36:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3556a2141fd7ddd6f1ca613f45c9910967df0a0dce156c64a8bf8aca613308ed`  
		Last Modified: Mon, 05 May 2025 16:36:10 GMT  
		Size: 88.0 MB (88001378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d89f1a9c469a18ee9860e8e33779f216e4714152922d9325049905dee678e`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c49333e5b3764451c9a045b1aea615006667e0af6effe78ddd4300645a795ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74694eee6af01b81437105d9f60caba1c61216990d7d3831459d2d14dad53daf`

```dockerfile
```

-	Layers:
	-	`sha256:95c78b1deef0dc54f7356abbc7a705e53694f2657d9ab55941808d46874d9dae`  
		Last Modified: Mon, 05 May 2025 16:36:08 GMT  
		Size: 5.2 MB (5224350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d3b843c6e5b09ff2a1c30733c60b9194033de23162251e8dc8010d2c126d8`  
		Last Modified: Mon, 05 May 2025 16:36:07 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:80c27682256f3e4fcfea8261f6c3f81d7bffb009e25d4712cc0cc4371c548ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114639082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0d34bf852cb210d8974ff9c7a0c57b49f116e93fb4a9d63ae8ee70158a3d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bcf3c21481e53716fa9a3662000d527ea14a33bbe4340524a5d6cb9f6c8732`  
		Last Modified: Wed, 09 Apr 2025 08:21:05 GMT  
		Size: 87.3 MB (87283569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8625c0832bbea8472720f18c0197fb1011b03d836210c1a2cb4f7e37339dc`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e20de0b31af9d076509247d7c8bbad67e00c4e8d87d6f4919340522f872001d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208c216c335e5718536792fe9fa8ad6e2e5c0a119961f1bde3a4c43aed94746d`

```dockerfile
```

-	Layers:
	-	`sha256:ad7e94740d3f36834d5e62ccd8a6e4e992d145988e9c0dc7c700ec5e26701dd4`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 5.2 MB (5230676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f72a519d54e71cffbe64db28f74d9846c13414da85cd8a3393cb657b20ddf40`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:d7c2ce3a315dc2cb8c2f8fbc77bcdb114e7eed734e5e2fbd3f28a6e5d0560571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:9467b3977e0e9dc17df19a4680cd42595f555c17eb62b9ace0962526d4bef8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d503bfc17d654969b0a73037cd5689b0e9dc8e288caec382ca3196d9942c3b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa262f908b62de8e4bc68d19bb86861048f0dc293b35cf5ee463afa82b2dc8c`  
		Last Modified: Mon, 05 May 2025 16:36:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3556a2141fd7ddd6f1ca613f45c9910967df0a0dce156c64a8bf8aca613308ed`  
		Last Modified: Mon, 05 May 2025 16:36:10 GMT  
		Size: 88.0 MB (88001378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d89f1a9c469a18ee9860e8e33779f216e4714152922d9325049905dee678e`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:c49333e5b3764451c9a045b1aea615006667e0af6effe78ddd4300645a795ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74694eee6af01b81437105d9f60caba1c61216990d7d3831459d2d14dad53daf`

```dockerfile
```

-	Layers:
	-	`sha256:95c78b1deef0dc54f7356abbc7a705e53694f2657d9ab55941808d46874d9dae`  
		Last Modified: Mon, 05 May 2025 16:36:08 GMT  
		Size: 5.2 MB (5224350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d3b843c6e5b09ff2a1c30733c60b9194033de23162251e8dc8010d2c126d8`  
		Last Modified: Mon, 05 May 2025 16:36:07 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:80c27682256f3e4fcfea8261f6c3f81d7bffb009e25d4712cc0cc4371c548ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114639082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0d34bf852cb210d8974ff9c7a0c57b49f116e93fb4a9d63ae8ee70158a3d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bcf3c21481e53716fa9a3662000d527ea14a33bbe4340524a5d6cb9f6c8732`  
		Last Modified: Wed, 09 Apr 2025 08:21:05 GMT  
		Size: 87.3 MB (87283569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8625c0832bbea8472720f18c0197fb1011b03d836210c1a2cb4f7e37339dc`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:e20de0b31af9d076509247d7c8bbad67e00c4e8d87d6f4919340522f872001d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208c216c335e5718536792fe9fa8ad6e2e5c0a119961f1bde3a4c43aed94746d`

```dockerfile
```

-	Layers:
	-	`sha256:ad7e94740d3f36834d5e62ccd8a6e4e992d145988e9c0dc7c700ec5e26701dd4`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 5.2 MB (5230676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f72a519d54e71cffbe64db28f74d9846c13414da85cd8a3393cb657b20ddf40`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:d7c2ce3a315dc2cb8c2f8fbc77bcdb114e7eed734e5e2fbd3f28a6e5d0560571
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9467b3977e0e9dc17df19a4680cd42595f555c17eb62b9ace0962526d4bef8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d503bfc17d654969b0a73037cd5689b0e9dc8e288caec382ca3196d9942c3b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa262f908b62de8e4bc68d19bb86861048f0dc293b35cf5ee463afa82b2dc8c`  
		Last Modified: Mon, 05 May 2025 16:36:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3556a2141fd7ddd6f1ca613f45c9910967df0a0dce156c64a8bf8aca613308ed`  
		Last Modified: Mon, 05 May 2025 16:36:10 GMT  
		Size: 88.0 MB (88001378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41d89f1a9c469a18ee9860e8e33779f216e4714152922d9325049905dee678e`  
		Last Modified: Mon, 05 May 2025 16:35:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c49333e5b3764451c9a045b1aea615006667e0af6effe78ddd4300645a795ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74694eee6af01b81437105d9f60caba1c61216990d7d3831459d2d14dad53daf`

```dockerfile
```

-	Layers:
	-	`sha256:95c78b1deef0dc54f7356abbc7a705e53694f2657d9ab55941808d46874d9dae`  
		Last Modified: Mon, 05 May 2025 16:36:08 GMT  
		Size: 5.2 MB (5224350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d3b843c6e5b09ff2a1c30733c60b9194033de23162251e8dc8010d2c126d8`  
		Last Modified: Mon, 05 May 2025 16:36:07 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:80c27682256f3e4fcfea8261f6c3f81d7bffb009e25d4712cc0cc4371c548ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114639082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0d34bf852cb210d8974ff9c7a0c57b49f116e93fb4a9d63ae8ee70158a3d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9987c8f32e670315b7a60bf5a2672a6f1435cf67a25e25cc8f06359cfa449bc3`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bcf3c21481e53716fa9a3662000d527ea14a33bbe4340524a5d6cb9f6c8732`  
		Last Modified: Wed, 09 Apr 2025 08:21:05 GMT  
		Size: 87.3 MB (87283569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c8625c0832bbea8472720f18c0197fb1011b03d836210c1a2cb4f7e37339dc`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e20de0b31af9d076509247d7c8bbad67e00c4e8d87d6f4919340522f872001d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208c216c335e5718536792fe9fa8ad6e2e5c0a119961f1bde3a4c43aed94746d`

```dockerfile
```

-	Layers:
	-	`sha256:ad7e94740d3f36834d5e62ccd8a6e4e992d145988e9c0dc7c700ec5e26701dd4`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 5.2 MB (5230676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f72a519d54e71cffbe64db28f74d9846c13414da85cd8a3393cb657b20ddf40`  
		Last Modified: Wed, 09 Apr 2025 08:21:03 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:81cb84a14ece9369a93b62ab055dec078efd6744c393d8c78ad49a681f26ff79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:64b511bd7904fb453b67a7546412f9fa90023fb0bc894b175c50c0738cad7bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120292359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29dee4714e746c926a4b043ffedfa7e53b2309d09049452a31e7d670e8ada6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33641554fa01162df8a1f58e295f7cd7500ea15d3384f0039376ca23ee59283b`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 90.6 MB (90573542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75156dcff079865c8eb035aefc6fee2747da1c5eebf4b4f27f159fb6c94ffec3`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:c640d31d180ef175d0ab0cbd49a316eae008b20b11a165557a47d84923da3307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71885738b53967ede0279526d34f0873f2b1b92fd10988fac560d143bc8efb3a`

```dockerfile
```

-	Layers:
	-	`sha256:f086e76b248ffde645e0977b09c477ba1b048dea0b3f840700a6ce629c55f832`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 5.3 MB (5289699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e7fb4268f68b7e8a15927e77eeb71bec82746caf10c48199b44fab0c9e9862`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fadcac914015602c659e84eaeb5a613bce26d8802e552e430d0e8081d611e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118733966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376ab1d5d1f06c7709e2de91c67eb7f9e679e5c1531839b901cff68e0430b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fb2e4918d8e46e87cafdab9800e8200b013313dea30d1e371b6b5a638c93f8`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e66824736c60174bbd80ffb5c8cc7936ce492d205165f933ad218f673d635`  
		Last Modified: Wed, 09 Apr 2025 08:20:06 GMT  
		Size: 89.9 MB (89885725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7d4eff5302e5c62b203443077f3c29e98b8a8d701b949f4368a40829b7054`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:d1137d667449bf4b6e3aa084601bd079d3f14ecd5ef371789763224d794a068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70af9163360fb26ba3244de5487a4c612789c16b7384a10ba213d688809113fc`

```dockerfile
```

-	Layers:
	-	`sha256:0ba117d7e761e4a87609c63563f83f6c34e132a843aa5b23cc5b5e71f4c90fa8`  
		Last Modified: Wed, 09 Apr 2025 08:20:04 GMT  
		Size: 5.3 MB (5296858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f99a09021aa6d5a1d4f1409373eb74121649f1bcc1ae8d0b428bb425f0c575`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:81cb84a14ece9369a93b62ab055dec078efd6744c393d8c78ad49a681f26ff79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:64b511bd7904fb453b67a7546412f9fa90023fb0bc894b175c50c0738cad7bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120292359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29dee4714e746c926a4b043ffedfa7e53b2309d09049452a31e7d670e8ada6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33641554fa01162df8a1f58e295f7cd7500ea15d3384f0039376ca23ee59283b`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 90.6 MB (90573542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75156dcff079865c8eb035aefc6fee2747da1c5eebf4b4f27f159fb6c94ffec3`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c640d31d180ef175d0ab0cbd49a316eae008b20b11a165557a47d84923da3307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71885738b53967ede0279526d34f0873f2b1b92fd10988fac560d143bc8efb3a`

```dockerfile
```

-	Layers:
	-	`sha256:f086e76b248ffde645e0977b09c477ba1b048dea0b3f840700a6ce629c55f832`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 5.3 MB (5289699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e7fb4268f68b7e8a15927e77eeb71bec82746caf10c48199b44fab0c9e9862`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fadcac914015602c659e84eaeb5a613bce26d8802e552e430d0e8081d611e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118733966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376ab1d5d1f06c7709e2de91c67eb7f9e679e5c1531839b901cff68e0430b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fb2e4918d8e46e87cafdab9800e8200b013313dea30d1e371b6b5a638c93f8`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e66824736c60174bbd80ffb5c8cc7936ce492d205165f933ad218f673d635`  
		Last Modified: Wed, 09 Apr 2025 08:20:06 GMT  
		Size: 89.9 MB (89885725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7d4eff5302e5c62b203443077f3c29e98b8a8d701b949f4368a40829b7054`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d1137d667449bf4b6e3aa084601bd079d3f14ecd5ef371789763224d794a068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70af9163360fb26ba3244de5487a4c612789c16b7384a10ba213d688809113fc`

```dockerfile
```

-	Layers:
	-	`sha256:0ba117d7e761e4a87609c63563f83f6c34e132a843aa5b23cc5b5e71f4c90fa8`  
		Last Modified: Wed, 09 Apr 2025 08:20:04 GMT  
		Size: 5.3 MB (5296858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f99a09021aa6d5a1d4f1409373eb74121649f1bcc1ae8d0b428bb425f0c575`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.0`

```console
$ docker pull kong@sha256:81cb84a14ece9369a93b62ab055dec078efd6744c393d8c78ad49a681f26ff79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.0` - linux; amd64

```console
$ docker pull kong@sha256:64b511bd7904fb453b67a7546412f9fa90023fb0bc894b175c50c0738cad7bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120292359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29dee4714e746c926a4b043ffedfa7e53b2309d09049452a31e7d670e8ada6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33641554fa01162df8a1f58e295f7cd7500ea15d3384f0039376ca23ee59283b`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 90.6 MB (90573542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75156dcff079865c8eb035aefc6fee2747da1c5eebf4b4f27f159fb6c94ffec3`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0` - unknown; unknown

```console
$ docker pull kong@sha256:c640d31d180ef175d0ab0cbd49a316eae008b20b11a165557a47d84923da3307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71885738b53967ede0279526d34f0873f2b1b92fd10988fac560d143bc8efb3a`

```dockerfile
```

-	Layers:
	-	`sha256:f086e76b248ffde645e0977b09c477ba1b048dea0b3f840700a6ce629c55f832`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 5.3 MB (5289699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e7fb4268f68b7e8a15927e77eeb71bec82746caf10c48199b44fab0c9e9862`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fadcac914015602c659e84eaeb5a613bce26d8802e552e430d0e8081d611e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118733966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376ab1d5d1f06c7709e2de91c67eb7f9e679e5c1531839b901cff68e0430b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fb2e4918d8e46e87cafdab9800e8200b013313dea30d1e371b6b5a638c93f8`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e66824736c60174bbd80ffb5c8cc7936ce492d205165f933ad218f673d635`  
		Last Modified: Wed, 09 Apr 2025 08:20:06 GMT  
		Size: 89.9 MB (89885725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7d4eff5302e5c62b203443077f3c29e98b8a8d701b949f4368a40829b7054`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0` - unknown; unknown

```console
$ docker pull kong@sha256:d1137d667449bf4b6e3aa084601bd079d3f14ecd5ef371789763224d794a068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70af9163360fb26ba3244de5487a4c612789c16b7384a10ba213d688809113fc`

```dockerfile
```

-	Layers:
	-	`sha256:0ba117d7e761e4a87609c63563f83f6c34e132a843aa5b23cc5b5e71f4c90fa8`  
		Last Modified: Wed, 09 Apr 2025 08:20:04 GMT  
		Size: 5.3 MB (5296858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f99a09021aa6d5a1d4f1409373eb74121649f1bcc1ae8d0b428bb425f0c575`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.0-ubuntu`

```console
$ docker pull kong@sha256:81cb84a14ece9369a93b62ab055dec078efd6744c393d8c78ad49a681f26ff79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:64b511bd7904fb453b67a7546412f9fa90023fb0bc894b175c50c0738cad7bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120292359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29dee4714e746c926a4b043ffedfa7e53b2309d09049452a31e7d670e8ada6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33641554fa01162df8a1f58e295f7cd7500ea15d3384f0039376ca23ee59283b`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 90.6 MB (90573542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75156dcff079865c8eb035aefc6fee2747da1c5eebf4b4f27f159fb6c94ffec3`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c640d31d180ef175d0ab0cbd49a316eae008b20b11a165557a47d84923da3307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71885738b53967ede0279526d34f0873f2b1b92fd10988fac560d143bc8efb3a`

```dockerfile
```

-	Layers:
	-	`sha256:f086e76b248ffde645e0977b09c477ba1b048dea0b3f840700a6ce629c55f832`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 5.3 MB (5289699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e7fb4268f68b7e8a15927e77eeb71bec82746caf10c48199b44fab0c9e9862`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fadcac914015602c659e84eaeb5a613bce26d8802e552e430d0e8081d611e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118733966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376ab1d5d1f06c7709e2de91c67eb7f9e679e5c1531839b901cff68e0430b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fb2e4918d8e46e87cafdab9800e8200b013313dea30d1e371b6b5a638c93f8`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e66824736c60174bbd80ffb5c8cc7936ce492d205165f933ad218f673d635`  
		Last Modified: Wed, 09 Apr 2025 08:20:06 GMT  
		Size: 89.9 MB (89885725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7d4eff5302e5c62b203443077f3c29e98b8a8d701b949f4368a40829b7054`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d1137d667449bf4b6e3aa084601bd079d3f14ecd5ef371789763224d794a068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70af9163360fb26ba3244de5487a4c612789c16b7384a10ba213d688809113fc`

```dockerfile
```

-	Layers:
	-	`sha256:0ba117d7e761e4a87609c63563f83f6c34e132a843aa5b23cc5b5e71f4c90fa8`  
		Last Modified: Wed, 09 Apr 2025 08:20:04 GMT  
		Size: 5.3 MB (5296858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f99a09021aa6d5a1d4f1409373eb74121649f1bcc1ae8d0b428bb425f0c575`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:81cb84a14ece9369a93b62ab055dec078efd6744c393d8c78ad49a681f26ff79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:64b511bd7904fb453b67a7546412f9fa90023fb0bc894b175c50c0738cad7bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120292359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29dee4714e746c926a4b043ffedfa7e53b2309d09049452a31e7d670e8ada6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33641554fa01162df8a1f58e295f7cd7500ea15d3384f0039376ca23ee59283b`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 90.6 MB (90573542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75156dcff079865c8eb035aefc6fee2747da1c5eebf4b4f27f159fb6c94ffec3`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:c640d31d180ef175d0ab0cbd49a316eae008b20b11a165557a47d84923da3307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71885738b53967ede0279526d34f0873f2b1b92fd10988fac560d143bc8efb3a`

```dockerfile
```

-	Layers:
	-	`sha256:f086e76b248ffde645e0977b09c477ba1b048dea0b3f840700a6ce629c55f832`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 5.3 MB (5289699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e7fb4268f68b7e8a15927e77eeb71bec82746caf10c48199b44fab0c9e9862`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fadcac914015602c659e84eaeb5a613bce26d8802e552e430d0e8081d611e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118733966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376ab1d5d1f06c7709e2de91c67eb7f9e679e5c1531839b901cff68e0430b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fb2e4918d8e46e87cafdab9800e8200b013313dea30d1e371b6b5a638c93f8`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e66824736c60174bbd80ffb5c8cc7936ce492d205165f933ad218f673d635`  
		Last Modified: Wed, 09 Apr 2025 08:20:06 GMT  
		Size: 89.9 MB (89885725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7d4eff5302e5c62b203443077f3c29e98b8a8d701b949f4368a40829b7054`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:d1137d667449bf4b6e3aa084601bd079d3f14ecd5ef371789763224d794a068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70af9163360fb26ba3244de5487a4c612789c16b7384a10ba213d688809113fc`

```dockerfile
```

-	Layers:
	-	`sha256:0ba117d7e761e4a87609c63563f83f6c34e132a843aa5b23cc5b5e71f4c90fa8`  
		Last Modified: Wed, 09 Apr 2025 08:20:04 GMT  
		Size: 5.3 MB (5296858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f99a09021aa6d5a1d4f1409373eb74121649f1bcc1ae8d0b428bb425f0c575`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:81cb84a14ece9369a93b62ab055dec078efd6744c393d8c78ad49a681f26ff79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:64b511bd7904fb453b67a7546412f9fa90023fb0bc894b175c50c0738cad7bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120292359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a29dee4714e746c926a4b043ffedfa7e53b2309d09049452a31e7d670e8ada6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Mon, 28 Apr 2025 10:53:49 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0b0f21f3adc30e9649a35c7a192d0cd18910cdfbb142e7b949b06375c6ff6`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33641554fa01162df8a1f58e295f7cd7500ea15d3384f0039376ca23ee59283b`  
		Last Modified: Mon, 05 May 2025 16:35:52 GMT  
		Size: 90.6 MB (90573542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75156dcff079865c8eb035aefc6fee2747da1c5eebf4b4f27f159fb6c94ffec3`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c640d31d180ef175d0ab0cbd49a316eae008b20b11a165557a47d84923da3307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71885738b53967ede0279526d34f0873f2b1b92fd10988fac560d143bc8efb3a`

```dockerfile
```

-	Layers:
	-	`sha256:f086e76b248ffde645e0977b09c477ba1b048dea0b3f840700a6ce629c55f832`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 5.3 MB (5289699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e7fb4268f68b7e8a15927e77eeb71bec82746caf10c48199b44fab0c9e9862`  
		Last Modified: Mon, 05 May 2025 16:35:51 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:fadcac914015602c659e84eaeb5a613bce26d8802e552e430d0e8081d611e347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118733966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3376ab1d5d1f06c7709e2de91c67eb7f9e679e5c1531839b901cff68e0430b83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 20 Dec 2024 21:36:52 GMT
ARG RELEASE
# Fri, 20 Dec 2024 21:36:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 20 Dec 2024 21:36:52 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2024 21:36:52 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 20 Dec 2024 21:36:52 GMT
ARG ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ENV ASSET=ce
# Fri, 20 Dec 2024 21:36:52 GMT
ARG EE_PORTS
# Fri, 20 Dec 2024 21:36:52 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ENV KONG_VERSION=3.9.0
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40
# Fri, 20 Dec 2024 21:36:52 GMT
ARG KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
# Fri, 20 Dec 2024 21:36:52 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.0 KONG_AMD64_SHA=c05ef5dc312676e032627c1cb0934056061d97b43ed8eb20bea9218916d90b40 KONG_ARM64_SHA=b487f95079a3a8ec07d331725e02b5a489e979f0d5e95ad16278bf60a665b34d
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 20 Dec 2024 21:36:52 GMT
USER kong
# Fri, 20 Dec 2024 21:36:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 20 Dec 2024 21:36:52 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 20 Dec 2024 21:36:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 20 Dec 2024 21:36:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 20 Dec 2024 21:36:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fb2e4918d8e46e87cafdab9800e8200b013313dea30d1e371b6b5a638c93f8`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50e66824736c60174bbd80ffb5c8cc7936ce492d205165f933ad218f673d635`  
		Last Modified: Wed, 09 Apr 2025 08:20:06 GMT  
		Size: 89.9 MB (89885725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7d4eff5302e5c62b203443077f3c29e98b8a8d701b949f4368a40829b7054`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d1137d667449bf4b6e3aa084601bd079d3f14ecd5ef371789763224d794a068e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70af9163360fb26ba3244de5487a4c612789c16b7384a10ba213d688809113fc`

```dockerfile
```

-	Layers:
	-	`sha256:0ba117d7e761e4a87609c63563f83f6c34e132a843aa5b23cc5b5e71f4c90fa8`  
		Last Modified: Wed, 09 Apr 2025 08:20:04 GMT  
		Size: 5.3 MB (5296858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f99a09021aa6d5a1d4f1409373eb74121649f1bcc1ae8d0b428bb425f0c575`  
		Last Modified: Wed, 09 Apr 2025 08:20:03 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json
