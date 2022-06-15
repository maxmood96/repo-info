<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.5`](#kong25)
-	[`kong:2.5-ubuntu`](#kong25-ubuntu)
-	[`kong:2.5.2`](#kong252)
-	[`kong:2.5.2-alpine`](#kong252-alpine)
-	[`kong:2.5.2-ubuntu`](#kong252-ubuntu)
-	[`kong:2.6`](#kong26)
-	[`kong:2.6-ubuntu`](#kong26-ubuntu)
-	[`kong:2.6.1`](#kong261)
-	[`kong:2.6.1-alpine`](#kong261-alpine)
-	[`kong:2.6.1-ubuntu`](#kong261-ubuntu)
-	[`kong:2.7`](#kong27)
-	[`kong:2.7-ubuntu`](#kong27-ubuntu)
-	[`kong:2.7.2`](#kong272)
-	[`kong:2.7.2-alpine`](#kong272-alpine)
-	[`kong:2.7.2-ubuntu`](#kong272-ubuntu)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.1`](#kong281)
-	[`kong:2.8.1-alpine`](#kong281-alpine)
-	[`kong:2.8.1-ubuntu`](#kong281-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:039fec0213d68fb1ffa38927d1b891528c73699c6f0f876b50b31329f6ce3687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:a0d612338232e5d773bfb6440c54ad6bf1f9046a49550184860bbc0a5d5c7c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49257384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0dc442785ca21c9a26e742457eca32887f901d9527f262d0e7c4ab94db08ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:21:59 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:21:59 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:00 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 14 Jun 2022 23:22:00 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 14 Jun 2022 23:22:09 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:22:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:22:10 GMT
USER kong
# Tue, 14 Jun 2022 23:22:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:22:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc00107c129ed9d95b3bde9ef14383f4d2add948d804fbcd95b869bd5357cfb9`  
		Last Modified: Tue, 14 Jun 2022 23:24:41 GMT  
		Size: 46.4 MB (46441813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a242f4dbbee02267f5bbc99223ad51b78268a4ee3f9a4aba5c5f412555d07f5`  
		Last Modified: Tue, 14 Jun 2022 23:24:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:957e57f2b9c0829c34d13b0d8265b02e0bf35ae83f146277dd8c8654fcbe7a48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48454987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a17b19da5dc5465a8dd445817a828add16fe1f2a7259466a1765beaace9556a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:43:44 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:43:45 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:43:46 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 14 Jun 2022 23:43:47 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 14 Jun 2022 23:44:04 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:44:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:44:06 GMT
USER kong
# Tue, 14 Jun 2022 23:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:44:08 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:44:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:44:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:44:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bacf982454fc41d2f3ebb14b393201b104f475d0da93209335fa9340b3d92c`  
		Last Modified: Tue, 14 Jun 2022 23:47:39 GMT  
		Size: 45.7 MB (45737498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20de48a6f80d46f4f6b392acc51fbaae039378d1db277b69725f9b20b22b65ce`  
		Last Modified: Tue, 14 Jun 2022 23:47:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:447357d50ad6393cd4b7baa045c1b9ce43294d15cfee531f710e97c31ba4d815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7b779407b10ad5645905dcb962fbcba0e3d8006eac268bae762bd6e101c402b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121305426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf802a8434b5f2f26de4feddb6b6f63bbbf9f8654966734060d49e41cdaac930`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:13 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 14 Jun 2022 23:22:33 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:22:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:22:34 GMT
USER kong
# Tue, 14 Jun 2022 23:22:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:22:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:22:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:22:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:22:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1dfb679acc17d7d224b74832d6650b64e4e2a73df45a29b9712b90ae1444b2`  
		Last Modified: Tue, 14 Jun 2022 23:25:05 GMT  
		Size: 67.6 MB (67649951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de9cf24cfa64449f509d580c84c4c141998711caf4c75b40416710725aff28c`  
		Last Modified: Tue, 14 Jun 2022 23:24:53 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4d78b67ffc52535176510c5f1ba119df523b6122270603661c6e02f2a50dde06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118343120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913ca4999397f03acef93722d99d461566c64071b34e043bf756b67e16eb6e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:44:17 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:44:18 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:44:19 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 14 Jun 2022 23:44:20 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 14 Jun 2022 23:44:53 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:44:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:44:54 GMT
USER kong
# Tue, 14 Jun 2022 23:44:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:44:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:44:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:44:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:44:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be098501d93df45466127ba9fd7f67f42d591984b2102a7b118c00422cacfcae`  
		Last Modified: Tue, 14 Jun 2022 23:48:03 GMT  
		Size: 66.1 MB (66069066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8d2a3d441f6730eaa0a2f4e65d4b036ae32f8e13e6078011dbd7c273199a27`  
		Last Modified: Tue, 14 Jun 2022 23:47:52 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2`

```console
$ docker pull kong@sha256:039fec0213d68fb1ffa38927d1b891528c73699c6f0f876b50b31329f6ce3687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2` - linux; amd64

```console
$ docker pull kong@sha256:a0d612338232e5d773bfb6440c54ad6bf1f9046a49550184860bbc0a5d5c7c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49257384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0dc442785ca21c9a26e742457eca32887f901d9527f262d0e7c4ab94db08ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:21:59 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:21:59 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:00 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 14 Jun 2022 23:22:00 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 14 Jun 2022 23:22:09 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:22:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:22:10 GMT
USER kong
# Tue, 14 Jun 2022 23:22:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:22:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc00107c129ed9d95b3bde9ef14383f4d2add948d804fbcd95b869bd5357cfb9`  
		Last Modified: Tue, 14 Jun 2022 23:24:41 GMT  
		Size: 46.4 MB (46441813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a242f4dbbee02267f5bbc99223ad51b78268a4ee3f9a4aba5c5f412555d07f5`  
		Last Modified: Tue, 14 Jun 2022 23:24:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:957e57f2b9c0829c34d13b0d8265b02e0bf35ae83f146277dd8c8654fcbe7a48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48454987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a17b19da5dc5465a8dd445817a828add16fe1f2a7259466a1765beaace9556a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:43:44 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:43:45 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:43:46 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 14 Jun 2022 23:43:47 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 14 Jun 2022 23:44:04 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:44:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:44:06 GMT
USER kong
# Tue, 14 Jun 2022 23:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:44:08 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:44:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:44:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:44:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bacf982454fc41d2f3ebb14b393201b104f475d0da93209335fa9340b3d92c`  
		Last Modified: Tue, 14 Jun 2022 23:47:39 GMT  
		Size: 45.7 MB (45737498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20de48a6f80d46f4f6b392acc51fbaae039378d1db277b69725f9b20b22b65ce`  
		Last Modified: Tue, 14 Jun 2022 23:47:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-alpine`

```console
$ docker pull kong@sha256:039fec0213d68fb1ffa38927d1b891528c73699c6f0f876b50b31329f6ce3687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:a0d612338232e5d773bfb6440c54ad6bf1f9046a49550184860bbc0a5d5c7c2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49257384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0dc442785ca21c9a26e742457eca32887f901d9527f262d0e7c4ab94db08ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:21:59 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:21:59 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:00 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 14 Jun 2022 23:22:00 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 14 Jun 2022 23:22:09 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:22:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:22:10 GMT
USER kong
# Tue, 14 Jun 2022 23:22:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:22:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc00107c129ed9d95b3bde9ef14383f4d2add948d804fbcd95b869bd5357cfb9`  
		Last Modified: Tue, 14 Jun 2022 23:24:41 GMT  
		Size: 46.4 MB (46441813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a242f4dbbee02267f5bbc99223ad51b78268a4ee3f9a4aba5c5f412555d07f5`  
		Last Modified: Tue, 14 Jun 2022 23:24:34 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:957e57f2b9c0829c34d13b0d8265b02e0bf35ae83f146277dd8c8654fcbe7a48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48454987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a17b19da5dc5465a8dd445817a828add16fe1f2a7259466a1765beaace9556a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:43:44 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:43:45 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:43:46 GMT
ARG KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d
# Tue, 14 Jun 2022 23:43:47 GMT
ARG KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
# Tue, 14 Jun 2022 23:44:04 GMT
# ARGS: KONG_AMD64_SHA=d4bc93bcb14cce8c37ced136632a290b441050c540db779e742bcd88e5cfd70d KONG_ARM64_SHA=691e1dc29e96d6a95b60674513932c4f7547773014685ce0130549f980c1c46e
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:44:06 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:44:06 GMT
USER kong
# Tue, 14 Jun 2022 23:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:44:08 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:44:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:44:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:44:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bacf982454fc41d2f3ebb14b393201b104f475d0da93209335fa9340b3d92c`  
		Last Modified: Tue, 14 Jun 2022 23:47:39 GMT  
		Size: 45.7 MB (45737498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20de48a6f80d46f4f6b392acc51fbaae039378d1db277b69725f9b20b22b65ce`  
		Last Modified: Tue, 14 Jun 2022 23:47:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.2-ubuntu`

```console
$ docker pull kong@sha256:447357d50ad6393cd4b7baa045c1b9ce43294d15cfee531f710e97c31ba4d815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7b779407b10ad5645905dcb962fbcba0e3d8006eac268bae762bd6e101c402b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121305426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf802a8434b5f2f26de4feddb6b6f63bbbf9f8654966734060d49e41cdaac930`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:13 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 14 Jun 2022 23:22:13 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 14 Jun 2022 23:22:33 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:22:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:22:34 GMT
USER kong
# Tue, 14 Jun 2022 23:22:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:22:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:22:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:22:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:22:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1dfb679acc17d7d224b74832d6650b64e4e2a73df45a29b9712b90ae1444b2`  
		Last Modified: Tue, 14 Jun 2022 23:25:05 GMT  
		Size: 67.6 MB (67649951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de9cf24cfa64449f509d580c84c4c141998711caf4c75b40416710725aff28c`  
		Last Modified: Tue, 14 Jun 2022 23:24:53 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4d78b67ffc52535176510c5f1ba119df523b6122270603661c6e02f2a50dde06
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.3 MB (118343120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9913ca4999397f03acef93722d99d461566c64071b34e043bf756b67e16eb6e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:44:17 GMT
ARG KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:44:18 GMT
ENV KONG_VERSION=2.5.2
# Tue, 14 Jun 2022 23:44:19 GMT
ARG KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96
# Tue, 14 Jun 2022 23:44:20 GMT
ARG KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
# Tue, 14 Jun 2022 23:44:53 GMT
# ARGS: KONG_AMD64_SHA=ae65ac9eb35f682768abfb080c61581440347db8dafd0a495639ff666a406a96 KONG_ARM64_SHA=b4720e3d0831d13364cc749200c77df356a2145478f6a55fd48618a9aa1967d9
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:44:54 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:44:54 GMT
USER kong
# Tue, 14 Jun 2022 23:44:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:44:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:44:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:44:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:44:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be098501d93df45466127ba9fd7f67f42d591984b2102a7b118c00422cacfcae`  
		Last Modified: Tue, 14 Jun 2022 23:48:03 GMT  
		Size: 66.1 MB (66069066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8d2a3d441f6730eaa0a2f4e65d4b036ae32f8e13e6078011dbd7c273199a27`  
		Last Modified: Tue, 14 Jun 2022 23:47:52 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:3eb2f5af81b5573f6bd260eee2c4dab0323bf784233a1d34bda6aa140b647eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6c732184cbecaf07004a58f98a9caa08eafa9a69bd39a9adfdbcf3e4e489ff08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128178153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c45108fd2c98886ff41659d5b9f9fdf029902a28ec6d17ed46182e387f474e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:27:51 GMT
ARG KONG_VERSION=2.6.1
# Tue, 07 Jun 2022 00:27:51 GMT
ENV KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:21:31 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 14 Jun 2022 23:21:31 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 14 Jun 2022 23:21:52 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:21:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:21:53 GMT
USER kong
# Tue, 14 Jun 2022 23:21:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:21:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:21:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:21:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:21:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a6ad0ac64b328847492648b99c0589ac8f8e6b5b6be0bac479fed0b97074c`  
		Last Modified: Tue, 14 Jun 2022 23:24:24 GMT  
		Size: 74.5 MB (74522678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acebe9b9e2a441ecdfeb94361c4990beb6565b5de4f647440284b1238eb5cab`  
		Last Modified: Tue, 14 Jun 2022 23:24:12 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9edbb82a5cab25824f6a9a5b5fa74099b44dac3ec28a916e8ae1f1007b08f48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125230801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b89305f90c32f975ddc48dc705ba3866dd39e5418bf61a7414eba6061c9ada4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:43:01 GMT
ARG KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:43:02 GMT
ENV KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:43:03 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 14 Jun 2022 23:43:04 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 14 Jun 2022 23:43:32 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:43:33 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:43:33 GMT
USER kong
# Tue, 14 Jun 2022 23:43:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:43:35 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:43:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:43:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:43:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051bb9dc9743d6e00ab1a027ec2e3207ac5a7456b5d4116cd1ea944ee768fe3`  
		Last Modified: Tue, 14 Jun 2022 23:47:20 GMT  
		Size: 73.0 MB (72956746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dd3c509211b3538841a5134650c43551da0e3d7817006fca2cb5ae9b9b5185`  
		Last Modified: Tue, 14 Jun 2022 23:47:08 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-alpine`

```console
$ docker pull kong@sha256:e44b180d4cca4d068923ae7e0b12c657ea308fca884098db1f802a4321e2c6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:a68fadbfb98fa3af88866ae49f51c42509a4ab329cfc48fb461d93764901c3ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d25cced91d05f9b228b3df44b49d24d490baeafeac92210ae3c83525d14c9b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 19:32:44 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 19:32:51 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:52 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:52 GMT
USER kong
# Tue, 12 Apr 2022 19:32:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:52 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846119c04e88b6dc84b3411cf74dde70115ceaa39a9dc3801638e336f40ff6c`  
		Last Modified: Tue, 12 Apr 2022 19:35:40 GMT  
		Size: 47.4 MB (47393221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d957996ac9c41a86d979da49d6d918aa912d47a5e8c14e6b3abef267167b47`  
		Last Modified: Tue, 12 Apr 2022 19:35:32 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:985bd739862dfba2323e1ef2edfe4b6510aff21ed446d78fd55abf634355a764
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a42260facc31b5de9fd189f8a7b54fc41e97032df13c475e688c1cfb6bad4b2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:05:22 GMT
ARG KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:23 GMT
ENV KONG_VERSION=2.6.1
# Tue, 12 Apr 2022 20:05:24 GMT
ARG KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87
# Tue, 12 Apr 2022 20:05:25 GMT
ARG KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
# Tue, 12 Apr 2022 20:05:42 GMT
# ARGS: KONG_AMD64_SHA=9e7618ad06c148ed216be8bbf65a9c7cb95301e5349ef61b996fbb55ec4cfa87 KONG_ARM64_SHA=0fbf008685c6eac510d221595172e9e7bd51a846d410972d6950d9207cf400de
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:05:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:05:43 GMT
USER kong
# Tue, 12 Apr 2022 20:05:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:05:45 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:05:46 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:05:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:05:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486691177c648ec000964290cee697eab648dbfe2f56efc837a618da681bee22`  
		Last Modified: Tue, 12 Apr 2022 20:11:59 GMT  
		Size: 46.9 MB (46902616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826214118a31a9c5bc16f53e85a4afe7e72467d247ce5ef4a15ebb2c4b11f330`  
		Last Modified: Tue, 12 Apr 2022 20:11:50 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.1-ubuntu`

```console
$ docker pull kong@sha256:3eb2f5af81b5573f6bd260eee2c4dab0323bf784233a1d34bda6aa140b647eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:6c732184cbecaf07004a58f98a9caa08eafa9a69bd39a9adfdbcf3e4e489ff08
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128178153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c45108fd2c98886ff41659d5b9f9fdf029902a28ec6d17ed46182e387f474e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:27:51 GMT
ARG KONG_VERSION=2.6.1
# Tue, 07 Jun 2022 00:27:51 GMT
ENV KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:21:31 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 14 Jun 2022 23:21:31 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 14 Jun 2022 23:21:52 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:21:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:21:53 GMT
USER kong
# Tue, 14 Jun 2022 23:21:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:21:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:21:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:21:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:21:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a6ad0ac64b328847492648b99c0589ac8f8e6b5b6be0bac479fed0b97074c`  
		Last Modified: Tue, 14 Jun 2022 23:24:24 GMT  
		Size: 74.5 MB (74522678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acebe9b9e2a441ecdfeb94361c4990beb6565b5de4f647440284b1238eb5cab`  
		Last Modified: Tue, 14 Jun 2022 23:24:12 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:9edbb82a5cab25824f6a9a5b5fa74099b44dac3ec28a916e8ae1f1007b08f48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125230801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b89305f90c32f975ddc48dc705ba3866dd39e5418bf61a7414eba6061c9ada4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:43:01 GMT
ARG KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:43:02 GMT
ENV KONG_VERSION=2.6.1
# Tue, 14 Jun 2022 23:43:03 GMT
ARG KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e
# Tue, 14 Jun 2022 23:43:04 GMT
ARG KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
# Tue, 14 Jun 2022 23:43:32 GMT
# ARGS: KONG_AMD64_SHA=f70757f9317a1d40316f0187ae6e91c0c94b5b4346e564f7ae8430775bf7ad7e KONG_ARM64_SHA=5cba6e7e28685fb7d80b77b70586cfb92c1de4b5198a6218bb1ca0c7f2502c89
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:43:33 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:43:33 GMT
USER kong
# Tue, 14 Jun 2022 23:43:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:43:35 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:43:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:43:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:43:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7051bb9dc9743d6e00ab1a027ec2e3207ac5a7456b5d4116cd1ea944ee768fe3`  
		Last Modified: Tue, 14 Jun 2022 23:47:20 GMT  
		Size: 73.0 MB (72956746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dd3c509211b3538841a5134650c43551da0e3d7817006fca2cb5ae9b9b5185`  
		Last Modified: Tue, 14 Jun 2022 23:47:08 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:9547499e0db869d571fb76c9e65186a2209bdc2f4022a19d97ac129b9f5cef52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d50ccbfbbf0058ab4e4dbc26727ee1f051fd850a73c0389ccd89d85d055bde13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128089282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b25366321406d551fe15b9c128d8d93ae121d70743a0ca0c9bea69db7b63ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:26:55 GMT
ARG KONG_VERSION=2.7.2
# Tue, 07 Jun 2022 00:26:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:21:01 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 14 Jun 2022 23:21:01 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 14 Jun 2022 23:21:23 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:21:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:21:24 GMT
USER kong
# Tue, 14 Jun 2022 23:21:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:21:24 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:21:24 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:21:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:21:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f40ef21bcbfbfddd22aaa8c284036f53c749c2ce6aaaf483b2984b15140ee08`  
		Last Modified: Tue, 14 Jun 2022 23:24:01 GMT  
		Size: 74.4 MB (74433808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13147babdcbaf37d0add6eed3e252f5726db6a53fb32a7544f92ae934097ef1f`  
		Last Modified: Tue, 14 Jun 2022 23:23:49 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:288e255e36500d19d5e2c8638533629382eb9246b298ebfb8d57bec058d167bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125134863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08324449eb0cd5ffa32fbb4d8036a3fba00eeabf8da9699c2307bc667975278`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:41:54 GMT
ARG KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:41:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:41:56 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 14 Jun 2022 23:41:57 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 14 Jun 2022 23:42:37 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:42:39 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:42:39 GMT
USER kong
# Tue, 14 Jun 2022 23:42:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:42:41 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:42:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:42:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:42:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210ba2a0418dcc22653325535fe628a771663eb3d502d910071f83bba73914d`  
		Last Modified: Tue, 14 Jun 2022 23:46:56 GMT  
		Size: 72.9 MB (72860810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db5446eb906fe4ad4cc3845b976b3f163473fb069894b88e61b3417c1f624e3`  
		Last Modified: Tue, 14 Jun 2022 23:46:44 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-alpine`

```console
$ docker pull kong@sha256:4dfe51c0cb836192982dc712c37812c491995cd7b3694d196391f303fc54e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:c0181f30d526cd839045da3c1f8de9eedd3349ada68cbf6a6bfcec0d563f4461
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50121348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4896b6c8b9c3f39159184c8b8bbe6dca33cd854f8ff6782d8fa3a0cb6928eb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 19:32:00 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 19:32:08 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 19:32:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 19:32:09 GMT
USER kong
# Tue, 12 Apr 2022 19:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 19:32:09 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 19:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 19:32:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 19:32:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d565044977d85c458ac0b142bcd82fbc325e637602315e9817d6b4ec7c9b666`  
		Last Modified: Tue, 12 Apr 2022 19:34:57 GMT  
		Size: 47.3 MB (47305777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b549f27ad073929c3f594f4b83ef3334ace38c2175b39ca52783c23b0f825`  
		Last Modified: Tue, 12 Apr 2022 19:34:49 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f3bc86efee406011153e7acdba5309956ad3c04a526e6d793965454ec09fd35c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49524423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59e65c552d7762c16f5a4ed65c0b8239113c4fe26c0d8737539412b9418db7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 12 Apr 2022 20:01:32 GMT
ARG KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:33 GMT
ENV KONG_VERSION=2.7.2
# Tue, 12 Apr 2022 20:01:34 GMT
ARG KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b
# Tue, 12 Apr 2022 20:01:35 GMT
ARG KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
# Tue, 12 Apr 2022 20:01:44 GMT
# ARGS: KONG_AMD64_SHA=16990765aee26fc194992f0f90fc81e78a46d77cd0fc1e6670f3b2f797c1fe6b KONG_ARM64_SHA=3e5dde2479d53299e81dd903a04e30302108b0864c996a3662fda24ca7aee9f6
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 12 Apr 2022 20:01:45 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 12 Apr 2022 20:01:45 GMT
USER kong
# Tue, 12 Apr 2022 20:01:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 12 Apr 2022 20:01:47 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 12 Apr 2022 20:01:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Apr 2022 20:01:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 12 Apr 2022 20:01:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc39d004f3484e0c617d28bfcc3b54061de5edd6e0e17b49a5e971559293cd08`  
		Last Modified: Tue, 12 Apr 2022 20:11:35 GMT  
		Size: 46.8 MB (46806935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694b4ff209cd89703c3efd09e664c43367dc9a4e9d6fe83fa7fbfc578126ed6c`  
		Last Modified: Tue, 12 Apr 2022 20:11:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.2-ubuntu`

```console
$ docker pull kong@sha256:9547499e0db869d571fb76c9e65186a2209bdc2f4022a19d97ac129b9f5cef52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d50ccbfbbf0058ab4e4dbc26727ee1f051fd850a73c0389ccd89d85d055bde13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128089282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b25366321406d551fe15b9c128d8d93ae121d70743a0ca0c9bea69db7b63ac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:26:55 GMT
ARG KONG_VERSION=2.7.2
# Tue, 07 Jun 2022 00:26:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:21:01 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 14 Jun 2022 23:21:01 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 14 Jun 2022 23:21:23 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:21:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:21:24 GMT
USER kong
# Tue, 14 Jun 2022 23:21:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:21:24 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:21:24 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:21:24 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:21:24 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f40ef21bcbfbfddd22aaa8c284036f53c749c2ce6aaaf483b2984b15140ee08`  
		Last Modified: Tue, 14 Jun 2022 23:24:01 GMT  
		Size: 74.4 MB (74433808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13147babdcbaf37d0add6eed3e252f5726db6a53fb32a7544f92ae934097ef1f`  
		Last Modified: Tue, 14 Jun 2022 23:23:49 GMT  
		Size: 879.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:288e255e36500d19d5e2c8638533629382eb9246b298ebfb8d57bec058d167bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125134863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08324449eb0cd5ffa32fbb4d8036a3fba00eeabf8da9699c2307bc667975278`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:41:54 GMT
ARG KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:41:55 GMT
ENV KONG_VERSION=2.7.2
# Tue, 14 Jun 2022 23:41:56 GMT
ARG KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc
# Tue, 14 Jun 2022 23:41:57 GMT
ARG KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
# Tue, 14 Jun 2022 23:42:37 GMT
# ARGS: KONG_AMD64_SHA=8124ddbfe80a1627b19a54e14b20ff0e176549699491cf5c61a4f0355470f8fc KONG_ARM64_SHA=f40e616539ab64cb4fd333d19895ec9768b742bc25e5f2dbcb7f162bf90421d8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:42:39 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:42:39 GMT
USER kong
# Tue, 14 Jun 2022 23:42:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:42:41 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:42:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:42:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:42:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e210ba2a0418dcc22653325535fe628a771663eb3d502d910071f83bba73914d`  
		Last Modified: Tue, 14 Jun 2022 23:46:56 GMT  
		Size: 72.9 MB (72860810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db5446eb906fe4ad4cc3845b976b3f163473fb069894b88e61b3417c1f624e3`  
		Last Modified: Tue, 14 Jun 2022 23:46:44 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:ccd3afeabf26a2374e9568cf0f61b861d80682335194d7bed87d318af6ef4715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:00fc002b10478a139e4fb78039e1be09d6e142b796949dcb0e4383f218655093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49323979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e457308de474df0374bc9806cfd5a2ed0d22ff349755c39f9efb3f418353556f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:20:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:20:05 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:20:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:20:05 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:05 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:20:14 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:20:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:15 GMT
USER kong
# Tue, 14 Jun 2022 23:20:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:15 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4a0f94ff505e724dea49d4258ec459689de32f04b8d9ded7f3411a722d3a`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6cc27046536b1c86842b2d9707c65497a25b3992b4f73f9220872c6ce2450`  
		Last Modified: Tue, 14 Jun 2022 23:23:08 GMT  
		Size: 46.5 MB (46524082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99d957fe7c2031bad3f2e33dbd73bce1d00acb8d71cac06422e08d0ceed794e`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:64267576731e74289828538851030ec834a559e14fa363f4ca05ebafbedaa5d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1864ea8724748393f5f25914e8a4528a63e66fbfedf8d18310f136e43e5c4ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:40:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:40:12 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:13 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:14 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:40:16 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:17 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:18 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:40:19 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:40:29 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:40:30 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:40:30 GMT
USER kong
# Tue, 14 Jun 2022 23:40:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:40:32 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:40:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:40:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476f8dce6828a8607533bcb3deb56a868f64719e0474630bc8d40cb78889970`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cc504b1a59567621f131f2088eb3f540a068f841f8e5e153c6ae9a654496c`  
		Last Modified: Tue, 14 Jun 2022 23:45:57 GMT  
		Size: 45.8 MB (45811466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d8f9b8280aaccbbec32b89c6867f1392fd1950147c40f7e6c4bc4cb87a705c`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:27ba987186ac8913235d0bea44433e295511b776e37cc24cad69be56659b44c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5d2559d9967e39a7c0285643a484dc59a434a3dcc73b66183b4d9811ba81bb95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121229036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9348939116e58d77efb379d00687a58a85516ea07a901e5ce6f610ae2ce4ce68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:20:55 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:20:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:55 GMT
USER kong
# Tue, 14 Jun 2022 23:20:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4724d8b04ccf412df4c2eab1db30e216e64b5c7753529b193353c2ba6c8a0b0`  
		Last Modified: Tue, 14 Jun 2022 23:23:36 GMT  
		Size: 67.6 MB (67573561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de5e8494dca4441e0ee102c3ef5807cd89429f162901e8e26c43625fab30f8`  
		Last Modified: Tue, 14 Jun 2022 23:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d35bf65fd2f20eac2327eedb0ad547d92ff8dc60ef0fbd382a72b2e90ee872ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121726118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26405f0174d52a4756cb1ca6e56ab10d1323b68a9697f02b56213d57c47e5f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:40:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:47 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:48 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:40:49 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:41:31 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:41:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:41:32 GMT
USER kong
# Tue, 14 Jun 2022 23:41:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:41:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:41:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:41:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:41:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66957df71376f98a0e8eb085ef05d9bd8e0647ee35f7576de662cfeed4227cdd`  
		Last Modified: Tue, 14 Jun 2022 23:46:28 GMT  
		Size: 69.5 MB (69452065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b313f50a105849eb0f70997fd0b89b8499f1d2ad74d56b0d467902d67f1bd1`  
		Last Modified: Tue, 14 Jun 2022 23:46:16 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1`

```console
$ docker pull kong@sha256:ccd3afeabf26a2374e9568cf0f61b861d80682335194d7bed87d318af6ef4715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1` - linux; amd64

```console
$ docker pull kong@sha256:00fc002b10478a139e4fb78039e1be09d6e142b796949dcb0e4383f218655093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49323979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e457308de474df0374bc9806cfd5a2ed0d22ff349755c39f9efb3f418353556f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:20:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:20:05 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:20:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:20:05 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:05 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:20:14 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:20:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:15 GMT
USER kong
# Tue, 14 Jun 2022 23:20:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:15 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4a0f94ff505e724dea49d4258ec459689de32f04b8d9ded7f3411a722d3a`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6cc27046536b1c86842b2d9707c65497a25b3992b4f73f9220872c6ce2450`  
		Last Modified: Tue, 14 Jun 2022 23:23:08 GMT  
		Size: 46.5 MB (46524082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99d957fe7c2031bad3f2e33dbd73bce1d00acb8d71cac06422e08d0ceed794e`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:64267576731e74289828538851030ec834a559e14fa363f4ca05ebafbedaa5d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1864ea8724748393f5f25914e8a4528a63e66fbfedf8d18310f136e43e5c4ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:40:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:40:12 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:13 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:14 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:40:16 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:17 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:18 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:40:19 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:40:29 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:40:30 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:40:30 GMT
USER kong
# Tue, 14 Jun 2022 23:40:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:40:32 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:40:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:40:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476f8dce6828a8607533bcb3deb56a868f64719e0474630bc8d40cb78889970`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cc504b1a59567621f131f2088eb3f540a068f841f8e5e153c6ae9a654496c`  
		Last Modified: Tue, 14 Jun 2022 23:45:57 GMT  
		Size: 45.8 MB (45811466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d8f9b8280aaccbbec32b89c6867f1392fd1950147c40f7e6c4bc4cb87a705c`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-alpine`

```console
$ docker pull kong@sha256:ccd3afeabf26a2374e9568cf0f61b861d80682335194d7bed87d318af6ef4715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:00fc002b10478a139e4fb78039e1be09d6e142b796949dcb0e4383f218655093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49323979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e457308de474df0374bc9806cfd5a2ed0d22ff349755c39f9efb3f418353556f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:20:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:20:05 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:20:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:20:05 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:05 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:20:14 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:20:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:15 GMT
USER kong
# Tue, 14 Jun 2022 23:20:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:15 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4a0f94ff505e724dea49d4258ec459689de32f04b8d9ded7f3411a722d3a`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6cc27046536b1c86842b2d9707c65497a25b3992b4f73f9220872c6ce2450`  
		Last Modified: Tue, 14 Jun 2022 23:23:08 GMT  
		Size: 46.5 MB (46524082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99d957fe7c2031bad3f2e33dbd73bce1d00acb8d71cac06422e08d0ceed794e`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:64267576731e74289828538851030ec834a559e14fa363f4ca05ebafbedaa5d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1864ea8724748393f5f25914e8a4528a63e66fbfedf8d18310f136e43e5c4ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:40:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:40:12 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:13 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:14 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:40:16 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:17 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:18 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:40:19 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:40:29 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:40:30 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:40:30 GMT
USER kong
# Tue, 14 Jun 2022 23:40:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:40:32 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:40:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:40:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476f8dce6828a8607533bcb3deb56a868f64719e0474630bc8d40cb78889970`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cc504b1a59567621f131f2088eb3f540a068f841f8e5e153c6ae9a654496c`  
		Last Modified: Tue, 14 Jun 2022 23:45:57 GMT  
		Size: 45.8 MB (45811466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d8f9b8280aaccbbec32b89c6867f1392fd1950147c40f7e6c4bc4cb87a705c`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.1-ubuntu`

```console
$ docker pull kong@sha256:27ba987186ac8913235d0bea44433e295511b776e37cc24cad69be56659b44c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5d2559d9967e39a7c0285643a484dc59a434a3dcc73b66183b4d9811ba81bb95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121229036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9348939116e58d77efb379d00687a58a85516ea07a901e5ce6f610ae2ce4ce68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:20:55 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:20:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:55 GMT
USER kong
# Tue, 14 Jun 2022 23:20:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4724d8b04ccf412df4c2eab1db30e216e64b5c7753529b193353c2ba6c8a0b0`  
		Last Modified: Tue, 14 Jun 2022 23:23:36 GMT  
		Size: 67.6 MB (67573561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de5e8494dca4441e0ee102c3ef5807cd89429f162901e8e26c43625fab30f8`  
		Last Modified: Tue, 14 Jun 2022 23:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d35bf65fd2f20eac2327eedb0ad547d92ff8dc60ef0fbd382a72b2e90ee872ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121726118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26405f0174d52a4756cb1ca6e56ab10d1323b68a9697f02b56213d57c47e5f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:40:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:47 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:48 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:40:49 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:41:31 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:41:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:41:32 GMT
USER kong
# Tue, 14 Jun 2022 23:41:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:41:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:41:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:41:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:41:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66957df71376f98a0e8eb085ef05d9bd8e0647ee35f7576de662cfeed4227cdd`  
		Last Modified: Tue, 14 Jun 2022 23:46:28 GMT  
		Size: 69.5 MB (69452065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b313f50a105849eb0f70997fd0b89b8499f1d2ad74d56b0d467902d67f1bd1`  
		Last Modified: Tue, 14 Jun 2022 23:46:16 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:ccd3afeabf26a2374e9568cf0f61b861d80682335194d7bed87d318af6ef4715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:00fc002b10478a139e4fb78039e1be09d6e142b796949dcb0e4383f218655093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49323979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e457308de474df0374bc9806cfd5a2ed0d22ff349755c39f9efb3f418353556f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:20:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:20:05 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:20:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:20:05 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:05 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:20:14 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:20:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:15 GMT
USER kong
# Tue, 14 Jun 2022 23:20:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:15 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4a0f94ff505e724dea49d4258ec459689de32f04b8d9ded7f3411a722d3a`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6cc27046536b1c86842b2d9707c65497a25b3992b4f73f9220872c6ce2450`  
		Last Modified: Tue, 14 Jun 2022 23:23:08 GMT  
		Size: 46.5 MB (46524082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99d957fe7c2031bad3f2e33dbd73bce1d00acb8d71cac06422e08d0ceed794e`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:64267576731e74289828538851030ec834a559e14fa363f4ca05ebafbedaa5d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1864ea8724748393f5f25914e8a4528a63e66fbfedf8d18310f136e43e5c4ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:40:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:40:12 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:13 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:14 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:40:16 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:17 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:18 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:40:19 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:40:29 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:40:30 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:40:30 GMT
USER kong
# Tue, 14 Jun 2022 23:40:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:40:32 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:40:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:40:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476f8dce6828a8607533bcb3deb56a868f64719e0474630bc8d40cb78889970`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cc504b1a59567621f131f2088eb3f540a068f841f8e5e153c6ae9a654496c`  
		Last Modified: Tue, 14 Jun 2022 23:45:57 GMT  
		Size: 45.8 MB (45811466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d8f9b8280aaccbbec32b89c6867f1392fd1950147c40f7e6c4bc4cb87a705c`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:ccd3afeabf26a2374e9568cf0f61b861d80682335194d7bed87d318af6ef4715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:00fc002b10478a139e4fb78039e1be09d6e142b796949dcb0e4383f218655093
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49323979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e457308de474df0374bc9806cfd5a2ed0d22ff349755c39f9efb3f418353556f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:20:05 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:20:05 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:20:05 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:20:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:20:05 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:05 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:20:06 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:20:14 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:20:15 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:15 GMT
USER kong
# Tue, 14 Jun 2022 23:20:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:15 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cade4a0f94ff505e724dea49d4258ec459689de32f04b8d9ded7f3411a722d3a`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6cc27046536b1c86842b2d9707c65497a25b3992b4f73f9220872c6ce2450`  
		Last Modified: Tue, 14 Jun 2022 23:23:08 GMT  
		Size: 46.5 MB (46524082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99d957fe7c2031bad3f2e33dbd73bce1d00acb8d71cac06422e08d0ceed794e`  
		Last Modified: Tue, 14 Jun 2022 23:23:01 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:64267576731e74289828538851030ec834a559e14fa363f4ca05ebafbedaa5d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48506941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1864ea8724748393f5f25914e8a4528a63e66fbfedf8d18310f136e43e5c4ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Tue, 14 Jun 2022 23:40:11 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 14 Jun 2022 23:40:12 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:13 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:14 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:16 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 14 Jun 2022 23:40:16 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:17 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:18 GMT
ARG KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0
# Tue, 14 Jun 2022 23:40:19 GMT
ARG KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
# Tue, 14 Jun 2022 23:40:29 GMT
# ARGS: KONG_AMD64_SHA=ccda33bf02803b6b8dd46b22990f92265fe61d900ba94e3e0fa26db0433098c0 KONG_ARM64_SHA=d21690332a89adf9900f7266e083f41f565eb009f2771ef112f3564878eeff53
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 14 Jun 2022 23:40:30 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:40:30 GMT
USER kong
# Tue, 14 Jun 2022 23:40:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:40:32 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:40:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:40:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0476f8dce6828a8607533bcb3deb56a868f64719e0474630bc8d40cb78889970`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cc504b1a59567621f131f2088eb3f540a068f841f8e5e153c6ae9a654496c`  
		Last Modified: Tue, 14 Jun 2022 23:45:57 GMT  
		Size: 45.8 MB (45811466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d8f9b8280aaccbbec32b89c6867f1392fd1950147c40f7e6c4bc4cb87a705c`  
		Last Modified: Tue, 14 Jun 2022 23:45:48 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:27ba987186ac8913235d0bea44433e295511b776e37cc24cad69be56659b44c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5d2559d9967e39a7c0285643a484dc59a434a3dcc73b66183b4d9811ba81bb95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121229036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9348939116e58d77efb379d00687a58a85516ea07a901e5ce6f610ae2ce4ce68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:25:49 GMT
ARG ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ENV ASSET=ce
# Tue, 07 Jun 2022 00:25:50 GMT
ARG EE_PORTS
# Tue, 07 Jun 2022 00:25:50 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 07 Jun 2022 00:25:50 GMT
ARG KONG_VERSION=2.8.1
# Tue, 07 Jun 2022 00:25:50 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:20:19 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:20:55 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:20:55 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:20:55 GMT
USER kong
# Tue, 14 Jun 2022 23:20:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:20:56 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:20:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:20:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:20:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a98d6d56529c16f261415f31709ae633666ee56cd5a645f459dfcf5ec555de`  
		Last Modified: Tue, 07 Jun 2022 00:29:41 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4724d8b04ccf412df4c2eab1db30e216e64b5c7753529b193353c2ba6c8a0b0`  
		Last Modified: Tue, 14 Jun 2022 23:23:36 GMT  
		Size: 67.6 MB (67573561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de5e8494dca4441e0ee102c3ef5807cd89429f162901e8e26c43625fab30f8`  
		Last Modified: Tue, 14 Jun 2022 23:23:25 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d35bf65fd2f20eac2327eedb0ad547d92ff8dc60ef0fbd382a72b2e90ee872ff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121726118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26405f0174d52a4756cb1ca6e56ab10d1323b68a9697f02b56213d57c47e5f7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:15 GMT
ADD file:8bb0809a8ac8e978274cf731cff7529372088d22c5b0233a28f01ef414aefbca in / 
# Tue, 07 Jun 2022 01:25:16 GMT
CMD ["bash"]
# Tue, 14 Jun 2022 23:40:42 GMT
ARG ASSET=ce
# Tue, 14 Jun 2022 23:40:43 GMT
ENV ASSET=ce
# Tue, 14 Jun 2022 23:40:44 GMT
ARG EE_PORTS
# Tue, 14 Jun 2022 23:40:46 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 14 Jun 2022 23:40:46 GMT
ARG KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:47 GMT
ENV KONG_VERSION=2.8.1
# Tue, 14 Jun 2022 23:40:48 GMT
ARG KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361
# Tue, 14 Jun 2022 23:40:49 GMT
ARG KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
# Tue, 14 Jun 2022 23:41:31 GMT
# ARGS: KONG_AMD64_SHA=10d12d23e5890414d666663094d51a42de41f8a9806fbc0baaf9ac4d37794361 KONG_ARM64_SHA=61c13219ef64dac9aeae5ae775411e8cfcd406f068cf3e75d463f916ae6513cb
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 14 Jun 2022 23:41:32 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 14 Jun 2022 23:41:32 GMT
USER kong
# Tue, 14 Jun 2022 23:41:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jun 2022 23:41:34 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 14 Jun 2022 23:41:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Jun 2022 23:41:36 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 14 Jun 2022 23:41:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:11e23ac719b33170b39b7e30b8027dc09c9cbad6b503b2b6b3ebbd9d33f4adad`  
		Last Modified: Thu, 02 Jun 2022 08:33:07 GMT  
		Size: 27.2 MB (27191210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7affe9ac42c644d3c68131c471c8ef36152d0e9fa8700ec3273b5f9a7db4fde`  
		Last Modified: Tue, 14 Jun 2022 23:46:19 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66957df71376f98a0e8eb085ef05d9bd8e0647ee35f7576de662cfeed4227cdd`  
		Last Modified: Tue, 14 Jun 2022 23:46:28 GMT  
		Size: 69.5 MB (69452065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b313f50a105849eb0f70997fd0b89b8499f1d2ad74d56b0d467902d67f1bd1`  
		Last Modified: Tue, 14 Jun 2022 23:46:16 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
