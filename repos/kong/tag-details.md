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
$ docker pull kong@sha256:d7149e430860bd575baa446828426d502c6648e2e8eeed45e96891206a0c8828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1d5021e727f34352a754a507cbb2375a2ea62d8c2060b0d07a935a7c2109539d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185239248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1276b126e99252f8f0db9f5ad1b96514ed4878f54260d454b8c16027b3fe48c6`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5f4cfb3f5d06b98f988c448c629a00c0f1a59f7826b2b1c2a217a9c196004`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 25.1 MB (25081958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539c7da7f671de831ad2bfcd9cf729aa4fdf54383620efa1caf0284937fa80aa`  
		Last Modified: Wed, 09 Apr 2025 01:19:28 GMT  
		Size: 130.6 MB (130624044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06521641537a8ccd6f0471a06a2efab23ea048f79559ca176d5e8a690c6dcf39`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:2cb5d7bcf7f18ca25892b9fd60113835a9c7d33d3693e2d95ad254be5cf4810a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7147408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cddd03e1123e10ed66eac5a4419fb2e33d2dc7ba71cfa28bc195f6e66eb2f7`

```dockerfile
```

-	Layers:
	-	`sha256:29009f7f90a25cd781e530050aac74fcd5f0ec4911e646f21df8f9547c8aa7bc`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 7.1 MB (7132923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad71ca32b6cfe1422b55451576c2ef3c3cd82bd2c6099699c0a73d47a7dc6c`  
		Last Modified: Wed, 09 Apr 2025 01:19:23 GMT  
		Size: 14.5 KB (14485 bytes)  
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
$ docker pull kong@sha256:d7149e430860bd575baa446828426d502c6648e2e8eeed45e96891206a0c8828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1d5021e727f34352a754a507cbb2375a2ea62d8c2060b0d07a935a7c2109539d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185239248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1276b126e99252f8f0db9f5ad1b96514ed4878f54260d454b8c16027b3fe48c6`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5f4cfb3f5d06b98f988c448c629a00c0f1a59f7826b2b1c2a217a9c196004`  
		Last Modified: Wed, 09 Apr 2025 01:19:25 GMT  
		Size: 25.1 MB (25081958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539c7da7f671de831ad2bfcd9cf729aa4fdf54383620efa1caf0284937fa80aa`  
		Last Modified: Wed, 09 Apr 2025 01:19:28 GMT  
		Size: 130.6 MB (130624044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06521641537a8ccd6f0471a06a2efab23ea048f79559ca176d5e8a690c6dcf39`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:2cb5d7bcf7f18ca25892b9fd60113835a9c7d33d3693e2d95ad254be5cf4810a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7147408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7cddd03e1123e10ed66eac5a4419fb2e33d2dc7ba71cfa28bc195f6e66eb2f7`

```dockerfile
```

-	Layers:
	-	`sha256:29009f7f90a25cd781e530050aac74fcd5f0ec4911e646f21df8f9547c8aa7bc`  
		Last Modified: Wed, 09 Apr 2025 01:19:24 GMT  
		Size: 7.1 MB (7132923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ad71ca32b6cfe1422b55451576c2ef3c3cd82bd2c6099699c0a73d47a7dc6c`  
		Last Modified: Wed, 09 Apr 2025 01:19:23 GMT  
		Size: 14.5 KB (14485 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:cf2acb894c59d3787ba073d3af28e324ff8676767e14f0d76a0aa62bbb88f9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:9f4b69c724abf3f47022cb3b79f0c0319865790514c195df7bf912cc94e4061a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73229a3e72b932fe837e92c9a3000a65290283c1680e4aecf0584f68bf72a19`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d41b4e733d82a5e5ab61f3a6904a65be63535e1795afa1b0f4a74727587b85`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01275fa05ac0c87ca35f2201fa089940bef6c868e711b4df463f4b8bb3aebe6`  
		Last Modified: Wed, 09 Apr 2025 01:47:24 GMT  
		Size: 90.6 MB (90571302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7158348f8eb1e15fe35dc5a6856c899c3caf44788c000bb3497ffd6cf68cf`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:1cfd54dedf60d5cccd73a49d4ff4849d0092cc1a5dcf0ee8ed50a59c1a1e4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db9eb61c46b72c1645da62a500870910066254c9d63fb03ee348cd28690cd7`

```dockerfile
```

-	Layers:
	-	`sha256:2a79a0fb806ac8f3bf0c3ebb13bddc606a2f815059e24bbf30bf78b7ae85ce14`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 5.3 MB (5289691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef52b25644dfbdf0b0b35c0adfdca93f8961d89499f2683bf3fbc932be912c9`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 16.3 KB (16260 bytes)  
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
$ docker pull kong@sha256:a5fbcf06d9e7ba9a3888fc82cf44258207fdd9d70d5f4398f234a84bbcf435b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:3c6b13b0cb1c3df394ae546ecea04e283241682cd291f15dfa8f0b980b6b8d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92272156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c93c7e400e38268cdda5a9fd578ffb8c2932c534c18cae176a765ef062ea3`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf6f7f8e9ea9f10122877e222394b37fffd1c7eb887467996671f90d0a2e7e4`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8bde7af2d2f7916f29d672d6db92b62d632b499feed8145231095f8aa3ae17`  
		Last Modified: Wed, 09 Apr 2025 01:18:58 GMT  
		Size: 62.7 MB (62738505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0788f096c69eb8bc612d6081167b565b49c15bb44e437600bddd3685104f9a`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:3296aa7df8689583c98f542d47feb8169727f52dec548c0c2e4728b45273c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ea86b9b9311c36aabae36c6f52883ee1f20a248cf8370cdf140c99784059a`

```dockerfile
```

-	Layers:
	-	`sha256:d18af2b03f39781a4be9512c5f0b0f31d760dfddb12aed7a3ab93e92744d3e9c`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 5.9 MB (5920970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9399e17cdf5d1e7a469d16f9dc10ec7eee08e42d4a4f01bc9561bf30c24fbc9`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 15.4 KB (15389 bytes)  
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
$ docker pull kong@sha256:a5fbcf06d9e7ba9a3888fc82cf44258207fdd9d70d5f4398f234a84bbcf435b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3c6b13b0cb1c3df394ae546ecea04e283241682cd291f15dfa8f0b980b6b8d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92272156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c93c7e400e38268cdda5a9fd578ffb8c2932c534c18cae176a765ef062ea3`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf6f7f8e9ea9f10122877e222394b37fffd1c7eb887467996671f90d0a2e7e4`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8bde7af2d2f7916f29d672d6db92b62d632b499feed8145231095f8aa3ae17`  
		Last Modified: Wed, 09 Apr 2025 01:18:58 GMT  
		Size: 62.7 MB (62738505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0788f096c69eb8bc612d6081167b565b49c15bb44e437600bddd3685104f9a`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:3296aa7df8689583c98f542d47feb8169727f52dec548c0c2e4728b45273c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ea86b9b9311c36aabae36c6f52883ee1f20a248cf8370cdf140c99784059a`

```dockerfile
```

-	Layers:
	-	`sha256:d18af2b03f39781a4be9512c5f0b0f31d760dfddb12aed7a3ab93e92744d3e9c`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 5.9 MB (5920970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9399e17cdf5d1e7a469d16f9dc10ec7eee08e42d4a4f01bc9561bf30c24fbc9`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 15.4 KB (15389 bytes)  
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
$ docker pull kong@sha256:a5fbcf06d9e7ba9a3888fc82cf44258207fdd9d70d5f4398f234a84bbcf435b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:3c6b13b0cb1c3df394ae546ecea04e283241682cd291f15dfa8f0b980b6b8d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92272156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c93c7e400e38268cdda5a9fd578ffb8c2932c534c18cae176a765ef062ea3`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf6f7f8e9ea9f10122877e222394b37fffd1c7eb887467996671f90d0a2e7e4`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8bde7af2d2f7916f29d672d6db92b62d632b499feed8145231095f8aa3ae17`  
		Last Modified: Wed, 09 Apr 2025 01:18:58 GMT  
		Size: 62.7 MB (62738505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0788f096c69eb8bc612d6081167b565b49c15bb44e437600bddd3685104f9a`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:3296aa7df8689583c98f542d47feb8169727f52dec548c0c2e4728b45273c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ea86b9b9311c36aabae36c6f52883ee1f20a248cf8370cdf140c99784059a`

```dockerfile
```

-	Layers:
	-	`sha256:d18af2b03f39781a4be9512c5f0b0f31d760dfddb12aed7a3ab93e92744d3e9c`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 5.9 MB (5920970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9399e17cdf5d1e7a469d16f9dc10ec7eee08e42d4a4f01bc9561bf30c24fbc9`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 15.4 KB (15389 bytes)  
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
$ docker pull kong@sha256:a5fbcf06d9e7ba9a3888fc82cf44258207fdd9d70d5f4398f234a84bbcf435b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3c6b13b0cb1c3df394ae546ecea04e283241682cd291f15dfa8f0b980b6b8d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92272156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c93c7e400e38268cdda5a9fd578ffb8c2932c534c18cae176a765ef062ea3`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf6f7f8e9ea9f10122877e222394b37fffd1c7eb887467996671f90d0a2e7e4`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8bde7af2d2f7916f29d672d6db92b62d632b499feed8145231095f8aa3ae17`  
		Last Modified: Wed, 09 Apr 2025 01:18:58 GMT  
		Size: 62.7 MB (62738505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0788f096c69eb8bc612d6081167b565b49c15bb44e437600bddd3685104f9a`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:3296aa7df8689583c98f542d47feb8169727f52dec548c0c2e4728b45273c07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:575ea86b9b9311c36aabae36c6f52883ee1f20a248cf8370cdf140c99784059a`

```dockerfile
```

-	Layers:
	-	`sha256:d18af2b03f39781a4be9512c5f0b0f31d760dfddb12aed7a3ab93e92744d3e9c`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 5.9 MB (5920970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9399e17cdf5d1e7a469d16f9dc10ec7eee08e42d4a4f01bc9561bf30c24fbc9`  
		Last Modified: Wed, 09 Apr 2025 01:18:57 GMT  
		Size: 15.4 KB (15389 bytes)  
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
$ docker pull kong@sha256:eaf0b207205dd885ab290a24d78a1e0d6ba913a0a8209608e54b7aef927c1e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6` - linux; amd64

```console
$ docker pull kong@sha256:54adf406e0042a09301a073eccb70b3dd62c4b287eb1dcf20aac7c8c9b28d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97236399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd49c10487f814c5df1e79b986f8d33dca885d07105e0a36f7390f9f6f6c007`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4d2dffa85e51eeedb626bce451eb0397c1cba0fcd79250edabc75f44f40f49`  
		Last Modified: Wed, 09 Apr 2025 01:19:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788deb0373274976422a25a1dfc376580c89026d1ea6d5d01ec5c04ec6643afb`  
		Last Modified: Wed, 09 Apr 2025 01:19:05 GMT  
		Size: 67.7 MB (67702750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8278fd134de925a65b29e4e66071fb8babba6d2f27aa92fe2eadd0fe256cbf1`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:d064ead9aa54ad3fbd5902fb4bdb1fdb11ee2bbc9d55dd6eccdd86338b9e47b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20b71e0f3ee55c689d4477d31f0b47864366920de14ab91f6d13813ba80d766`

```dockerfile
```

-	Layers:
	-	`sha256:90d1b4a435272cf5bf1b80bb792d011f035be29a1d61a25a94dbb445dffa06d1`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
		Size: 5.0 MB (4952059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7061bdf5d0d67a0dd0c318c97e24017dee728bada41192806499e538afae5d`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
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
$ docker pull kong@sha256:eaf0b207205dd885ab290a24d78a1e0d6ba913a0a8209608e54b7aef927c1e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:54adf406e0042a09301a073eccb70b3dd62c4b287eb1dcf20aac7c8c9b28d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97236399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd49c10487f814c5df1e79b986f8d33dca885d07105e0a36f7390f9f6f6c007`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4d2dffa85e51eeedb626bce451eb0397c1cba0fcd79250edabc75f44f40f49`  
		Last Modified: Wed, 09 Apr 2025 01:19:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788deb0373274976422a25a1dfc376580c89026d1ea6d5d01ec5c04ec6643afb`  
		Last Modified: Wed, 09 Apr 2025 01:19:05 GMT  
		Size: 67.7 MB (67702750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8278fd134de925a65b29e4e66071fb8babba6d2f27aa92fe2eadd0fe256cbf1`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d064ead9aa54ad3fbd5902fb4bdb1fdb11ee2bbc9d55dd6eccdd86338b9e47b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20b71e0f3ee55c689d4477d31f0b47864366920de14ab91f6d13813ba80d766`

```dockerfile
```

-	Layers:
	-	`sha256:90d1b4a435272cf5bf1b80bb792d011f035be29a1d61a25a94dbb445dffa06d1`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
		Size: 5.0 MB (4952059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7061bdf5d0d67a0dd0c318c97e24017dee728bada41192806499e538afae5d`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
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
$ docker pull kong@sha256:eaf0b207205dd885ab290a24d78a1e0d6ba913a0a8209608e54b7aef927c1e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1` - linux; amd64

```console
$ docker pull kong@sha256:54adf406e0042a09301a073eccb70b3dd62c4b287eb1dcf20aac7c8c9b28d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97236399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd49c10487f814c5df1e79b986f8d33dca885d07105e0a36f7390f9f6f6c007`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4d2dffa85e51eeedb626bce451eb0397c1cba0fcd79250edabc75f44f40f49`  
		Last Modified: Wed, 09 Apr 2025 01:19:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788deb0373274976422a25a1dfc376580c89026d1ea6d5d01ec5c04ec6643afb`  
		Last Modified: Wed, 09 Apr 2025 01:19:05 GMT  
		Size: 67.7 MB (67702750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8278fd134de925a65b29e4e66071fb8babba6d2f27aa92fe2eadd0fe256cbf1`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:d064ead9aa54ad3fbd5902fb4bdb1fdb11ee2bbc9d55dd6eccdd86338b9e47b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20b71e0f3ee55c689d4477d31f0b47864366920de14ab91f6d13813ba80d766`

```dockerfile
```

-	Layers:
	-	`sha256:90d1b4a435272cf5bf1b80bb792d011f035be29a1d61a25a94dbb445dffa06d1`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
		Size: 5.0 MB (4952059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7061bdf5d0d67a0dd0c318c97e24017dee728bada41192806499e538afae5d`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
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
$ docker pull kong@sha256:eaf0b207205dd885ab290a24d78a1e0d6ba913a0a8209608e54b7aef927c1e5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:54adf406e0042a09301a073eccb70b3dd62c4b287eb1dcf20aac7c8c9b28d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97236399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd49c10487f814c5df1e79b986f8d33dca885d07105e0a36f7390f9f6f6c007`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4d2dffa85e51eeedb626bce451eb0397c1cba0fcd79250edabc75f44f40f49`  
		Last Modified: Wed, 09 Apr 2025 01:19:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788deb0373274976422a25a1dfc376580c89026d1ea6d5d01ec5c04ec6643afb`  
		Last Modified: Wed, 09 Apr 2025 01:19:05 GMT  
		Size: 67.7 MB (67702750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8278fd134de925a65b29e4e66071fb8babba6d2f27aa92fe2eadd0fe256cbf1`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d064ead9aa54ad3fbd5902fb4bdb1fdb11ee2bbc9d55dd6eccdd86338b9e47b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20b71e0f3ee55c689d4477d31f0b47864366920de14ab91f6d13813ba80d766`

```dockerfile
```

-	Layers:
	-	`sha256:90d1b4a435272cf5bf1b80bb792d011f035be29a1d61a25a94dbb445dffa06d1`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
		Size: 5.0 MB (4952059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7061bdf5d0d67a0dd0c318c97e24017dee728bada41192806499e538afae5d`  
		Last Modified: Wed, 09 Apr 2025 01:19:02 GMT  
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
$ docker pull kong@sha256:c252653df12096b4b281418feb747b44f079ac47345ebb9294514e98913eeef9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7` - linux; amd64

```console
$ docker pull kong@sha256:b3a8aba5bf3bc061272a121a65216f67861c58d70ed0695aecd6238a7787293d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97275742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb506b43ce454112c9cd734345495dafff796c4a4a719454aeec82f66fa69fa1`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06b8756939873ea891f0af06df814cc630b51a8882951c49219b865b15fbade`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfc15908d026e4ba08a9cedbf3892a0bb8b63e9f5d0d0d02dd8e3b1e9cd2911`  
		Last Modified: Wed, 09 Apr 2025 01:18:44 GMT  
		Size: 67.7 MB (67742090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde3950eb17d0eb4cbaa1d22516436d918978b76cecd6a1e7d35f562e575bdc`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:18c9f6ec22d518b6ca7be5d17b263625fc50a9d1978567bb7971cbaa370b270b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2231c083386f1098dcaaaa9d2142dc0ffcd99e0b5ce27961f8ea5fae5d2e406c`

```dockerfile
```

-	Layers:
	-	`sha256:d3259492af50bf863a25c99e273683b3f0d000d12bf79a24e63b69b2ee061914`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 5.0 MB (5030507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81392f739d9632d54a1ce43f536ecbc6fdc5fcdc990074326b3d6df7ef343000`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
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
$ docker pull kong@sha256:c252653df12096b4b281418feb747b44f079ac47345ebb9294514e98913eeef9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b3a8aba5bf3bc061272a121a65216f67861c58d70ed0695aecd6238a7787293d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97275742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb506b43ce454112c9cd734345495dafff796c4a4a719454aeec82f66fa69fa1`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06b8756939873ea891f0af06df814cc630b51a8882951c49219b865b15fbade`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfc15908d026e4ba08a9cedbf3892a0bb8b63e9f5d0d0d02dd8e3b1e9cd2911`  
		Last Modified: Wed, 09 Apr 2025 01:18:44 GMT  
		Size: 67.7 MB (67742090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde3950eb17d0eb4cbaa1d22516436d918978b76cecd6a1e7d35f562e575bdc`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:18c9f6ec22d518b6ca7be5d17b263625fc50a9d1978567bb7971cbaa370b270b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2231c083386f1098dcaaaa9d2142dc0ffcd99e0b5ce27961f8ea5fae5d2e406c`

```dockerfile
```

-	Layers:
	-	`sha256:d3259492af50bf863a25c99e273683b3f0d000d12bf79a24e63b69b2ee061914`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 5.0 MB (5030507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81392f739d9632d54a1ce43f536ecbc6fdc5fcdc990074326b3d6df7ef343000`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
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
$ docker pull kong@sha256:c252653df12096b4b281418feb747b44f079ac47345ebb9294514e98913eeef9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1` - linux; amd64

```console
$ docker pull kong@sha256:b3a8aba5bf3bc061272a121a65216f67861c58d70ed0695aecd6238a7787293d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97275742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb506b43ce454112c9cd734345495dafff796c4a4a719454aeec82f66fa69fa1`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06b8756939873ea891f0af06df814cc630b51a8882951c49219b865b15fbade`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfc15908d026e4ba08a9cedbf3892a0bb8b63e9f5d0d0d02dd8e3b1e9cd2911`  
		Last Modified: Wed, 09 Apr 2025 01:18:44 GMT  
		Size: 67.7 MB (67742090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde3950eb17d0eb4cbaa1d22516436d918978b76cecd6a1e7d35f562e575bdc`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:18c9f6ec22d518b6ca7be5d17b263625fc50a9d1978567bb7971cbaa370b270b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2231c083386f1098dcaaaa9d2142dc0ffcd99e0b5ce27961f8ea5fae5d2e406c`

```dockerfile
```

-	Layers:
	-	`sha256:d3259492af50bf863a25c99e273683b3f0d000d12bf79a24e63b69b2ee061914`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 5.0 MB (5030507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81392f739d9632d54a1ce43f536ecbc6fdc5fcdc990074326b3d6df7ef343000`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
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
$ docker pull kong@sha256:c252653df12096b4b281418feb747b44f079ac47345ebb9294514e98913eeef9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b3a8aba5bf3bc061272a121a65216f67861c58d70ed0695aecd6238a7787293d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97275742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb506b43ce454112c9cd734345495dafff796c4a4a719454aeec82f66fa69fa1`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06b8756939873ea891f0af06df814cc630b51a8882951c49219b865b15fbade`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfc15908d026e4ba08a9cedbf3892a0bb8b63e9f5d0d0d02dd8e3b1e9cd2911`  
		Last Modified: Wed, 09 Apr 2025 01:18:44 GMT  
		Size: 67.7 MB (67742090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdde3950eb17d0eb4cbaa1d22516436d918978b76cecd6a1e7d35f562e575bdc`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:18c9f6ec22d518b6ca7be5d17b263625fc50a9d1978567bb7971cbaa370b270b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2231c083386f1098dcaaaa9d2142dc0ffcd99e0b5ce27961f8ea5fae5d2e406c`

```dockerfile
```

-	Layers:
	-	`sha256:d3259492af50bf863a25c99e273683b3f0d000d12bf79a24e63b69b2ee061914`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 5.0 MB (5030507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81392f739d9632d54a1ce43f536ecbc6fdc5fcdc990074326b3d6df7ef343000`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
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
$ docker pull kong@sha256:58a09330c05d5fcc401e47a3d0247993ebcf88c47eb04a658bbe523b78d4162c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:2fa416b6bf5f8ee2e4352fb67dcf6ab89e7da5456d6c2151e881fbdfb96e26e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19580cb6e668c017955034f06ec4ff355fe489296577d91aa097427948f188d0`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec1afeeaabf81529efa229b26d014d7053191f7dd4a455de0d4674730e6c653`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767a1ddec5a1635ca2fed90002f7ec25419f79a3f08226565a03be8dbe99160`  
		Last Modified: Wed, 09 Apr 2025 01:18:58 GMT  
		Size: 88.0 MB (88001474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46217e070a3d993c1d6d031beaa9f771a574b520bb5646cabb07a3d903f47338`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:6f38e5c320496f6efefe2cb621c237527ed8d1bbde4805bc0f2833b47edeb583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae7fa7f42ec303a16f71a09c58eaa39f0fb570cb0ac68798f07b89481e63544`

```dockerfile
```

-	Layers:
	-	`sha256:9ee006367c8bc807fdd8c7348b075cff7fdbcb0b97a94996bdd539c24f051fe1`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 5.2 MB (5224350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea377288ef16a9ea556fd7e20847a59923b4d6cf3f5b4bcc2cdc8c12ed35784`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
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
$ docker pull kong@sha256:58a09330c05d5fcc401e47a3d0247993ebcf88c47eb04a658bbe523b78d4162c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2fa416b6bf5f8ee2e4352fb67dcf6ab89e7da5456d6c2151e881fbdfb96e26e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19580cb6e668c017955034f06ec4ff355fe489296577d91aa097427948f188d0`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec1afeeaabf81529efa229b26d014d7053191f7dd4a455de0d4674730e6c653`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767a1ddec5a1635ca2fed90002f7ec25419f79a3f08226565a03be8dbe99160`  
		Last Modified: Wed, 09 Apr 2025 01:18:58 GMT  
		Size: 88.0 MB (88001474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46217e070a3d993c1d6d031beaa9f771a574b520bb5646cabb07a3d903f47338`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:6f38e5c320496f6efefe2cb621c237527ed8d1bbde4805bc0f2833b47edeb583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae7fa7f42ec303a16f71a09c58eaa39f0fb570cb0ac68798f07b89481e63544`

```dockerfile
```

-	Layers:
	-	`sha256:9ee006367c8bc807fdd8c7348b075cff7fdbcb0b97a94996bdd539c24f051fe1`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 5.2 MB (5224350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea377288ef16a9ea556fd7e20847a59923b4d6cf3f5b4bcc2cdc8c12ed35784`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
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
$ docker pull kong@sha256:58a09330c05d5fcc401e47a3d0247993ebcf88c47eb04a658bbe523b78d4162c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:2fa416b6bf5f8ee2e4352fb67dcf6ab89e7da5456d6c2151e881fbdfb96e26e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19580cb6e668c017955034f06ec4ff355fe489296577d91aa097427948f188d0`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec1afeeaabf81529efa229b26d014d7053191f7dd4a455de0d4674730e6c653`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767a1ddec5a1635ca2fed90002f7ec25419f79a3f08226565a03be8dbe99160`  
		Last Modified: Wed, 09 Apr 2025 01:18:58 GMT  
		Size: 88.0 MB (88001474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46217e070a3d993c1d6d031beaa9f771a574b520bb5646cabb07a3d903f47338`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:6f38e5c320496f6efefe2cb621c237527ed8d1bbde4805bc0f2833b47edeb583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae7fa7f42ec303a16f71a09c58eaa39f0fb570cb0ac68798f07b89481e63544`

```dockerfile
```

-	Layers:
	-	`sha256:9ee006367c8bc807fdd8c7348b075cff7fdbcb0b97a94996bdd539c24f051fe1`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 5.2 MB (5224350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea377288ef16a9ea556fd7e20847a59923b4d6cf3f5b4bcc2cdc8c12ed35784`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
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
$ docker pull kong@sha256:58a09330c05d5fcc401e47a3d0247993ebcf88c47eb04a658bbe523b78d4162c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2fa416b6bf5f8ee2e4352fb67dcf6ab89e7da5456d6c2151e881fbdfb96e26e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117535125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19580cb6e668c017955034f06ec4ff355fe489296577d91aa097427948f188d0`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec1afeeaabf81529efa229b26d014d7053191f7dd4a455de0d4674730e6c653`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767a1ddec5a1635ca2fed90002f7ec25419f79a3f08226565a03be8dbe99160`  
		Last Modified: Wed, 09 Apr 2025 01:18:58 GMT  
		Size: 88.0 MB (88001474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46217e070a3d993c1d6d031beaa9f771a574b520bb5646cabb07a3d903f47338`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:6f38e5c320496f6efefe2cb621c237527ed8d1bbde4805bc0f2833b47edeb583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae7fa7f42ec303a16f71a09c58eaa39f0fb570cb0ac68798f07b89481e63544`

```dockerfile
```

-	Layers:
	-	`sha256:9ee006367c8bc807fdd8c7348b075cff7fdbcb0b97a94996bdd539c24f051fe1`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
		Size: 5.2 MB (5224350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea377288ef16a9ea556fd7e20847a59923b4d6cf3f5b4bcc2cdc8c12ed35784`  
		Last Modified: Wed, 09 Apr 2025 01:18:56 GMT  
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
$ docker pull kong@sha256:cf2acb894c59d3787ba073d3af28e324ff8676767e14f0d76a0aa62bbb88f9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:9f4b69c724abf3f47022cb3b79f0c0319865790514c195df7bf912cc94e4061a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73229a3e72b932fe837e92c9a3000a65290283c1680e4aecf0584f68bf72a19`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d41b4e733d82a5e5ab61f3a6904a65be63535e1795afa1b0f4a74727587b85`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01275fa05ac0c87ca35f2201fa089940bef6c868e711b4df463f4b8bb3aebe6`  
		Last Modified: Wed, 09 Apr 2025 01:47:24 GMT  
		Size: 90.6 MB (90571302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7158348f8eb1e15fe35dc5a6856c899c3caf44788c000bb3497ffd6cf68cf`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:1cfd54dedf60d5cccd73a49d4ff4849d0092cc1a5dcf0ee8ed50a59c1a1e4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db9eb61c46b72c1645da62a500870910066254c9d63fb03ee348cd28690cd7`

```dockerfile
```

-	Layers:
	-	`sha256:2a79a0fb806ac8f3bf0c3ebb13bddc606a2f815059e24bbf30bf78b7ae85ce14`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 5.3 MB (5289691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef52b25644dfbdf0b0b35c0adfdca93f8961d89499f2683bf3fbc932be912c9`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 16.3 KB (16260 bytes)  
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
$ docker pull kong@sha256:cf2acb894c59d3787ba073d3af28e324ff8676767e14f0d76a0aa62bbb88f9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9f4b69c724abf3f47022cb3b79f0c0319865790514c195df7bf912cc94e4061a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73229a3e72b932fe837e92c9a3000a65290283c1680e4aecf0584f68bf72a19`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d41b4e733d82a5e5ab61f3a6904a65be63535e1795afa1b0f4a74727587b85`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01275fa05ac0c87ca35f2201fa089940bef6c868e711b4df463f4b8bb3aebe6`  
		Last Modified: Wed, 09 Apr 2025 01:47:24 GMT  
		Size: 90.6 MB (90571302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7158348f8eb1e15fe35dc5a6856c899c3caf44788c000bb3497ffd6cf68cf`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1cfd54dedf60d5cccd73a49d4ff4849d0092cc1a5dcf0ee8ed50a59c1a1e4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db9eb61c46b72c1645da62a500870910066254c9d63fb03ee348cd28690cd7`

```dockerfile
```

-	Layers:
	-	`sha256:2a79a0fb806ac8f3bf0c3ebb13bddc606a2f815059e24bbf30bf78b7ae85ce14`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 5.3 MB (5289691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef52b25644dfbdf0b0b35c0adfdca93f8961d89499f2683bf3fbc932be912c9`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 16.3 KB (16260 bytes)  
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
$ docker pull kong@sha256:cf2acb894c59d3787ba073d3af28e324ff8676767e14f0d76a0aa62bbb88f9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.0` - linux; amd64

```console
$ docker pull kong@sha256:9f4b69c724abf3f47022cb3b79f0c0319865790514c195df7bf912cc94e4061a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73229a3e72b932fe837e92c9a3000a65290283c1680e4aecf0584f68bf72a19`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d41b4e733d82a5e5ab61f3a6904a65be63535e1795afa1b0f4a74727587b85`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01275fa05ac0c87ca35f2201fa089940bef6c868e711b4df463f4b8bb3aebe6`  
		Last Modified: Wed, 09 Apr 2025 01:47:24 GMT  
		Size: 90.6 MB (90571302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7158348f8eb1e15fe35dc5a6856c899c3caf44788c000bb3497ffd6cf68cf`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0` - unknown; unknown

```console
$ docker pull kong@sha256:1cfd54dedf60d5cccd73a49d4ff4849d0092cc1a5dcf0ee8ed50a59c1a1e4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db9eb61c46b72c1645da62a500870910066254c9d63fb03ee348cd28690cd7`

```dockerfile
```

-	Layers:
	-	`sha256:2a79a0fb806ac8f3bf0c3ebb13bddc606a2f815059e24bbf30bf78b7ae85ce14`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 5.3 MB (5289691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef52b25644dfbdf0b0b35c0adfdca93f8961d89499f2683bf3fbc932be912c9`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 16.3 KB (16260 bytes)  
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
$ docker pull kong@sha256:cf2acb894c59d3787ba073d3af28e324ff8676767e14f0d76a0aa62bbb88f9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9f4b69c724abf3f47022cb3b79f0c0319865790514c195df7bf912cc94e4061a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73229a3e72b932fe837e92c9a3000a65290283c1680e4aecf0584f68bf72a19`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d41b4e733d82a5e5ab61f3a6904a65be63535e1795afa1b0f4a74727587b85`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01275fa05ac0c87ca35f2201fa089940bef6c868e711b4df463f4b8bb3aebe6`  
		Last Modified: Wed, 09 Apr 2025 01:47:24 GMT  
		Size: 90.6 MB (90571302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7158348f8eb1e15fe35dc5a6856c899c3caf44788c000bb3497ffd6cf68cf`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1cfd54dedf60d5cccd73a49d4ff4849d0092cc1a5dcf0ee8ed50a59c1a1e4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db9eb61c46b72c1645da62a500870910066254c9d63fb03ee348cd28690cd7`

```dockerfile
```

-	Layers:
	-	`sha256:2a79a0fb806ac8f3bf0c3ebb13bddc606a2f815059e24bbf30bf78b7ae85ce14`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 5.3 MB (5289691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef52b25644dfbdf0b0b35c0adfdca93f8961d89499f2683bf3fbc932be912c9`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 16.3 KB (16260 bytes)  
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
$ docker pull kong@sha256:cf2acb894c59d3787ba073d3af28e324ff8676767e14f0d76a0aa62bbb88f9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:9f4b69c724abf3f47022cb3b79f0c0319865790514c195df7bf912cc94e4061a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73229a3e72b932fe837e92c9a3000a65290283c1680e4aecf0584f68bf72a19`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d41b4e733d82a5e5ab61f3a6904a65be63535e1795afa1b0f4a74727587b85`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01275fa05ac0c87ca35f2201fa089940bef6c868e711b4df463f4b8bb3aebe6`  
		Last Modified: Wed, 09 Apr 2025 01:47:24 GMT  
		Size: 90.6 MB (90571302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7158348f8eb1e15fe35dc5a6856c899c3caf44788c000bb3497ffd6cf68cf`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:1cfd54dedf60d5cccd73a49d4ff4849d0092cc1a5dcf0ee8ed50a59c1a1e4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db9eb61c46b72c1645da62a500870910066254c9d63fb03ee348cd28690cd7`

```dockerfile
```

-	Layers:
	-	`sha256:2a79a0fb806ac8f3bf0c3ebb13bddc606a2f815059e24bbf30bf78b7ae85ce14`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 5.3 MB (5289691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef52b25644dfbdf0b0b35c0adfdca93f8961d89499f2683bf3fbc932be912c9`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 16.3 KB (16260 bytes)  
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
$ docker pull kong@sha256:cf2acb894c59d3787ba073d3af28e324ff8676767e14f0d76a0aa62bbb88f9d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9f4b69c724abf3f47022cb3b79f0c0319865790514c195df7bf912cc94e4061a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120290246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73229a3e72b932fe837e92c9a3000a65290283c1680e4aecf0584f68bf72a19`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d41b4e733d82a5e5ab61f3a6904a65be63535e1795afa1b0f4a74727587b85`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01275fa05ac0c87ca35f2201fa089940bef6c868e711b4df463f4b8bb3aebe6`  
		Last Modified: Wed, 09 Apr 2025 01:47:24 GMT  
		Size: 90.6 MB (90571302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7158348f8eb1e15fe35dc5a6856c899c3caf44788c000bb3497ffd6cf68cf`  
		Last Modified: Wed, 09 Apr 2025 01:47:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1cfd54dedf60d5cccd73a49d4ff4849d0092cc1a5dcf0ee8ed50a59c1a1e4250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db9eb61c46b72c1645da62a500870910066254c9d63fb03ee348cd28690cd7`

```dockerfile
```

-	Layers:
	-	`sha256:2a79a0fb806ac8f3bf0c3ebb13bddc606a2f815059e24bbf30bf78b7ae85ce14`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 5.3 MB (5289691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef52b25644dfbdf0b0b35c0adfdca93f8961d89499f2683bf3fbc932be912c9`  
		Last Modified: Wed, 09 Apr 2025 01:47:23 GMT  
		Size: 16.3 KB (16260 bytes)  
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
