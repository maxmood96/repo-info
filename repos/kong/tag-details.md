<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.5-ubuntu`](#kong285-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.4`](#kong34)
-	[`kong:3.4-ubuntu`](#kong34-ubuntu)
-	[`kong:3.4.2`](#kong342)
-	[`kong:3.4.2-ubuntu`](#kong342-ubuntu)
-	[`kong:3.8`](#kong38)
-	[`kong:3.8-ubuntu`](#kong38-ubuntu)
-	[`kong:3.8.0`](#kong380)
-	[`kong:3.8.0-ubuntu`](#kong380-ubuntu)
-	[`kong:3.9`](#kong39)
-	[`kong:3.9-ubuntu`](#kong39-ubuntu)
-	[`kong:3.9.1`](#kong391)
-	[`kong:3.9.1-ubuntu`](#kong391-ubuntu)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:beb4b9506e2cb8e4615e29acf1b2f592dd82fde87d481dcfee04642ed53089cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2c7acf3e4fc93bf7af3a9d70c09f6369bfb5373ea70927382d613965c70c6830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185245126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa40df4d0779c08b8e7f6365df062cb66baeb74a0c35eed03aca546a7e1480d6`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487af8cc105485e7372d0c58eec9818c50b36f2bec022f65f3c6ffc167dd7199`  
		Last Modified: Tue, 02 Sep 2025 00:22:18 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b575259c30f029013b016e7bab6bdd5684659bc183f108fdab96e48251b43d`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 130.6 MB (130625342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ecc199431aa6d1b006d2011c35ac05a1c0a1e3cda0effb9055d16030023b3e`  
		Last Modified: Tue, 02 Sep 2025 00:22:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c84f9b3f7864fe4365c4561963fab041d5a41e6a1ca9374fd0593d7ca57f3244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3114959927b45333c98133ad95038e83eca0e215db9a0f8513e7f82ce098b25`

```dockerfile
```

-	Layers:
	-	`sha256:4d7937da6501ce01a30dfc748407696ea91d0d175b735f7431efc2c5bafd6647`  
		Last Modified: Tue, 02 Sep 2025 02:51:18 GMT  
		Size: 7.3 MB (7347718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcc8b60f592f89701140eebef4b7abee251390255736e1f15a7177925837c143`  
		Last Modified: Tue, 02 Sep 2025 02:51:19 GMT  
		Size: 14.5 KB (14486 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:beb4b9506e2cb8e4615e29acf1b2f592dd82fde87d481dcfee04642ed53089cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2c7acf3e4fc93bf7af3a9d70c09f6369bfb5373ea70927382d613965c70c6830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185245126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa40df4d0779c08b8e7f6365df062cb66baeb74a0c35eed03aca546a7e1480d6`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487af8cc105485e7372d0c58eec9818c50b36f2bec022f65f3c6ffc167dd7199`  
		Last Modified: Tue, 02 Sep 2025 00:22:18 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b575259c30f029013b016e7bab6bdd5684659bc183f108fdab96e48251b43d`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 130.6 MB (130625342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ecc199431aa6d1b006d2011c35ac05a1c0a1e3cda0effb9055d16030023b3e`  
		Last Modified: Tue, 02 Sep 2025 00:22:16 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c84f9b3f7864fe4365c4561963fab041d5a41e6a1ca9374fd0593d7ca57f3244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3114959927b45333c98133ad95038e83eca0e215db9a0f8513e7f82ce098b25`

```dockerfile
```

-	Layers:
	-	`sha256:4d7937da6501ce01a30dfc748407696ea91d0d175b735f7431efc2c5bafd6647`  
		Last Modified: Tue, 02 Sep 2025 02:51:18 GMT  
		Size: 7.3 MB (7347718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcc8b60f592f89701140eebef4b7abee251390255736e1f15a7177925837c143`  
		Last Modified: Tue, 02 Sep 2025 02:51:19 GMT  
		Size: 14.5 KB (14486 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:30597ffe2fc98160b979311d18f7649edd1ed3bf145063e99b1ef89775a668d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:4c19d5e04a76d2ae7df943a376ace1c3e23beaed5236adc4c0e87aac1c665d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38930d56606d4e6c271cce8c63b4bf401a728c8887517ebb0ea15823411cd51b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a737aeb4167a859699887d661b37d589e3912ec02074d61c9874d05dffce9`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd7d3d0fb9226e4d5f77687f5c6ff36bb9dd1d1add48fa190ab6aa5f66926f`  
		Last Modified: Mon, 15 Sep 2025 22:20:01 GMT  
		Size: 90.7 MB (90683414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30bba013e8ad37a8eefab77989731e08963276c2b67790edf321591f2a25ae`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:2fef901c98c46906a1354c398f4bac15fd535f413fb1b7fb1226964801e2c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900359cfd9dd50cf616c65d415c62228193851fd8b3ccbc50ca6fe9af4e39654`

```dockerfile
```

-	Layers:
	-	`sha256:7aab9f71b6b92b83016eba41bc8aebad9641898b5bfa9989d6d7de910cf6198b`  
		Last Modified: Mon, 15 Sep 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0125d3b6f729fe5019e34209322e91d0ab2f975dcc3c4fb9533f757fc115d36`  
		Last Modified: Mon, 15 Sep 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d86a6b9a4b3faec087553390345c2031dea5cb9debcf932f5e43faee0beb97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9c7a014f198480b766b5ce5ed41186b357e2e5c60c94c8b3929484850d2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086a091e2e1c2a02d87a8e877d82423698cec857fbbdeb1da6d5228b8855c00`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6068b25573db1ae2c976e98bf35c9a3842e28bbee1cc9c62896d24e5f642e5c`  
		Last Modified: Thu, 02 Oct 2025 01:25:06 GMT  
		Size: 92.2 MB (92229492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f0ef82511f19628f19bacaba5f2349580bd3e55ace63e3ab4e0a217d45860`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:82df75418b58a6cb1e5047fea79d2f2cad8cd772e74a2d38148c590fc0beffc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd82f42126f80f41756ee10d8dfb7eeae8cc26af48eddb9fe7c045baeb88a55`

```dockerfile
```

-	Layers:
	-	`sha256:a064f1c26d8055f0cb3784ccf93a4954f27f39da3d9329d9c2a498c39e67172f`  
		Last Modified: Thu, 02 Oct 2025 02:51:22 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429a20f1215dd81cf6717a62dc17d3a905ac39afcd1c1d61e0484eefd645cbcd`  
		Last Modified: Thu, 02 Oct 2025 02:51:23 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:10bd90f1e7e9c5c3dafc2be4802de36fd9b205a198d65d21442e46a7183eaa2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:05421491851c41a796d22721770f6485bac3b24727a6928bb8c1e30b712cee52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92275381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d649a27c3b5fb6e8be8af3491dc98dcae334e15782ba1340a9ee071cf665fc`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67d807cccfa32d330d5e8682cf626892a350dc0b1265d72bcf29b50599c00c`  
		Last Modified: Mon, 01 Sep 2025 23:46:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee5e13d19ae48b52740f0ded1133a99dc9b0608ee05d1072fd44de8faa8f2b9`  
		Last Modified: Tue, 02 Sep 2025 02:52:04 GMT  
		Size: 62.7 MB (62737161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ace93a63517de5a4b032c75d99e76e4c4e357a2708d5742f0b3e7d3e6ff0e06`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:cb824842772c21a8c7f5b177342be4f635d01e9945ab2113aa8bcff1863c06b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3350d797b1309d080d4b66d12641efe94ce2f8565af71e77b3d1642fd8b922e6`

```dockerfile
```

-	Layers:
	-	`sha256:05d092f2e3540d48068e69a681bc724685ed879a8a9ec9fc3cc4ab1508fb924b`  
		Last Modified: Tue, 02 Sep 2025 02:51:26 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1c371a7338141cb64b21aeb6bfbce094aeac34e282021b42b29d1d048c6a1d`  
		Last Modified: Tue, 02 Sep 2025 02:51:27 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3559030056713a6abeada341445c7c199caa7052bf65b9bc49ada1803b913d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88584268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ce4925c088aee491fd91540a540b5c30d9e6bade5b06dbb8ac3249962e0e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47434bf502c669d95107dc51c5c58d0f0f64ab263e9456c9a6fe5f2ab6f3b593`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72784660d74ec50ce0ce1416474fb1f51ee94bd9e297cef3179e252ba625aeb`  
		Last Modified: Thu, 02 Oct 2025 01:25:03 GMT  
		Size: 61.2 MB (61199879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86ca58e35b8411a2c9b00b6dc47832491f7d3a873d08e7fd8a240293552748`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:6ff25837c352f4acabefd68a435270685c3a597a7252e0df88444206c4071e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb497b36ae7f60ff96c58dda0229e90708c32d490b62791525177b51ed957cd`

```dockerfile
```

-	Layers:
	-	`sha256:1296d7d4ff88a0ef15e4a013c6d8ade66c8e2013b3d34fc27e5d5d1d2f1d8425`  
		Last Modified: Thu, 02 Oct 2025 02:51:27 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929a8f45e069d23a4b8e515dddfe3a1112519c598718920b00e188eac58dd1c`  
		Last Modified: Thu, 02 Oct 2025 02:51:28 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:10bd90f1e7e9c5c3dafc2be4802de36fd9b205a198d65d21442e46a7183eaa2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:05421491851c41a796d22721770f6485bac3b24727a6928bb8c1e30b712cee52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92275381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d649a27c3b5fb6e8be8af3491dc98dcae334e15782ba1340a9ee071cf665fc`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67d807cccfa32d330d5e8682cf626892a350dc0b1265d72bcf29b50599c00c`  
		Last Modified: Mon, 01 Sep 2025 23:46:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee5e13d19ae48b52740f0ded1133a99dc9b0608ee05d1072fd44de8faa8f2b9`  
		Last Modified: Tue, 02 Sep 2025 02:52:04 GMT  
		Size: 62.7 MB (62737161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ace93a63517de5a4b032c75d99e76e4c4e357a2708d5742f0b3e7d3e6ff0e06`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:cb824842772c21a8c7f5b177342be4f635d01e9945ab2113aa8bcff1863c06b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3350d797b1309d080d4b66d12641efe94ce2f8565af71e77b3d1642fd8b922e6`

```dockerfile
```

-	Layers:
	-	`sha256:05d092f2e3540d48068e69a681bc724685ed879a8a9ec9fc3cc4ab1508fb924b`  
		Last Modified: Tue, 02 Sep 2025 02:51:26 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1c371a7338141cb64b21aeb6bfbce094aeac34e282021b42b29d1d048c6a1d`  
		Last Modified: Tue, 02 Sep 2025 02:51:27 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3559030056713a6abeada341445c7c199caa7052bf65b9bc49ada1803b913d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88584268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ce4925c088aee491fd91540a540b5c30d9e6bade5b06dbb8ac3249962e0e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47434bf502c669d95107dc51c5c58d0f0f64ab263e9456c9a6fe5f2ab6f3b593`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72784660d74ec50ce0ce1416474fb1f51ee94bd9e297cef3179e252ba625aeb`  
		Last Modified: Thu, 02 Oct 2025 01:25:03 GMT  
		Size: 61.2 MB (61199879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86ca58e35b8411a2c9b00b6dc47832491f7d3a873d08e7fd8a240293552748`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:6ff25837c352f4acabefd68a435270685c3a597a7252e0df88444206c4071e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb497b36ae7f60ff96c58dda0229e90708c32d490b62791525177b51ed957cd`

```dockerfile
```

-	Layers:
	-	`sha256:1296d7d4ff88a0ef15e4a013c6d8ade66c8e2013b3d34fc27e5d5d1d2f1d8425`  
		Last Modified: Thu, 02 Oct 2025 02:51:27 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929a8f45e069d23a4b8e515dddfe3a1112519c598718920b00e188eac58dd1c`  
		Last Modified: Thu, 02 Oct 2025 02:51:28 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:10bd90f1e7e9c5c3dafc2be4802de36fd9b205a198d65d21442e46a7183eaa2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:05421491851c41a796d22721770f6485bac3b24727a6928bb8c1e30b712cee52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92275381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d649a27c3b5fb6e8be8af3491dc98dcae334e15782ba1340a9ee071cf665fc`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67d807cccfa32d330d5e8682cf626892a350dc0b1265d72bcf29b50599c00c`  
		Last Modified: Mon, 01 Sep 2025 23:46:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee5e13d19ae48b52740f0ded1133a99dc9b0608ee05d1072fd44de8faa8f2b9`  
		Last Modified: Tue, 02 Sep 2025 02:52:04 GMT  
		Size: 62.7 MB (62737161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ace93a63517de5a4b032c75d99e76e4c4e357a2708d5742f0b3e7d3e6ff0e06`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:cb824842772c21a8c7f5b177342be4f635d01e9945ab2113aa8bcff1863c06b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3350d797b1309d080d4b66d12641efe94ce2f8565af71e77b3d1642fd8b922e6`

```dockerfile
```

-	Layers:
	-	`sha256:05d092f2e3540d48068e69a681bc724685ed879a8a9ec9fc3cc4ab1508fb924b`  
		Last Modified: Tue, 02 Sep 2025 02:51:26 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1c371a7338141cb64b21aeb6bfbce094aeac34e282021b42b29d1d048c6a1d`  
		Last Modified: Tue, 02 Sep 2025 02:51:27 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3559030056713a6abeada341445c7c199caa7052bf65b9bc49ada1803b913d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88584268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ce4925c088aee491fd91540a540b5c30d9e6bade5b06dbb8ac3249962e0e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47434bf502c669d95107dc51c5c58d0f0f64ab263e9456c9a6fe5f2ab6f3b593`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72784660d74ec50ce0ce1416474fb1f51ee94bd9e297cef3179e252ba625aeb`  
		Last Modified: Thu, 02 Oct 2025 01:25:03 GMT  
		Size: 61.2 MB (61199879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86ca58e35b8411a2c9b00b6dc47832491f7d3a873d08e7fd8a240293552748`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:6ff25837c352f4acabefd68a435270685c3a597a7252e0df88444206c4071e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb497b36ae7f60ff96c58dda0229e90708c32d490b62791525177b51ed957cd`

```dockerfile
```

-	Layers:
	-	`sha256:1296d7d4ff88a0ef15e4a013c6d8ade66c8e2013b3d34fc27e5d5d1d2f1d8425`  
		Last Modified: Thu, 02 Oct 2025 02:51:27 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929a8f45e069d23a4b8e515dddfe3a1112519c598718920b00e188eac58dd1c`  
		Last Modified: Thu, 02 Oct 2025 02:51:28 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:10bd90f1e7e9c5c3dafc2be4802de36fd9b205a198d65d21442e46a7183eaa2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:05421491851c41a796d22721770f6485bac3b24727a6928bb8c1e30b712cee52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92275381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d649a27c3b5fb6e8be8af3491dc98dcae334e15782ba1340a9ee071cf665fc`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67d807cccfa32d330d5e8682cf626892a350dc0b1265d72bcf29b50599c00c`  
		Last Modified: Mon, 01 Sep 2025 23:46:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee5e13d19ae48b52740f0ded1133a99dc9b0608ee05d1072fd44de8faa8f2b9`  
		Last Modified: Tue, 02 Sep 2025 02:52:04 GMT  
		Size: 62.7 MB (62737161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ace93a63517de5a4b032c75d99e76e4c4e357a2708d5742f0b3e7d3e6ff0e06`  
		Last Modified: Mon, 01 Sep 2025 23:46:43 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:cb824842772c21a8c7f5b177342be4f635d01e9945ab2113aa8bcff1863c06b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3350d797b1309d080d4b66d12641efe94ce2f8565af71e77b3d1642fd8b922e6`

```dockerfile
```

-	Layers:
	-	`sha256:05d092f2e3540d48068e69a681bc724685ed879a8a9ec9fc3cc4ab1508fb924b`  
		Last Modified: Tue, 02 Sep 2025 02:51:26 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de1c371a7338141cb64b21aeb6bfbce094aeac34e282021b42b29d1d048c6a1d`  
		Last Modified: Tue, 02 Sep 2025 02:51:27 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3559030056713a6abeada341445c7c199caa7052bf65b9bc49ada1803b913d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88584268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ce4925c088aee491fd91540a540b5c30d9e6bade5b06dbb8ac3249962e0e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47434bf502c669d95107dc51c5c58d0f0f64ab263e9456c9a6fe5f2ab6f3b593`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72784660d74ec50ce0ce1416474fb1f51ee94bd9e297cef3179e252ba625aeb`  
		Last Modified: Thu, 02 Oct 2025 01:25:03 GMT  
		Size: 61.2 MB (61199879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86ca58e35b8411a2c9b00b6dc47832491f7d3a873d08e7fd8a240293552748`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:6ff25837c352f4acabefd68a435270685c3a597a7252e0df88444206c4071e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb497b36ae7f60ff96c58dda0229e90708c32d490b62791525177b51ed957cd`

```dockerfile
```

-	Layers:
	-	`sha256:1296d7d4ff88a0ef15e4a013c6d8ade66c8e2013b3d34fc27e5d5d1d2f1d8425`  
		Last Modified: Thu, 02 Oct 2025 02:51:27 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929a8f45e069d23a4b8e515dddfe3a1112519c598718920b00e188eac58dd1c`  
		Last Modified: Thu, 02 Oct 2025 02:51:28 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:ddd6a4132429a75f4f16624232d9522a6417bb8605a119a1aa8e8acb61153939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:f7a53565cf35425cf949cdc9d378c0aeed82b0e63ca76d003ff0d77256f7acfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05facc9141bc34d09d9eb14d0fb2fc9e83da24995bbb01841fc0e09170a67771`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69fdc95cc22a965412d881dbbe03be202c34c4884f9ef61d7b23a0ee10e5dae`  
		Last Modified: Tue, 02 Sep 2025 00:19:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe400747c25841953b7cbcae4a563be95610b01b260426ffa1364b5fdfcc9f5`  
		Last Modified: Tue, 02 Sep 2025 00:19:51 GMT  
		Size: 88.0 MB (88008897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad893804ee541d2ec5e132d86fae2e3cc712e934d5b5c8ea3b8ae1178f819506`  
		Last Modified: Tue, 02 Sep 2025 00:19:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:913f34c8c27653219a84112a6f9161d3c8c96f1a00aeb22e842666529b132598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe63802bfd4ee9033ccbe702f40014715459f4874180efd15dd32ad6a6710a48`

```dockerfile
```

-	Layers:
	-	`sha256:6c6a22bbe112faa95eff45138cd315a4e7dc40440c19960eaab549f1910b862c`  
		Last Modified: Tue, 02 Sep 2025 02:51:32 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe2fb1c8c9418b40b324f2b12a579ac35082e2f24b4b7fde29be74843ca0042`  
		Last Modified: Tue, 02 Sep 2025 02:51:33 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:00bcb1d6d2387431b80bc9ba15750b62a9c71dcfb4c366d9ebd1f15a1241fb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377e4a788ccecb7ffce6de75d6515dae4882073788e3e4d6708014c8af3b17f`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949273f4e970672a127ace61c92f81f44dbffdf72658e45fc61f400f7faf13ed`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b4c898a3fe17a62b9b6b98c16d71d79afc21b938a4542c199ee07831a2e72`  
		Last Modified: Thu, 02 Oct 2025 03:00:19 GMT  
		Size: 87.3 MB (87288753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43350dce70d6057816696573088ffbbf7ad09dad213b371045e682e018aecdc7`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:9637d8a6e47598df42c530d9291cdd295e00ad01db774cf9d0329f64d43e8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d3442492c15262e8c4b84bd8c5cd55e98a611e2122cb56bcf5fca115b22de`

```dockerfile
```

-	Layers:
	-	`sha256:cce72a388571b32b0aa26b8069576ecbc150345bd022f9b785166139ef67b445`  
		Last Modified: Thu, 02 Oct 2025 02:51:41 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79166d0edf21eb7ab069f03a3db3b98582e00959a53b1c880a367ca14c63db03`  
		Last Modified: Thu, 02 Oct 2025 02:51:42 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:ddd6a4132429a75f4f16624232d9522a6417bb8605a119a1aa8e8acb61153939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f7a53565cf35425cf949cdc9d378c0aeed82b0e63ca76d003ff0d77256f7acfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05facc9141bc34d09d9eb14d0fb2fc9e83da24995bbb01841fc0e09170a67771`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69fdc95cc22a965412d881dbbe03be202c34c4884f9ef61d7b23a0ee10e5dae`  
		Last Modified: Tue, 02 Sep 2025 00:19:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe400747c25841953b7cbcae4a563be95610b01b260426ffa1364b5fdfcc9f5`  
		Last Modified: Tue, 02 Sep 2025 00:19:51 GMT  
		Size: 88.0 MB (88008897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad893804ee541d2ec5e132d86fae2e3cc712e934d5b5c8ea3b8ae1178f819506`  
		Last Modified: Tue, 02 Sep 2025 00:19:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:913f34c8c27653219a84112a6f9161d3c8c96f1a00aeb22e842666529b132598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe63802bfd4ee9033ccbe702f40014715459f4874180efd15dd32ad6a6710a48`

```dockerfile
```

-	Layers:
	-	`sha256:6c6a22bbe112faa95eff45138cd315a4e7dc40440c19960eaab549f1910b862c`  
		Last Modified: Tue, 02 Sep 2025 02:51:32 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe2fb1c8c9418b40b324f2b12a579ac35082e2f24b4b7fde29be74843ca0042`  
		Last Modified: Tue, 02 Sep 2025 02:51:33 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:00bcb1d6d2387431b80bc9ba15750b62a9c71dcfb4c366d9ebd1f15a1241fb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377e4a788ccecb7ffce6de75d6515dae4882073788e3e4d6708014c8af3b17f`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949273f4e970672a127ace61c92f81f44dbffdf72658e45fc61f400f7faf13ed`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b4c898a3fe17a62b9b6b98c16d71d79afc21b938a4542c199ee07831a2e72`  
		Last Modified: Thu, 02 Oct 2025 03:00:19 GMT  
		Size: 87.3 MB (87288753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43350dce70d6057816696573088ffbbf7ad09dad213b371045e682e018aecdc7`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9637d8a6e47598df42c530d9291cdd295e00ad01db774cf9d0329f64d43e8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d3442492c15262e8c4b84bd8c5cd55e98a611e2122cb56bcf5fca115b22de`

```dockerfile
```

-	Layers:
	-	`sha256:cce72a388571b32b0aa26b8069576ecbc150345bd022f9b785166139ef67b445`  
		Last Modified: Thu, 02 Oct 2025 02:51:41 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79166d0edf21eb7ab069f03a3db3b98582e00959a53b1c880a367ca14c63db03`  
		Last Modified: Thu, 02 Oct 2025 02:51:42 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:ddd6a4132429a75f4f16624232d9522a6417bb8605a119a1aa8e8acb61153939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:f7a53565cf35425cf949cdc9d378c0aeed82b0e63ca76d003ff0d77256f7acfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05facc9141bc34d09d9eb14d0fb2fc9e83da24995bbb01841fc0e09170a67771`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69fdc95cc22a965412d881dbbe03be202c34c4884f9ef61d7b23a0ee10e5dae`  
		Last Modified: Tue, 02 Sep 2025 00:19:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe400747c25841953b7cbcae4a563be95610b01b260426ffa1364b5fdfcc9f5`  
		Last Modified: Tue, 02 Sep 2025 00:19:51 GMT  
		Size: 88.0 MB (88008897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad893804ee541d2ec5e132d86fae2e3cc712e934d5b5c8ea3b8ae1178f819506`  
		Last Modified: Tue, 02 Sep 2025 00:19:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:913f34c8c27653219a84112a6f9161d3c8c96f1a00aeb22e842666529b132598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe63802bfd4ee9033ccbe702f40014715459f4874180efd15dd32ad6a6710a48`

```dockerfile
```

-	Layers:
	-	`sha256:6c6a22bbe112faa95eff45138cd315a4e7dc40440c19960eaab549f1910b862c`  
		Last Modified: Tue, 02 Sep 2025 02:51:32 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe2fb1c8c9418b40b324f2b12a579ac35082e2f24b4b7fde29be74843ca0042`  
		Last Modified: Tue, 02 Sep 2025 02:51:33 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:00bcb1d6d2387431b80bc9ba15750b62a9c71dcfb4c366d9ebd1f15a1241fb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377e4a788ccecb7ffce6de75d6515dae4882073788e3e4d6708014c8af3b17f`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949273f4e970672a127ace61c92f81f44dbffdf72658e45fc61f400f7faf13ed`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b4c898a3fe17a62b9b6b98c16d71d79afc21b938a4542c199ee07831a2e72`  
		Last Modified: Thu, 02 Oct 2025 03:00:19 GMT  
		Size: 87.3 MB (87288753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43350dce70d6057816696573088ffbbf7ad09dad213b371045e682e018aecdc7`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:9637d8a6e47598df42c530d9291cdd295e00ad01db774cf9d0329f64d43e8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d3442492c15262e8c4b84bd8c5cd55e98a611e2122cb56bcf5fca115b22de`

```dockerfile
```

-	Layers:
	-	`sha256:cce72a388571b32b0aa26b8069576ecbc150345bd022f9b785166139ef67b445`  
		Last Modified: Thu, 02 Oct 2025 02:51:41 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79166d0edf21eb7ab069f03a3db3b98582e00959a53b1c880a367ca14c63db03`  
		Last Modified: Thu, 02 Oct 2025 02:51:42 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:ddd6a4132429a75f4f16624232d9522a6417bb8605a119a1aa8e8acb61153939
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f7a53565cf35425cf949cdc9d378c0aeed82b0e63ca76d003ff0d77256f7acfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05facc9141bc34d09d9eb14d0fb2fc9e83da24995bbb01841fc0e09170a67771`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69fdc95cc22a965412d881dbbe03be202c34c4884f9ef61d7b23a0ee10e5dae`  
		Last Modified: Tue, 02 Sep 2025 00:19:41 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe400747c25841953b7cbcae4a563be95610b01b260426ffa1364b5fdfcc9f5`  
		Last Modified: Tue, 02 Sep 2025 00:19:51 GMT  
		Size: 88.0 MB (88008897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad893804ee541d2ec5e132d86fae2e3cc712e934d5b5c8ea3b8ae1178f819506`  
		Last Modified: Tue, 02 Sep 2025 00:19:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:913f34c8c27653219a84112a6f9161d3c8c96f1a00aeb22e842666529b132598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe63802bfd4ee9033ccbe702f40014715459f4874180efd15dd32ad6a6710a48`

```dockerfile
```

-	Layers:
	-	`sha256:6c6a22bbe112faa95eff45138cd315a4e7dc40440c19960eaab549f1910b862c`  
		Last Modified: Tue, 02 Sep 2025 02:51:32 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe2fb1c8c9418b40b324f2b12a579ac35082e2f24b4b7fde29be74843ca0042`  
		Last Modified: Tue, 02 Sep 2025 02:51:33 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:00bcb1d6d2387431b80bc9ba15750b62a9c71dcfb4c366d9ebd1f15a1241fb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377e4a788ccecb7ffce6de75d6515dae4882073788e3e4d6708014c8af3b17f`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949273f4e970672a127ace61c92f81f44dbffdf72658e45fc61f400f7faf13ed`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b4c898a3fe17a62b9b6b98c16d71d79afc21b938a4542c199ee07831a2e72`  
		Last Modified: Thu, 02 Oct 2025 03:00:19 GMT  
		Size: 87.3 MB (87288753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43350dce70d6057816696573088ffbbf7ad09dad213b371045e682e018aecdc7`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9637d8a6e47598df42c530d9291cdd295e00ad01db774cf9d0329f64d43e8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d3442492c15262e8c4b84bd8c5cd55e98a611e2122cb56bcf5fca115b22de`

```dockerfile
```

-	Layers:
	-	`sha256:cce72a388571b32b0aa26b8069576ecbc150345bd022f9b785166139ef67b445`  
		Last Modified: Thu, 02 Oct 2025 02:51:41 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79166d0edf21eb7ab069f03a3db3b98582e00959a53b1c880a367ca14c63db03`  
		Last Modified: Thu, 02 Oct 2025 02:51:42 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:30597ffe2fc98160b979311d18f7649edd1ed3bf145063e99b1ef89775a668d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:4c19d5e04a76d2ae7df943a376ace1c3e23beaed5236adc4c0e87aac1c665d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38930d56606d4e6c271cce8c63b4bf401a728c8887517ebb0ea15823411cd51b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a737aeb4167a859699887d661b37d589e3912ec02074d61c9874d05dffce9`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd7d3d0fb9226e4d5f77687f5c6ff36bb9dd1d1add48fa190ab6aa5f66926f`  
		Last Modified: Mon, 15 Sep 2025 22:20:01 GMT  
		Size: 90.7 MB (90683414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30bba013e8ad37a8eefab77989731e08963276c2b67790edf321591f2a25ae`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:2fef901c98c46906a1354c398f4bac15fd535f413fb1b7fb1226964801e2c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900359cfd9dd50cf616c65d415c62228193851fd8b3ccbc50ca6fe9af4e39654`

```dockerfile
```

-	Layers:
	-	`sha256:7aab9f71b6b92b83016eba41bc8aebad9641898b5bfa9989d6d7de910cf6198b`  
		Last Modified: Mon, 15 Sep 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0125d3b6f729fe5019e34209322e91d0ab2f975dcc3c4fb9533f757fc115d36`  
		Last Modified: Mon, 15 Sep 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d86a6b9a4b3faec087553390345c2031dea5cb9debcf932f5e43faee0beb97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9c7a014f198480b766b5ce5ed41186b357e2e5c60c94c8b3929484850d2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086a091e2e1c2a02d87a8e877d82423698cec857fbbdeb1da6d5228b8855c00`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6068b25573db1ae2c976e98bf35c9a3842e28bbee1cc9c62896d24e5f642e5c`  
		Last Modified: Thu, 02 Oct 2025 01:25:06 GMT  
		Size: 92.2 MB (92229492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f0ef82511f19628f19bacaba5f2349580bd3e55ace63e3ab4e0a217d45860`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:82df75418b58a6cb1e5047fea79d2f2cad8cd772e74a2d38148c590fc0beffc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd82f42126f80f41756ee10d8dfb7eeae8cc26af48eddb9fe7c045baeb88a55`

```dockerfile
```

-	Layers:
	-	`sha256:a064f1c26d8055f0cb3784ccf93a4954f27f39da3d9329d9c2a498c39e67172f`  
		Last Modified: Thu, 02 Oct 2025 02:51:22 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429a20f1215dd81cf6717a62dc17d3a905ac39afcd1c1d61e0484eefd645cbcd`  
		Last Modified: Thu, 02 Oct 2025 02:51:23 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:30597ffe2fc98160b979311d18f7649edd1ed3bf145063e99b1ef89775a668d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:4c19d5e04a76d2ae7df943a376ace1c3e23beaed5236adc4c0e87aac1c665d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38930d56606d4e6c271cce8c63b4bf401a728c8887517ebb0ea15823411cd51b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a737aeb4167a859699887d661b37d589e3912ec02074d61c9874d05dffce9`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd7d3d0fb9226e4d5f77687f5c6ff36bb9dd1d1add48fa190ab6aa5f66926f`  
		Last Modified: Mon, 15 Sep 2025 22:20:01 GMT  
		Size: 90.7 MB (90683414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30bba013e8ad37a8eefab77989731e08963276c2b67790edf321591f2a25ae`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:2fef901c98c46906a1354c398f4bac15fd535f413fb1b7fb1226964801e2c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900359cfd9dd50cf616c65d415c62228193851fd8b3ccbc50ca6fe9af4e39654`

```dockerfile
```

-	Layers:
	-	`sha256:7aab9f71b6b92b83016eba41bc8aebad9641898b5bfa9989d6d7de910cf6198b`  
		Last Modified: Mon, 15 Sep 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0125d3b6f729fe5019e34209322e91d0ab2f975dcc3c4fb9533f757fc115d36`  
		Last Modified: Mon, 15 Sep 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d86a6b9a4b3faec087553390345c2031dea5cb9debcf932f5e43faee0beb97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9c7a014f198480b766b5ce5ed41186b357e2e5c60c94c8b3929484850d2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086a091e2e1c2a02d87a8e877d82423698cec857fbbdeb1da6d5228b8855c00`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6068b25573db1ae2c976e98bf35c9a3842e28bbee1cc9c62896d24e5f642e5c`  
		Last Modified: Thu, 02 Oct 2025 01:25:06 GMT  
		Size: 92.2 MB (92229492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f0ef82511f19628f19bacaba5f2349580bd3e55ace63e3ab4e0a217d45860`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:82df75418b58a6cb1e5047fea79d2f2cad8cd772e74a2d38148c590fc0beffc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd82f42126f80f41756ee10d8dfb7eeae8cc26af48eddb9fe7c045baeb88a55`

```dockerfile
```

-	Layers:
	-	`sha256:a064f1c26d8055f0cb3784ccf93a4954f27f39da3d9329d9c2a498c39e67172f`  
		Last Modified: Thu, 02 Oct 2025 02:51:22 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429a20f1215dd81cf6717a62dc17d3a905ac39afcd1c1d61e0484eefd645cbcd`  
		Last Modified: Thu, 02 Oct 2025 02:51:23 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:30597ffe2fc98160b979311d18f7649edd1ed3bf145063e99b1ef89775a668d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:4c19d5e04a76d2ae7df943a376ace1c3e23beaed5236adc4c0e87aac1c665d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38930d56606d4e6c271cce8c63b4bf401a728c8887517ebb0ea15823411cd51b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a737aeb4167a859699887d661b37d589e3912ec02074d61c9874d05dffce9`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd7d3d0fb9226e4d5f77687f5c6ff36bb9dd1d1add48fa190ab6aa5f66926f`  
		Last Modified: Mon, 15 Sep 2025 22:20:01 GMT  
		Size: 90.7 MB (90683414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30bba013e8ad37a8eefab77989731e08963276c2b67790edf321591f2a25ae`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:2fef901c98c46906a1354c398f4bac15fd535f413fb1b7fb1226964801e2c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900359cfd9dd50cf616c65d415c62228193851fd8b3ccbc50ca6fe9af4e39654`

```dockerfile
```

-	Layers:
	-	`sha256:7aab9f71b6b92b83016eba41bc8aebad9641898b5bfa9989d6d7de910cf6198b`  
		Last Modified: Mon, 15 Sep 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0125d3b6f729fe5019e34209322e91d0ab2f975dcc3c4fb9533f757fc115d36`  
		Last Modified: Mon, 15 Sep 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d86a6b9a4b3faec087553390345c2031dea5cb9debcf932f5e43faee0beb97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9c7a014f198480b766b5ce5ed41186b357e2e5c60c94c8b3929484850d2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086a091e2e1c2a02d87a8e877d82423698cec857fbbdeb1da6d5228b8855c00`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6068b25573db1ae2c976e98bf35c9a3842e28bbee1cc9c62896d24e5f642e5c`  
		Last Modified: Thu, 02 Oct 2025 01:25:06 GMT  
		Size: 92.2 MB (92229492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f0ef82511f19628f19bacaba5f2349580bd3e55ace63e3ab4e0a217d45860`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:82df75418b58a6cb1e5047fea79d2f2cad8cd772e74a2d38148c590fc0beffc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd82f42126f80f41756ee10d8dfb7eeae8cc26af48eddb9fe7c045baeb88a55`

```dockerfile
```

-	Layers:
	-	`sha256:a064f1c26d8055f0cb3784ccf93a4954f27f39da3d9329d9c2a498c39e67172f`  
		Last Modified: Thu, 02 Oct 2025 02:51:22 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429a20f1215dd81cf6717a62dc17d3a905ac39afcd1c1d61e0484eefd645cbcd`  
		Last Modified: Thu, 02 Oct 2025 02:51:23 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:30597ffe2fc98160b979311d18f7649edd1ed3bf145063e99b1ef89775a668d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:4c19d5e04a76d2ae7df943a376ace1c3e23beaed5236adc4c0e87aac1c665d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38930d56606d4e6c271cce8c63b4bf401a728c8887517ebb0ea15823411cd51b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a737aeb4167a859699887d661b37d589e3912ec02074d61c9874d05dffce9`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd7d3d0fb9226e4d5f77687f5c6ff36bb9dd1d1add48fa190ab6aa5f66926f`  
		Last Modified: Mon, 15 Sep 2025 22:20:01 GMT  
		Size: 90.7 MB (90683414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30bba013e8ad37a8eefab77989731e08963276c2b67790edf321591f2a25ae`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:2fef901c98c46906a1354c398f4bac15fd535f413fb1b7fb1226964801e2c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900359cfd9dd50cf616c65d415c62228193851fd8b3ccbc50ca6fe9af4e39654`

```dockerfile
```

-	Layers:
	-	`sha256:7aab9f71b6b92b83016eba41bc8aebad9641898b5bfa9989d6d7de910cf6198b`  
		Last Modified: Mon, 15 Sep 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0125d3b6f729fe5019e34209322e91d0ab2f975dcc3c4fb9533f757fc115d36`  
		Last Modified: Mon, 15 Sep 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d86a6b9a4b3faec087553390345c2031dea5cb9debcf932f5e43faee0beb97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9c7a014f198480b766b5ce5ed41186b357e2e5c60c94c8b3929484850d2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086a091e2e1c2a02d87a8e877d82423698cec857fbbdeb1da6d5228b8855c00`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6068b25573db1ae2c976e98bf35c9a3842e28bbee1cc9c62896d24e5f642e5c`  
		Last Modified: Thu, 02 Oct 2025 01:25:06 GMT  
		Size: 92.2 MB (92229492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f0ef82511f19628f19bacaba5f2349580bd3e55ace63e3ab4e0a217d45860`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:82df75418b58a6cb1e5047fea79d2f2cad8cd772e74a2d38148c590fc0beffc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd82f42126f80f41756ee10d8dfb7eeae8cc26af48eddb9fe7c045baeb88a55`

```dockerfile
```

-	Layers:
	-	`sha256:a064f1c26d8055f0cb3784ccf93a4954f27f39da3d9329d9c2a498c39e67172f`  
		Last Modified: Thu, 02 Oct 2025 02:51:22 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429a20f1215dd81cf6717a62dc17d3a905ac39afcd1c1d61e0484eefd645cbcd`  
		Last Modified: Thu, 02 Oct 2025 02:51:23 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:30597ffe2fc98160b979311d18f7649edd1ed3bf145063e99b1ef89775a668d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:4c19d5e04a76d2ae7df943a376ace1c3e23beaed5236adc4c0e87aac1c665d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38930d56606d4e6c271cce8c63b4bf401a728c8887517ebb0ea15823411cd51b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a737aeb4167a859699887d661b37d589e3912ec02074d61c9874d05dffce9`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd7d3d0fb9226e4d5f77687f5c6ff36bb9dd1d1add48fa190ab6aa5f66926f`  
		Last Modified: Mon, 15 Sep 2025 22:20:01 GMT  
		Size: 90.7 MB (90683414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30bba013e8ad37a8eefab77989731e08963276c2b67790edf321591f2a25ae`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:2fef901c98c46906a1354c398f4bac15fd535f413fb1b7fb1226964801e2c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900359cfd9dd50cf616c65d415c62228193851fd8b3ccbc50ca6fe9af4e39654`

```dockerfile
```

-	Layers:
	-	`sha256:7aab9f71b6b92b83016eba41bc8aebad9641898b5bfa9989d6d7de910cf6198b`  
		Last Modified: Mon, 15 Sep 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0125d3b6f729fe5019e34209322e91d0ab2f975dcc3c4fb9533f757fc115d36`  
		Last Modified: Mon, 15 Sep 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d86a6b9a4b3faec087553390345c2031dea5cb9debcf932f5e43faee0beb97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9c7a014f198480b766b5ce5ed41186b357e2e5c60c94c8b3929484850d2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086a091e2e1c2a02d87a8e877d82423698cec857fbbdeb1da6d5228b8855c00`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6068b25573db1ae2c976e98bf35c9a3842e28bbee1cc9c62896d24e5f642e5c`  
		Last Modified: Thu, 02 Oct 2025 01:25:06 GMT  
		Size: 92.2 MB (92229492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f0ef82511f19628f19bacaba5f2349580bd3e55ace63e3ab4e0a217d45860`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:82df75418b58a6cb1e5047fea79d2f2cad8cd772e74a2d38148c590fc0beffc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd82f42126f80f41756ee10d8dfb7eeae8cc26af48eddb9fe7c045baeb88a55`

```dockerfile
```

-	Layers:
	-	`sha256:a064f1c26d8055f0cb3784ccf93a4954f27f39da3d9329d9c2a498c39e67172f`  
		Last Modified: Thu, 02 Oct 2025 02:51:22 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429a20f1215dd81cf6717a62dc17d3a905ac39afcd1c1d61e0484eefd645cbcd`  
		Last Modified: Thu, 02 Oct 2025 02:51:23 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:30597ffe2fc98160b979311d18f7649edd1ed3bf145063e99b1ef89775a668d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:4c19d5e04a76d2ae7df943a376ace1c3e23beaed5236adc4c0e87aac1c665d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38930d56606d4e6c271cce8c63b4bf401a728c8887517ebb0ea15823411cd51b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a737aeb4167a859699887d661b37d589e3912ec02074d61c9874d05dffce9`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd7d3d0fb9226e4d5f77687f5c6ff36bb9dd1d1add48fa190ab6aa5f66926f`  
		Last Modified: Mon, 15 Sep 2025 22:20:01 GMT  
		Size: 90.7 MB (90683414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30bba013e8ad37a8eefab77989731e08963276c2b67790edf321591f2a25ae`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:2fef901c98c46906a1354c398f4bac15fd535f413fb1b7fb1226964801e2c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900359cfd9dd50cf616c65d415c62228193851fd8b3ccbc50ca6fe9af4e39654`

```dockerfile
```

-	Layers:
	-	`sha256:7aab9f71b6b92b83016eba41bc8aebad9641898b5bfa9989d6d7de910cf6198b`  
		Last Modified: Mon, 15 Sep 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0125d3b6f729fe5019e34209322e91d0ab2f975dcc3c4fb9533f757fc115d36`  
		Last Modified: Mon, 15 Sep 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d86a6b9a4b3faec087553390345c2031dea5cb9debcf932f5e43faee0beb97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9c7a014f198480b766b5ce5ed41186b357e2e5c60c94c8b3929484850d2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086a091e2e1c2a02d87a8e877d82423698cec857fbbdeb1da6d5228b8855c00`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6068b25573db1ae2c976e98bf35c9a3842e28bbee1cc9c62896d24e5f642e5c`  
		Last Modified: Thu, 02 Oct 2025 01:25:06 GMT  
		Size: 92.2 MB (92229492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f0ef82511f19628f19bacaba5f2349580bd3e55ace63e3ab4e0a217d45860`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:82df75418b58a6cb1e5047fea79d2f2cad8cd772e74a2d38148c590fc0beffc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd82f42126f80f41756ee10d8dfb7eeae8cc26af48eddb9fe7c045baeb88a55`

```dockerfile
```

-	Layers:
	-	`sha256:a064f1c26d8055f0cb3784ccf93a4954f27f39da3d9329d9c2a498c39e67172f`  
		Last Modified: Thu, 02 Oct 2025 02:51:22 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429a20f1215dd81cf6717a62dc17d3a905ac39afcd1c1d61e0484eefd645cbcd`  
		Last Modified: Thu, 02 Oct 2025 02:51:23 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json
