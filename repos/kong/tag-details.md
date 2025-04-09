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
$ docker pull kong@sha256:04aa131c817ab6a41ff662cc19a15a07277cc5df99a074bfaac8d9cff4bf78c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:201a82530361f141bd785bb29f29db37bec979c56d073afae64878d94fb57630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185241523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0e357e7915320672d324cf0d14912c7405e4d360d12bc57fffd2b6f7764b14`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba6700c94e3a6554cd9099c348d1d4bfc95fac41c84ed42e30da824a32bea2d`  
		Last Modified: Tue, 04 Feb 2025 04:25:11 GMT  
		Size: 25.1 MB (25081958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5dbf8c00a4809759147210d8947bb7079d7b00a4a4ef02ac4bd132a258481f`  
		Last Modified: Tue, 04 Feb 2025 04:25:12 GMT  
		Size: 130.6 MB (130622741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdbbf51e73324169e31f2a5c4f5af0aa34b5aa7b00a3e23d1d7e8c30723f1cf`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5ffaa8876fc378717ce10595c05ce57dffb2cae0ac65f4ddf30b7fa9867a6cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7147289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c171974f36f03d31c0d192d047f44c2e85c3c0bbd76561273d6f0cc032dc74`

```dockerfile
```

-	Layers:
	-	`sha256:1e56f5c75cedd8302ad7aebab6aa56d2b8702984731898f9782c6ed148d38d2d`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
		Size: 7.1 MB (7132803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ab85b43d0e2c98d4f1e0ae9c93274c8260fcbc57de9306e7d49d95a8a96c857`  
		Last Modified: Tue, 04 Feb 2025 04:25:10 GMT  
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
$ docker pull kong@sha256:04b662eec72ffc48190539a0829e026696ea04eda61ce90520b1074285e2e921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:028f43b4c09fd4a52fa7cacc2b36695863d76fdce727da4d8857bbcb02970d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd909108d5f7f769fefee23e29461020a1860fa87e0c6f414f5490f9a7d5aa0`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075643277a2b761d3c08c1c45d62f0f7d721eb11275364e41915c0167e603f1f`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b823bfcf332d5ca5eb55775ede00932b91a7f09690038b43dd708f8364b6e61`  
		Last Modified: Tue, 04 Feb 2025 04:24:40 GMT  
		Size: 93.0 MB (92983194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482488644e4650c1f07b4872c6f295c1cf063154d3b268e27a355a3aff34efa`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:996feca40b9b47939755a8c876a66fd0907f627b343dfb1c7c63e493e70f829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624776cd0890ed9e0edeb45ad243eb4ea6171c6989459765e56054b24ef09248`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c0784c80e23bdad6be3dbe9c7e0299665911692e268335bf11e31ea595507`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 5.3 MB (5291918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e19162236e8c066577ff22466bdb94d348e359945734ebc0a0ec5ef58fd4dd4`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b1b5d4553561125dd503e17c1b16876fc91fc988f8f34b4083ab3259cb91fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121163151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0e963987a10b02458821d680f6cdc4596754add641aac1a45e4d928bca1f3`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69974675d6d49cc7b689c346021aa57d7d8a833b1aafdc14483ed71b6b1e26`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105827f107035063431f24e8c473a1f00ae759d79eee5fd428eaf204cb94bf5b`  
		Last Modified: Tue, 04 Feb 2025 09:59:32 GMT  
		Size: 92.3 MB (92268266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e3660773e699436700d2a4377df6f191f3be81209966de40d506ab28e2db`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:5d72f79fe16c26234efc84680099249e1947b2f0f9a7d55b23a7325af3281641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02a7ffc35598a574642969ba8de27e956de9f221678fd7c6f52717176810bb`

```dockerfile
```

-	Layers:
	-	`sha256:10f78b687995432d2131937079f4b796e708f2b3d83cf1debdea83afd4a71723`  
		Last Modified: Tue, 04 Feb 2025 09:59:30 GMT  
		Size: 5.3 MB (5299085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d16181a078fd25315dcd17e3966bbc64dbc7c1b8f08fb87c44a18350856b66`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:5f6e646d10552f325c32b3c1b909dbda44b043ec6a411193fc2f1fec565ab3af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:4221fa7b08a4482aaa677847de2545e8494caa97c6765d94613224d8fc2ba5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92267268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba5f7246be45c6bc489e2a47eee59cac37e77e6ed7c9f1f34a8388f16a51b08`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959848b6d654831dc2f2b08a50313cb2a511ac68a5cec97d8b4df8ee6b2a1c5c`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59591d48f3b248be76369c93a05fb07e4cfdacbca83c71ebb5efebaa7934789`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 62.7 MB (62730043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c979b261ea4bf0fe8bddb1b39a78e7241e42504a2d42c2eedf41ce96db56c30d`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:b1c8ed046d3d13a245752cb7497069006fd9fcc15d76e8705e9a30ab7b779f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479eaa3e21470990f036b8385dd7b01dffd2af5db209f03034a9df0f04094bf3`

```dockerfile
```

-	Layers:
	-	`sha256:78282cb62434eb0a0a3b4e0045e7f5b63b0b8c221e230f70b116db994fd8ca3e`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.9 MB (5920882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f2ad7046f0cabdd49987623eade3e60c4c14cbe7345d43d117dd3c362b40fb`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:450de53ca9ad99a3d64f975221c4e024442677bc92b40ff0ce11ce69ae088a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88528610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b5042036f1ccd31353f5c1ce6f6b1ad2f258035bd9b2b3e01cc0dc419b5d3`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f0331371a45a418153fe50cacfc2f8475f1c09026636188fbd5706dc41f17`  
		Last Modified: Tue, 04 Feb 2025 10:02:59 GMT  
		Size: 61.2 MB (61169141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a70e3d0660c8e82d4d9c2157da70364780e18bc1c6c59f94f537c587d6af80f`  
		Last Modified: Tue, 04 Feb 2025 10:02:56 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:4a119b6864d34379857ba4f00c51dd210cd69bace9ddf995a4643beeeefa85a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff977b349f18feccc754a6ac396beccca9edc211cf8335bb697a054abcd22e49`

```dockerfile
```

-	Layers:
	-	`sha256:dce85540ea35c635b43b27a445014fd0c090f511dfebc7f3ee7326dbc7cfcf8f`  
		Last Modified: Tue, 04 Feb 2025 10:02:57 GMT  
		Size: 5.9 MB (5898961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4264a0d8901a79da14fd8cfd0df99b1888966b5a77b54b4f515f247279d59c9`  
		Last Modified: Tue, 04 Feb 2025 10:02:56 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:5f6e646d10552f325c32b3c1b909dbda44b043ec6a411193fc2f1fec565ab3af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:4221fa7b08a4482aaa677847de2545e8494caa97c6765d94613224d8fc2ba5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92267268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba5f7246be45c6bc489e2a47eee59cac37e77e6ed7c9f1f34a8388f16a51b08`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959848b6d654831dc2f2b08a50313cb2a511ac68a5cec97d8b4df8ee6b2a1c5c`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59591d48f3b248be76369c93a05fb07e4cfdacbca83c71ebb5efebaa7934789`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 62.7 MB (62730043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c979b261ea4bf0fe8bddb1b39a78e7241e42504a2d42c2eedf41ce96db56c30d`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:b1c8ed046d3d13a245752cb7497069006fd9fcc15d76e8705e9a30ab7b779f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479eaa3e21470990f036b8385dd7b01dffd2af5db209f03034a9df0f04094bf3`

```dockerfile
```

-	Layers:
	-	`sha256:78282cb62434eb0a0a3b4e0045e7f5b63b0b8c221e230f70b116db994fd8ca3e`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.9 MB (5920882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f2ad7046f0cabdd49987623eade3e60c4c14cbe7345d43d117dd3c362b40fb`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:450de53ca9ad99a3d64f975221c4e024442677bc92b40ff0ce11ce69ae088a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88528610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b5042036f1ccd31353f5c1ce6f6b1ad2f258035bd9b2b3e01cc0dc419b5d3`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f0331371a45a418153fe50cacfc2f8475f1c09026636188fbd5706dc41f17`  
		Last Modified: Tue, 04 Feb 2025 10:02:59 GMT  
		Size: 61.2 MB (61169141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a70e3d0660c8e82d4d9c2157da70364780e18bc1c6c59f94f537c587d6af80f`  
		Last Modified: Tue, 04 Feb 2025 10:02:56 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:4a119b6864d34379857ba4f00c51dd210cd69bace9ddf995a4643beeeefa85a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff977b349f18feccc754a6ac396beccca9edc211cf8335bb697a054abcd22e49`

```dockerfile
```

-	Layers:
	-	`sha256:dce85540ea35c635b43b27a445014fd0c090f511dfebc7f3ee7326dbc7cfcf8f`  
		Last Modified: Tue, 04 Feb 2025 10:02:57 GMT  
		Size: 5.9 MB (5898961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4264a0d8901a79da14fd8cfd0df99b1888966b5a77b54b4f515f247279d59c9`  
		Last Modified: Tue, 04 Feb 2025 10:02:56 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:5f6e646d10552f325c32b3c1b909dbda44b043ec6a411193fc2f1fec565ab3af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:4221fa7b08a4482aaa677847de2545e8494caa97c6765d94613224d8fc2ba5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92267268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba5f7246be45c6bc489e2a47eee59cac37e77e6ed7c9f1f34a8388f16a51b08`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959848b6d654831dc2f2b08a50313cb2a511ac68a5cec97d8b4df8ee6b2a1c5c`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59591d48f3b248be76369c93a05fb07e4cfdacbca83c71ebb5efebaa7934789`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 62.7 MB (62730043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c979b261ea4bf0fe8bddb1b39a78e7241e42504a2d42c2eedf41ce96db56c30d`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:b1c8ed046d3d13a245752cb7497069006fd9fcc15d76e8705e9a30ab7b779f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479eaa3e21470990f036b8385dd7b01dffd2af5db209f03034a9df0f04094bf3`

```dockerfile
```

-	Layers:
	-	`sha256:78282cb62434eb0a0a3b4e0045e7f5b63b0b8c221e230f70b116db994fd8ca3e`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.9 MB (5920882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f2ad7046f0cabdd49987623eade3e60c4c14cbe7345d43d117dd3c362b40fb`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:450de53ca9ad99a3d64f975221c4e024442677bc92b40ff0ce11ce69ae088a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88528610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b5042036f1ccd31353f5c1ce6f6b1ad2f258035bd9b2b3e01cc0dc419b5d3`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f0331371a45a418153fe50cacfc2f8475f1c09026636188fbd5706dc41f17`  
		Last Modified: Tue, 04 Feb 2025 10:02:59 GMT  
		Size: 61.2 MB (61169141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a70e3d0660c8e82d4d9c2157da70364780e18bc1c6c59f94f537c587d6af80f`  
		Last Modified: Tue, 04 Feb 2025 10:02:56 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:4a119b6864d34379857ba4f00c51dd210cd69bace9ddf995a4643beeeefa85a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff977b349f18feccc754a6ac396beccca9edc211cf8335bb697a054abcd22e49`

```dockerfile
```

-	Layers:
	-	`sha256:dce85540ea35c635b43b27a445014fd0c090f511dfebc7f3ee7326dbc7cfcf8f`  
		Last Modified: Tue, 04 Feb 2025 10:02:57 GMT  
		Size: 5.9 MB (5898961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4264a0d8901a79da14fd8cfd0df99b1888966b5a77b54b4f515f247279d59c9`  
		Last Modified: Tue, 04 Feb 2025 10:02:56 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:dad30257ff34d0a7e1fd82e9e63121fb8f7d1ad518e17c3657ea104b1be842a1
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
$ docker pull kong@sha256:450de53ca9ad99a3d64f975221c4e024442677bc92b40ff0ce11ce69ae088a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88528610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9b5042036f1ccd31353f5c1ce6f6b1ad2f258035bd9b2b3e01cc0dc419b5d3`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230f0331371a45a418153fe50cacfc2f8475f1c09026636188fbd5706dc41f17`  
		Last Modified: Tue, 04 Feb 2025 10:02:59 GMT  
		Size: 61.2 MB (61169141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a70e3d0660c8e82d4d9c2157da70364780e18bc1c6c59f94f537c587d6af80f`  
		Last Modified: Tue, 04 Feb 2025 10:02:56 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:4a119b6864d34379857ba4f00c51dd210cd69bace9ddf995a4643beeeefa85a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5914454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff977b349f18feccc754a6ac396beccca9edc211cf8335bb697a054abcd22e49`

```dockerfile
```

-	Layers:
	-	`sha256:dce85540ea35c635b43b27a445014fd0c090f511dfebc7f3ee7326dbc7cfcf8f`  
		Last Modified: Tue, 04 Feb 2025 10:02:57 GMT  
		Size: 5.9 MB (5898961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4264a0d8901a79da14fd8cfd0df99b1888966b5a77b54b4f515f247279d59c9`  
		Last Modified: Tue, 04 Feb 2025 10:02:56 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6`

```console
$ docker pull kong@sha256:79b99f6c76c62682a74bc3f77e6c1a7698954d193c6d29ce772eb0a791b415a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6` - linux; amd64

```console
$ docker pull kong@sha256:59948609336d6d237546331162c8d9de357713579df5f3a27cea8b4b6f6a2145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e7612e69ac9649db833c245f8c0fd842eacb7b6f7975d608bd4b85ff8ed8e2`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88199f8875288da91d714c0c9eaf05b7ef6ae7647a8746f6893ac018d93f1db7`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181aa4bd68db44833d1ebb1f09dfeedd426f47a6c836cdf3b18023c2910f657e`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 67.7 MB (67704226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4afe0502b812cb9965d39129f6888420555972a2a334a798f166243d0a4b2`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:9a48e55dab4406fe0e40f3bd8d8cada1711319d8c0251784c4543f7aad974aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a751d858718d2ea76755c2a5c424324b16fc6da0487be009e6bfa99e1821ed65`

```dockerfile
```

-	Layers:
	-	`sha256:0cf32d3101666e165e7dbb4c51fab1f519b9df42d236f737e410cba72fe415cf`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 5.0 MB (4951975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4d65e9023095344ac7c8031969041daad151fc998b9f5ac67e440fcab94123`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:13af3bbc7a6dc767ac0692792b4c51e343f4c8ec8b274b4a1378b055c7693e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94589774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9d7d426c2041890a14ca6c1456590804b27a59ceec3d22e37df19a1fc9ad0`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be23ecbabbfe2613fa9d58de4096fee1faa086655a385b684c4ec83afba2fb91`  
		Last Modified: Tue, 04 Feb 2025 10:02:07 GMT  
		Size: 67.2 MB (67230306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862e0fafbfe75b122de1cead3efcb1bd0222c5d8ecaeaa895223fc36a5af18f6`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:26cabb79af4f6332c262f4a3a307fa4c974d114015a1c437aff158c04dd71a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9424ca09adf646ba547664dbebda02a05acd49cad5bbcb728db066b485666466`

```dockerfile
```

-	Layers:
	-	`sha256:3447e50eb8f42b9e1e3f2169c1b44be666e50276beddb0c1a8d14e680f985c6c`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 5.0 MB (4958301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f9fe27327fda04df10fce5a891144d3d806498811e6b3c60493b029fc53768`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:79b99f6c76c62682a74bc3f77e6c1a7698954d193c6d29ce772eb0a791b415a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:59948609336d6d237546331162c8d9de357713579df5f3a27cea8b4b6f6a2145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e7612e69ac9649db833c245f8c0fd842eacb7b6f7975d608bd4b85ff8ed8e2`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88199f8875288da91d714c0c9eaf05b7ef6ae7647a8746f6893ac018d93f1db7`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181aa4bd68db44833d1ebb1f09dfeedd426f47a6c836cdf3b18023c2910f657e`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 67.7 MB (67704226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4afe0502b812cb9965d39129f6888420555972a2a334a798f166243d0a4b2`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9a48e55dab4406fe0e40f3bd8d8cada1711319d8c0251784c4543f7aad974aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a751d858718d2ea76755c2a5c424324b16fc6da0487be009e6bfa99e1821ed65`

```dockerfile
```

-	Layers:
	-	`sha256:0cf32d3101666e165e7dbb4c51fab1f519b9df42d236f737e410cba72fe415cf`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 5.0 MB (4951975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4d65e9023095344ac7c8031969041daad151fc998b9f5ac67e440fcab94123`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:13af3bbc7a6dc767ac0692792b4c51e343f4c8ec8b274b4a1378b055c7693e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94589774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9d7d426c2041890a14ca6c1456590804b27a59ceec3d22e37df19a1fc9ad0`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be23ecbabbfe2613fa9d58de4096fee1faa086655a385b684c4ec83afba2fb91`  
		Last Modified: Tue, 04 Feb 2025 10:02:07 GMT  
		Size: 67.2 MB (67230306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862e0fafbfe75b122de1cead3efcb1bd0222c5d8ecaeaa895223fc36a5af18f6`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:26cabb79af4f6332c262f4a3a307fa4c974d114015a1c437aff158c04dd71a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9424ca09adf646ba547664dbebda02a05acd49cad5bbcb728db066b485666466`

```dockerfile
```

-	Layers:
	-	`sha256:3447e50eb8f42b9e1e3f2169c1b44be666e50276beddb0c1a8d14e680f985c6c`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 5.0 MB (4958301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f9fe27327fda04df10fce5a891144d3d806498811e6b3c60493b029fc53768`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6.1`

```console
$ docker pull kong@sha256:79b99f6c76c62682a74bc3f77e6c1a7698954d193c6d29ce772eb0a791b415a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1` - linux; amd64

```console
$ docker pull kong@sha256:59948609336d6d237546331162c8d9de357713579df5f3a27cea8b4b6f6a2145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e7612e69ac9649db833c245f8c0fd842eacb7b6f7975d608bd4b85ff8ed8e2`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88199f8875288da91d714c0c9eaf05b7ef6ae7647a8746f6893ac018d93f1db7`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181aa4bd68db44833d1ebb1f09dfeedd426f47a6c836cdf3b18023c2910f657e`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 67.7 MB (67704226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4afe0502b812cb9965d39129f6888420555972a2a334a798f166243d0a4b2`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:9a48e55dab4406fe0e40f3bd8d8cada1711319d8c0251784c4543f7aad974aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a751d858718d2ea76755c2a5c424324b16fc6da0487be009e6bfa99e1821ed65`

```dockerfile
```

-	Layers:
	-	`sha256:0cf32d3101666e165e7dbb4c51fab1f519b9df42d236f737e410cba72fe415cf`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 5.0 MB (4951975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4d65e9023095344ac7c8031969041daad151fc998b9f5ac67e440fcab94123`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:13af3bbc7a6dc767ac0692792b4c51e343f4c8ec8b274b4a1378b055c7693e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94589774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9d7d426c2041890a14ca6c1456590804b27a59ceec3d22e37df19a1fc9ad0`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be23ecbabbfe2613fa9d58de4096fee1faa086655a385b684c4ec83afba2fb91`  
		Last Modified: Tue, 04 Feb 2025 10:02:07 GMT  
		Size: 67.2 MB (67230306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862e0fafbfe75b122de1cead3efcb1bd0222c5d8ecaeaa895223fc36a5af18f6`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:26cabb79af4f6332c262f4a3a307fa4c974d114015a1c437aff158c04dd71a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9424ca09adf646ba547664dbebda02a05acd49cad5bbcb728db066b485666466`

```dockerfile
```

-	Layers:
	-	`sha256:3447e50eb8f42b9e1e3f2169c1b44be666e50276beddb0c1a8d14e680f985c6c`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 5.0 MB (4958301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f9fe27327fda04df10fce5a891144d3d806498811e6b3c60493b029fc53768`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:79b99f6c76c62682a74bc3f77e6c1a7698954d193c6d29ce772eb0a791b415a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:59948609336d6d237546331162c8d9de357713579df5f3a27cea8b4b6f6a2145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97241453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e7612e69ac9649db833c245f8c0fd842eacb7b6f7975d608bd4b85ff8ed8e2`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88199f8875288da91d714c0c9eaf05b7ef6ae7647a8746f6893ac018d93f1db7`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181aa4bd68db44833d1ebb1f09dfeedd426f47a6c836cdf3b18023c2910f657e`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 67.7 MB (67704226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4afe0502b812cb9965d39129f6888420555972a2a334a798f166243d0a4b2`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9a48e55dab4406fe0e40f3bd8d8cada1711319d8c0251784c4543f7aad974aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a751d858718d2ea76755c2a5c424324b16fc6da0487be009e6bfa99e1821ed65`

```dockerfile
```

-	Layers:
	-	`sha256:0cf32d3101666e165e7dbb4c51fab1f519b9df42d236f737e410cba72fe415cf`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 5.0 MB (4951975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4d65e9023095344ac7c8031969041daad151fc998b9f5ac67e440fcab94123`  
		Last Modified: Tue, 04 Feb 2025 04:24:48 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:13af3bbc7a6dc767ac0692792b4c51e343f4c8ec8b274b4a1378b055c7693e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94589774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9d7d426c2041890a14ca6c1456590804b27a59ceec3d22e37df19a1fc9ad0`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be23ecbabbfe2613fa9d58de4096fee1faa086655a385b684c4ec83afba2fb91`  
		Last Modified: Tue, 04 Feb 2025 10:02:07 GMT  
		Size: 67.2 MB (67230306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862e0fafbfe75b122de1cead3efcb1bd0222c5d8ecaeaa895223fc36a5af18f6`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:26cabb79af4f6332c262f4a3a307fa4c974d114015a1c437aff158c04dd71a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9424ca09adf646ba547664dbebda02a05acd49cad5bbcb728db066b485666466`

```dockerfile
```

-	Layers:
	-	`sha256:3447e50eb8f42b9e1e3f2169c1b44be666e50276beddb0c1a8d14e680f985c6c`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 5.0 MB (4958301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79f9fe27327fda04df10fce5a891144d3d806498811e6b3c60493b029fc53768`  
		Last Modified: Tue, 04 Feb 2025 10:02:05 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7`

```console
$ docker pull kong@sha256:e2ec26bae369a2e50083f456a8ccca18a276379f7d86fa61eb201c858d4f59db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7` - linux; amd64

```console
$ docker pull kong@sha256:927101b9ff33a1185a1b6bcf6a0f96d3cd6acf495416363f1c8b1c8148b1239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97278043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08219089a4b6daa4c2e5fbe5fa0972a3147fb5c10cc060e3cd133aac67e63a97`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235de49acae2da370547894e338695486290870963616ebf82652295c6c3ea2`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20205ecc65f886ab340c2b4798c9f9431091145f1b86a0060581071c50bf5e85`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 67.7 MB (67740817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d545e160d16c419b9bd89a0e669f4e96ff6d911533c429c40b4579e36da30028`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:5b6d9a3660f75b1082b42b4709ccdb598108bde45307cac25ecd5af2952ac04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd2b1e8471612e72d5b5dc3eca30a28c8e897ee54c76e5a50b65a338833df9d`

```dockerfile
```

-	Layers:
	-	`sha256:0ead825d17a736595a8d68d8b4f5fb19197608e98aac03bde33c559f06b32458`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.0 MB (5030423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0191fe8c994c2f0011dcab52e3666bed38adfee3cf30ddceeabe5b1d33d42960`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a464e9f2748a1566df37a3724b95d1a1a69f290ac96447951671c83a550067ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd8b86639da4308fc12076a3bedc7fb62d2c24ed8bff5ef402ff017fbc7192c`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d66ce338e12d0a15108f0c8e9ac5fdf6b81805b726881f9b134314dc0a0fc88`  
		Last Modified: Tue, 04 Feb 2025 10:01:24 GMT  
		Size: 67.7 MB (67656005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e52051c8cda773cb8964f44dad5417e7108440620c3a93457479ae9da006b3d`  
		Last Modified: Tue, 04 Feb 2025 10:01:21 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:b80c2211d5e87359c11d33e807d152dc3e3d55c3de5e037bb291336eb458ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5052241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f68ad0d6548d4e85cd781b4e7ac854f89386f6f040d54740d464484df0473c`

```dockerfile
```

-	Layers:
	-	`sha256:3f4680d65fd004d89d874b5f6a4e56fa772ae1684e09ef9c4a4270d257d152c3`  
		Last Modified: Tue, 04 Feb 2025 10:01:22 GMT  
		Size: 5.0 MB (5036749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf114dd44ca7714902a8167ed2224de969999df5c754e43272ac1f57826ada6`  
		Last Modified: Tue, 04 Feb 2025 10:01:21 GMT  
		Size: 15.5 KB (15492 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7-ubuntu`

```console
$ docker pull kong@sha256:e2ec26bae369a2e50083f456a8ccca18a276379f7d86fa61eb201c858d4f59db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:927101b9ff33a1185a1b6bcf6a0f96d3cd6acf495416363f1c8b1c8148b1239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97278043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08219089a4b6daa4c2e5fbe5fa0972a3147fb5c10cc060e3cd133aac67e63a97`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235de49acae2da370547894e338695486290870963616ebf82652295c6c3ea2`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20205ecc65f886ab340c2b4798c9f9431091145f1b86a0060581071c50bf5e85`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 67.7 MB (67740817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d545e160d16c419b9bd89a0e669f4e96ff6d911533c429c40b4579e36da30028`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5b6d9a3660f75b1082b42b4709ccdb598108bde45307cac25ecd5af2952ac04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd2b1e8471612e72d5b5dc3eca30a28c8e897ee54c76e5a50b65a338833df9d`

```dockerfile
```

-	Layers:
	-	`sha256:0ead825d17a736595a8d68d8b4f5fb19197608e98aac03bde33c559f06b32458`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.0 MB (5030423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0191fe8c994c2f0011dcab52e3666bed38adfee3cf30ddceeabe5b1d33d42960`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a464e9f2748a1566df37a3724b95d1a1a69f290ac96447951671c83a550067ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd8b86639da4308fc12076a3bedc7fb62d2c24ed8bff5ef402ff017fbc7192c`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d66ce338e12d0a15108f0c8e9ac5fdf6b81805b726881f9b134314dc0a0fc88`  
		Last Modified: Tue, 04 Feb 2025 10:01:24 GMT  
		Size: 67.7 MB (67656005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e52051c8cda773cb8964f44dad5417e7108440620c3a93457479ae9da006b3d`  
		Last Modified: Tue, 04 Feb 2025 10:01:21 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:b80c2211d5e87359c11d33e807d152dc3e3d55c3de5e037bb291336eb458ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5052241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f68ad0d6548d4e85cd781b4e7ac854f89386f6f040d54740d464484df0473c`

```dockerfile
```

-	Layers:
	-	`sha256:3f4680d65fd004d89d874b5f6a4e56fa772ae1684e09ef9c4a4270d257d152c3`  
		Last Modified: Tue, 04 Feb 2025 10:01:22 GMT  
		Size: 5.0 MB (5036749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf114dd44ca7714902a8167ed2224de969999df5c754e43272ac1f57826ada6`  
		Last Modified: Tue, 04 Feb 2025 10:01:21 GMT  
		Size: 15.5 KB (15492 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.1`

```console
$ docker pull kong@sha256:e2ec26bae369a2e50083f456a8ccca18a276379f7d86fa61eb201c858d4f59db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1` - linux; amd64

```console
$ docker pull kong@sha256:927101b9ff33a1185a1b6bcf6a0f96d3cd6acf495416363f1c8b1c8148b1239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97278043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08219089a4b6daa4c2e5fbe5fa0972a3147fb5c10cc060e3cd133aac67e63a97`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235de49acae2da370547894e338695486290870963616ebf82652295c6c3ea2`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20205ecc65f886ab340c2b4798c9f9431091145f1b86a0060581071c50bf5e85`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 67.7 MB (67740817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d545e160d16c419b9bd89a0e669f4e96ff6d911533c429c40b4579e36da30028`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:5b6d9a3660f75b1082b42b4709ccdb598108bde45307cac25ecd5af2952ac04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd2b1e8471612e72d5b5dc3eca30a28c8e897ee54c76e5a50b65a338833df9d`

```dockerfile
```

-	Layers:
	-	`sha256:0ead825d17a736595a8d68d8b4f5fb19197608e98aac03bde33c559f06b32458`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.0 MB (5030423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0191fe8c994c2f0011dcab52e3666bed38adfee3cf30ddceeabe5b1d33d42960`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a464e9f2748a1566df37a3724b95d1a1a69f290ac96447951671c83a550067ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd8b86639da4308fc12076a3bedc7fb62d2c24ed8bff5ef402ff017fbc7192c`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d66ce338e12d0a15108f0c8e9ac5fdf6b81805b726881f9b134314dc0a0fc88`  
		Last Modified: Tue, 04 Feb 2025 10:01:24 GMT  
		Size: 67.7 MB (67656005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e52051c8cda773cb8964f44dad5417e7108440620c3a93457479ae9da006b3d`  
		Last Modified: Tue, 04 Feb 2025 10:01:21 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:b80c2211d5e87359c11d33e807d152dc3e3d55c3de5e037bb291336eb458ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5052241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f68ad0d6548d4e85cd781b4e7ac854f89386f6f040d54740d464484df0473c`

```dockerfile
```

-	Layers:
	-	`sha256:3f4680d65fd004d89d874b5f6a4e56fa772ae1684e09ef9c4a4270d257d152c3`  
		Last Modified: Tue, 04 Feb 2025 10:01:22 GMT  
		Size: 5.0 MB (5036749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf114dd44ca7714902a8167ed2224de969999df5c754e43272ac1f57826ada6`  
		Last Modified: Tue, 04 Feb 2025 10:01:21 GMT  
		Size: 15.5 KB (15492 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.1-ubuntu`

```console
$ docker pull kong@sha256:e2ec26bae369a2e50083f456a8ccca18a276379f7d86fa61eb201c858d4f59db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:927101b9ff33a1185a1b6bcf6a0f96d3cd6acf495416363f1c8b1c8148b1239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97278043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08219089a4b6daa4c2e5fbe5fa0972a3147fb5c10cc060e3cd133aac67e63a97`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3235de49acae2da370547894e338695486290870963616ebf82652295c6c3ea2`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20205ecc65f886ab340c2b4798c9f9431091145f1b86a0060581071c50bf5e85`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 67.7 MB (67740817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d545e160d16c419b9bd89a0e669f4e96ff6d911533c429c40b4579e36da30028`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5b6d9a3660f75b1082b42b4709ccdb598108bde45307cac25ecd5af2952ac04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5045811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd2b1e8471612e72d5b5dc3eca30a28c8e897ee54c76e5a50b65a338833df9d`

```dockerfile
```

-	Layers:
	-	`sha256:0ead825d17a736595a8d68d8b4f5fb19197608e98aac03bde33c559f06b32458`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.0 MB (5030423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0191fe8c994c2f0011dcab52e3666bed38adfee3cf30ddceeabe5b1d33d42960`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a464e9f2748a1566df37a3724b95d1a1a69f290ac96447951671c83a550067ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd8b86639da4308fc12076a3bedc7fb62d2c24ed8bff5ef402ff017fbc7192c`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d66ce338e12d0a15108f0c8e9ac5fdf6b81805b726881f9b134314dc0a0fc88`  
		Last Modified: Tue, 04 Feb 2025 10:01:24 GMT  
		Size: 67.7 MB (67656005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e52051c8cda773cb8964f44dad5417e7108440620c3a93457479ae9da006b3d`  
		Last Modified: Tue, 04 Feb 2025 10:01:21 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:b80c2211d5e87359c11d33e807d152dc3e3d55c3de5e037bb291336eb458ea53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5052241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f68ad0d6548d4e85cd781b4e7ac854f89386f6f040d54740d464484df0473c`

```dockerfile
```

-	Layers:
	-	`sha256:3f4680d65fd004d89d874b5f6a4e56fa772ae1684e09ef9c4a4270d257d152c3`  
		Last Modified: Tue, 04 Feb 2025 10:01:22 GMT  
		Size: 5.0 MB (5036749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cf114dd44ca7714902a8167ed2224de969999df5c754e43272ac1f57826ada6`  
		Last Modified: Tue, 04 Feb 2025 10:01:21 GMT  
		Size: 15.5 KB (15492 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:bc465056a5ebb9730a3945a762937763b83862b493fc1101f11b3d0245711b54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:8fcdddfa7c76408e7db1c42978cf34072fe70ae44d525a7561b0d00ec7962926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117537008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed1b48bc9599ac703159cad79ebba285d8d837ac377fd2c3ad385d7ebc811e5`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da1c4a310b7fa45b63f773b07fd8455852aec7c32ff1a28859d6b69c11b654`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da5392f820339123f871f8286590b21d1e3ac1bacf68548fe6b914aeebb2d8`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 88.0 MB (87999780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e28b96f5953bcf3a025d470e244bf97a6495415c03feb4832fe386cfe6fa07`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:aca9e8f6e5123cbe148e25b12ccff8c7312b9555ad29c6723e324966a8e57803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839cce49ffee9e3b349a99d2d5e6a1dc3c4ec39fa3c94d96dc814f3a36643d53`

```dockerfile
```

-	Layers:
	-	`sha256:cad614db2d9a7739fa6ad1b608cd0f3c0de481ed4b65e686e02db6c3bbdfcf55`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.2 MB (5224266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9ccefc10a1d228dd7d7df6bf71b2191aab69994bae6fc027b8f5348429fc3a`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c1c14ae46476eab1ac3b752a3b8e891a2b2faa6fccdc15ff4cddbaeb4d2675cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114639854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe18cabec9721a3aba985e570e4f2f08c972b1427b10492559f875cd8f4cc60`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61180f349d073f0bc701a35b115815ea0083b56c1a6de0d1d19e2e7ff6397b5d`  
		Last Modified: Tue, 04 Feb 2025 10:00:31 GMT  
		Size: 87.3 MB (87280387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826f6d3aec7550f0bda7977bedbe3b20d5b462c81bfb3cbb6626c7cf6b002565`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:9b76ec7b10f14aff8d179ffc00a0b4b4bbbe37e2faeca4f20130ab171b3f5b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763f85f9c3a74c42b058dc05f7e130bd4f9c4ccce8ad70d9f9002408588dcd2e`

```dockerfile
```

-	Layers:
	-	`sha256:31006b90b386f27cda10edc832bb4245ded4b4800eef607c4280b8fa105c40fc`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 5.2 MB (5230592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d613ae7d2727578f13d07e6cfefefeeaeb7fe1681a49f6bc5ead2109f724eb`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:bc465056a5ebb9730a3945a762937763b83862b493fc1101f11b3d0245711b54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8fcdddfa7c76408e7db1c42978cf34072fe70ae44d525a7561b0d00ec7962926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117537008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed1b48bc9599ac703159cad79ebba285d8d837ac377fd2c3ad385d7ebc811e5`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da1c4a310b7fa45b63f773b07fd8455852aec7c32ff1a28859d6b69c11b654`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da5392f820339123f871f8286590b21d1e3ac1bacf68548fe6b914aeebb2d8`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 88.0 MB (87999780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e28b96f5953bcf3a025d470e244bf97a6495415c03feb4832fe386cfe6fa07`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:aca9e8f6e5123cbe148e25b12ccff8c7312b9555ad29c6723e324966a8e57803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839cce49ffee9e3b349a99d2d5e6a1dc3c4ec39fa3c94d96dc814f3a36643d53`

```dockerfile
```

-	Layers:
	-	`sha256:cad614db2d9a7739fa6ad1b608cd0f3c0de481ed4b65e686e02db6c3bbdfcf55`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.2 MB (5224266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9ccefc10a1d228dd7d7df6bf71b2191aab69994bae6fc027b8f5348429fc3a`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c1c14ae46476eab1ac3b752a3b8e891a2b2faa6fccdc15ff4cddbaeb4d2675cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114639854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe18cabec9721a3aba985e570e4f2f08c972b1427b10492559f875cd8f4cc60`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61180f349d073f0bc701a35b115815ea0083b56c1a6de0d1d19e2e7ff6397b5d`  
		Last Modified: Tue, 04 Feb 2025 10:00:31 GMT  
		Size: 87.3 MB (87280387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826f6d3aec7550f0bda7977bedbe3b20d5b462c81bfb3cbb6626c7cf6b002565`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9b76ec7b10f14aff8d179ffc00a0b4b4bbbe37e2faeca4f20130ab171b3f5b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763f85f9c3a74c42b058dc05f7e130bd4f9c4ccce8ad70d9f9002408588dcd2e`

```dockerfile
```

-	Layers:
	-	`sha256:31006b90b386f27cda10edc832bb4245ded4b4800eef607c4280b8fa105c40fc`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 5.2 MB (5230592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d613ae7d2727578f13d07e6cfefefeeaeb7fe1681a49f6bc5ead2109f724eb`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:bc465056a5ebb9730a3945a762937763b83862b493fc1101f11b3d0245711b54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:8fcdddfa7c76408e7db1c42978cf34072fe70ae44d525a7561b0d00ec7962926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117537008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed1b48bc9599ac703159cad79ebba285d8d837ac377fd2c3ad385d7ebc811e5`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da1c4a310b7fa45b63f773b07fd8455852aec7c32ff1a28859d6b69c11b654`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da5392f820339123f871f8286590b21d1e3ac1bacf68548fe6b914aeebb2d8`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 88.0 MB (87999780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e28b96f5953bcf3a025d470e244bf97a6495415c03feb4832fe386cfe6fa07`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:aca9e8f6e5123cbe148e25b12ccff8c7312b9555ad29c6723e324966a8e57803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839cce49ffee9e3b349a99d2d5e6a1dc3c4ec39fa3c94d96dc814f3a36643d53`

```dockerfile
```

-	Layers:
	-	`sha256:cad614db2d9a7739fa6ad1b608cd0f3c0de481ed4b65e686e02db6c3bbdfcf55`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.2 MB (5224266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9ccefc10a1d228dd7d7df6bf71b2191aab69994bae6fc027b8f5348429fc3a`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c1c14ae46476eab1ac3b752a3b8e891a2b2faa6fccdc15ff4cddbaeb4d2675cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114639854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe18cabec9721a3aba985e570e4f2f08c972b1427b10492559f875cd8f4cc60`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61180f349d073f0bc701a35b115815ea0083b56c1a6de0d1d19e2e7ff6397b5d`  
		Last Modified: Tue, 04 Feb 2025 10:00:31 GMT  
		Size: 87.3 MB (87280387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826f6d3aec7550f0bda7977bedbe3b20d5b462c81bfb3cbb6626c7cf6b002565`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:9b76ec7b10f14aff8d179ffc00a0b4b4bbbe37e2faeca4f20130ab171b3f5b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763f85f9c3a74c42b058dc05f7e130bd4f9c4ccce8ad70d9f9002408588dcd2e`

```dockerfile
```

-	Layers:
	-	`sha256:31006b90b386f27cda10edc832bb4245ded4b4800eef607c4280b8fa105c40fc`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 5.2 MB (5230592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d613ae7d2727578f13d07e6cfefefeeaeb7fe1681a49f6bc5ead2109f724eb`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:bc465056a5ebb9730a3945a762937763b83862b493fc1101f11b3d0245711b54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8fcdddfa7c76408e7db1c42978cf34072fe70ae44d525a7561b0d00ec7962926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117537008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed1b48bc9599ac703159cad79ebba285d8d837ac377fd2c3ad385d7ebc811e5`
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
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41da1c4a310b7fa45b63f773b07fd8455852aec7c32ff1a28859d6b69c11b654`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23da5392f820339123f871f8286590b21d1e3ac1bacf68548fe6b914aeebb2d8`  
		Last Modified: Tue, 04 Feb 2025 04:24:51 GMT  
		Size: 88.0 MB (87999780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e28b96f5953bcf3a025d470e244bf97a6495415c03feb4832fe386cfe6fa07`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:aca9e8f6e5123cbe148e25b12ccff8c7312b9555ad29c6723e324966a8e57803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5239654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839cce49ffee9e3b349a99d2d5e6a1dc3c4ec39fa3c94d96dc814f3a36643d53`

```dockerfile
```

-	Layers:
	-	`sha256:cad614db2d9a7739fa6ad1b608cd0f3c0de481ed4b65e686e02db6c3bbdfcf55`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 5.2 MB (5224266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9ccefc10a1d228dd7d7df6bf71b2191aab69994bae6fc027b8f5348429fc3a`  
		Last Modified: Tue, 04 Feb 2025 04:24:50 GMT  
		Size: 15.4 KB (15388 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c1c14ae46476eab1ac3b752a3b8e891a2b2faa6fccdc15ff4cddbaeb4d2675cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114639854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe18cabec9721a3aba985e570e4f2f08c972b1427b10492559f875cd8f4cc60`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc013a315fe52c9b7bcba67721595b018c5dcd4af632b8af5de2b2ee21f8fdc4`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61180f349d073f0bc701a35b115815ea0083b56c1a6de0d1d19e2e7ff6397b5d`  
		Last Modified: Tue, 04 Feb 2025 10:00:31 GMT  
		Size: 87.3 MB (87280387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826f6d3aec7550f0bda7977bedbe3b20d5b462c81bfb3cbb6626c7cf6b002565`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9b76ec7b10f14aff8d179ffc00a0b4b4bbbe37e2faeca4f20130ab171b3f5b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763f85f9c3a74c42b058dc05f7e130bd4f9c4ccce8ad70d9f9002408588dcd2e`

```dockerfile
```

-	Layers:
	-	`sha256:31006b90b386f27cda10edc832bb4245ded4b4800eef607c4280b8fa105c40fc`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 5.2 MB (5230592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d613ae7d2727578f13d07e6cfefefeeaeb7fe1681a49f6bc5ead2109f724eb`  
		Last Modified: Tue, 04 Feb 2025 10:00:28 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:04b662eec72ffc48190539a0829e026696ea04eda61ce90520b1074285e2e921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:028f43b4c09fd4a52fa7cacc2b36695863d76fdce727da4d8857bbcb02970d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd909108d5f7f769fefee23e29461020a1860fa87e0c6f414f5490f9a7d5aa0`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075643277a2b761d3c08c1c45d62f0f7d721eb11275364e41915c0167e603f1f`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b823bfcf332d5ca5eb55775ede00932b91a7f09690038b43dd708f8364b6e61`  
		Last Modified: Tue, 04 Feb 2025 04:24:40 GMT  
		Size: 93.0 MB (92983194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482488644e4650c1f07b4872c6f295c1cf063154d3b268e27a355a3aff34efa`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:996feca40b9b47939755a8c876a66fd0907f627b343dfb1c7c63e493e70f829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624776cd0890ed9e0edeb45ad243eb4ea6171c6989459765e56054b24ef09248`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c0784c80e23bdad6be3dbe9c7e0299665911692e268335bf11e31ea595507`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 5.3 MB (5291918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e19162236e8c066577ff22466bdb94d348e359945734ebc0a0ec5ef58fd4dd4`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b1b5d4553561125dd503e17c1b16876fc91fc988f8f34b4083ab3259cb91fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121163151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0e963987a10b02458821d680f6cdc4596754add641aac1a45e4d928bca1f3`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69974675d6d49cc7b689c346021aa57d7d8a833b1aafdc14483ed71b6b1e26`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105827f107035063431f24e8c473a1f00ae759d79eee5fd428eaf204cb94bf5b`  
		Last Modified: Tue, 04 Feb 2025 09:59:32 GMT  
		Size: 92.3 MB (92268266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e3660773e699436700d2a4377df6f191f3be81209966de40d506ab28e2db`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:5d72f79fe16c26234efc84680099249e1947b2f0f9a7d55b23a7325af3281641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02a7ffc35598a574642969ba8de27e956de9f221678fd7c6f52717176810bb`

```dockerfile
```

-	Layers:
	-	`sha256:10f78b687995432d2131937079f4b796e708f2b3d83cf1debdea83afd4a71723`  
		Last Modified: Tue, 04 Feb 2025 09:59:30 GMT  
		Size: 5.3 MB (5299085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d16181a078fd25315dcd17e3966bbc64dbc7c1b8f08fb87c44a18350856b66`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:04b662eec72ffc48190539a0829e026696ea04eda61ce90520b1074285e2e921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:028f43b4c09fd4a52fa7cacc2b36695863d76fdce727da4d8857bbcb02970d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd909108d5f7f769fefee23e29461020a1860fa87e0c6f414f5490f9a7d5aa0`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075643277a2b761d3c08c1c45d62f0f7d721eb11275364e41915c0167e603f1f`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b823bfcf332d5ca5eb55775ede00932b91a7f09690038b43dd708f8364b6e61`  
		Last Modified: Tue, 04 Feb 2025 04:24:40 GMT  
		Size: 93.0 MB (92983194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482488644e4650c1f07b4872c6f295c1cf063154d3b268e27a355a3aff34efa`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:996feca40b9b47939755a8c876a66fd0907f627b343dfb1c7c63e493e70f829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624776cd0890ed9e0edeb45ad243eb4ea6171c6989459765e56054b24ef09248`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c0784c80e23bdad6be3dbe9c7e0299665911692e268335bf11e31ea595507`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 5.3 MB (5291918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e19162236e8c066577ff22466bdb94d348e359945734ebc0a0ec5ef58fd4dd4`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b1b5d4553561125dd503e17c1b16876fc91fc988f8f34b4083ab3259cb91fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121163151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0e963987a10b02458821d680f6cdc4596754add641aac1a45e4d928bca1f3`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69974675d6d49cc7b689c346021aa57d7d8a833b1aafdc14483ed71b6b1e26`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105827f107035063431f24e8c473a1f00ae759d79eee5fd428eaf204cb94bf5b`  
		Last Modified: Tue, 04 Feb 2025 09:59:32 GMT  
		Size: 92.3 MB (92268266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e3660773e699436700d2a4377df6f191f3be81209966de40d506ab28e2db`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5d72f79fe16c26234efc84680099249e1947b2f0f9a7d55b23a7325af3281641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02a7ffc35598a574642969ba8de27e956de9f221678fd7c6f52717176810bb`

```dockerfile
```

-	Layers:
	-	`sha256:10f78b687995432d2131937079f4b796e708f2b3d83cf1debdea83afd4a71723`  
		Last Modified: Tue, 04 Feb 2025 09:59:30 GMT  
		Size: 5.3 MB (5299085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d16181a078fd25315dcd17e3966bbc64dbc7c1b8f08fb87c44a18350856b66`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.0`

```console
$ docker pull kong@sha256:04b662eec72ffc48190539a0829e026696ea04eda61ce90520b1074285e2e921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.0` - linux; amd64

```console
$ docker pull kong@sha256:028f43b4c09fd4a52fa7cacc2b36695863d76fdce727da4d8857bbcb02970d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd909108d5f7f769fefee23e29461020a1860fa87e0c6f414f5490f9a7d5aa0`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075643277a2b761d3c08c1c45d62f0f7d721eb11275364e41915c0167e603f1f`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b823bfcf332d5ca5eb55775ede00932b91a7f09690038b43dd708f8364b6e61`  
		Last Modified: Tue, 04 Feb 2025 04:24:40 GMT  
		Size: 93.0 MB (92983194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482488644e4650c1f07b4872c6f295c1cf063154d3b268e27a355a3aff34efa`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0` - unknown; unknown

```console
$ docker pull kong@sha256:996feca40b9b47939755a8c876a66fd0907f627b343dfb1c7c63e493e70f829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624776cd0890ed9e0edeb45ad243eb4ea6171c6989459765e56054b24ef09248`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c0784c80e23bdad6be3dbe9c7e0299665911692e268335bf11e31ea595507`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 5.3 MB (5291918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e19162236e8c066577ff22466bdb94d348e359945734ebc0a0ec5ef58fd4dd4`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b1b5d4553561125dd503e17c1b16876fc91fc988f8f34b4083ab3259cb91fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121163151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0e963987a10b02458821d680f6cdc4596754add641aac1a45e4d928bca1f3`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69974675d6d49cc7b689c346021aa57d7d8a833b1aafdc14483ed71b6b1e26`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105827f107035063431f24e8c473a1f00ae759d79eee5fd428eaf204cb94bf5b`  
		Last Modified: Tue, 04 Feb 2025 09:59:32 GMT  
		Size: 92.3 MB (92268266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e3660773e699436700d2a4377df6f191f3be81209966de40d506ab28e2db`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0` - unknown; unknown

```console
$ docker pull kong@sha256:5d72f79fe16c26234efc84680099249e1947b2f0f9a7d55b23a7325af3281641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02a7ffc35598a574642969ba8de27e956de9f221678fd7c6f52717176810bb`

```dockerfile
```

-	Layers:
	-	`sha256:10f78b687995432d2131937079f4b796e708f2b3d83cf1debdea83afd4a71723`  
		Last Modified: Tue, 04 Feb 2025 09:59:30 GMT  
		Size: 5.3 MB (5299085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d16181a078fd25315dcd17e3966bbc64dbc7c1b8f08fb87c44a18350856b66`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.0-ubuntu`

```console
$ docker pull kong@sha256:ae7305b2a81bcf14bf90f0369f4e336e8839db2ca361da455752719a244798af
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
$ docker pull kong@sha256:b1b5d4553561125dd503e17c1b16876fc91fc988f8f34b4083ab3259cb91fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121163151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0e963987a10b02458821d680f6cdc4596754add641aac1a45e4d928bca1f3`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69974675d6d49cc7b689c346021aa57d7d8a833b1aafdc14483ed71b6b1e26`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105827f107035063431f24e8c473a1f00ae759d79eee5fd428eaf204cb94bf5b`  
		Last Modified: Tue, 04 Feb 2025 09:59:32 GMT  
		Size: 92.3 MB (92268266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e3660773e699436700d2a4377df6f191f3be81209966de40d506ab28e2db`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5d72f79fe16c26234efc84680099249e1947b2f0f9a7d55b23a7325af3281641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02a7ffc35598a574642969ba8de27e956de9f221678fd7c6f52717176810bb`

```dockerfile
```

-	Layers:
	-	`sha256:10f78b687995432d2131937079f4b796e708f2b3d83cf1debdea83afd4a71723`  
		Last Modified: Tue, 04 Feb 2025 09:59:30 GMT  
		Size: 5.3 MB (5299085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d16181a078fd25315dcd17e3966bbc64dbc7c1b8f08fb87c44a18350856b66`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:04b662eec72ffc48190539a0829e026696ea04eda61ce90520b1074285e2e921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:028f43b4c09fd4a52fa7cacc2b36695863d76fdce727da4d8857bbcb02970d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd909108d5f7f769fefee23e29461020a1860fa87e0c6f414f5490f9a7d5aa0`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075643277a2b761d3c08c1c45d62f0f7d721eb11275364e41915c0167e603f1f`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b823bfcf332d5ca5eb55775ede00932b91a7f09690038b43dd708f8364b6e61`  
		Last Modified: Tue, 04 Feb 2025 04:24:40 GMT  
		Size: 93.0 MB (92983194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482488644e4650c1f07b4872c6f295c1cf063154d3b268e27a355a3aff34efa`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:996feca40b9b47939755a8c876a66fd0907f627b343dfb1c7c63e493e70f829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624776cd0890ed9e0edeb45ad243eb4ea6171c6989459765e56054b24ef09248`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c0784c80e23bdad6be3dbe9c7e0299665911692e268335bf11e31ea595507`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 5.3 MB (5291918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e19162236e8c066577ff22466bdb94d348e359945734ebc0a0ec5ef58fd4dd4`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b1b5d4553561125dd503e17c1b16876fc91fc988f8f34b4083ab3259cb91fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121163151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0e963987a10b02458821d680f6cdc4596754add641aac1a45e4d928bca1f3`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69974675d6d49cc7b689c346021aa57d7d8a833b1aafdc14483ed71b6b1e26`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105827f107035063431f24e8c473a1f00ae759d79eee5fd428eaf204cb94bf5b`  
		Last Modified: Tue, 04 Feb 2025 09:59:32 GMT  
		Size: 92.3 MB (92268266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e3660773e699436700d2a4377df6f191f3be81209966de40d506ab28e2db`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:5d72f79fe16c26234efc84680099249e1947b2f0f9a7d55b23a7325af3281641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02a7ffc35598a574642969ba8de27e956de9f221678fd7c6f52717176810bb`

```dockerfile
```

-	Layers:
	-	`sha256:10f78b687995432d2131937079f4b796e708f2b3d83cf1debdea83afd4a71723`  
		Last Modified: Tue, 04 Feb 2025 09:59:30 GMT  
		Size: 5.3 MB (5299085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d16181a078fd25315dcd17e3966bbc64dbc7c1b8f08fb87c44a18350856b66`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:04b662eec72ffc48190539a0829e026696ea04eda61ce90520b1074285e2e921
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:028f43b4c09fd4a52fa7cacc2b36695863d76fdce727da4d8857bbcb02970d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122738778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd909108d5f7f769fefee23e29461020a1860fa87e0c6f414f5490f9a7d5aa0`
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
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
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
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075643277a2b761d3c08c1c45d62f0f7d721eb11275364e41915c0167e603f1f`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b823bfcf332d5ca5eb55775ede00932b91a7f09690038b43dd708f8364b6e61`  
		Last Modified: Tue, 04 Feb 2025 04:24:40 GMT  
		Size: 93.0 MB (92983194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4482488644e4650c1f07b4872c6f295c1cf063154d3b268e27a355a3aff34efa`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:996feca40b9b47939755a8c876a66fd0907f627b343dfb1c7c63e493e70f829e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624776cd0890ed9e0edeb45ad243eb4ea6171c6989459765e56054b24ef09248`

```dockerfile
```

-	Layers:
	-	`sha256:9e4c0784c80e23bdad6be3dbe9c7e0299665911692e268335bf11e31ea595507`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 5.3 MB (5291918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e19162236e8c066577ff22466bdb94d348e359945734ebc0a0ec5ef58fd4dd4`  
		Last Modified: Tue, 04 Feb 2025 04:24:39 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b1b5d4553561125dd503e17c1b16876fc91fc988f8f34b4083ab3259cb91fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121163151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc0e963987a10b02458821d680f6cdc4596754add641aac1a45e4d928bca1f3`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69974675d6d49cc7b689c346021aa57d7d8a833b1aafdc14483ed71b6b1e26`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105827f107035063431f24e8c473a1f00ae759d79eee5fd428eaf204cb94bf5b`  
		Last Modified: Tue, 04 Feb 2025 09:59:32 GMT  
		Size: 92.3 MB (92268266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3062e3660773e699436700d2a4377df6f191f3be81209966de40d506ab28e2db`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5d72f79fe16c26234efc84680099249e1947b2f0f9a7d55b23a7325af3281641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b02a7ffc35598a574642969ba8de27e956de9f221678fd7c6f52717176810bb`

```dockerfile
```

-	Layers:
	-	`sha256:10f78b687995432d2131937079f4b796e708f2b3d83cf1debdea83afd4a71723`  
		Last Modified: Tue, 04 Feb 2025 09:59:30 GMT  
		Size: 5.3 MB (5299085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d16181a078fd25315dcd17e3966bbc64dbc7c1b8f08fb87c44a18350856b66`  
		Last Modified: Tue, 04 Feb 2025 09:59:29 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json
