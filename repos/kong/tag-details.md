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
$ docker pull kong@sha256:a9922cf145faab5fe1bba0401b4fd259433420adcf48a7d7ac5e1272a79dda49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:b80d732ec99671080cd8d9e04f6221597ec0a4d6d04fbcb388be129af5d40fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36529779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26eab18ae97e7cc0912eecb82c423f6dc6808c53ec7c8f51a7b64e31e62af60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cfeaf6c0377e57030ffcb875fdcd78128d6275a61f8a1760c90a960258f62`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d612756d8c09c88a3da6257448a41113165c7cee257cec51b92a52fd0f62df`  
		Last Modified: Tue, 12 Nov 2024 02:18:00 GMT  
		Size: 33.1 MB (33112365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c92156102c206cc52bc5777df2533d21b9242fb946dd5a9e7bd088b688356`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2` - unknown; unknown

```console
$ docker pull kong@sha256:52ebb86e96028a7cec296361e81f2eb471ac98add872ed4e1cb979d1506d14d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9948ad0c9452de06fd6603831d7cda92e2583f794d6ed77b55c9d1fd485914e`

```dockerfile
```

-	Layers:
	-	`sha256:e866c0b4a5a79b975bacc225dd19abff68892990f3e18dade10960f862a4bd7f`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 1.9 MB (1921147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360852558c7af12598460f785216d65e3fd8168810380ebfe6c0d2708307a394`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8`

```console
$ docker pull kong@sha256:a9922cf145faab5fe1bba0401b4fd259433420adcf48a7d7ac5e1272a79dda49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:b80d732ec99671080cd8d9e04f6221597ec0a4d6d04fbcb388be129af5d40fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36529779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26eab18ae97e7cc0912eecb82c423f6dc6808c53ec7c8f51a7b64e31e62af60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cfeaf6c0377e57030ffcb875fdcd78128d6275a61f8a1760c90a960258f62`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d612756d8c09c88a3da6257448a41113165c7cee257cec51b92a52fd0f62df`  
		Last Modified: Tue, 12 Nov 2024 02:18:00 GMT  
		Size: 33.1 MB (33112365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c92156102c206cc52bc5777df2533d21b9242fb946dd5a9e7bd088b688356`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8` - unknown; unknown

```console
$ docker pull kong@sha256:52ebb86e96028a7cec296361e81f2eb471ac98add872ed4e1cb979d1506d14d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9948ad0c9452de06fd6603831d7cda92e2583f794d6ed77b55c9d1fd485914e`

```dockerfile
```

-	Layers:
	-	`sha256:e866c0b4a5a79b975bacc225dd19abff68892990f3e18dade10960f862a4bd7f`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 1.9 MB (1921147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360852558c7af12598460f785216d65e3fd8168810380ebfe6c0d2708307a394`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8-alpine`

```console
$ docker pull kong@sha256:a9922cf145faab5fe1bba0401b4fd259433420adcf48a7d7ac5e1272a79dda49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-alpine` - linux; amd64

```console
$ docker pull kong@sha256:b80d732ec99671080cd8d9e04f6221597ec0a4d6d04fbcb388be129af5d40fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36529779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26eab18ae97e7cc0912eecb82c423f6dc6808c53ec7c8f51a7b64e31e62af60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cfeaf6c0377e57030ffcb875fdcd78128d6275a61f8a1760c90a960258f62`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d612756d8c09c88a3da6257448a41113165c7cee257cec51b92a52fd0f62df`  
		Last Modified: Tue, 12 Nov 2024 02:18:00 GMT  
		Size: 33.1 MB (33112365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c92156102c206cc52bc5777df2533d21b9242fb946dd5a9e7bd088b688356`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-alpine` - unknown; unknown

```console
$ docker pull kong@sha256:52ebb86e96028a7cec296361e81f2eb471ac98add872ed4e1cb979d1506d14d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9948ad0c9452de06fd6603831d7cda92e2583f794d6ed77b55c9d1fd485914e`

```dockerfile
```

-	Layers:
	-	`sha256:e866c0b4a5a79b975bacc225dd19abff68892990f3e18dade10960f862a4bd7f`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 1.9 MB (1921147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360852558c7af12598460f785216d65e3fd8168810380ebfe6c0d2708307a394`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:0a963c0efc93e87893ba327addb67b07bb56d6a033d8286a0df6d3c3d9141f1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:72ca404b9ba0a8ce41d9ecd5b08fd9dc051fce353054163214444080f6912816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185216409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d545da5f0f64ca5b92197aacd76e30f85ca07f666cccdd99b06a7055ea6b362c`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a063bf11eab36bb71804044e9ac359f2fcea0a9c352ef5744b4783ed2939776d`  
		Last Modified: Tue, 17 Sep 2024 00:59:21 GMT  
		Size: 25.1 MB (25081958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48ba90245998d3ef0afbfba3eafd2a820612d9ab526d0d082f71e6aaef87680`  
		Last Modified: Tue, 17 Sep 2024 00:59:23 GMT  
		Size: 130.6 MB (130597882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4a5b4d43c6f008b61c760d4ac426bc77e78038673b89a10912091e00f67f98`  
		Last Modified: Tue, 17 Sep 2024 00:59:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e739926fbef2090e332d277399a1ff68df527f3237a5be44950d9b57ab4b8ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7124160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0651e1f1ce49a2869e7679d6db92e7c601aad09330bc891093b5ba99d54f5e3d`

```dockerfile
```

-	Layers:
	-	`sha256:dbb94002d2e06c36d53a36fa72662750d6dfa70a01fe695ae417ca1e5de0b65a`  
		Last Modified: Tue, 17 Sep 2024 00:59:22 GMT  
		Size: 7.1 MB (7109928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19575f5bf8ee3d36d0bdb6ef67338c060c3e6a7dec7419cc22b01dc6ca28551d`  
		Last Modified: Tue, 17 Sep 2024 00:59:21 GMT  
		Size: 14.2 KB (14232 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5`

```console
$ docker pull kong@sha256:a9922cf145faab5fe1bba0401b4fd259433420adcf48a7d7ac5e1272a79dda49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5` - linux; amd64

```console
$ docker pull kong@sha256:b80d732ec99671080cd8d9e04f6221597ec0a4d6d04fbcb388be129af5d40fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36529779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26eab18ae97e7cc0912eecb82c423f6dc6808c53ec7c8f51a7b64e31e62af60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cfeaf6c0377e57030ffcb875fdcd78128d6275a61f8a1760c90a960258f62`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d612756d8c09c88a3da6257448a41113165c7cee257cec51b92a52fd0f62df`  
		Last Modified: Tue, 12 Nov 2024 02:18:00 GMT  
		Size: 33.1 MB (33112365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c92156102c206cc52bc5777df2533d21b9242fb946dd5a9e7bd088b688356`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5` - unknown; unknown

```console
$ docker pull kong@sha256:52ebb86e96028a7cec296361e81f2eb471ac98add872ed4e1cb979d1506d14d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9948ad0c9452de06fd6603831d7cda92e2583f794d6ed77b55c9d1fd485914e`

```dockerfile
```

-	Layers:
	-	`sha256:e866c0b4a5a79b975bacc225dd19abff68892990f3e18dade10960f862a4bd7f`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 1.9 MB (1921147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360852558c7af12598460f785216d65e3fd8168810380ebfe6c0d2708307a394`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-alpine`

```console
$ docker pull kong@sha256:a9922cf145faab5fe1bba0401b4fd259433420adcf48a7d7ac5e1272a79dda49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-alpine` - linux; amd64

```console
$ docker pull kong@sha256:b80d732ec99671080cd8d9e04f6221597ec0a4d6d04fbcb388be129af5d40fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36529779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26eab18ae97e7cc0912eecb82c423f6dc6808c53ec7c8f51a7b64e31e62af60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350cfeaf6c0377e57030ffcb875fdcd78128d6275a61f8a1760c90a960258f62`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d612756d8c09c88a3da6257448a41113165c7cee257cec51b92a52fd0f62df`  
		Last Modified: Tue, 12 Nov 2024 02:18:00 GMT  
		Size: 33.1 MB (33112365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c92156102c206cc52bc5777df2533d21b9242fb946dd5a9e7bd088b688356`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 880.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-alpine` - unknown; unknown

```console
$ docker pull kong@sha256:52ebb86e96028a7cec296361e81f2eb471ac98add872ed4e1cb979d1506d14d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1935361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9948ad0c9452de06fd6603831d7cda92e2583f794d6ed77b55c9d1fd485914e`

```dockerfile
```

-	Layers:
	-	`sha256:e866c0b4a5a79b975bacc225dd19abff68892990f3e18dade10960f862a4bd7f`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 1.9 MB (1921147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360852558c7af12598460f785216d65e3fd8168810380ebfe6c0d2708307a394`  
		Last Modified: Tue, 12 Nov 2024 02:17:59 GMT  
		Size: 14.2 KB (14214 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:0a963c0efc93e87893ba327addb67b07bb56d6a033d8286a0df6d3c3d9141f1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:72ca404b9ba0a8ce41d9ecd5b08fd9dc051fce353054163214444080f6912816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185216409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d545da5f0f64ca5b92197aacd76e30f85ca07f666cccdd99b06a7055ea6b362c`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a063bf11eab36bb71804044e9ac359f2fcea0a9c352ef5744b4783ed2939776d`  
		Last Modified: Tue, 17 Sep 2024 00:59:21 GMT  
		Size: 25.1 MB (25081958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48ba90245998d3ef0afbfba3eafd2a820612d9ab526d0d082f71e6aaef87680`  
		Last Modified: Tue, 17 Sep 2024 00:59:23 GMT  
		Size: 130.6 MB (130597882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4a5b4d43c6f008b61c760d4ac426bc77e78038673b89a10912091e00f67f98`  
		Last Modified: Tue, 17 Sep 2024 00:59:21 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e739926fbef2090e332d277399a1ff68df527f3237a5be44950d9b57ab4b8ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7124160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0651e1f1ce49a2869e7679d6db92e7c601aad09330bc891093b5ba99d54f5e3d`

```dockerfile
```

-	Layers:
	-	`sha256:dbb94002d2e06c36d53a36fa72662750d6dfa70a01fe695ae417ca1e5de0b65a`  
		Last Modified: Tue, 17 Sep 2024 00:59:22 GMT  
		Size: 7.1 MB (7109928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19575f5bf8ee3d36d0bdb6ef67338c060c3e6a7dec7419cc22b01dc6ca28551d`  
		Last Modified: Tue, 17 Sep 2024 00:59:21 GMT  
		Size: 14.2 KB (14232 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:616b2ab5a4c7b6c14022e8a1495ff34930ced76f25f3d418e76758717fec335f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:06b3649c4042b55d108b9c8c81d8a2c64d9dae4f7c38d70d259b13491057b532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7ae7008ea25ffba6803d5b7a98ef953ae6a8b1ebdb86e1d19925383e204ff7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f4cf5b05541c564470dd9c31a7e069849fe848969e0c72fd0657b1b7023e8`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0183922cc67aa6ce647c5310fa77fa3173aab6526e09a61e3bbbd08622be182c`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 88.0 MB (87985692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175c32a1e68fba6caa9437a6a4c1c0130d167f491c6efeb582ae6b8bd601beb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:c8a2b3627a6d88cc74af3261c942d29dbfb003ff8f44829124ac9e3ad4040e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43fe51359c2a239d9e304afa52b97bd9c7d5743758cbe92258a7792d3c5257`

```dockerfile
```

-	Layers:
	-	`sha256:88ab2fbad70a567af0795094b4ac81186dacff845957f5d7b7b494cb3c6659a1`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 3.1 KB (3103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113141d1145c121da26cb1fa8f9d8710810dcdd1342c244f15540551b94207ae`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e1bcfd118241be8875a4412e28e6145c23451226c575ab9c7b329533214f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81cf7b05f70576eff155ee2611ebf287bd1b75bd1b5eb4999e6ba406b7d65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b35d5aac6da9ddec8a4f7853b45ab07c6248faaed3f6ef9451521393925963e`  
		Last Modified: Tue, 17 Sep 2024 02:19:00 GMT  
		Size: 87.3 MB (87268634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605e2e738b1db6eed7febb8b0207fed07e84735407b538f80e76957263d4b17`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:69626ecd1cf471d17e8034ad1cd9a145fa31ab80bbe97a5079caef58bb4ec50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c0249e28b8ef13e22d961b1bea53d4fa73aa5108612ecd7b1ccea2128ae384`

```dockerfile
```

-	Layers:
	-	`sha256:276d6979b92c2d6471950fb9e7261ed079d21598b5aec398095675d8da5cd25b`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 5.2 MB (5216658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d503c6dda6a2b36a5b99f7170e43d9a1740cec1b195b5401721a39effd009`  
		Last Modified: Tue, 17 Sep 2024 02:18:57 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:245fc131ba9dee73e4ceb1b152ede53c96d8b58200ea26a9f7bf614a9f81fa9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:2ada2c3e7e05b3bb3fe821e552f31c844b2aa6f75c0122b8a0c7f8da38676a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92254818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176aa50808b82fb13a1650b28f0b653b12df11d8a4c227c23432facc02baf5e6`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e2fd999df51906cdccfcedaf920e01f7608269a9277373b2c1aaaf00114077`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242be8294227195d2167c8972b2bff01103e09928107390a33373006a31d18a2`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 62.7 MB (62717846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1572abe74a5b278158243ab24efbebbd158a63ce0eb676dbf5d254bbe44073e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:61c9880c7801e7a4a65b1e34f7ad2aa547cdd0bde2b02df13a4a3020e7d8e8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76811f3411a069471c4496d00ee77b8296dbeac2fda45aae43105874421ca19`

```dockerfile
```

-	Layers:
	-	`sha256:9a1db11ec6ad2ab12dfca7ff74e15b587daae7ada7eb6c5d33d4b9502a29a604`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 5.9 MB (5906050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501cb57c9b669ad4f9d09575f7859c9e055c196d08a2f538b7f5a37552a37f00`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:404a41ffcb0eda58503c7d726ed758c95d9ab2b9c07144b6f5d4bb2fb8850753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88503012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d23275e367ac7acf455f0e668d2a6fb74f79581f2fde2a6aab81f1461ca6a8`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242197bb3e31cdb9f704a298844171f4096c60f4d12bf9eefa9136941de6b90`  
		Last Modified: Tue, 17 Sep 2024 02:22:28 GMT  
		Size: 61.1 MB (61143400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c216536ccfcb172c60fa3ca8b5151596a90b038c780c100c4fbe6886458d31b1`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:f0894fdcfc66e799b656a6ed4e49521ba15fdf5559b40e95b17682113519dca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc61aab5f3772bd9d6bbe869ffc205cbd376f05923f65852d10517a5611bdff`

```dockerfile
```

-	Layers:
	-	`sha256:2ab7f1c87fa98a442a6f8a186bad8a649713fc8e62a007894037a0f2c2dc4942`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 5.9 MB (5884099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5036d6def21f22217c2ffd1632681dc8b281a97adffe40cf0a901ca090a420fa`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:245fc131ba9dee73e4ceb1b152ede53c96d8b58200ea26a9f7bf614a9f81fa9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2ada2c3e7e05b3bb3fe821e552f31c844b2aa6f75c0122b8a0c7f8da38676a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92254818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176aa50808b82fb13a1650b28f0b653b12df11d8a4c227c23432facc02baf5e6`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e2fd999df51906cdccfcedaf920e01f7608269a9277373b2c1aaaf00114077`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242be8294227195d2167c8972b2bff01103e09928107390a33373006a31d18a2`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 62.7 MB (62717846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1572abe74a5b278158243ab24efbebbd158a63ce0eb676dbf5d254bbe44073e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:61c9880c7801e7a4a65b1e34f7ad2aa547cdd0bde2b02df13a4a3020e7d8e8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76811f3411a069471c4496d00ee77b8296dbeac2fda45aae43105874421ca19`

```dockerfile
```

-	Layers:
	-	`sha256:9a1db11ec6ad2ab12dfca7ff74e15b587daae7ada7eb6c5d33d4b9502a29a604`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 5.9 MB (5906050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501cb57c9b669ad4f9d09575f7859c9e055c196d08a2f538b7f5a37552a37f00`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:404a41ffcb0eda58503c7d726ed758c95d9ab2b9c07144b6f5d4bb2fb8850753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88503012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d23275e367ac7acf455f0e668d2a6fb74f79581f2fde2a6aab81f1461ca6a8`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242197bb3e31cdb9f704a298844171f4096c60f4d12bf9eefa9136941de6b90`  
		Last Modified: Tue, 17 Sep 2024 02:22:28 GMT  
		Size: 61.1 MB (61143400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c216536ccfcb172c60fa3ca8b5151596a90b038c780c100c4fbe6886458d31b1`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f0894fdcfc66e799b656a6ed4e49521ba15fdf5559b40e95b17682113519dca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc61aab5f3772bd9d6bbe869ffc205cbd376f05923f65852d10517a5611bdff`

```dockerfile
```

-	Layers:
	-	`sha256:2ab7f1c87fa98a442a6f8a186bad8a649713fc8e62a007894037a0f2c2dc4942`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 5.9 MB (5884099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5036d6def21f22217c2ffd1632681dc8b281a97adffe40cf0a901ca090a420fa`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:245fc131ba9dee73e4ceb1b152ede53c96d8b58200ea26a9f7bf614a9f81fa9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:2ada2c3e7e05b3bb3fe821e552f31c844b2aa6f75c0122b8a0c7f8da38676a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92254818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176aa50808b82fb13a1650b28f0b653b12df11d8a4c227c23432facc02baf5e6`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e2fd999df51906cdccfcedaf920e01f7608269a9277373b2c1aaaf00114077`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242be8294227195d2167c8972b2bff01103e09928107390a33373006a31d18a2`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 62.7 MB (62717846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1572abe74a5b278158243ab24efbebbd158a63ce0eb676dbf5d254bbe44073e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:61c9880c7801e7a4a65b1e34f7ad2aa547cdd0bde2b02df13a4a3020e7d8e8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76811f3411a069471c4496d00ee77b8296dbeac2fda45aae43105874421ca19`

```dockerfile
```

-	Layers:
	-	`sha256:9a1db11ec6ad2ab12dfca7ff74e15b587daae7ada7eb6c5d33d4b9502a29a604`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 5.9 MB (5906050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501cb57c9b669ad4f9d09575f7859c9e055c196d08a2f538b7f5a37552a37f00`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:404a41ffcb0eda58503c7d726ed758c95d9ab2b9c07144b6f5d4bb2fb8850753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88503012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d23275e367ac7acf455f0e668d2a6fb74f79581f2fde2a6aab81f1461ca6a8`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242197bb3e31cdb9f704a298844171f4096c60f4d12bf9eefa9136941de6b90`  
		Last Modified: Tue, 17 Sep 2024 02:22:28 GMT  
		Size: 61.1 MB (61143400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c216536ccfcb172c60fa3ca8b5151596a90b038c780c100c4fbe6886458d31b1`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:f0894fdcfc66e799b656a6ed4e49521ba15fdf5559b40e95b17682113519dca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc61aab5f3772bd9d6bbe869ffc205cbd376f05923f65852d10517a5611bdff`

```dockerfile
```

-	Layers:
	-	`sha256:2ab7f1c87fa98a442a6f8a186bad8a649713fc8e62a007894037a0f2c2dc4942`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 5.9 MB (5884099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5036d6def21f22217c2ffd1632681dc8b281a97adffe40cf0a901ca090a420fa`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:245fc131ba9dee73e4ceb1b152ede53c96d8b58200ea26a9f7bf614a9f81fa9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2ada2c3e7e05b3bb3fe821e552f31c844b2aa6f75c0122b8a0c7f8da38676a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92254818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176aa50808b82fb13a1650b28f0b653b12df11d8a4c227c23432facc02baf5e6`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e2fd999df51906cdccfcedaf920e01f7608269a9277373b2c1aaaf00114077`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242be8294227195d2167c8972b2bff01103e09928107390a33373006a31d18a2`  
		Last Modified: Tue, 17 Sep 2024 00:59:06 GMT  
		Size: 62.7 MB (62717846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1572abe74a5b278158243ab24efbebbd158a63ce0eb676dbf5d254bbe44073e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:61c9880c7801e7a4a65b1e34f7ad2aa547cdd0bde2b02df13a4a3020e7d8e8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5921185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76811f3411a069471c4496d00ee77b8296dbeac2fda45aae43105874421ca19`

```dockerfile
```

-	Layers:
	-	`sha256:9a1db11ec6ad2ab12dfca7ff74e15b587daae7ada7eb6c5d33d4b9502a29a604`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 5.9 MB (5906050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:501cb57c9b669ad4f9d09575f7859c9e055c196d08a2f538b7f5a37552a37f00`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:404a41ffcb0eda58503c7d726ed758c95d9ab2b9c07144b6f5d4bb2fb8850753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88503012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d23275e367ac7acf455f0e668d2a6fb74f79581f2fde2a6aab81f1461ca6a8`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242197bb3e31cdb9f704a298844171f4096c60f4d12bf9eefa9136941de6b90`  
		Last Modified: Tue, 17 Sep 2024 02:22:28 GMT  
		Size: 61.1 MB (61143400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c216536ccfcb172c60fa3ca8b5151596a90b038c780c100c4fbe6886458d31b1`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f0894fdcfc66e799b656a6ed4e49521ba15fdf5559b40e95b17682113519dca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5899535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc61aab5f3772bd9d6bbe869ffc205cbd376f05923f65852d10517a5611bdff`

```dockerfile
```

-	Layers:
	-	`sha256:2ab7f1c87fa98a442a6f8a186bad8a649713fc8e62a007894037a0f2c2dc4942`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 5.9 MB (5884099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5036d6def21f22217c2ffd1632681dc8b281a97adffe40cf0a901ca090a420fa`  
		Last Modified: Tue, 17 Sep 2024 02:22:26 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6`

```console
$ docker pull kong@sha256:0a5b9a7673a4375ac8789b01a81c18c970d0efb010ec510b72c752b9e7f05741
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6` - linux; amd64

```console
$ docker pull kong@sha256:55099b9d23395ee1db31af370b990ec77ad5e156f1bb2e5a7bc6ad484b96151f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97206081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e99fd0ebd1ea323a398ec0536c4b8d1e1f3fa9693a72952a45f3f541001a3f5`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b517eafcefa5bb3670bd51e2df70b303ba30cd18af6eca36fd8e1e5b47bb239`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572087cef64d645584167504a298708d2697afb3a904274dec3e519e2a6c5ad`  
		Last Modified: Tue, 17 Sep 2024 00:59:17 GMT  
		Size: 67.7 MB (67669108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b9899da84a06b40219d7cf62ab1fc4fde8fe57ba14fe238aa6c52eb30e7d76`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:52b300b46fbb3eeee8b91046ca7f7096ab73a2257fb12d71f169e2f467126720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4951802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c19d1dbb60e3edf6763fedbcb9ed09e1700a9982f680929af4d1f5fd36f4c5`

```dockerfile
```

-	Layers:
	-	`sha256:98bafad402c311f80e6215f3e994a41ceec3dc435787227a82bbd6d85b82faa7`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 4.9 MB (4936668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d687c7f45e06f1025b83603cac88f7d7e8a93a217891bde1426760bece1711`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9817ec9e0746ae1d32a073eb4651bf8d1a14d8dc91eb1d13ef9ae11f2cd41222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94582679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fad5e1ecdc5566ecbcb94240b6f163cce2c0252f5314c50f71aee0c0dd4c6`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71772e2bb265f5e1a65dc6d01e0eaf8405b5cb1521ecaac2113a6a6b6cc6571`  
		Last Modified: Tue, 17 Sep 2024 02:20:48 GMT  
		Size: 67.2 MB (67223068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9242abbe5e7681afe369ebafa22feb5e4066c1aab9fe8c55af12e845c058e4c`  
		Last Modified: Tue, 17 Sep 2024 02:20:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:c38e237fa13e444881b8181b8d72e6c4c925066d5238ed171bc3fb5430655f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4958436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4a7ecdc2a3f0d1763c076ebd7231ab8f63f3890354f2cb723b497577e599be`

```dockerfile
```

-	Layers:
	-	`sha256:1f539ed35a87a6a15633c9ff340a7d511d500013af25d4266687492d783a9bad`  
		Last Modified: Tue, 17 Sep 2024 02:20:47 GMT  
		Size: 4.9 MB (4943000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630d9f4288f8b325bddf123eddee819bbca763da3e9424fa6e44d124a7eb45f5`  
		Last Modified: Tue, 17 Sep 2024 02:20:46 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:0a5b9a7673a4375ac8789b01a81c18c970d0efb010ec510b72c752b9e7f05741
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:55099b9d23395ee1db31af370b990ec77ad5e156f1bb2e5a7bc6ad484b96151f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97206081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e99fd0ebd1ea323a398ec0536c4b8d1e1f3fa9693a72952a45f3f541001a3f5`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b517eafcefa5bb3670bd51e2df70b303ba30cd18af6eca36fd8e1e5b47bb239`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572087cef64d645584167504a298708d2697afb3a904274dec3e519e2a6c5ad`  
		Last Modified: Tue, 17 Sep 2024 00:59:17 GMT  
		Size: 67.7 MB (67669108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b9899da84a06b40219d7cf62ab1fc4fde8fe57ba14fe238aa6c52eb30e7d76`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:52b300b46fbb3eeee8b91046ca7f7096ab73a2257fb12d71f169e2f467126720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4951802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c19d1dbb60e3edf6763fedbcb9ed09e1700a9982f680929af4d1f5fd36f4c5`

```dockerfile
```

-	Layers:
	-	`sha256:98bafad402c311f80e6215f3e994a41ceec3dc435787227a82bbd6d85b82faa7`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 4.9 MB (4936668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d687c7f45e06f1025b83603cac88f7d7e8a93a217891bde1426760bece1711`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9817ec9e0746ae1d32a073eb4651bf8d1a14d8dc91eb1d13ef9ae11f2cd41222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94582679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fad5e1ecdc5566ecbcb94240b6f163cce2c0252f5314c50f71aee0c0dd4c6`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71772e2bb265f5e1a65dc6d01e0eaf8405b5cb1521ecaac2113a6a6b6cc6571`  
		Last Modified: Tue, 17 Sep 2024 02:20:48 GMT  
		Size: 67.2 MB (67223068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9242abbe5e7681afe369ebafa22feb5e4066c1aab9fe8c55af12e845c058e4c`  
		Last Modified: Tue, 17 Sep 2024 02:20:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c38e237fa13e444881b8181b8d72e6c4c925066d5238ed171bc3fb5430655f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4958436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4a7ecdc2a3f0d1763c076ebd7231ab8f63f3890354f2cb723b497577e599be`

```dockerfile
```

-	Layers:
	-	`sha256:1f539ed35a87a6a15633c9ff340a7d511d500013af25d4266687492d783a9bad`  
		Last Modified: Tue, 17 Sep 2024 02:20:47 GMT  
		Size: 4.9 MB (4943000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630d9f4288f8b325bddf123eddee819bbca763da3e9424fa6e44d124a7eb45f5`  
		Last Modified: Tue, 17 Sep 2024 02:20:46 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6.1`

```console
$ docker pull kong@sha256:0a5b9a7673a4375ac8789b01a81c18c970d0efb010ec510b72c752b9e7f05741
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1` - linux; amd64

```console
$ docker pull kong@sha256:55099b9d23395ee1db31af370b990ec77ad5e156f1bb2e5a7bc6ad484b96151f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97206081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e99fd0ebd1ea323a398ec0536c4b8d1e1f3fa9693a72952a45f3f541001a3f5`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b517eafcefa5bb3670bd51e2df70b303ba30cd18af6eca36fd8e1e5b47bb239`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572087cef64d645584167504a298708d2697afb3a904274dec3e519e2a6c5ad`  
		Last Modified: Tue, 17 Sep 2024 00:59:17 GMT  
		Size: 67.7 MB (67669108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b9899da84a06b40219d7cf62ab1fc4fde8fe57ba14fe238aa6c52eb30e7d76`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:52b300b46fbb3eeee8b91046ca7f7096ab73a2257fb12d71f169e2f467126720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4951802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c19d1dbb60e3edf6763fedbcb9ed09e1700a9982f680929af4d1f5fd36f4c5`

```dockerfile
```

-	Layers:
	-	`sha256:98bafad402c311f80e6215f3e994a41ceec3dc435787227a82bbd6d85b82faa7`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 4.9 MB (4936668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d687c7f45e06f1025b83603cac88f7d7e8a93a217891bde1426760bece1711`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9817ec9e0746ae1d32a073eb4651bf8d1a14d8dc91eb1d13ef9ae11f2cd41222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94582679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fad5e1ecdc5566ecbcb94240b6f163cce2c0252f5314c50f71aee0c0dd4c6`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71772e2bb265f5e1a65dc6d01e0eaf8405b5cb1521ecaac2113a6a6b6cc6571`  
		Last Modified: Tue, 17 Sep 2024 02:20:48 GMT  
		Size: 67.2 MB (67223068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9242abbe5e7681afe369ebafa22feb5e4066c1aab9fe8c55af12e845c058e4c`  
		Last Modified: Tue, 17 Sep 2024 02:20:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:c38e237fa13e444881b8181b8d72e6c4c925066d5238ed171bc3fb5430655f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4958436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4a7ecdc2a3f0d1763c076ebd7231ab8f63f3890354f2cb723b497577e599be`

```dockerfile
```

-	Layers:
	-	`sha256:1f539ed35a87a6a15633c9ff340a7d511d500013af25d4266687492d783a9bad`  
		Last Modified: Tue, 17 Sep 2024 02:20:47 GMT  
		Size: 4.9 MB (4943000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630d9f4288f8b325bddf123eddee819bbca763da3e9424fa6e44d124a7eb45f5`  
		Last Modified: Tue, 17 Sep 2024 02:20:46 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:0a5b9a7673a4375ac8789b01a81c18c970d0efb010ec510b72c752b9e7f05741
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:55099b9d23395ee1db31af370b990ec77ad5e156f1bb2e5a7bc6ad484b96151f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97206081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e99fd0ebd1ea323a398ec0536c4b8d1e1f3fa9693a72952a45f3f541001a3f5`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b517eafcefa5bb3670bd51e2df70b303ba30cd18af6eca36fd8e1e5b47bb239`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572087cef64d645584167504a298708d2697afb3a904274dec3e519e2a6c5ad`  
		Last Modified: Tue, 17 Sep 2024 00:59:17 GMT  
		Size: 67.7 MB (67669108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b9899da84a06b40219d7cf62ab1fc4fde8fe57ba14fe238aa6c52eb30e7d76`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:52b300b46fbb3eeee8b91046ca7f7096ab73a2257fb12d71f169e2f467126720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4951802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c19d1dbb60e3edf6763fedbcb9ed09e1700a9982f680929af4d1f5fd36f4c5`

```dockerfile
```

-	Layers:
	-	`sha256:98bafad402c311f80e6215f3e994a41ceec3dc435787227a82bbd6d85b82faa7`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 4.9 MB (4936668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d687c7f45e06f1025b83603cac88f7d7e8a93a217891bde1426760bece1711`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9817ec9e0746ae1d32a073eb4651bf8d1a14d8dc91eb1d13ef9ae11f2cd41222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94582679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0fad5e1ecdc5566ecbcb94240b6f163cce2c0252f5314c50f71aee0c0dd4c6`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71772e2bb265f5e1a65dc6d01e0eaf8405b5cb1521ecaac2113a6a6b6cc6571`  
		Last Modified: Tue, 17 Sep 2024 02:20:48 GMT  
		Size: 67.2 MB (67223068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9242abbe5e7681afe369ebafa22feb5e4066c1aab9fe8c55af12e845c058e4c`  
		Last Modified: Tue, 17 Sep 2024 02:20:46 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c38e237fa13e444881b8181b8d72e6c4c925066d5238ed171bc3fb5430655f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4958436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4a7ecdc2a3f0d1763c076ebd7231ab8f63f3890354f2cb723b497577e599be`

```dockerfile
```

-	Layers:
	-	`sha256:1f539ed35a87a6a15633c9ff340a7d511d500013af25d4266687492d783a9bad`  
		Last Modified: Tue, 17 Sep 2024 02:20:47 GMT  
		Size: 4.9 MB (4943000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630d9f4288f8b325bddf123eddee819bbca763da3e9424fa6e44d124a7eb45f5`  
		Last Modified: Tue, 17 Sep 2024 02:20:46 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7`

```console
$ docker pull kong@sha256:4f011c1f306eb6f3be999e903cc170b94bce6f4ecc66cb0a1d7b89d237d16c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7` - linux; amd64

```console
$ docker pull kong@sha256:0d08c2b349a66f9e159c1ab8bf9ba67f6d98cd18ea71a7ed98d017ba13e5e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084144a5b676aa9cf65920665641166b1452b8762d416f39488e5a8112e8684d`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a156af603f3a03b081a983c7e973e8a1736084868614fb76f7e7a581b49758`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e032d2b24653f4c22de4d915dce3406c6aa1980e06780bd87a402da054e37094`  
		Last Modified: Tue, 17 Sep 2024 00:59:15 GMT  
		Size: 67.7 MB (67708615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1572abe74a5b278158243ab24efbebbd158a63ce0eb676dbf5d254bbe44073e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:d6f1c1dd3349bb7687a7584b9f375f52a163b1cf560e0fb6f758f6f427c541cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86ffdd56b6fc6b43522b1fd48ae936505cac4f715f133821587bd2fde90e8f2`

```dockerfile
```

-	Layers:
	-	`sha256:f744f247366e6c390395d191add41453b0704f7c8a8f05e3dddbcd19634f79bb`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 5.0 MB (5015252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee05fe939486cb664b9c09428d563b15815c10d4f9665c5c54913225803288d`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:693d41e97969a3b09bdc72841f4abe4b9d8966cda18f1f5fc819eeadc0356348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95006558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdd67b469ec36f7a6d61e8d1286337fdd059342785ba793c555bd6a19554700`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a11b74d0eb46a4c9c7e7568b215c46625d3581bada3826ffcbac7e41946e96`  
		Last Modified: Tue, 17 Sep 2024 02:19:59 GMT  
		Size: 67.6 MB (67646946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b641deca7a61ba77a09e62061b7b4ffddf0549958445c4670531101516c5e82`  
		Last Modified: Tue, 17 Sep 2024 02:19:56 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:84fdeede9e71fb976f918cc6e6a366abbeeb0ed0ba9289c2fcc7e3ea39756259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf6647df0a1b6ce7d41a730a93117bdd1b6eb4445a74e6f53499cf8ebda6971`

```dockerfile
```

-	Layers:
	-	`sha256:6c301b4f52a71e1f5dc9d40dd4ac5d9aa4cad3a6c7334ca665941b8fa1252cc1`  
		Last Modified: Tue, 17 Sep 2024 02:19:57 GMT  
		Size: 5.0 MB (5021584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497bb535bed0dbb14dfb43e86b1632b8b90b0b2de13b666a07bc9893af97db15`  
		Last Modified: Tue, 17 Sep 2024 02:19:57 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7-ubuntu`

```console
$ docker pull kong@sha256:4f011c1f306eb6f3be999e903cc170b94bce6f4ecc66cb0a1d7b89d237d16c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:0d08c2b349a66f9e159c1ab8bf9ba67f6d98cd18ea71a7ed98d017ba13e5e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084144a5b676aa9cf65920665641166b1452b8762d416f39488e5a8112e8684d`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a156af603f3a03b081a983c7e973e8a1736084868614fb76f7e7a581b49758`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e032d2b24653f4c22de4d915dce3406c6aa1980e06780bd87a402da054e37094`  
		Last Modified: Tue, 17 Sep 2024 00:59:15 GMT  
		Size: 67.7 MB (67708615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1572abe74a5b278158243ab24efbebbd158a63ce0eb676dbf5d254bbe44073e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d6f1c1dd3349bb7687a7584b9f375f52a163b1cf560e0fb6f758f6f427c541cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86ffdd56b6fc6b43522b1fd48ae936505cac4f715f133821587bd2fde90e8f2`

```dockerfile
```

-	Layers:
	-	`sha256:f744f247366e6c390395d191add41453b0704f7c8a8f05e3dddbcd19634f79bb`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 5.0 MB (5015252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee05fe939486cb664b9c09428d563b15815c10d4f9665c5c54913225803288d`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:693d41e97969a3b09bdc72841f4abe4b9d8966cda18f1f5fc819eeadc0356348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95006558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdd67b469ec36f7a6d61e8d1286337fdd059342785ba793c555bd6a19554700`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a11b74d0eb46a4c9c7e7568b215c46625d3581bada3826ffcbac7e41946e96`  
		Last Modified: Tue, 17 Sep 2024 02:19:59 GMT  
		Size: 67.6 MB (67646946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b641deca7a61ba77a09e62061b7b4ffddf0549958445c4670531101516c5e82`  
		Last Modified: Tue, 17 Sep 2024 02:19:56 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:84fdeede9e71fb976f918cc6e6a366abbeeb0ed0ba9289c2fcc7e3ea39756259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf6647df0a1b6ce7d41a730a93117bdd1b6eb4445a74e6f53499cf8ebda6971`

```dockerfile
```

-	Layers:
	-	`sha256:6c301b4f52a71e1f5dc9d40dd4ac5d9aa4cad3a6c7334ca665941b8fa1252cc1`  
		Last Modified: Tue, 17 Sep 2024 02:19:57 GMT  
		Size: 5.0 MB (5021584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497bb535bed0dbb14dfb43e86b1632b8b90b0b2de13b666a07bc9893af97db15`  
		Last Modified: Tue, 17 Sep 2024 02:19:57 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.1`

```console
$ docker pull kong@sha256:4f011c1f306eb6f3be999e903cc170b94bce6f4ecc66cb0a1d7b89d237d16c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1` - linux; amd64

```console
$ docker pull kong@sha256:0d08c2b349a66f9e159c1ab8bf9ba67f6d98cd18ea71a7ed98d017ba13e5e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084144a5b676aa9cf65920665641166b1452b8762d416f39488e5a8112e8684d`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a156af603f3a03b081a983c7e973e8a1736084868614fb76f7e7a581b49758`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e032d2b24653f4c22de4d915dce3406c6aa1980e06780bd87a402da054e37094`  
		Last Modified: Tue, 17 Sep 2024 00:59:15 GMT  
		Size: 67.7 MB (67708615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1572abe74a5b278158243ab24efbebbd158a63ce0eb676dbf5d254bbe44073e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:d6f1c1dd3349bb7687a7584b9f375f52a163b1cf560e0fb6f758f6f427c541cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86ffdd56b6fc6b43522b1fd48ae936505cac4f715f133821587bd2fde90e8f2`

```dockerfile
```

-	Layers:
	-	`sha256:f744f247366e6c390395d191add41453b0704f7c8a8f05e3dddbcd19634f79bb`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 5.0 MB (5015252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee05fe939486cb664b9c09428d563b15815c10d4f9665c5c54913225803288d`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:693d41e97969a3b09bdc72841f4abe4b9d8966cda18f1f5fc819eeadc0356348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95006558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdd67b469ec36f7a6d61e8d1286337fdd059342785ba793c555bd6a19554700`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a11b74d0eb46a4c9c7e7568b215c46625d3581bada3826ffcbac7e41946e96`  
		Last Modified: Tue, 17 Sep 2024 02:19:59 GMT  
		Size: 67.6 MB (67646946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b641deca7a61ba77a09e62061b7b4ffddf0549958445c4670531101516c5e82`  
		Last Modified: Tue, 17 Sep 2024 02:19:56 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:84fdeede9e71fb976f918cc6e6a366abbeeb0ed0ba9289c2fcc7e3ea39756259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf6647df0a1b6ce7d41a730a93117bdd1b6eb4445a74e6f53499cf8ebda6971`

```dockerfile
```

-	Layers:
	-	`sha256:6c301b4f52a71e1f5dc9d40dd4ac5d9aa4cad3a6c7334ca665941b8fa1252cc1`  
		Last Modified: Tue, 17 Sep 2024 02:19:57 GMT  
		Size: 5.0 MB (5021584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497bb535bed0dbb14dfb43e86b1632b8b90b0b2de13b666a07bc9893af97db15`  
		Last Modified: Tue, 17 Sep 2024 02:19:57 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.1-ubuntu`

```console
$ docker pull kong@sha256:4f011c1f306eb6f3be999e903cc170b94bce6f4ecc66cb0a1d7b89d237d16c0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:0d08c2b349a66f9e159c1ab8bf9ba67f6d98cd18ea71a7ed98d017ba13e5e313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084144a5b676aa9cf65920665641166b1452b8762d416f39488e5a8112e8684d`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a156af603f3a03b081a983c7e973e8a1736084868614fb76f7e7a581b49758`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e032d2b24653f4c22de4d915dce3406c6aa1980e06780bd87a402da054e37094`  
		Last Modified: Tue, 17 Sep 2024 00:59:15 GMT  
		Size: 67.7 MB (67708615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1572abe74a5b278158243ab24efbebbd158a63ce0eb676dbf5d254bbe44073e`  
		Last Modified: Tue, 17 Sep 2024 00:59:05 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d6f1c1dd3349bb7687a7584b9f375f52a163b1cf560e0fb6f758f6f427c541cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86ffdd56b6fc6b43522b1fd48ae936505cac4f715f133821587bd2fde90e8f2`

```dockerfile
```

-	Layers:
	-	`sha256:f744f247366e6c390395d191add41453b0704f7c8a8f05e3dddbcd19634f79bb`  
		Last Modified: Tue, 17 Sep 2024 00:59:14 GMT  
		Size: 5.0 MB (5015252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee05fe939486cb664b9c09428d563b15815c10d4f9665c5c54913225803288d`  
		Last Modified: Tue, 17 Sep 2024 00:59:13 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:693d41e97969a3b09bdc72841f4abe4b9d8966cda18f1f5fc819eeadc0356348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95006558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdd67b469ec36f7a6d61e8d1286337fdd059342785ba793c555bd6a19554700`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a11b74d0eb46a4c9c7e7568b215c46625d3581bada3826ffcbac7e41946e96`  
		Last Modified: Tue, 17 Sep 2024 02:19:59 GMT  
		Size: 67.6 MB (67646946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b641deca7a61ba77a09e62061b7b4ffddf0549958445c4670531101516c5e82`  
		Last Modified: Tue, 17 Sep 2024 02:19:56 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:84fdeede9e71fb976f918cc6e6a366abbeeb0ed0ba9289c2fcc7e3ea39756259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf6647df0a1b6ce7d41a730a93117bdd1b6eb4445a74e6f53499cf8ebda6971`

```dockerfile
```

-	Layers:
	-	`sha256:6c301b4f52a71e1f5dc9d40dd4ac5d9aa4cad3a6c7334ca665941b8fa1252cc1`  
		Last Modified: Tue, 17 Sep 2024 02:19:57 GMT  
		Size: 5.0 MB (5021584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:497bb535bed0dbb14dfb43e86b1632b8b90b0b2de13b666a07bc9893af97db15`  
		Last Modified: Tue, 17 Sep 2024 02:19:57 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:616b2ab5a4c7b6c14022e8a1495ff34930ced76f25f3d418e76758717fec335f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:06b3649c4042b55d108b9c8c81d8a2c64d9dae4f7c38d70d259b13491057b532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7ae7008ea25ffba6803d5b7a98ef953ae6a8b1ebdb86e1d19925383e204ff7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f4cf5b05541c564470dd9c31a7e069849fe848969e0c72fd0657b1b7023e8`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0183922cc67aa6ce647c5310fa77fa3173aab6526e09a61e3bbbd08622be182c`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 88.0 MB (87985692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175c32a1e68fba6caa9437a6a4c1c0130d167f491c6efeb582ae6b8bd601beb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:c8a2b3627a6d88cc74af3261c942d29dbfb003ff8f44829124ac9e3ad4040e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43fe51359c2a239d9e304afa52b97bd9c7d5743758cbe92258a7792d3c5257`

```dockerfile
```

-	Layers:
	-	`sha256:88ab2fbad70a567af0795094b4ac81186dacff845957f5d7b7b494cb3c6659a1`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 3.1 KB (3103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113141d1145c121da26cb1fa8f9d8710810dcdd1342c244f15540551b94207ae`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e1bcfd118241be8875a4412e28e6145c23451226c575ab9c7b329533214f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81cf7b05f70576eff155ee2611ebf287bd1b75bd1b5eb4999e6ba406b7d65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b35d5aac6da9ddec8a4f7853b45ab07c6248faaed3f6ef9451521393925963e`  
		Last Modified: Tue, 17 Sep 2024 02:19:00 GMT  
		Size: 87.3 MB (87268634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605e2e738b1db6eed7febb8b0207fed07e84735407b538f80e76957263d4b17`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:69626ecd1cf471d17e8034ad1cd9a145fa31ab80bbe97a5079caef58bb4ec50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c0249e28b8ef13e22d961b1bea53d4fa73aa5108612ecd7b1ccea2128ae384`

```dockerfile
```

-	Layers:
	-	`sha256:276d6979b92c2d6471950fb9e7261ed079d21598b5aec398095675d8da5cd25b`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 5.2 MB (5216658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d503c6dda6a2b36a5b99f7170e43d9a1740cec1b195b5401721a39effd009`  
		Last Modified: Tue, 17 Sep 2024 02:18:57 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:616b2ab5a4c7b6c14022e8a1495ff34930ced76f25f3d418e76758717fec335f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:06b3649c4042b55d108b9c8c81d8a2c64d9dae4f7c38d70d259b13491057b532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7ae7008ea25ffba6803d5b7a98ef953ae6a8b1ebdb86e1d19925383e204ff7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f4cf5b05541c564470dd9c31a7e069849fe848969e0c72fd0657b1b7023e8`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0183922cc67aa6ce647c5310fa77fa3173aab6526e09a61e3bbbd08622be182c`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 88.0 MB (87985692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175c32a1e68fba6caa9437a6a4c1c0130d167f491c6efeb582ae6b8bd601beb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c8a2b3627a6d88cc74af3261c942d29dbfb003ff8f44829124ac9e3ad4040e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43fe51359c2a239d9e304afa52b97bd9c7d5743758cbe92258a7792d3c5257`

```dockerfile
```

-	Layers:
	-	`sha256:88ab2fbad70a567af0795094b4ac81186dacff845957f5d7b7b494cb3c6659a1`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 3.1 KB (3103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113141d1145c121da26cb1fa8f9d8710810dcdd1342c244f15540551b94207ae`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e1bcfd118241be8875a4412e28e6145c23451226c575ab9c7b329533214f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81cf7b05f70576eff155ee2611ebf287bd1b75bd1b5eb4999e6ba406b7d65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b35d5aac6da9ddec8a4f7853b45ab07c6248faaed3f6ef9451521393925963e`  
		Last Modified: Tue, 17 Sep 2024 02:19:00 GMT  
		Size: 87.3 MB (87268634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605e2e738b1db6eed7febb8b0207fed07e84735407b538f80e76957263d4b17`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:69626ecd1cf471d17e8034ad1cd9a145fa31ab80bbe97a5079caef58bb4ec50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c0249e28b8ef13e22d961b1bea53d4fa73aa5108612ecd7b1ccea2128ae384`

```dockerfile
```

-	Layers:
	-	`sha256:276d6979b92c2d6471950fb9e7261ed079d21598b5aec398095675d8da5cd25b`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 5.2 MB (5216658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d503c6dda6a2b36a5b99f7170e43d9a1740cec1b195b5401721a39effd009`  
		Last Modified: Tue, 17 Sep 2024 02:18:57 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:616b2ab5a4c7b6c14022e8a1495ff34930ced76f25f3d418e76758717fec335f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:06b3649c4042b55d108b9c8c81d8a2c64d9dae4f7c38d70d259b13491057b532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7ae7008ea25ffba6803d5b7a98ef953ae6a8b1ebdb86e1d19925383e204ff7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f4cf5b05541c564470dd9c31a7e069849fe848969e0c72fd0657b1b7023e8`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0183922cc67aa6ce647c5310fa77fa3173aab6526e09a61e3bbbd08622be182c`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 88.0 MB (87985692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175c32a1e68fba6caa9437a6a4c1c0130d167f491c6efeb582ae6b8bd601beb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:c8a2b3627a6d88cc74af3261c942d29dbfb003ff8f44829124ac9e3ad4040e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43fe51359c2a239d9e304afa52b97bd9c7d5743758cbe92258a7792d3c5257`

```dockerfile
```

-	Layers:
	-	`sha256:88ab2fbad70a567af0795094b4ac81186dacff845957f5d7b7b494cb3c6659a1`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 3.1 KB (3103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113141d1145c121da26cb1fa8f9d8710810dcdd1342c244f15540551b94207ae`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e1bcfd118241be8875a4412e28e6145c23451226c575ab9c7b329533214f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81cf7b05f70576eff155ee2611ebf287bd1b75bd1b5eb4999e6ba406b7d65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b35d5aac6da9ddec8a4f7853b45ab07c6248faaed3f6ef9451521393925963e`  
		Last Modified: Tue, 17 Sep 2024 02:19:00 GMT  
		Size: 87.3 MB (87268634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605e2e738b1db6eed7febb8b0207fed07e84735407b538f80e76957263d4b17`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:69626ecd1cf471d17e8034ad1cd9a145fa31ab80bbe97a5079caef58bb4ec50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c0249e28b8ef13e22d961b1bea53d4fa73aa5108612ecd7b1ccea2128ae384`

```dockerfile
```

-	Layers:
	-	`sha256:276d6979b92c2d6471950fb9e7261ed079d21598b5aec398095675d8da5cd25b`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 5.2 MB (5216658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d503c6dda6a2b36a5b99f7170e43d9a1740cec1b195b5401721a39effd009`  
		Last Modified: Tue, 17 Sep 2024 02:18:57 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:616b2ab5a4c7b6c14022e8a1495ff34930ced76f25f3d418e76758717fec335f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:06b3649c4042b55d108b9c8c81d8a2c64d9dae4f7c38d70d259b13491057b532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7ae7008ea25ffba6803d5b7a98ef953ae6a8b1ebdb86e1d19925383e204ff7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f4cf5b05541c564470dd9c31a7e069849fe848969e0c72fd0657b1b7023e8`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0183922cc67aa6ce647c5310fa77fa3173aab6526e09a61e3bbbd08622be182c`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 88.0 MB (87985692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175c32a1e68fba6caa9437a6a4c1c0130d167f491c6efeb582ae6b8bd601beb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c8a2b3627a6d88cc74af3261c942d29dbfb003ff8f44829124ac9e3ad4040e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43fe51359c2a239d9e304afa52b97bd9c7d5743758cbe92258a7792d3c5257`

```dockerfile
```

-	Layers:
	-	`sha256:88ab2fbad70a567af0795094b4ac81186dacff845957f5d7b7b494cb3c6659a1`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 3.1 KB (3103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113141d1145c121da26cb1fa8f9d8710810dcdd1342c244f15540551b94207ae`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e1bcfd118241be8875a4412e28e6145c23451226c575ab9c7b329533214f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81cf7b05f70576eff155ee2611ebf287bd1b75bd1b5eb4999e6ba406b7d65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b35d5aac6da9ddec8a4f7853b45ab07c6248faaed3f6ef9451521393925963e`  
		Last Modified: Tue, 17 Sep 2024 02:19:00 GMT  
		Size: 87.3 MB (87268634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605e2e738b1db6eed7febb8b0207fed07e84735407b538f80e76957263d4b17`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:69626ecd1cf471d17e8034ad1cd9a145fa31ab80bbe97a5079caef58bb4ec50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c0249e28b8ef13e22d961b1bea53d4fa73aa5108612ecd7b1ccea2128ae384`

```dockerfile
```

-	Layers:
	-	`sha256:276d6979b92c2d6471950fb9e7261ed079d21598b5aec398095675d8da5cd25b`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 5.2 MB (5216658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d503c6dda6a2b36a5b99f7170e43d9a1740cec1b195b5401721a39effd009`  
		Last Modified: Tue, 17 Sep 2024 02:18:57 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

**does not exist** (yet?)

## `kong:3.9-ubuntu`

**does not exist** (yet?)

## `kong:3.9.0`

**does not exist** (yet?)

## `kong:3.9.0-ubuntu`

**does not exist** (yet?)

## `kong:latest`

```console
$ docker pull kong@sha256:616b2ab5a4c7b6c14022e8a1495ff34930ced76f25f3d418e76758717fec335f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:06b3649c4042b55d108b9c8c81d8a2c64d9dae4f7c38d70d259b13491057b532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7ae7008ea25ffba6803d5b7a98ef953ae6a8b1ebdb86e1d19925383e204ff7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f4cf5b05541c564470dd9c31a7e069849fe848969e0c72fd0657b1b7023e8`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0183922cc67aa6ce647c5310fa77fa3173aab6526e09a61e3bbbd08622be182c`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 88.0 MB (87985692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175c32a1e68fba6caa9437a6a4c1c0130d167f491c6efeb582ae6b8bd601beb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:c8a2b3627a6d88cc74af3261c942d29dbfb003ff8f44829124ac9e3ad4040e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43fe51359c2a239d9e304afa52b97bd9c7d5743758cbe92258a7792d3c5257`

```dockerfile
```

-	Layers:
	-	`sha256:88ab2fbad70a567af0795094b4ac81186dacff845957f5d7b7b494cb3c6659a1`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 3.1 KB (3103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113141d1145c121da26cb1fa8f9d8710810dcdd1342c244f15540551b94207ae`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e1bcfd118241be8875a4412e28e6145c23451226c575ab9c7b329533214f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81cf7b05f70576eff155ee2611ebf287bd1b75bd1b5eb4999e6ba406b7d65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b35d5aac6da9ddec8a4f7853b45ab07c6248faaed3f6ef9451521393925963e`  
		Last Modified: Tue, 17 Sep 2024 02:19:00 GMT  
		Size: 87.3 MB (87268634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605e2e738b1db6eed7febb8b0207fed07e84735407b538f80e76957263d4b17`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:69626ecd1cf471d17e8034ad1cd9a145fa31ab80bbe97a5079caef58bb4ec50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c0249e28b8ef13e22d961b1bea53d4fa73aa5108612ecd7b1ccea2128ae384`

```dockerfile
```

-	Layers:
	-	`sha256:276d6979b92c2d6471950fb9e7261ed079d21598b5aec398095675d8da5cd25b`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 5.2 MB (5216658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d503c6dda6a2b36a5b99f7170e43d9a1740cec1b195b5401721a39effd009`  
		Last Modified: Tue, 17 Sep 2024 02:18:57 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:616b2ab5a4c7b6c14022e8a1495ff34930ced76f25f3d418e76758717fec335f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:06b3649c4042b55d108b9c8c81d8a2c64d9dae4f7c38d70d259b13491057b532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117522664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7ae7008ea25ffba6803d5b7a98ef953ae6a8b1ebdb86e1d19925383e204ff7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
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
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2f4cf5b05541c564470dd9c31a7e069849fe848969e0c72fd0657b1b7023e8`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0183922cc67aa6ce647c5310fa77fa3173aab6526e09a61e3bbbd08622be182c`  
		Last Modified: Tue, 17 Sep 2024 00:58:59 GMT  
		Size: 88.0 MB (87985692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175c32a1e68fba6caa9437a6a4c1c0130d167f491c6efeb582ae6b8bd601beb`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c8a2b3627a6d88cc74af3261c942d29dbfb003ff8f44829124ac9e3ad4040e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad43fe51359c2a239d9e304afa52b97bd9c7d5743758cbe92258a7792d3c5257`

```dockerfile
```

-	Layers:
	-	`sha256:88ab2fbad70a567af0795094b4ac81186dacff845957f5d7b7b494cb3c6659a1`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 3.1 KB (3103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113141d1145c121da26cb1fa8f9d8710810dcdd1342c244f15540551b94207ae`  
		Last Modified: Tue, 17 Sep 2024 00:58:58 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e1bcfd118241be8875a4412e28e6145c23451226c575ab9c7b329533214f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e81cf7b05f70576eff155ee2611ebf287bd1b75bd1b5eb4999e6ba406b7d65b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
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
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3aa62581876de35f39e3006576ae17be1ba694443d06f16438ffdf97929df3`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b35d5aac6da9ddec8a4f7853b45ab07c6248faaed3f6ef9451521393925963e`  
		Last Modified: Tue, 17 Sep 2024 02:19:00 GMT  
		Size: 87.3 MB (87268634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605e2e738b1db6eed7febb8b0207fed07e84735407b538f80e76957263d4b17`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:69626ecd1cf471d17e8034ad1cd9a145fa31ab80bbe97a5079caef58bb4ec50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5233002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3c0249e28b8ef13e22d961b1bea53d4fa73aa5108612ecd7b1ccea2128ae384`

```dockerfile
```

-	Layers:
	-	`sha256:276d6979b92c2d6471950fb9e7261ed079d21598b5aec398095675d8da5cd25b`  
		Last Modified: Tue, 17 Sep 2024 02:18:58 GMT  
		Size: 5.2 MB (5216658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486d503c6dda6a2b36a5b99f7170e43d9a1740cec1b195b5401721a39effd009`  
		Last Modified: Tue, 17 Sep 2024 02:18:57 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
