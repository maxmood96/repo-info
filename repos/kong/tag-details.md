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
$ docker pull kong@sha256:30f468b3b734735afb1f6b10731e2ca915fd308321e12d17aee90d93f373f3b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:a8149ffa0b32afe6fd1b2412766be38e99b48fc934dd71f4c88dabf6d73a91b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185647814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bc6a7d9c58bf211029cd50367ca2c53c4977887b178dd60edc78fa77db8900`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:00 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:00 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:00 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:00 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:00 GMT
ARG KONG_VERSION=2.8.5
# Wed, 15 Apr 2026 20:44:00 GMT
ENV KONG_VERSION=2.8.5
# Wed, 15 Apr 2026 20:44:00 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Wed, 15 Apr 2026 20:44:00 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Wed, 15 Apr 2026 20:44:40 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:40 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:40 GMT
USER kong
# Wed, 15 Apr 2026 20:44:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:40 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675dd6d665db8ee9bc3cd7b556d3138714b83db68ca44074807f4af9a175c7d2`  
		Last Modified: Wed, 15 Apr 2026 20:45:01 GMT  
		Size: 25.1 MB (25081972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f56e80391f8ebc07d8274bd3354fe19ddee2090450f2feb9202f98eba0a9daa`  
		Last Modified: Wed, 15 Apr 2026 20:45:04 GMT  
		Size: 130.8 MB (130828463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf4b37717882db07b2378e00009c15d95d8cc24b76f4dbb9c58f32e05ea3054`  
		Last Modified: Wed, 15 Apr 2026 20:45:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:644eb7f5789ce8763e67f0172e6612df899db44db605ce5ff07b934a01c56e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54255022e63f0eee3eb52a63672a27d8d88cd219b70c476c630fa584f8d7b6cf`

```dockerfile
```

-	Layers:
	-	`sha256:c919d53cece8f897e51c70848c0ca85c3f1a823d16f9cc0a37202ce1f725d4e5`  
		Last Modified: Wed, 15 Apr 2026 20:45:00 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15370fb0d1623191aec7c69887764b7e1d018b7e306d7c7093366c7418892bd`  
		Last Modified: Wed, 15 Apr 2026 20:45:00 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:30f468b3b734735afb1f6b10731e2ca915fd308321e12d17aee90d93f373f3b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:a8149ffa0b32afe6fd1b2412766be38e99b48fc934dd71f4c88dabf6d73a91b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185647814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bc6a7d9c58bf211029cd50367ca2c53c4977887b178dd60edc78fa77db8900`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:00 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:00 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:00 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:00 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:00 GMT
ARG KONG_VERSION=2.8.5
# Wed, 15 Apr 2026 20:44:00 GMT
ENV KONG_VERSION=2.8.5
# Wed, 15 Apr 2026 20:44:00 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Wed, 15 Apr 2026 20:44:00 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Wed, 15 Apr 2026 20:44:40 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:40 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:40 GMT
USER kong
# Wed, 15 Apr 2026 20:44:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:40 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675dd6d665db8ee9bc3cd7b556d3138714b83db68ca44074807f4af9a175c7d2`  
		Last Modified: Wed, 15 Apr 2026 20:45:01 GMT  
		Size: 25.1 MB (25081972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f56e80391f8ebc07d8274bd3354fe19ddee2090450f2feb9202f98eba0a9daa`  
		Last Modified: Wed, 15 Apr 2026 20:45:04 GMT  
		Size: 130.8 MB (130828463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf4b37717882db07b2378e00009c15d95d8cc24b76f4dbb9c58f32e05ea3054`  
		Last Modified: Wed, 15 Apr 2026 20:45:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:644eb7f5789ce8763e67f0172e6612df899db44db605ce5ff07b934a01c56e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54255022e63f0eee3eb52a63672a27d8d88cd219b70c476c630fa584f8d7b6cf`

```dockerfile
```

-	Layers:
	-	`sha256:c919d53cece8f897e51c70848c0ca85c3f1a823d16f9cc0a37202ce1f725d4e5`  
		Last Modified: Wed, 15 Apr 2026 20:45:00 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15370fb0d1623191aec7c69887764b7e1d018b7e306d7c7093366c7418892bd`  
		Last Modified: Wed, 15 Apr 2026 20:45:00 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:a2b2ec9964bba34065943e8be1d56791a4a06b7b0c10222f05564b372ca87840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:327f289717c95bb4780359d3e36d40be69960621ab6165ca3f819be382225835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06902e2a23f12073e9d6e937826fb1a8b61a157e1351e608caf9429b3380ffa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
USER kong
# Wed, 15 Apr 2026 20:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:07 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd65b6a11ddee18686b3f2be07f2f1ea1ab77ada9001da0cf99da8978ce58d`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 90.7 MB (90691111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:db937d9840283ccc1083064491a7c519b0b81f424034fa128a0b06255d672ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76ca1bdcd9a017df41ea6533c554608985c56d0cf1186eec902555adecea7c`

```dockerfile
```

-	Layers:
	-	`sha256:087fe040fe3a3bf1389000b321f51b45316b473b2c8a70d17b1864616ad4abc6`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618d457dd129f5d6a0b05fa3adba7a0dcba5dc06750059a6ecf3dd2d5c89c97d`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:82c6be19b8ed0787102cde0be8ddc1aed906f071eba22fae4499801e95cdf021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118880294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce7cd715d3b3ecb6f2a1b96e44613228892cc83b93bd44ffe4fd748dc525e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
USER kong
# Wed, 15 Apr 2026 20:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3febfbf6304e46967730813d4032e5fa853fb66e54adbfaf5aeb196451edcc7`  
		Last Modified: Wed, 15 Apr 2026 20:44:28 GMT  
		Size: 90.0 MB (90003223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:97fcb364af332a92fd33df1e4bcc90bf8d4e2b22d1dfc4fe95b07a6cc64cd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d8ed64c042638f54746d10f8b7d0f98053c281e6f1460fe09b3e2d652fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:f47e9de54c27b6bb889f34dadc202d113b69995730cd05a81f212b129f0bb201`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0232072f65cfe0f74a70d8a0ecc05c7d1fbc882c740111d9e144af0a2a95050c`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:ea85737d353c163b0c846cb1773ecfec0101397f9d7b525ee1eefdc0ad20d7f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:45ce1b3dcf7a5e1bb7a0ac70f88e6386331adeeef2807ffab15974c2137d498b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92477734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88b2ef9de1f06f15a504c1391bb53cd2f7872a218ae162cffd562bb50b88a80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:53 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:53 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:53 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:53 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:43:53 GMT
ENV KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 15 Apr 2026 20:44:15 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:15 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:15 GMT
USER kong
# Wed, 15 Apr 2026 20:44:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:15 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdf2b7803739501653b4cc27b29ceb2817c4af6ffdac905c76d3eec567d6324`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9414d556581353f3222377df9b33744f5720ef5de5d380efe97a47ca79988eeb`  
		Last Modified: Wed, 15 Apr 2026 20:44:31 GMT  
		Size: 62.7 MB (62739955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abae510c54db04fd1551664e0f43283ca4e6a7d8001bb21294be4fce1f64bd5`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:f2b9ca27f1b7bc1c7ead0c3e234f79410d8710316d421cf2f385922cc3f9cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b00ce5d0602ca92da49c18aa41999da28a7fdbc85136a63cbc688f0a827a6ed`

```dockerfile
```

-	Layers:
	-	`sha256:6e1ae54c5d215c440e3e940db8971c9358712516ce9ec54fa8ce0fb926204195`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1645c7f12ed4b8f2af4ddc478f9e2af326746b7d88bb7ba8c5b6abde1b80c418`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0a0dd77781af5017a0de77becd15bd6417c788468fb53cb48b91df9b0e409147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88813013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0738393c39c566ec83c2be09902a7096812a6270241e56979b3ee6d1a688a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:44:05 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:05 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:05 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:05 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:44:05 GMT
ENV KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 15 Apr 2026 20:44:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
USER kong
# Wed, 15 Apr 2026 20:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1f6f3b729273de8849986322f6f0f0103a7f2bfbbf6518692a5b4174ab28d`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4234a7ee4b4daafa2367b4c8a705dc6b14985bb7e3a735455b8bb721aa9dc4`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 61.2 MB (61205184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cfe3a536eac97f384562c7e4f166042abda445738aeac30d43ece5a58b48dc`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:afe6d763403b265aa745baa0ba81a00b91b446e00883f8bff85fd0136e654c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd2b03706694d1b4f44843b4a4edee5c0dd45e890563da15f776455d1840576`

```dockerfile
```

-	Layers:
	-	`sha256:e90fe2fbd024c64dd61ce1e38922a8f176af130b252f6b009da9a5654269f5a6`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853369987859d63ebefa5a5c339f61b5b64e5a6a18fe35621655885e399c62a7`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:ea85737d353c163b0c846cb1773ecfec0101397f9d7b525ee1eefdc0ad20d7f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:45ce1b3dcf7a5e1bb7a0ac70f88e6386331adeeef2807ffab15974c2137d498b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92477734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88b2ef9de1f06f15a504c1391bb53cd2f7872a218ae162cffd562bb50b88a80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:53 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:53 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:53 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:53 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:43:53 GMT
ENV KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 15 Apr 2026 20:44:15 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:15 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:15 GMT
USER kong
# Wed, 15 Apr 2026 20:44:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:15 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdf2b7803739501653b4cc27b29ceb2817c4af6ffdac905c76d3eec567d6324`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9414d556581353f3222377df9b33744f5720ef5de5d380efe97a47ca79988eeb`  
		Last Modified: Wed, 15 Apr 2026 20:44:31 GMT  
		Size: 62.7 MB (62739955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abae510c54db04fd1551664e0f43283ca4e6a7d8001bb21294be4fce1f64bd5`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f2b9ca27f1b7bc1c7ead0c3e234f79410d8710316d421cf2f385922cc3f9cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b00ce5d0602ca92da49c18aa41999da28a7fdbc85136a63cbc688f0a827a6ed`

```dockerfile
```

-	Layers:
	-	`sha256:6e1ae54c5d215c440e3e940db8971c9358712516ce9ec54fa8ce0fb926204195`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1645c7f12ed4b8f2af4ddc478f9e2af326746b7d88bb7ba8c5b6abde1b80c418`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0a0dd77781af5017a0de77becd15bd6417c788468fb53cb48b91df9b0e409147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88813013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0738393c39c566ec83c2be09902a7096812a6270241e56979b3ee6d1a688a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:44:05 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:05 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:05 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:05 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:44:05 GMT
ENV KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 15 Apr 2026 20:44:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
USER kong
# Wed, 15 Apr 2026 20:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1f6f3b729273de8849986322f6f0f0103a7f2bfbbf6518692a5b4174ab28d`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4234a7ee4b4daafa2367b4c8a705dc6b14985bb7e3a735455b8bb721aa9dc4`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 61.2 MB (61205184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cfe3a536eac97f384562c7e4f166042abda445738aeac30d43ece5a58b48dc`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:afe6d763403b265aa745baa0ba81a00b91b446e00883f8bff85fd0136e654c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd2b03706694d1b4f44843b4a4edee5c0dd45e890563da15f776455d1840576`

```dockerfile
```

-	Layers:
	-	`sha256:e90fe2fbd024c64dd61ce1e38922a8f176af130b252f6b009da9a5654269f5a6`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853369987859d63ebefa5a5c339f61b5b64e5a6a18fe35621655885e399c62a7`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:ea85737d353c163b0c846cb1773ecfec0101397f9d7b525ee1eefdc0ad20d7f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:45ce1b3dcf7a5e1bb7a0ac70f88e6386331adeeef2807ffab15974c2137d498b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92477734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88b2ef9de1f06f15a504c1391bb53cd2f7872a218ae162cffd562bb50b88a80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:53 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:53 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:53 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:53 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:43:53 GMT
ENV KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 15 Apr 2026 20:44:15 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:15 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:15 GMT
USER kong
# Wed, 15 Apr 2026 20:44:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:15 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdf2b7803739501653b4cc27b29ceb2817c4af6ffdac905c76d3eec567d6324`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9414d556581353f3222377df9b33744f5720ef5de5d380efe97a47ca79988eeb`  
		Last Modified: Wed, 15 Apr 2026 20:44:31 GMT  
		Size: 62.7 MB (62739955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abae510c54db04fd1551664e0f43283ca4e6a7d8001bb21294be4fce1f64bd5`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:f2b9ca27f1b7bc1c7ead0c3e234f79410d8710316d421cf2f385922cc3f9cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b00ce5d0602ca92da49c18aa41999da28a7fdbc85136a63cbc688f0a827a6ed`

```dockerfile
```

-	Layers:
	-	`sha256:6e1ae54c5d215c440e3e940db8971c9358712516ce9ec54fa8ce0fb926204195`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1645c7f12ed4b8f2af4ddc478f9e2af326746b7d88bb7ba8c5b6abde1b80c418`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0a0dd77781af5017a0de77becd15bd6417c788468fb53cb48b91df9b0e409147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88813013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0738393c39c566ec83c2be09902a7096812a6270241e56979b3ee6d1a688a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:44:05 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:05 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:05 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:05 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:44:05 GMT
ENV KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 15 Apr 2026 20:44:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
USER kong
# Wed, 15 Apr 2026 20:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1f6f3b729273de8849986322f6f0f0103a7f2bfbbf6518692a5b4174ab28d`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4234a7ee4b4daafa2367b4c8a705dc6b14985bb7e3a735455b8bb721aa9dc4`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 61.2 MB (61205184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cfe3a536eac97f384562c7e4f166042abda445738aeac30d43ece5a58b48dc`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:afe6d763403b265aa745baa0ba81a00b91b446e00883f8bff85fd0136e654c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd2b03706694d1b4f44843b4a4edee5c0dd45e890563da15f776455d1840576`

```dockerfile
```

-	Layers:
	-	`sha256:e90fe2fbd024c64dd61ce1e38922a8f176af130b252f6b009da9a5654269f5a6`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853369987859d63ebefa5a5c339f61b5b64e5a6a18fe35621655885e399c62a7`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:ea85737d353c163b0c846cb1773ecfec0101397f9d7b525ee1eefdc0ad20d7f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:45ce1b3dcf7a5e1bb7a0ac70f88e6386331adeeef2807ffab15974c2137d498b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92477734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88b2ef9de1f06f15a504c1391bb53cd2f7872a218ae162cffd562bb50b88a80`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:53 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:53 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:53 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:53 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:53 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:43:53 GMT
ENV KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 15 Apr 2026 20:43:53 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 15 Apr 2026 20:44:15 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:15 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:15 GMT
USER kong
# Wed, 15 Apr 2026 20:44:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:15 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdf2b7803739501653b4cc27b29ceb2817c4af6ffdac905c76d3eec567d6324`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9414d556581353f3222377df9b33744f5720ef5de5d380efe97a47ca79988eeb`  
		Last Modified: Wed, 15 Apr 2026 20:44:31 GMT  
		Size: 62.7 MB (62739955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abae510c54db04fd1551664e0f43283ca4e6a7d8001bb21294be4fce1f64bd5`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:f2b9ca27f1b7bc1c7ead0c3e234f79410d8710316d421cf2f385922cc3f9cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b00ce5d0602ca92da49c18aa41999da28a7fdbc85136a63cbc688f0a827a6ed`

```dockerfile
```

-	Layers:
	-	`sha256:6e1ae54c5d215c440e3e940db8971c9358712516ce9ec54fa8ce0fb926204195`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1645c7f12ed4b8f2af4ddc478f9e2af326746b7d88bb7ba8c5b6abde1b80c418`  
		Last Modified: Wed, 15 Apr 2026 20:44:29 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0a0dd77781af5017a0de77becd15bd6417c788468fb53cb48b91df9b0e409147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88813013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0738393c39c566ec83c2be09902a7096812a6270241e56979b3ee6d1a688a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:44:05 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:05 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:05 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:05 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:44:05 GMT
ENV KONG_VERSION=3.4.2
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 15 Apr 2026 20:44:05 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 15 Apr 2026 20:44:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
USER kong
# Wed, 15 Apr 2026 20:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca1f6f3b729273de8849986322f6f0f0103a7f2bfbbf6518692a5b4174ab28d`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4234a7ee4b4daafa2367b4c8a705dc6b14985bb7e3a735455b8bb721aa9dc4`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 61.2 MB (61205184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cfe3a536eac97f384562c7e4f166042abda445738aeac30d43ece5a58b48dc`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:afe6d763403b265aa745baa0ba81a00b91b446e00883f8bff85fd0136e654c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd2b03706694d1b4f44843b4a4edee5c0dd45e890563da15f776455d1840576`

```dockerfile
```

-	Layers:
	-	`sha256:e90fe2fbd024c64dd61ce1e38922a8f176af130b252f6b009da9a5654269f5a6`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:853369987859d63ebefa5a5c339f61b5b64e5a6a18fe35621655885e399c62a7`  
		Last Modified: Wed, 15 Apr 2026 20:44:48 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:5ed5111047676680bc447869771c049c60763a0a22a734e70216f9c34e660294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:2fc6fda349e1f8e821f868c9791639531b820a3c5d4998ee7cb195316ec319c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117754776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f21e4bcb2bea5645f0c41ad1cda0805e73733d647e668b70a407e667e5b41c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:47 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:47 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:47 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:43:47 GMT
ENV KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 15 Apr 2026 20:44:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:09 GMT
USER kong
# Wed, 15 Apr 2026 20:44:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0d1721dc44241bef70bc9998c15ad9548ea54912ff7028dbcab52b5a7b582b`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aede5ba52367fb0ac2ce63d1881dab4616788f58c0672d5f1858c90dd66c1696`  
		Last Modified: Wed, 15 Apr 2026 20:44:27 GMT  
		Size: 88.0 MB (88016993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6ad23c09377ac667d69bd256994c1ce6f17e265fe09f789d27a0bc1a79e3`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:957f36c236ea078e52fe532b19844f0121a2382df908b4bb2da926290460242b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e429cd56ec090122d8fdd94805c831dccc1542c7d33fd3339aa5e58eb94f6c63`

```dockerfile
```

-	Layers:
	-	`sha256:8cfe7cc13351d01d31aa38a522d3f09e37384fc4fa913d98314190479620f9b7`  
		Last Modified: Wed, 15 Apr 2026 20:44:25 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e503ce033f7e1301a885efc652669e1e9e545bc51fa062b9a125873e3a8b2cc`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 15.3 KB (15345 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:78b4f2c403eeb190aad742de690c184d3456c21c9e401a219eca192cea4faaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114931501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a402345f85502b0753503c97e441849166576a2c47746de248e2f557b982f8f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:03 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:44:03 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:03 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:03 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:03 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:44:03 GMT
ENV KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 15 Apr 2026 20:44:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
USER kong
# Wed, 15 Apr 2026 20:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4ee17b398c7ab0b25f472279a8cbce64edcf69af97520f4805d642942e5ce`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6964682687ceb6c26767a6a683086bf02261e7d2ec88f0f42a81f11b30a921a`  
		Last Modified: Wed, 15 Apr 2026 20:44:53 GMT  
		Size: 87.3 MB (87323676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b995e8a59177bc2ae3f84444165e9ec350489a207b125ba1424ae4799385b603`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:1c9385d2a54853c848242467c3cf95d6dfe088aeb4bf72a9202ac20c90de44ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024091a70d5c8f65d8b9dc5c4524c9f1fd3c7b6a5230e109344afae2c3bbbbc0`

```dockerfile
```

-	Layers:
	-	`sha256:15bfafe16b3fe2b0386f17746476a60b6d4e6471384c82962c25d7240bd31247`  
		Last Modified: Wed, 15 Apr 2026 20:44:51 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c9271b1d4de042126aad10b99825b00ae52979f4935af0c816985a52adf0e0`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:5ed5111047676680bc447869771c049c60763a0a22a734e70216f9c34e660294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2fc6fda349e1f8e821f868c9791639531b820a3c5d4998ee7cb195316ec319c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117754776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f21e4bcb2bea5645f0c41ad1cda0805e73733d647e668b70a407e667e5b41c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:47 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:47 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:47 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:43:47 GMT
ENV KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 15 Apr 2026 20:44:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:09 GMT
USER kong
# Wed, 15 Apr 2026 20:44:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0d1721dc44241bef70bc9998c15ad9548ea54912ff7028dbcab52b5a7b582b`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aede5ba52367fb0ac2ce63d1881dab4616788f58c0672d5f1858c90dd66c1696`  
		Last Modified: Wed, 15 Apr 2026 20:44:27 GMT  
		Size: 88.0 MB (88016993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6ad23c09377ac667d69bd256994c1ce6f17e265fe09f789d27a0bc1a79e3`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:957f36c236ea078e52fe532b19844f0121a2382df908b4bb2da926290460242b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e429cd56ec090122d8fdd94805c831dccc1542c7d33fd3339aa5e58eb94f6c63`

```dockerfile
```

-	Layers:
	-	`sha256:8cfe7cc13351d01d31aa38a522d3f09e37384fc4fa913d98314190479620f9b7`  
		Last Modified: Wed, 15 Apr 2026 20:44:25 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e503ce033f7e1301a885efc652669e1e9e545bc51fa062b9a125873e3a8b2cc`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 15.3 KB (15345 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:78b4f2c403eeb190aad742de690c184d3456c21c9e401a219eca192cea4faaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114931501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a402345f85502b0753503c97e441849166576a2c47746de248e2f557b982f8f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:03 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:44:03 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:03 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:03 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:03 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:44:03 GMT
ENV KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 15 Apr 2026 20:44:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
USER kong
# Wed, 15 Apr 2026 20:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4ee17b398c7ab0b25f472279a8cbce64edcf69af97520f4805d642942e5ce`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6964682687ceb6c26767a6a683086bf02261e7d2ec88f0f42a81f11b30a921a`  
		Last Modified: Wed, 15 Apr 2026 20:44:53 GMT  
		Size: 87.3 MB (87323676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b995e8a59177bc2ae3f84444165e9ec350489a207b125ba1424ae4799385b603`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1c9385d2a54853c848242467c3cf95d6dfe088aeb4bf72a9202ac20c90de44ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024091a70d5c8f65d8b9dc5c4524c9f1fd3c7b6a5230e109344afae2c3bbbbc0`

```dockerfile
```

-	Layers:
	-	`sha256:15bfafe16b3fe2b0386f17746476a60b6d4e6471384c82962c25d7240bd31247`  
		Last Modified: Wed, 15 Apr 2026 20:44:51 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c9271b1d4de042126aad10b99825b00ae52979f4935af0c816985a52adf0e0`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:5ed5111047676680bc447869771c049c60763a0a22a734e70216f9c34e660294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:2fc6fda349e1f8e821f868c9791639531b820a3c5d4998ee7cb195316ec319c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117754776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f21e4bcb2bea5645f0c41ad1cda0805e73733d647e668b70a407e667e5b41c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:47 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:47 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:47 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:43:47 GMT
ENV KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 15 Apr 2026 20:44:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:09 GMT
USER kong
# Wed, 15 Apr 2026 20:44:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0d1721dc44241bef70bc9998c15ad9548ea54912ff7028dbcab52b5a7b582b`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aede5ba52367fb0ac2ce63d1881dab4616788f58c0672d5f1858c90dd66c1696`  
		Last Modified: Wed, 15 Apr 2026 20:44:27 GMT  
		Size: 88.0 MB (88016993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6ad23c09377ac667d69bd256994c1ce6f17e265fe09f789d27a0bc1a79e3`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:957f36c236ea078e52fe532b19844f0121a2382df908b4bb2da926290460242b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e429cd56ec090122d8fdd94805c831dccc1542c7d33fd3339aa5e58eb94f6c63`

```dockerfile
```

-	Layers:
	-	`sha256:8cfe7cc13351d01d31aa38a522d3f09e37384fc4fa913d98314190479620f9b7`  
		Last Modified: Wed, 15 Apr 2026 20:44:25 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e503ce033f7e1301a885efc652669e1e9e545bc51fa062b9a125873e3a8b2cc`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 15.3 KB (15345 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:78b4f2c403eeb190aad742de690c184d3456c21c9e401a219eca192cea4faaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114931501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a402345f85502b0753503c97e441849166576a2c47746de248e2f557b982f8f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:03 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:44:03 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:03 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:03 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:03 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:44:03 GMT
ENV KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 15 Apr 2026 20:44:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
USER kong
# Wed, 15 Apr 2026 20:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4ee17b398c7ab0b25f472279a8cbce64edcf69af97520f4805d642942e5ce`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6964682687ceb6c26767a6a683086bf02261e7d2ec88f0f42a81f11b30a921a`  
		Last Modified: Wed, 15 Apr 2026 20:44:53 GMT  
		Size: 87.3 MB (87323676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b995e8a59177bc2ae3f84444165e9ec350489a207b125ba1424ae4799385b603`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:1c9385d2a54853c848242467c3cf95d6dfe088aeb4bf72a9202ac20c90de44ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024091a70d5c8f65d8b9dc5c4524c9f1fd3c7b6a5230e109344afae2c3bbbbc0`

```dockerfile
```

-	Layers:
	-	`sha256:15bfafe16b3fe2b0386f17746476a60b6d4e6471384c82962c25d7240bd31247`  
		Last Modified: Wed, 15 Apr 2026 20:44:51 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c9271b1d4de042126aad10b99825b00ae52979f4935af0c816985a52adf0e0`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:5ed5111047676680bc447869771c049c60763a0a22a734e70216f9c34e660294
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2fc6fda349e1f8e821f868c9791639531b820a3c5d4998ee7cb195316ec319c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117754776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f21e4bcb2bea5645f0c41ad1cda0805e73733d647e668b70a407e667e5b41c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:47 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:47 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:47 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:43:47 GMT
ENV KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 15 Apr 2026 20:43:47 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 15 Apr 2026 20:44:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:09 GMT
USER kong
# Wed, 15 Apr 2026 20:44:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0d1721dc44241bef70bc9998c15ad9548ea54912ff7028dbcab52b5a7b582b`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aede5ba52367fb0ac2ce63d1881dab4616788f58c0672d5f1858c90dd66c1696`  
		Last Modified: Wed, 15 Apr 2026 20:44:27 GMT  
		Size: 88.0 MB (88016993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acf6ad23c09377ac667d69bd256994c1ce6f17e265fe09f789d27a0bc1a79e3`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:957f36c236ea078e52fe532b19844f0121a2382df908b4bb2da926290460242b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e429cd56ec090122d8fdd94805c831dccc1542c7d33fd3339aa5e58eb94f6c63`

```dockerfile
```

-	Layers:
	-	`sha256:8cfe7cc13351d01d31aa38a522d3f09e37384fc4fa913d98314190479620f9b7`  
		Last Modified: Wed, 15 Apr 2026 20:44:25 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e503ce033f7e1301a885efc652669e1e9e545bc51fa062b9a125873e3a8b2cc`  
		Last Modified: Wed, 15 Apr 2026 20:44:24 GMT  
		Size: 15.3 KB (15345 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:78b4f2c403eeb190aad742de690c184d3456c21c9e401a219eca192cea4faaf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114931501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a402345f85502b0753503c97e441849166576a2c47746de248e2f557b982f8f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:44:03 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:44:03 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:44:03 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:44:03 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:44:03 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:44:03 GMT
ENV KONG_VERSION=3.8.0
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 15 Apr 2026 20:44:03 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 15 Apr 2026 20:44:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:33 GMT
USER kong
# Wed, 15 Apr 2026 20:44:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a4ee17b398c7ab0b25f472279a8cbce64edcf69af97520f4805d642942e5ce`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6964682687ceb6c26767a6a683086bf02261e7d2ec88f0f42a81f11b30a921a`  
		Last Modified: Wed, 15 Apr 2026 20:44:53 GMT  
		Size: 87.3 MB (87323676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b995e8a59177bc2ae3f84444165e9ec350489a207b125ba1424ae4799385b603`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1c9385d2a54853c848242467c3cf95d6dfe088aeb4bf72a9202ac20c90de44ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024091a70d5c8f65d8b9dc5c4524c9f1fd3c7b6a5230e109344afae2c3bbbbc0`

```dockerfile
```

-	Layers:
	-	`sha256:15bfafe16b3fe2b0386f17746476a60b6d4e6471384c82962c25d7240bd31247`  
		Last Modified: Wed, 15 Apr 2026 20:44:51 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65c9271b1d4de042126aad10b99825b00ae52979f4935af0c816985a52adf0e0`  
		Last Modified: Wed, 15 Apr 2026 20:44:50 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:a2b2ec9964bba34065943e8be1d56791a4a06b7b0c10222f05564b372ca87840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:327f289717c95bb4780359d3e36d40be69960621ab6165ca3f819be382225835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06902e2a23f12073e9d6e937826fb1a8b61a157e1351e608caf9429b3380ffa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
USER kong
# Wed, 15 Apr 2026 20:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:07 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd65b6a11ddee18686b3f2be07f2f1ea1ab77ada9001da0cf99da8978ce58d`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 90.7 MB (90691111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:db937d9840283ccc1083064491a7c519b0b81f424034fa128a0b06255d672ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76ca1bdcd9a017df41ea6533c554608985c56d0cf1186eec902555adecea7c`

```dockerfile
```

-	Layers:
	-	`sha256:087fe040fe3a3bf1389000b321f51b45316b473b2c8a70d17b1864616ad4abc6`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618d457dd129f5d6a0b05fa3adba7a0dcba5dc06750059a6ecf3dd2d5c89c97d`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:82c6be19b8ed0787102cde0be8ddc1aed906f071eba22fae4499801e95cdf021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118880294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce7cd715d3b3ecb6f2a1b96e44613228892cc83b93bd44ffe4fd748dc525e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
USER kong
# Wed, 15 Apr 2026 20:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3febfbf6304e46967730813d4032e5fa853fb66e54adbfaf5aeb196451edcc7`  
		Last Modified: Wed, 15 Apr 2026 20:44:28 GMT  
		Size: 90.0 MB (90003223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:97fcb364af332a92fd33df1e4bcc90bf8d4e2b22d1dfc4fe95b07a6cc64cd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d8ed64c042638f54746d10f8b7d0f98053c281e6f1460fe09b3e2d652fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:f47e9de54c27b6bb889f34dadc202d113b69995730cd05a81f212b129f0bb201`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0232072f65cfe0f74a70d8a0ecc05c7d1fbc882c740111d9e144af0a2a95050c`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:a2b2ec9964bba34065943e8be1d56791a4a06b7b0c10222f05564b372ca87840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:327f289717c95bb4780359d3e36d40be69960621ab6165ca3f819be382225835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06902e2a23f12073e9d6e937826fb1a8b61a157e1351e608caf9429b3380ffa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
USER kong
# Wed, 15 Apr 2026 20:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:07 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd65b6a11ddee18686b3f2be07f2f1ea1ab77ada9001da0cf99da8978ce58d`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 90.7 MB (90691111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:db937d9840283ccc1083064491a7c519b0b81f424034fa128a0b06255d672ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76ca1bdcd9a017df41ea6533c554608985c56d0cf1186eec902555adecea7c`

```dockerfile
```

-	Layers:
	-	`sha256:087fe040fe3a3bf1389000b321f51b45316b473b2c8a70d17b1864616ad4abc6`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618d457dd129f5d6a0b05fa3adba7a0dcba5dc06750059a6ecf3dd2d5c89c97d`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:82c6be19b8ed0787102cde0be8ddc1aed906f071eba22fae4499801e95cdf021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118880294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce7cd715d3b3ecb6f2a1b96e44613228892cc83b93bd44ffe4fd748dc525e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
USER kong
# Wed, 15 Apr 2026 20:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3febfbf6304e46967730813d4032e5fa853fb66e54adbfaf5aeb196451edcc7`  
		Last Modified: Wed, 15 Apr 2026 20:44:28 GMT  
		Size: 90.0 MB (90003223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:97fcb364af332a92fd33df1e4bcc90bf8d4e2b22d1dfc4fe95b07a6cc64cd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d8ed64c042638f54746d10f8b7d0f98053c281e6f1460fe09b3e2d652fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:f47e9de54c27b6bb889f34dadc202d113b69995730cd05a81f212b129f0bb201`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0232072f65cfe0f74a70d8a0ecc05c7d1fbc882c740111d9e144af0a2a95050c`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:a2b2ec9964bba34065943e8be1d56791a4a06b7b0c10222f05564b372ca87840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:327f289717c95bb4780359d3e36d40be69960621ab6165ca3f819be382225835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06902e2a23f12073e9d6e937826fb1a8b61a157e1351e608caf9429b3380ffa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
USER kong
# Wed, 15 Apr 2026 20:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:07 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd65b6a11ddee18686b3f2be07f2f1ea1ab77ada9001da0cf99da8978ce58d`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 90.7 MB (90691111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:db937d9840283ccc1083064491a7c519b0b81f424034fa128a0b06255d672ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76ca1bdcd9a017df41ea6533c554608985c56d0cf1186eec902555adecea7c`

```dockerfile
```

-	Layers:
	-	`sha256:087fe040fe3a3bf1389000b321f51b45316b473b2c8a70d17b1864616ad4abc6`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618d457dd129f5d6a0b05fa3adba7a0dcba5dc06750059a6ecf3dd2d5c89c97d`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:82c6be19b8ed0787102cde0be8ddc1aed906f071eba22fae4499801e95cdf021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118880294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce7cd715d3b3ecb6f2a1b96e44613228892cc83b93bd44ffe4fd748dc525e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
USER kong
# Wed, 15 Apr 2026 20:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3febfbf6304e46967730813d4032e5fa853fb66e54adbfaf5aeb196451edcc7`  
		Last Modified: Wed, 15 Apr 2026 20:44:28 GMT  
		Size: 90.0 MB (90003223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:97fcb364af332a92fd33df1e4bcc90bf8d4e2b22d1dfc4fe95b07a6cc64cd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d8ed64c042638f54746d10f8b7d0f98053c281e6f1460fe09b3e2d652fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:f47e9de54c27b6bb889f34dadc202d113b69995730cd05a81f212b129f0bb201`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0232072f65cfe0f74a70d8a0ecc05c7d1fbc882c740111d9e144af0a2a95050c`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:a2b2ec9964bba34065943e8be1d56791a4a06b7b0c10222f05564b372ca87840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:327f289717c95bb4780359d3e36d40be69960621ab6165ca3f819be382225835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06902e2a23f12073e9d6e937826fb1a8b61a157e1351e608caf9429b3380ffa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
USER kong
# Wed, 15 Apr 2026 20:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:07 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd65b6a11ddee18686b3f2be07f2f1ea1ab77ada9001da0cf99da8978ce58d`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 90.7 MB (90691111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:db937d9840283ccc1083064491a7c519b0b81f424034fa128a0b06255d672ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76ca1bdcd9a017df41ea6533c554608985c56d0cf1186eec902555adecea7c`

```dockerfile
```

-	Layers:
	-	`sha256:087fe040fe3a3bf1389000b321f51b45316b473b2c8a70d17b1864616ad4abc6`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618d457dd129f5d6a0b05fa3adba7a0dcba5dc06750059a6ecf3dd2d5c89c97d`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:82c6be19b8ed0787102cde0be8ddc1aed906f071eba22fae4499801e95cdf021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118880294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce7cd715d3b3ecb6f2a1b96e44613228892cc83b93bd44ffe4fd748dc525e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
USER kong
# Wed, 15 Apr 2026 20:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3febfbf6304e46967730813d4032e5fa853fb66e54adbfaf5aeb196451edcc7`  
		Last Modified: Wed, 15 Apr 2026 20:44:28 GMT  
		Size: 90.0 MB (90003223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:97fcb364af332a92fd33df1e4bcc90bf8d4e2b22d1dfc4fe95b07a6cc64cd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d8ed64c042638f54746d10f8b7d0f98053c281e6f1460fe09b3e2d652fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:f47e9de54c27b6bb889f34dadc202d113b69995730cd05a81f212b129f0bb201`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0232072f65cfe0f74a70d8a0ecc05c7d1fbc882c740111d9e144af0a2a95050c`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:a2b2ec9964bba34065943e8be1d56791a4a06b7b0c10222f05564b372ca87840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:327f289717c95bb4780359d3e36d40be69960621ab6165ca3f819be382225835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06902e2a23f12073e9d6e937826fb1a8b61a157e1351e608caf9429b3380ffa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
USER kong
# Wed, 15 Apr 2026 20:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:07 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd65b6a11ddee18686b3f2be07f2f1ea1ab77ada9001da0cf99da8978ce58d`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 90.7 MB (90691111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:db937d9840283ccc1083064491a7c519b0b81f424034fa128a0b06255d672ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76ca1bdcd9a017df41ea6533c554608985c56d0cf1186eec902555adecea7c`

```dockerfile
```

-	Layers:
	-	`sha256:087fe040fe3a3bf1389000b321f51b45316b473b2c8a70d17b1864616ad4abc6`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618d457dd129f5d6a0b05fa3adba7a0dcba5dc06750059a6ecf3dd2d5c89c97d`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:82c6be19b8ed0787102cde0be8ddc1aed906f071eba22fae4499801e95cdf021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118880294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce7cd715d3b3ecb6f2a1b96e44613228892cc83b93bd44ffe4fd748dc525e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
USER kong
# Wed, 15 Apr 2026 20:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3febfbf6304e46967730813d4032e5fa853fb66e54adbfaf5aeb196451edcc7`  
		Last Modified: Wed, 15 Apr 2026 20:44:28 GMT  
		Size: 90.0 MB (90003223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:97fcb364af332a92fd33df1e4bcc90bf8d4e2b22d1dfc4fe95b07a6cc64cd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d8ed64c042638f54746d10f8b7d0f98053c281e6f1460fe09b3e2d652fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:f47e9de54c27b6bb889f34dadc202d113b69995730cd05a81f212b129f0bb201`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0232072f65cfe0f74a70d8a0ecc05c7d1fbc882c740111d9e144af0a2a95050c`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:a2b2ec9964bba34065943e8be1d56791a4a06b7b0c10222f05564b372ca87840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:327f289717c95bb4780359d3e36d40be69960621ab6165ca3f819be382225835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06902e2a23f12073e9d6e937826fb1a8b61a157e1351e608caf9429b3380ffa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:07 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:07 GMT
USER kong
# Wed, 15 Apr 2026 20:44:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:07 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:07 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:07 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd65b6a11ddee18686b3f2be07f2f1ea1ab77ada9001da0cf99da8978ce58d`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 90.7 MB (90691111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:db937d9840283ccc1083064491a7c519b0b81f424034fa128a0b06255d672ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b76ca1bdcd9a017df41ea6533c554608985c56d0cf1186eec902555adecea7c`

```dockerfile
```

-	Layers:
	-	`sha256:087fe040fe3a3bf1389000b321f51b45316b473b2c8a70d17b1864616ad4abc6`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:618d457dd129f5d6a0b05fa3adba7a0dcba5dc06750059a6ecf3dd2d5c89c97d`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:82c6be19b8ed0787102cde0be8ddc1aed906f071eba22fae4499801e95cdf021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118880294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3ce7cd715d3b3ecb6f2a1b96e44613228892cc83b93bd44ffe4fd748dc525e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:43:41 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 15 Apr 2026 20:43:41 GMT
ARG ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ENV ASSET=ce
# Wed, 15 Apr 2026 20:43:41 GMT
ARG EE_PORTS
# Wed, 15 Apr 2026 20:43:41 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ENV KONG_VERSION=3.9.1
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Wed, 15 Apr 2026 20:43:41 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Wed, 15 Apr 2026 20:44:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:44:08 GMT
USER kong
# Wed, 15 Apr 2026 20:44:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:44:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 15 Apr 2026 20:44:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:44:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 15 Apr 2026 20:44:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5077b8acd5c604b1d38c2a77fa2b68f1acf3fd3bc014983c3a6e0a52b8cfbe`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3febfbf6304e46967730813d4032e5fa853fb66e54adbfaf5aeb196451edcc7`  
		Last Modified: Wed, 15 Apr 2026 20:44:28 GMT  
		Size: 90.0 MB (90003223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5973c4ffecde023d881eec92952bd29877b227d83359c030decbc87ea785dd96`  
		Last Modified: Wed, 15 Apr 2026 20:44:23 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:97fcb364af332a92fd33df1e4bcc90bf8d4e2b22d1dfc4fe95b07a6cc64cd1cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357d8ed64c042638f54746d10f8b7d0f98053c281e6f1460fe09b3e2d652fcc1`

```dockerfile
```

-	Layers:
	-	`sha256:f47e9de54c27b6bb889f34dadc202d113b69995730cd05a81f212b129f0bb201`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0232072f65cfe0f74a70d8a0ecc05c7d1fbc882c740111d9e144af0a2a95050c`  
		Last Modified: Wed, 15 Apr 2026 20:44:26 GMT  
		Size: 16.4 KB (16356 bytes)  
		MIME: application/vnd.in-toto+json
