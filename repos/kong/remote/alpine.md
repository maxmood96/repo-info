## `kong:alpine`

```console
$ docker pull kong@sha256:46533612d90ba85bcda681f7f7eb9626b5c09e6e10f6640bb00cc8375b0b7423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:6679a83c22182e537683e5a7d927d2922818b79320d092e1683581815d88c788
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49796844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6b5f34fa906a3f05a677ff10f9b67d4ba90965d41e0009df391962a6b8798c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 15 Sep 2021 23:20:07 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 23:20:08 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 23:20:08 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 23:20:08 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 23:20:08 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 15 Sep 2021 23:20:08 GMT
ARG KONG_VERSION=2.5.1
# Wed, 15 Sep 2021 23:20:09 GMT
ENV KONG_VERSION=2.5.1
# Wed, 15 Sep 2021 23:20:09 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Wed, 15 Sep 2021 23:20:09 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Wed, 15 Sep 2021 23:20:09 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Wed, 15 Sep 2021 23:20:09 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Wed, 15 Sep 2021 23:20:17 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Wed, 15 Sep 2021 23:20:18 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 15 Sep 2021 23:20:18 GMT
USER kong
# Wed, 15 Sep 2021 23:20:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 23:20:18 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 15 Sep 2021 23:20:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Sep 2021 23:20:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 15 Sep 2021 23:20:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7e2c0ec31857d2cfb927962749512b048ffbf7701e394fc43f994413896b93`  
		Last Modified: Wed, 15 Sep 2021 23:22:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b48a90858082055ca0b96621dc1c439139c0955a2b5bd3ae3433ec5c994141`  
		Last Modified: Wed, 15 Sep 2021 23:22:42 GMT  
		Size: 47.0 MB (46981386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447d4c31d2897cca836eda629ae028e45a7aa0589410499a65e299ffa2283a49`  
		Last Modified: Wed, 15 Sep 2021 23:22:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:919a4836acd3da4255d36e5cd3919af69b2725097a6a83981f2d0d81aabb790c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49260344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daf56b078c005d27ead1030b12d5a1add7a96be7020eac1f57f55b108f27a88`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 15 Sep 2021 23:40:09 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 23:40:09 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 23:40:09 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 23:40:10 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 23:40:10 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Mon, 04 Oct 2021 23:39:59 GMT
ARG KONG_VERSION=2.6.0
# Mon, 04 Oct 2021 23:39:59 GMT
ENV KONG_VERSION=2.6.0
# Mon, 04 Oct 2021 23:39:59 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Mon, 04 Oct 2021 23:39:59 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Mon, 04 Oct 2021 23:39:59 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Mon, 04 Oct 2021 23:40:00 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Mon, 04 Oct 2021 23:40:07 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Mon, 04 Oct 2021 23:40:07 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Mon, 04 Oct 2021 23:40:07 GMT
USER kong
# Mon, 04 Oct 2021 23:40:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 04 Oct 2021 23:40:08 GMT
EXPOSE 8000 8001 8443 8444
# Mon, 04 Oct 2021 23:40:08 GMT
STOPSIGNAL SIGQUIT
# Mon, 04 Oct 2021 23:40:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Mon, 04 Oct 2021 23:40:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c360972f473f7b9d56e76befffc2525b7c40e33e380802c97b2b52414f64ef51`  
		Last Modified: Wed, 15 Sep 2021 23:42:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a2f32ff50696bebcde91b91e34692e0e0d1f28865369f7a2452099215d474a`  
		Last Modified: Mon, 04 Oct 2021 23:43:25 GMT  
		Size: 46.5 MB (46547505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb872f50ca49b8d57d2aa1917e36651435e063dfcad14bd18caa0dbd4571f91`  
		Last Modified: Mon, 04 Oct 2021 23:43:15 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
