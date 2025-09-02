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
$ docker pull kong@sha256:14c689c0caf1b8da1403a742016ec64d2f5b5b12ecdec2989f36b2c2c4aa1ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:ab67b9d67ae37184f16d8ccec620d663e0710a207d56b4e22b6c13f8043bee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da848aeb51c74301573e300ce714c1707829c1ae13b9123383b88b83855afa`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8f80519b28ebe548dc966edb51696e3747ca2acd3e8c60f635e8233f2fff9c`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b5b8588c9754dfb866e889fde741fc991362bed0091199037a9377fc1debf`  
		Last Modified: Tue, 02 Sep 2025 00:19:38 GMT  
		Size: 90.7 MB (90683182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e81df23c3dd57d43366a29cbca22a6775b9e60fee299c5c9b4b7e3f3974a61`  
		Last Modified: Mon, 01 Sep 2025 23:44:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:233d7440793922b61438dc692aae9ccadfa5852348f5eb22db1d4555f6529b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ba716976d025b1f798a772206b038332aff1e8d17847107d799e591af3c6c`

```dockerfile
```

-	Layers:
	-	`sha256:8d76c6ba7073680c6e8584b2e82b0a06348904dd5b15a3e3972b89568bce3d56`  
		Last Modified: Tue, 02 Sep 2025 02:51:20 GMT  
		Size: 5.4 MB (5421130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c1f8028ff3311abb80208eb61f7d970f27663d99ebead6aa8d9e03a3980344`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f17314da9b917207b426be4945000a447264fd769ffb75933187c47540eca32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118863429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c291b4d6b2e67d7969d90e0decf0b6e41d17885007113ab204c1ee67704ec`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d109c2e9b032042c67edd2b8f218cff324203972444b46c792c73cf9434b6e`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7695d67c09d74059c12114dcd578fafa7eb9154965b824415cd947a4e9ba2`  
		Last Modified: Tue, 02 Sep 2025 02:16:01 GMT  
		Size: 90.0 MB (90001900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23591ed706efb09741f302134107d502b7e1e030b7097c4a5a84510a6af5020`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:31335caa2da67fd1c40f2b395f2eb967fe2c9f93aef1d9e8d4097cdd6014e879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e73ff6eb993693eba955dbbd9a38c696550afdad8cb4242dd10be4391d51d`

```dockerfile
```

-	Layers:
	-	`sha256:391afd9f1d5071987f7c662c5b37a1c5cb050e3e20ce7a5a1f3ba2af2e5c4556`  
		Last Modified: Tue, 02 Sep 2025 05:51:21 GMT  
		Size: 5.4 MB (5428297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654358133ea0b3fae2e4935e1b3ffdd85714f607a062dac84e3701492e79c2c1`  
		Last Modified: Tue, 02 Sep 2025 05:51:22 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:5081faaeb332a6a2a924be45a0aaeb04b90b2714aa5931e1333b2e90e61b512c
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
$ docker pull kong@sha256:ebc606f75bae3d4998148d06a3f763547082d598cbb8fe606d67899eac3ccece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88538124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91ef73b91ae5b8dbc5af9c7972448d884980a240d9d343c0394ddf896289e80`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9d73d14dc03f67b3a8eb9687766cf6a44d81bfb3c6098af5c4c39b316c922`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699df6afd3c0ad3b0a9d164db09a31c05423a0fd65e05bd682b8fa032489736c`  
		Last Modified: Tue, 02 Sep 2025 02:17:42 GMT  
		Size: 61.2 MB (61175373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ed5d92746a91b08a4c586e3e51d9b019868838400090aa58e67ab0ef70d284`  
		Last Modified: Tue, 02 Sep 2025 02:17:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:f6957f04dc318e60c9878b2a0cd1989a38866b53f10bb225b2c1b81744f9bf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1184849ac2d105a71bba7007a4c20c97a85d5874430bbe115107524f21b7347c`

```dockerfile
```

-	Layers:
	-	`sha256:06e52558d7d289e80670c3fd35d99a505075c04e9870189e43fc215e0978e760`  
		Last Modified: Tue, 02 Sep 2025 05:51:25 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d00f10caf2aa368ba775f309845253d28625be181da4b8f6ae3c14de662fd8e`  
		Last Modified: Tue, 02 Sep 2025 05:51:25 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:5081faaeb332a6a2a924be45a0aaeb04b90b2714aa5931e1333b2e90e61b512c
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
$ docker pull kong@sha256:ebc606f75bae3d4998148d06a3f763547082d598cbb8fe606d67899eac3ccece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88538124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91ef73b91ae5b8dbc5af9c7972448d884980a240d9d343c0394ddf896289e80`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9d73d14dc03f67b3a8eb9687766cf6a44d81bfb3c6098af5c4c39b316c922`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699df6afd3c0ad3b0a9d164db09a31c05423a0fd65e05bd682b8fa032489736c`  
		Last Modified: Tue, 02 Sep 2025 02:17:42 GMT  
		Size: 61.2 MB (61175373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ed5d92746a91b08a4c586e3e51d9b019868838400090aa58e67ab0ef70d284`  
		Last Modified: Tue, 02 Sep 2025 02:17:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f6957f04dc318e60c9878b2a0cd1989a38866b53f10bb225b2c1b81744f9bf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1184849ac2d105a71bba7007a4c20c97a85d5874430bbe115107524f21b7347c`

```dockerfile
```

-	Layers:
	-	`sha256:06e52558d7d289e80670c3fd35d99a505075c04e9870189e43fc215e0978e760`  
		Last Modified: Tue, 02 Sep 2025 05:51:25 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d00f10caf2aa368ba775f309845253d28625be181da4b8f6ae3c14de662fd8e`  
		Last Modified: Tue, 02 Sep 2025 05:51:25 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:5081faaeb332a6a2a924be45a0aaeb04b90b2714aa5931e1333b2e90e61b512c
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
$ docker pull kong@sha256:ebc606f75bae3d4998148d06a3f763547082d598cbb8fe606d67899eac3ccece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88538124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91ef73b91ae5b8dbc5af9c7972448d884980a240d9d343c0394ddf896289e80`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9d73d14dc03f67b3a8eb9687766cf6a44d81bfb3c6098af5c4c39b316c922`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699df6afd3c0ad3b0a9d164db09a31c05423a0fd65e05bd682b8fa032489736c`  
		Last Modified: Tue, 02 Sep 2025 02:17:42 GMT  
		Size: 61.2 MB (61175373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ed5d92746a91b08a4c586e3e51d9b019868838400090aa58e67ab0ef70d284`  
		Last Modified: Tue, 02 Sep 2025 02:17:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:f6957f04dc318e60c9878b2a0cd1989a38866b53f10bb225b2c1b81744f9bf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1184849ac2d105a71bba7007a4c20c97a85d5874430bbe115107524f21b7347c`

```dockerfile
```

-	Layers:
	-	`sha256:06e52558d7d289e80670c3fd35d99a505075c04e9870189e43fc215e0978e760`  
		Last Modified: Tue, 02 Sep 2025 05:51:25 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d00f10caf2aa368ba775f309845253d28625be181da4b8f6ae3c14de662fd8e`  
		Last Modified: Tue, 02 Sep 2025 05:51:25 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:5081faaeb332a6a2a924be45a0aaeb04b90b2714aa5931e1333b2e90e61b512c
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
$ docker pull kong@sha256:ebc606f75bae3d4998148d06a3f763547082d598cbb8fe606d67899eac3ccece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88538124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91ef73b91ae5b8dbc5af9c7972448d884980a240d9d343c0394ddf896289e80`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9d73d14dc03f67b3a8eb9687766cf6a44d81bfb3c6098af5c4c39b316c922`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699df6afd3c0ad3b0a9d164db09a31c05423a0fd65e05bd682b8fa032489736c`  
		Last Modified: Tue, 02 Sep 2025 02:17:42 GMT  
		Size: 61.2 MB (61175373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ed5d92746a91b08a4c586e3e51d9b019868838400090aa58e67ab0ef70d284`  
		Last Modified: Tue, 02 Sep 2025 02:17:38 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f6957f04dc318e60c9878b2a0cd1989a38866b53f10bb225b2c1b81744f9bf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1184849ac2d105a71bba7007a4c20c97a85d5874430bbe115107524f21b7347c`

```dockerfile
```

-	Layers:
	-	`sha256:06e52558d7d289e80670c3fd35d99a505075c04e9870189e43fc215e0978e760`  
		Last Modified: Tue, 02 Sep 2025 05:51:25 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d00f10caf2aa368ba775f309845253d28625be181da4b8f6ae3c14de662fd8e`  
		Last Modified: Tue, 02 Sep 2025 05:51:25 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:0a149cd8f58c01a9c5846bbbf1951d0454b074d348af114f3d973eb31d49bc36
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
$ docker pull kong@sha256:5b9b9456eeabd8e4bd7c1a27183325015933f343418171f816838339cb294587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114646916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7815934e7ea5a10b330e0b6d734b09846b766ed3f566afb103f64a3b502fa4`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9d73d14dc03f67b3a8eb9687766cf6a44d81bfb3c6098af5c4c39b316c922`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127dd0bfb9c2afdc2a1ead2c6d13acf7a209778e67c1beabc133556969a86a0`  
		Last Modified: Tue, 02 Sep 2025 02:17:07 GMT  
		Size: 87.3 MB (87284166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b03cf70e2b787cb9de9342425c8e46e93bc49c13abb3d33d4919bf4f6dc0491`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:c3032f67dc605adf034bf6626190f6c6eb2290ae85f6f1c7d87f046fc360e270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c8838241bdebaa1f6caa28abc0ec0ef36d1f1155c4703b0000c7cb950d73a0`

```dockerfile
```

-	Layers:
	-	`sha256:0f95c917a2e53ea1b112111e301207740cf6ac6c21efb4eac5762991444662bd`  
		Last Modified: Tue, 02 Sep 2025 05:51:31 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6550743f5d0b683fc8fed2440ee0d6284d9363bc2394c2bdffbdc1ff2b2d5d58`  
		Last Modified: Tue, 02 Sep 2025 05:51:32 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:0a149cd8f58c01a9c5846bbbf1951d0454b074d348af114f3d973eb31d49bc36
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
$ docker pull kong@sha256:5b9b9456eeabd8e4bd7c1a27183325015933f343418171f816838339cb294587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114646916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7815934e7ea5a10b330e0b6d734b09846b766ed3f566afb103f64a3b502fa4`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9d73d14dc03f67b3a8eb9687766cf6a44d81bfb3c6098af5c4c39b316c922`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127dd0bfb9c2afdc2a1ead2c6d13acf7a209778e67c1beabc133556969a86a0`  
		Last Modified: Tue, 02 Sep 2025 02:17:07 GMT  
		Size: 87.3 MB (87284166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b03cf70e2b787cb9de9342425c8e46e93bc49c13abb3d33d4919bf4f6dc0491`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c3032f67dc605adf034bf6626190f6c6eb2290ae85f6f1c7d87f046fc360e270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c8838241bdebaa1f6caa28abc0ec0ef36d1f1155c4703b0000c7cb950d73a0`

```dockerfile
```

-	Layers:
	-	`sha256:0f95c917a2e53ea1b112111e301207740cf6ac6c21efb4eac5762991444662bd`  
		Last Modified: Tue, 02 Sep 2025 05:51:31 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6550743f5d0b683fc8fed2440ee0d6284d9363bc2394c2bdffbdc1ff2b2d5d58`  
		Last Modified: Tue, 02 Sep 2025 05:51:32 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:0a149cd8f58c01a9c5846bbbf1951d0454b074d348af114f3d973eb31d49bc36
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
$ docker pull kong@sha256:5b9b9456eeabd8e4bd7c1a27183325015933f343418171f816838339cb294587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114646916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7815934e7ea5a10b330e0b6d734b09846b766ed3f566afb103f64a3b502fa4`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9d73d14dc03f67b3a8eb9687766cf6a44d81bfb3c6098af5c4c39b316c922`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127dd0bfb9c2afdc2a1ead2c6d13acf7a209778e67c1beabc133556969a86a0`  
		Last Modified: Tue, 02 Sep 2025 02:17:07 GMT  
		Size: 87.3 MB (87284166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b03cf70e2b787cb9de9342425c8e46e93bc49c13abb3d33d4919bf4f6dc0491`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:c3032f67dc605adf034bf6626190f6c6eb2290ae85f6f1c7d87f046fc360e270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c8838241bdebaa1f6caa28abc0ec0ef36d1f1155c4703b0000c7cb950d73a0`

```dockerfile
```

-	Layers:
	-	`sha256:0f95c917a2e53ea1b112111e301207740cf6ac6c21efb4eac5762991444662bd`  
		Last Modified: Tue, 02 Sep 2025 05:51:31 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6550743f5d0b683fc8fed2440ee0d6284d9363bc2394c2bdffbdc1ff2b2d5d58`  
		Last Modified: Tue, 02 Sep 2025 05:51:32 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:0a149cd8f58c01a9c5846bbbf1951d0454b074d348af114f3d973eb31d49bc36
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
$ docker pull kong@sha256:5b9b9456eeabd8e4bd7c1a27183325015933f343418171f816838339cb294587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114646916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7815934e7ea5a10b330e0b6d734b09846b766ed3f566afb103f64a3b502fa4`
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
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
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
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a9d73d14dc03f67b3a8eb9687766cf6a44d81bfb3c6098af5c4c39b316c922`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127dd0bfb9c2afdc2a1ead2c6d13acf7a209778e67c1beabc133556969a86a0`  
		Last Modified: Tue, 02 Sep 2025 02:17:07 GMT  
		Size: 87.3 MB (87284166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b03cf70e2b787cb9de9342425c8e46e93bc49c13abb3d33d4919bf4f6dc0491`  
		Last Modified: Tue, 02 Sep 2025 02:16:39 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c3032f67dc605adf034bf6626190f6c6eb2290ae85f6f1c7d87f046fc360e270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c8838241bdebaa1f6caa28abc0ec0ef36d1f1155c4703b0000c7cb950d73a0`

```dockerfile
```

-	Layers:
	-	`sha256:0f95c917a2e53ea1b112111e301207740cf6ac6c21efb4eac5762991444662bd`  
		Last Modified: Tue, 02 Sep 2025 05:51:31 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6550743f5d0b683fc8fed2440ee0d6284d9363bc2394c2bdffbdc1ff2b2d5d58`  
		Last Modified: Tue, 02 Sep 2025 05:51:32 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:14c689c0caf1b8da1403a742016ec64d2f5b5b12ecdec2989f36b2c2c4aa1ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:ab67b9d67ae37184f16d8ccec620d663e0710a207d56b4e22b6c13f8043bee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da848aeb51c74301573e300ce714c1707829c1ae13b9123383b88b83855afa`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8f80519b28ebe548dc966edb51696e3747ca2acd3e8c60f635e8233f2fff9c`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b5b8588c9754dfb866e889fde741fc991362bed0091199037a9377fc1debf`  
		Last Modified: Tue, 02 Sep 2025 00:19:38 GMT  
		Size: 90.7 MB (90683182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e81df23c3dd57d43366a29cbca22a6775b9e60fee299c5c9b4b7e3f3974a61`  
		Last Modified: Mon, 01 Sep 2025 23:44:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:233d7440793922b61438dc692aae9ccadfa5852348f5eb22db1d4555f6529b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ba716976d025b1f798a772206b038332aff1e8d17847107d799e591af3c6c`

```dockerfile
```

-	Layers:
	-	`sha256:8d76c6ba7073680c6e8584b2e82b0a06348904dd5b15a3e3972b89568bce3d56`  
		Last Modified: Tue, 02 Sep 2025 02:51:20 GMT  
		Size: 5.4 MB (5421130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c1f8028ff3311abb80208eb61f7d970f27663d99ebead6aa8d9e03a3980344`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f17314da9b917207b426be4945000a447264fd769ffb75933187c47540eca32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118863429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c291b4d6b2e67d7969d90e0decf0b6e41d17885007113ab204c1ee67704ec`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d109c2e9b032042c67edd2b8f218cff324203972444b46c792c73cf9434b6e`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7695d67c09d74059c12114dcd578fafa7eb9154965b824415cd947a4e9ba2`  
		Last Modified: Tue, 02 Sep 2025 02:16:01 GMT  
		Size: 90.0 MB (90001900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23591ed706efb09741f302134107d502b7e1e030b7097c4a5a84510a6af5020`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:31335caa2da67fd1c40f2b395f2eb967fe2c9f93aef1d9e8d4097cdd6014e879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e73ff6eb993693eba955dbbd9a38c696550afdad8cb4242dd10be4391d51d`

```dockerfile
```

-	Layers:
	-	`sha256:391afd9f1d5071987f7c662c5b37a1c5cb050e3e20ce7a5a1f3ba2af2e5c4556`  
		Last Modified: Tue, 02 Sep 2025 05:51:21 GMT  
		Size: 5.4 MB (5428297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654358133ea0b3fae2e4935e1b3ffdd85714f607a062dac84e3701492e79c2c1`  
		Last Modified: Tue, 02 Sep 2025 05:51:22 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:14c689c0caf1b8da1403a742016ec64d2f5b5b12ecdec2989f36b2c2c4aa1ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ab67b9d67ae37184f16d8ccec620d663e0710a207d56b4e22b6c13f8043bee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da848aeb51c74301573e300ce714c1707829c1ae13b9123383b88b83855afa`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8f80519b28ebe548dc966edb51696e3747ca2acd3e8c60f635e8233f2fff9c`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b5b8588c9754dfb866e889fde741fc991362bed0091199037a9377fc1debf`  
		Last Modified: Tue, 02 Sep 2025 00:19:38 GMT  
		Size: 90.7 MB (90683182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e81df23c3dd57d43366a29cbca22a6775b9e60fee299c5c9b4b7e3f3974a61`  
		Last Modified: Mon, 01 Sep 2025 23:44:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:233d7440793922b61438dc692aae9ccadfa5852348f5eb22db1d4555f6529b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ba716976d025b1f798a772206b038332aff1e8d17847107d799e591af3c6c`

```dockerfile
```

-	Layers:
	-	`sha256:8d76c6ba7073680c6e8584b2e82b0a06348904dd5b15a3e3972b89568bce3d56`  
		Last Modified: Tue, 02 Sep 2025 02:51:20 GMT  
		Size: 5.4 MB (5421130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c1f8028ff3311abb80208eb61f7d970f27663d99ebead6aa8d9e03a3980344`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f17314da9b917207b426be4945000a447264fd769ffb75933187c47540eca32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118863429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c291b4d6b2e67d7969d90e0decf0b6e41d17885007113ab204c1ee67704ec`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d109c2e9b032042c67edd2b8f218cff324203972444b46c792c73cf9434b6e`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7695d67c09d74059c12114dcd578fafa7eb9154965b824415cd947a4e9ba2`  
		Last Modified: Tue, 02 Sep 2025 02:16:01 GMT  
		Size: 90.0 MB (90001900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23591ed706efb09741f302134107d502b7e1e030b7097c4a5a84510a6af5020`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:31335caa2da67fd1c40f2b395f2eb967fe2c9f93aef1d9e8d4097cdd6014e879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e73ff6eb993693eba955dbbd9a38c696550afdad8cb4242dd10be4391d51d`

```dockerfile
```

-	Layers:
	-	`sha256:391afd9f1d5071987f7c662c5b37a1c5cb050e3e20ce7a5a1f3ba2af2e5c4556`  
		Last Modified: Tue, 02 Sep 2025 05:51:21 GMT  
		Size: 5.4 MB (5428297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654358133ea0b3fae2e4935e1b3ffdd85714f607a062dac84e3701492e79c2c1`  
		Last Modified: Tue, 02 Sep 2025 05:51:22 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:14c689c0caf1b8da1403a742016ec64d2f5b5b12ecdec2989f36b2c2c4aa1ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:ab67b9d67ae37184f16d8ccec620d663e0710a207d56b4e22b6c13f8043bee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da848aeb51c74301573e300ce714c1707829c1ae13b9123383b88b83855afa`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8f80519b28ebe548dc966edb51696e3747ca2acd3e8c60f635e8233f2fff9c`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b5b8588c9754dfb866e889fde741fc991362bed0091199037a9377fc1debf`  
		Last Modified: Tue, 02 Sep 2025 00:19:38 GMT  
		Size: 90.7 MB (90683182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e81df23c3dd57d43366a29cbca22a6775b9e60fee299c5c9b4b7e3f3974a61`  
		Last Modified: Mon, 01 Sep 2025 23:44:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:233d7440793922b61438dc692aae9ccadfa5852348f5eb22db1d4555f6529b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ba716976d025b1f798a772206b038332aff1e8d17847107d799e591af3c6c`

```dockerfile
```

-	Layers:
	-	`sha256:8d76c6ba7073680c6e8584b2e82b0a06348904dd5b15a3e3972b89568bce3d56`  
		Last Modified: Tue, 02 Sep 2025 02:51:20 GMT  
		Size: 5.4 MB (5421130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c1f8028ff3311abb80208eb61f7d970f27663d99ebead6aa8d9e03a3980344`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f17314da9b917207b426be4945000a447264fd769ffb75933187c47540eca32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118863429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c291b4d6b2e67d7969d90e0decf0b6e41d17885007113ab204c1ee67704ec`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d109c2e9b032042c67edd2b8f218cff324203972444b46c792c73cf9434b6e`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7695d67c09d74059c12114dcd578fafa7eb9154965b824415cd947a4e9ba2`  
		Last Modified: Tue, 02 Sep 2025 02:16:01 GMT  
		Size: 90.0 MB (90001900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23591ed706efb09741f302134107d502b7e1e030b7097c4a5a84510a6af5020`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:31335caa2da67fd1c40f2b395f2eb967fe2c9f93aef1d9e8d4097cdd6014e879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e73ff6eb993693eba955dbbd9a38c696550afdad8cb4242dd10be4391d51d`

```dockerfile
```

-	Layers:
	-	`sha256:391afd9f1d5071987f7c662c5b37a1c5cb050e3e20ce7a5a1f3ba2af2e5c4556`  
		Last Modified: Tue, 02 Sep 2025 05:51:21 GMT  
		Size: 5.4 MB (5428297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654358133ea0b3fae2e4935e1b3ffdd85714f607a062dac84e3701492e79c2c1`  
		Last Modified: Tue, 02 Sep 2025 05:51:22 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:14c689c0caf1b8da1403a742016ec64d2f5b5b12ecdec2989f36b2c2c4aa1ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ab67b9d67ae37184f16d8ccec620d663e0710a207d56b4e22b6c13f8043bee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da848aeb51c74301573e300ce714c1707829c1ae13b9123383b88b83855afa`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8f80519b28ebe548dc966edb51696e3747ca2acd3e8c60f635e8233f2fff9c`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b5b8588c9754dfb866e889fde741fc991362bed0091199037a9377fc1debf`  
		Last Modified: Tue, 02 Sep 2025 00:19:38 GMT  
		Size: 90.7 MB (90683182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e81df23c3dd57d43366a29cbca22a6775b9e60fee299c5c9b4b7e3f3974a61`  
		Last Modified: Mon, 01 Sep 2025 23:44:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:233d7440793922b61438dc692aae9ccadfa5852348f5eb22db1d4555f6529b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ba716976d025b1f798a772206b038332aff1e8d17847107d799e591af3c6c`

```dockerfile
```

-	Layers:
	-	`sha256:8d76c6ba7073680c6e8584b2e82b0a06348904dd5b15a3e3972b89568bce3d56`  
		Last Modified: Tue, 02 Sep 2025 02:51:20 GMT  
		Size: 5.4 MB (5421130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c1f8028ff3311abb80208eb61f7d970f27663d99ebead6aa8d9e03a3980344`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f17314da9b917207b426be4945000a447264fd769ffb75933187c47540eca32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118863429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c291b4d6b2e67d7969d90e0decf0b6e41d17885007113ab204c1ee67704ec`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d109c2e9b032042c67edd2b8f218cff324203972444b46c792c73cf9434b6e`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7695d67c09d74059c12114dcd578fafa7eb9154965b824415cd947a4e9ba2`  
		Last Modified: Tue, 02 Sep 2025 02:16:01 GMT  
		Size: 90.0 MB (90001900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23591ed706efb09741f302134107d502b7e1e030b7097c4a5a84510a6af5020`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:31335caa2da67fd1c40f2b395f2eb967fe2c9f93aef1d9e8d4097cdd6014e879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e73ff6eb993693eba955dbbd9a38c696550afdad8cb4242dd10be4391d51d`

```dockerfile
```

-	Layers:
	-	`sha256:391afd9f1d5071987f7c662c5b37a1c5cb050e3e20ce7a5a1f3ba2af2e5c4556`  
		Last Modified: Tue, 02 Sep 2025 05:51:21 GMT  
		Size: 5.4 MB (5428297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654358133ea0b3fae2e4935e1b3ffdd85714f607a062dac84e3701492e79c2c1`  
		Last Modified: Tue, 02 Sep 2025 05:51:22 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:14c689c0caf1b8da1403a742016ec64d2f5b5b12ecdec2989f36b2c2c4aa1ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:ab67b9d67ae37184f16d8ccec620d663e0710a207d56b4e22b6c13f8043bee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da848aeb51c74301573e300ce714c1707829c1ae13b9123383b88b83855afa`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8f80519b28ebe548dc966edb51696e3747ca2acd3e8c60f635e8233f2fff9c`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b5b8588c9754dfb866e889fde741fc991362bed0091199037a9377fc1debf`  
		Last Modified: Tue, 02 Sep 2025 00:19:38 GMT  
		Size: 90.7 MB (90683182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e81df23c3dd57d43366a29cbca22a6775b9e60fee299c5c9b4b7e3f3974a61`  
		Last Modified: Mon, 01 Sep 2025 23:44:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:233d7440793922b61438dc692aae9ccadfa5852348f5eb22db1d4555f6529b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ba716976d025b1f798a772206b038332aff1e8d17847107d799e591af3c6c`

```dockerfile
```

-	Layers:
	-	`sha256:8d76c6ba7073680c6e8584b2e82b0a06348904dd5b15a3e3972b89568bce3d56`  
		Last Modified: Tue, 02 Sep 2025 02:51:20 GMT  
		Size: 5.4 MB (5421130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c1f8028ff3311abb80208eb61f7d970f27663d99ebead6aa8d9e03a3980344`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f17314da9b917207b426be4945000a447264fd769ffb75933187c47540eca32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118863429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c291b4d6b2e67d7969d90e0decf0b6e41d17885007113ab204c1ee67704ec`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d109c2e9b032042c67edd2b8f218cff324203972444b46c792c73cf9434b6e`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7695d67c09d74059c12114dcd578fafa7eb9154965b824415cd947a4e9ba2`  
		Last Modified: Tue, 02 Sep 2025 02:16:01 GMT  
		Size: 90.0 MB (90001900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23591ed706efb09741f302134107d502b7e1e030b7097c4a5a84510a6af5020`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:31335caa2da67fd1c40f2b395f2eb967fe2c9f93aef1d9e8d4097cdd6014e879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e73ff6eb993693eba955dbbd9a38c696550afdad8cb4242dd10be4391d51d`

```dockerfile
```

-	Layers:
	-	`sha256:391afd9f1d5071987f7c662c5b37a1c5cb050e3e20ce7a5a1f3ba2af2e5c4556`  
		Last Modified: Tue, 02 Sep 2025 05:51:21 GMT  
		Size: 5.4 MB (5428297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654358133ea0b3fae2e4935e1b3ffdd85714f607a062dac84e3701492e79c2c1`  
		Last Modified: Tue, 02 Sep 2025 05:51:22 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:14c689c0caf1b8da1403a742016ec64d2f5b5b12ecdec2989f36b2c2c4aa1ac0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:ab67b9d67ae37184f16d8ccec620d663e0710a207d56b4e22b6c13f8043bee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da848aeb51c74301573e300ce714c1707829c1ae13b9123383b88b83855afa`
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
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
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
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8f80519b28ebe548dc966edb51696e3747ca2acd3e8c60f635e8233f2fff9c`  
		Last Modified: Mon, 01 Sep 2025 23:44:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470b5b8588c9754dfb866e889fde741fc991362bed0091199037a9377fc1debf`  
		Last Modified: Tue, 02 Sep 2025 00:19:38 GMT  
		Size: 90.7 MB (90683182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e81df23c3dd57d43366a29cbca22a6775b9e60fee299c5c9b4b7e3f3974a61`  
		Last Modified: Mon, 01 Sep 2025 23:44:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:233d7440793922b61438dc692aae9ccadfa5852348f5eb22db1d4555f6529b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16ba716976d025b1f798a772206b038332aff1e8d17847107d799e591af3c6c`

```dockerfile
```

-	Layers:
	-	`sha256:8d76c6ba7073680c6e8584b2e82b0a06348904dd5b15a3e3972b89568bce3d56`  
		Last Modified: Tue, 02 Sep 2025 02:51:20 GMT  
		Size: 5.4 MB (5421130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c1f8028ff3311abb80208eb61f7d970f27663d99ebead6aa8d9e03a3980344`  
		Last Modified: Tue, 02 Sep 2025 02:51:21 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f17314da9b917207b426be4945000a447264fd769ffb75933187c47540eca32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118863429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9c291b4d6b2e67d7969d90e0decf0b6e41d17885007113ab204c1ee67704ec`
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
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
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
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d109c2e9b032042c67edd2b8f218cff324203972444b46c792c73cf9434b6e`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d7695d67c09d74059c12114dcd578fafa7eb9154965b824415cd947a4e9ba2`  
		Last Modified: Tue, 02 Sep 2025 02:16:01 GMT  
		Size: 90.0 MB (90001900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23591ed706efb09741f302134107d502b7e1e030b7097c4a5a84510a6af5020`  
		Last Modified: Tue, 02 Sep 2025 02:15:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:31335caa2da67fd1c40f2b395f2eb967fe2c9f93aef1d9e8d4097cdd6014e879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:791e73ff6eb993693eba955dbbd9a38c696550afdad8cb4242dd10be4391d51d`

```dockerfile
```

-	Layers:
	-	`sha256:391afd9f1d5071987f7c662c5b37a1c5cb050e3e20ce7a5a1f3ba2af2e5c4556`  
		Last Modified: Tue, 02 Sep 2025 05:51:21 GMT  
		Size: 5.4 MB (5428297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654358133ea0b3fae2e4935e1b3ffdd85714f607a062dac84e3701492e79c2c1`  
		Last Modified: Tue, 02 Sep 2025 05:51:22 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json
