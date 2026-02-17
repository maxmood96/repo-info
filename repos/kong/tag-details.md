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
$ docker pull kong@sha256:1afad250a350eefb3a5d80bb4e92d16575228fd006a057d70fb2eee208c90618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:fab41c503e9189f2ceefb69aabf85044a802fbc9dafe732e5d55ac241a48fffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185446133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653275fe160f6d39ba2e2e50a32e816399492c82ae067ccce46c61ce8d170d45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:27 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:27 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:27 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:27 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:27 GMT
ARG KONG_VERSION=2.8.5
# Tue, 17 Feb 2026 20:27:27 GMT
ENV KONG_VERSION=2.8.5
# Tue, 17 Feb 2026 20:27:27 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 17 Feb 2026 20:27:27 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 17 Feb 2026 20:28:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:28:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:28:08 GMT
USER kong
# Tue, 17 Feb 2026 20:28:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:28:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:28:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:28:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:28:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cea0d63b25013eabd90428bbaba27478449851f8fe13de680cf7f35bee1677`  
		Last Modified: Tue, 17 Feb 2026 20:28:31 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711e2716a72edc7bbf4d725033bc589cf83978350b8487f7475d5884be90a58`  
		Last Modified: Tue, 17 Feb 2026 20:28:34 GMT  
		Size: 130.8 MB (130825919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bf636a76b3edc4166cb428f96ffe259d34ab10916336422895abf607536dca`  
		Last Modified: Tue, 17 Feb 2026 20:28:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5391bacb27c264fb6bc959e910d7d4067a1d49a4874ecfb6a86416d200517de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d5dec1cffd0060563ab6d443784671e1b6dc118fb570e11af557ee598127eb`

```dockerfile
```

-	Layers:
	-	`sha256:e7172e3b1a6d7a9dc7bea9bdd7e4685d69175bc048b96603b759b518e3b82356`  
		Last Modified: Tue, 17 Feb 2026 20:28:31 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697f43d1fcc76732555dc8da3ea4677f6ac7d60fe6190df5b468a2f97a8778d8`  
		Last Modified: Tue, 17 Feb 2026 20:28:30 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:1afad250a350eefb3a5d80bb4e92d16575228fd006a057d70fb2eee208c90618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:fab41c503e9189f2ceefb69aabf85044a802fbc9dafe732e5d55ac241a48fffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185446133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653275fe160f6d39ba2e2e50a32e816399492c82ae067ccce46c61ce8d170d45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:27 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:27 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:27 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:27 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:27 GMT
ARG KONG_VERSION=2.8.5
# Tue, 17 Feb 2026 20:27:27 GMT
ENV KONG_VERSION=2.8.5
# Tue, 17 Feb 2026 20:27:27 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 17 Feb 2026 20:27:27 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 17 Feb 2026 20:28:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:28:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:28:08 GMT
USER kong
# Tue, 17 Feb 2026 20:28:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:28:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:28:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:28:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:28:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cea0d63b25013eabd90428bbaba27478449851f8fe13de680cf7f35bee1677`  
		Last Modified: Tue, 17 Feb 2026 20:28:31 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7711e2716a72edc7bbf4d725033bc589cf83978350b8487f7475d5884be90a58`  
		Last Modified: Tue, 17 Feb 2026 20:28:34 GMT  
		Size: 130.8 MB (130825919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bf636a76b3edc4166cb428f96ffe259d34ab10916336422895abf607536dca`  
		Last Modified: Tue, 17 Feb 2026 20:28:30 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:5391bacb27c264fb6bc959e910d7d4067a1d49a4874ecfb6a86416d200517de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d5dec1cffd0060563ab6d443784671e1b6dc118fb570e11af557ee598127eb`

```dockerfile
```

-	Layers:
	-	`sha256:e7172e3b1a6d7a9dc7bea9bdd7e4685d69175bc048b96603b759b518e3b82356`  
		Last Modified: Tue, 17 Feb 2026 20:28:31 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697f43d1fcc76732555dc8da3ea4677f6ac7d60fe6190df5b468a2f97a8778d8`  
		Last Modified: Tue, 17 Feb 2026 20:28:30 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:a4b9d61bec6563758acec108f5f9cd5d70dd3c90d73e663b04c021847a9a5f44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:05f39a6524ada9de672457837d782139b12a323cc3714655fbfe26ee55b38960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120416812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f331b97f150aef35a5a7246352d04dabf1694c957380ed309f8a5ecad13c6a89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:44 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:44 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:27:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
USER kong
# Tue, 17 Feb 2026 20:27:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a09760e339f51685ad58d90c9fa039ecabfdfdb0d580da80c5c6802ed29ad`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3439955f3b3fa77448790033fe53fa33b0db8937f61d8b378f2f81d58027f`  
		Last Modified: Tue, 17 Feb 2026 20:27:27 GMT  
		Size: 90.7 MB (90687917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca4f682b27bd913c5921b3306b8601c519f1179a6701a0faff1c6a28401256`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:7f20d7a32163ce18251231ffb76431fe7a76ccb125eb494883c96f964af8ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e33ed7b3d97dc7a16fca550e3a99a92b19063ae6afa12408bac813047f7a3c`

```dockerfile
```

-	Layers:
	-	`sha256:dc6a5566b66dab90dd178fd3d4138b42a77a6403d56890c2382545f051c7af88`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 5.4 MB (5421142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a558597074af99e79d3886a9b95094e63c96941dc9b35f4334a9e88ff11b6e78`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b599c361c53fb2ff57ccd03afaa0fd5a5e3a0c717d719155dda57bf00edf91cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118870191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef7534ea867288cd3f038ca4d945bf051e0a3d9aa28fa5b25bee1910392d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:25:59 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:25:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:26:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
USER kong
# Tue, 17 Feb 2026 20:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee99ec660cb97b75d0d5ab7125b75553d0e2e843dbbab29c99509902623e266b`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9282049c3210691a34ed0130307d3233df5a90b7c10165b99a190a9b8292e2`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 90.0 MB (90003781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434a120f9dcc7db6edabd21ad55231f977ea265d723d113b420aa105b748fde8`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:92bbbdc98c77df23b62b092d8c4d58f9a1f9e814531aba6694478fe5b4903428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b489fc02e26b037e8c29d9e1b5a666667ad0c23204fb16a5cdc0a58ffb6f6c2`

```dockerfile
```

-	Layers:
	-	`sha256:e98cfdc0ba28ab9eabb6bf149e4fad6acd32723c7bef036a25182f59054a46c9`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 5.4 MB (5428309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934b8384220e0b0161eeca5ab48b20d619940bfd8583310d540a0b6530d94da5`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:0a19db9f1cd2066f493a0977450ab396edb45a6661666cef4ac97540f6410b79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:45cf74595ba7a593b23fdab37917b954fe59bb71f592ca89769b5d2d7902d4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92278201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae7c690026f875d3ccd362a679b65f65fc01549fdb20f14351810359a4ec713`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:18 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:27:18 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:18 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:18 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:18 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:27:18 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Feb 2026 20:27:44 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:44 GMT
USER kong
# Tue, 17 Feb 2026 20:27:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:44 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3107729f85ebbe6129da54593fd8e95ce305ed5ee787814618e02a25544223`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b08ed25e32ea01c5f170b8bb23b018296d50f366d668f62b81fd953911537a4`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 62.7 MB (62739554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ba7330b151e473135dd7c5f5c61a4b41aa360761957cd6922d7d0920e43d7`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:887b01c11cacda2c9fc63cbbadce8f3d7934cec9e5a71d2e5ae686639adbc0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7d044131261af3663ad25c2d1f4cabf06d8f92a01ebcb33fa7be0cefb919a`

```dockerfile
```

-	Layers:
	-	`sha256:c38413d81e475f5149fb28ec0f5c291e3203db2fa923cc4a97f05e09dba125ae`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2e1564b841460cae178161c9610b996441148b0da996faf709074edfc58d70`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 15.3 KB (15345 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:21cc63b8e7da1c3d0942dff16bdca2e292706ef88d91acae6c49445e077cbc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88577889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94a8ae66441b7d447c00921e3801ce9eefa88c56a6caf6ac7d6a6e68e426f38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:04 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:04 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:04 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:04 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:26:04 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Feb 2026 20:26:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:29 GMT
USER kong
# Tue, 17 Feb 2026 20:26:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:29 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68e69830048d61d9b6bc4a1d52d30ea75016ffe954dc7acfd086c1021a22dad`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445c3ecf802eea76f883c5a74b04af8f3adfa3d116b08d5f3392cdf8ed42e8f`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 61.2 MB (61191665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4be0bbdb1e5f747b026137c7677055ff3093884d4549083606a2789c16f807`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:db44546f8989a5e543cc170f50e425c1639dff153fdb79b7d56349a2a16e8734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e48eaf5154cb4eebb92693933ad965410ce447fd6a783262013b90b49779262`

```dockerfile
```

-	Layers:
	-	`sha256:c272c7f5ea5f5469a2de71dcfeed64c2eb832c1656e6944651c2f41020fefb66`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314ac6662007ffcd277db87424553daa5866e12e8d4769ce27c4d7311fccd9a4`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:0a19db9f1cd2066f493a0977450ab396edb45a6661666cef4ac97540f6410b79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:45cf74595ba7a593b23fdab37917b954fe59bb71f592ca89769b5d2d7902d4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92278201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae7c690026f875d3ccd362a679b65f65fc01549fdb20f14351810359a4ec713`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:18 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:27:18 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:18 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:18 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:18 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:27:18 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Feb 2026 20:27:44 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:44 GMT
USER kong
# Tue, 17 Feb 2026 20:27:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:44 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3107729f85ebbe6129da54593fd8e95ce305ed5ee787814618e02a25544223`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b08ed25e32ea01c5f170b8bb23b018296d50f366d668f62b81fd953911537a4`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 62.7 MB (62739554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ba7330b151e473135dd7c5f5c61a4b41aa360761957cd6922d7d0920e43d7`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:887b01c11cacda2c9fc63cbbadce8f3d7934cec9e5a71d2e5ae686639adbc0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7d044131261af3663ad25c2d1f4cabf06d8f92a01ebcb33fa7be0cefb919a`

```dockerfile
```

-	Layers:
	-	`sha256:c38413d81e475f5149fb28ec0f5c291e3203db2fa923cc4a97f05e09dba125ae`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2e1564b841460cae178161c9610b996441148b0da996faf709074edfc58d70`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 15.3 KB (15345 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:21cc63b8e7da1c3d0942dff16bdca2e292706ef88d91acae6c49445e077cbc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88577889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94a8ae66441b7d447c00921e3801ce9eefa88c56a6caf6ac7d6a6e68e426f38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:04 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:04 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:04 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:04 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:26:04 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Feb 2026 20:26:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:29 GMT
USER kong
# Tue, 17 Feb 2026 20:26:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:29 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68e69830048d61d9b6bc4a1d52d30ea75016ffe954dc7acfd086c1021a22dad`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445c3ecf802eea76f883c5a74b04af8f3adfa3d116b08d5f3392cdf8ed42e8f`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 61.2 MB (61191665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4be0bbdb1e5f747b026137c7677055ff3093884d4549083606a2789c16f807`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:db44546f8989a5e543cc170f50e425c1639dff153fdb79b7d56349a2a16e8734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e48eaf5154cb4eebb92693933ad965410ce447fd6a783262013b90b49779262`

```dockerfile
```

-	Layers:
	-	`sha256:c272c7f5ea5f5469a2de71dcfeed64c2eb832c1656e6944651c2f41020fefb66`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314ac6662007ffcd277db87424553daa5866e12e8d4769ce27c4d7311fccd9a4`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:0a19db9f1cd2066f493a0977450ab396edb45a6661666cef4ac97540f6410b79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:45cf74595ba7a593b23fdab37917b954fe59bb71f592ca89769b5d2d7902d4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92278201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae7c690026f875d3ccd362a679b65f65fc01549fdb20f14351810359a4ec713`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:18 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:27:18 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:18 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:18 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:18 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:27:18 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Feb 2026 20:27:44 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:44 GMT
USER kong
# Tue, 17 Feb 2026 20:27:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:44 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3107729f85ebbe6129da54593fd8e95ce305ed5ee787814618e02a25544223`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b08ed25e32ea01c5f170b8bb23b018296d50f366d668f62b81fd953911537a4`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 62.7 MB (62739554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ba7330b151e473135dd7c5f5c61a4b41aa360761957cd6922d7d0920e43d7`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:887b01c11cacda2c9fc63cbbadce8f3d7934cec9e5a71d2e5ae686639adbc0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7d044131261af3663ad25c2d1f4cabf06d8f92a01ebcb33fa7be0cefb919a`

```dockerfile
```

-	Layers:
	-	`sha256:c38413d81e475f5149fb28ec0f5c291e3203db2fa923cc4a97f05e09dba125ae`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2e1564b841460cae178161c9610b996441148b0da996faf709074edfc58d70`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 15.3 KB (15345 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:21cc63b8e7da1c3d0942dff16bdca2e292706ef88d91acae6c49445e077cbc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88577889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94a8ae66441b7d447c00921e3801ce9eefa88c56a6caf6ac7d6a6e68e426f38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:04 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:04 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:04 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:04 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:26:04 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Feb 2026 20:26:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:29 GMT
USER kong
# Tue, 17 Feb 2026 20:26:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:29 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68e69830048d61d9b6bc4a1d52d30ea75016ffe954dc7acfd086c1021a22dad`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445c3ecf802eea76f883c5a74b04af8f3adfa3d116b08d5f3392cdf8ed42e8f`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 61.2 MB (61191665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4be0bbdb1e5f747b026137c7677055ff3093884d4549083606a2789c16f807`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:db44546f8989a5e543cc170f50e425c1639dff153fdb79b7d56349a2a16e8734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e48eaf5154cb4eebb92693933ad965410ce447fd6a783262013b90b49779262`

```dockerfile
```

-	Layers:
	-	`sha256:c272c7f5ea5f5469a2de71dcfeed64c2eb832c1656e6944651c2f41020fefb66`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314ac6662007ffcd277db87424553daa5866e12e8d4769ce27c4d7311fccd9a4`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:0a19db9f1cd2066f493a0977450ab396edb45a6661666cef4ac97540f6410b79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:45cf74595ba7a593b23fdab37917b954fe59bb71f592ca89769b5d2d7902d4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92278201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae7c690026f875d3ccd362a679b65f65fc01549fdb20f14351810359a4ec713`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:18 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:27:18 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:18 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:18 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:18 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:27:18 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Feb 2026 20:27:18 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Feb 2026 20:27:44 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:44 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:44 GMT
USER kong
# Tue, 17 Feb 2026 20:27:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:44 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3107729f85ebbe6129da54593fd8e95ce305ed5ee787814618e02a25544223`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b08ed25e32ea01c5f170b8bb23b018296d50f366d668f62b81fd953911537a4`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 62.7 MB (62739554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163ba7330b151e473135dd7c5f5c61a4b41aa360761957cd6922d7d0920e43d7`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:887b01c11cacda2c9fc63cbbadce8f3d7934cec9e5a71d2e5ae686639adbc0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7d044131261af3663ad25c2d1f4cabf06d8f92a01ebcb33fa7be0cefb919a`

```dockerfile
```

-	Layers:
	-	`sha256:c38413d81e475f5149fb28ec0f5c291e3203db2fa923cc4a97f05e09dba125ae`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2e1564b841460cae178161c9610b996441148b0da996faf709074edfc58d70`  
		Last Modified: Tue, 17 Feb 2026 20:27:58 GMT  
		Size: 15.3 KB (15345 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:21cc63b8e7da1c3d0942dff16bdca2e292706ef88d91acae6c49445e077cbc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88577889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94a8ae66441b7d447c00921e3801ce9eefa88c56a6caf6ac7d6a6e68e426f38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:04 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:04 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:04 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:04 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:04 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:26:04 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Feb 2026 20:26:04 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Feb 2026 20:26:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:29 GMT
USER kong
# Tue, 17 Feb 2026 20:26:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:29 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68e69830048d61d9b6bc4a1d52d30ea75016ffe954dc7acfd086c1021a22dad`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445c3ecf802eea76f883c5a74b04af8f3adfa3d116b08d5f3392cdf8ed42e8f`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 61.2 MB (61191665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4be0bbdb1e5f747b026137c7677055ff3093884d4549083606a2789c16f807`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:db44546f8989a5e543cc170f50e425c1639dff153fdb79b7d56349a2a16e8734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e48eaf5154cb4eebb92693933ad965410ce447fd6a783262013b90b49779262`

```dockerfile
```

-	Layers:
	-	`sha256:c272c7f5ea5f5469a2de71dcfeed64c2eb832c1656e6944651c2f41020fefb66`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:314ac6662007ffcd277db87424553daa5866e12e8d4769ce27c4d7311fccd9a4`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:8eee9bb8caf2dd57612d3eea37fdf0fb11a48cde55cd653107a5466267785aaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:79409605b68247f3295d3caebcf714a5bd20fe098bb22bd7abfec398c3b9b36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117549698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864355335afecd72fd7510621de590d9def276b149acbec08e63569e725b930c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:15 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:27:15 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:15 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:15 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:15 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:27:15 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Feb 2026 20:27:43 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:43 GMT
USER kong
# Tue, 17 Feb 2026 20:27:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:43 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:43 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af45cbb62c3c6bcff4a806a424542132fa12269ab7f92bf7e25f48d7b64abac`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e73352fccabd33b4f6e59e94c7ada1147072d3e899f9fe46c93b190e5780087`  
		Last Modified: Tue, 17 Feb 2026 20:28:03 GMT  
		Size: 88.0 MB (88011049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b6dc2550f8d275d1b8a2972d99eb7864e1484626d1705284e7a43110b14f18`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:a24bb9b53295e1f8931cd3878a74eaa4649000f82c62b43ec32c3ec784ffed0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8769ae7ac5dcb9743fbdafb0e203fa4880e4bff80edfc4cda391740b9cbdaa`

```dockerfile
```

-	Layers:
	-	`sha256:639fd74429e9187d057bed665cf1779a7b3652b24426242c497ddb45b29aaa9b`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be79e71e22990f85135cd8e5d6a99590d1175a7791655e3c74369b1172e44046`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:969b45dfc7b131986778d2b8652115839096d9ad5a5d4d250195d617ccd238b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8088cd01488abd4a3f17d881a56d67d888e966f7fdb76c26f8b535db49fd7d2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:05 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:05 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:05 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:05 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:05 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Feb 2026 20:26:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:33 GMT
USER kong
# Tue, 17 Feb 2026 20:26:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cf886d8a9811672edc5df676258379ed76526e78d6fa62a30e7f5a14685f9a`  
		Last Modified: Tue, 17 Feb 2026 20:26:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21de19eac50bf166665423e2a2951b89b8ae81452f8796b8736eb5832e1bac`  
		Last Modified: Tue, 17 Feb 2026 20:26:52 GMT  
		Size: 87.3 MB (87289649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4be0bbdb1e5f747b026137c7677055ff3093884d4549083606a2789c16f807`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:579d0d9d92bda0273b8c568691e6f3f96c077c7048a233a93fe3bad6393bd55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9951e6920d7b862455bb5763f74674963408ba20921f6cc4d25f0dfffa891628`

```dockerfile
```

-	Layers:
	-	`sha256:3dab3b9e8a828ae66ea1e2bab4c56cbfa3f6a16ea3b32ae3bc9a8f341e202cec`  
		Last Modified: Tue, 17 Feb 2026 20:26:51 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702a74df9c1bc6802f98f10f33b9f636fb030dbfd896f38acb64b3304cad5de5`  
		Last Modified: Tue, 17 Feb 2026 20:26:50 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:8eee9bb8caf2dd57612d3eea37fdf0fb11a48cde55cd653107a5466267785aaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:79409605b68247f3295d3caebcf714a5bd20fe098bb22bd7abfec398c3b9b36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117549698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864355335afecd72fd7510621de590d9def276b149acbec08e63569e725b930c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:15 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:27:15 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:15 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:15 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:15 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:27:15 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Feb 2026 20:27:43 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:43 GMT
USER kong
# Tue, 17 Feb 2026 20:27:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:43 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:43 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af45cbb62c3c6bcff4a806a424542132fa12269ab7f92bf7e25f48d7b64abac`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e73352fccabd33b4f6e59e94c7ada1147072d3e899f9fe46c93b190e5780087`  
		Last Modified: Tue, 17 Feb 2026 20:28:03 GMT  
		Size: 88.0 MB (88011049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b6dc2550f8d275d1b8a2972d99eb7864e1484626d1705284e7a43110b14f18`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:a24bb9b53295e1f8931cd3878a74eaa4649000f82c62b43ec32c3ec784ffed0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8769ae7ac5dcb9743fbdafb0e203fa4880e4bff80edfc4cda391740b9cbdaa`

```dockerfile
```

-	Layers:
	-	`sha256:639fd74429e9187d057bed665cf1779a7b3652b24426242c497ddb45b29aaa9b`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be79e71e22990f85135cd8e5d6a99590d1175a7791655e3c74369b1172e44046`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:969b45dfc7b131986778d2b8652115839096d9ad5a5d4d250195d617ccd238b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8088cd01488abd4a3f17d881a56d67d888e966f7fdb76c26f8b535db49fd7d2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:05 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:05 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:05 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:05 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:05 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Feb 2026 20:26:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:33 GMT
USER kong
# Tue, 17 Feb 2026 20:26:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cf886d8a9811672edc5df676258379ed76526e78d6fa62a30e7f5a14685f9a`  
		Last Modified: Tue, 17 Feb 2026 20:26:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21de19eac50bf166665423e2a2951b89b8ae81452f8796b8736eb5832e1bac`  
		Last Modified: Tue, 17 Feb 2026 20:26:52 GMT  
		Size: 87.3 MB (87289649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4be0bbdb1e5f747b026137c7677055ff3093884d4549083606a2789c16f807`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:579d0d9d92bda0273b8c568691e6f3f96c077c7048a233a93fe3bad6393bd55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9951e6920d7b862455bb5763f74674963408ba20921f6cc4d25f0dfffa891628`

```dockerfile
```

-	Layers:
	-	`sha256:3dab3b9e8a828ae66ea1e2bab4c56cbfa3f6a16ea3b32ae3bc9a8f341e202cec`  
		Last Modified: Tue, 17 Feb 2026 20:26:51 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702a74df9c1bc6802f98f10f33b9f636fb030dbfd896f38acb64b3304cad5de5`  
		Last Modified: Tue, 17 Feb 2026 20:26:50 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:8eee9bb8caf2dd57612d3eea37fdf0fb11a48cde55cd653107a5466267785aaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:79409605b68247f3295d3caebcf714a5bd20fe098bb22bd7abfec398c3b9b36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117549698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864355335afecd72fd7510621de590d9def276b149acbec08e63569e725b930c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:15 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:27:15 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:15 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:15 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:15 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:27:15 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Feb 2026 20:27:43 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:43 GMT
USER kong
# Tue, 17 Feb 2026 20:27:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:43 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:43 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af45cbb62c3c6bcff4a806a424542132fa12269ab7f92bf7e25f48d7b64abac`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e73352fccabd33b4f6e59e94c7ada1147072d3e899f9fe46c93b190e5780087`  
		Last Modified: Tue, 17 Feb 2026 20:28:03 GMT  
		Size: 88.0 MB (88011049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b6dc2550f8d275d1b8a2972d99eb7864e1484626d1705284e7a43110b14f18`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:a24bb9b53295e1f8931cd3878a74eaa4649000f82c62b43ec32c3ec784ffed0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8769ae7ac5dcb9743fbdafb0e203fa4880e4bff80edfc4cda391740b9cbdaa`

```dockerfile
```

-	Layers:
	-	`sha256:639fd74429e9187d057bed665cf1779a7b3652b24426242c497ddb45b29aaa9b`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be79e71e22990f85135cd8e5d6a99590d1175a7791655e3c74369b1172e44046`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:969b45dfc7b131986778d2b8652115839096d9ad5a5d4d250195d617ccd238b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8088cd01488abd4a3f17d881a56d67d888e966f7fdb76c26f8b535db49fd7d2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:05 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:05 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:05 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:05 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:05 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Feb 2026 20:26:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:33 GMT
USER kong
# Tue, 17 Feb 2026 20:26:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cf886d8a9811672edc5df676258379ed76526e78d6fa62a30e7f5a14685f9a`  
		Last Modified: Tue, 17 Feb 2026 20:26:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21de19eac50bf166665423e2a2951b89b8ae81452f8796b8736eb5832e1bac`  
		Last Modified: Tue, 17 Feb 2026 20:26:52 GMT  
		Size: 87.3 MB (87289649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4be0bbdb1e5f747b026137c7677055ff3093884d4549083606a2789c16f807`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:579d0d9d92bda0273b8c568691e6f3f96c077c7048a233a93fe3bad6393bd55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9951e6920d7b862455bb5763f74674963408ba20921f6cc4d25f0dfffa891628`

```dockerfile
```

-	Layers:
	-	`sha256:3dab3b9e8a828ae66ea1e2bab4c56cbfa3f6a16ea3b32ae3bc9a8f341e202cec`  
		Last Modified: Tue, 17 Feb 2026 20:26:51 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702a74df9c1bc6802f98f10f33b9f636fb030dbfd896f38acb64b3304cad5de5`  
		Last Modified: Tue, 17 Feb 2026 20:26:50 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:8eee9bb8caf2dd57612d3eea37fdf0fb11a48cde55cd653107a5466267785aaa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:79409605b68247f3295d3caebcf714a5bd20fe098bb22bd7abfec398c3b9b36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117549698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864355335afecd72fd7510621de590d9def276b149acbec08e63569e725b930c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:27:15 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:27:15 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:27:15 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:27:15 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:27:15 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:27:15 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Feb 2026 20:27:15 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Feb 2026 20:27:43 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:43 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:43 GMT
USER kong
# Tue, 17 Feb 2026 20:27:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:43 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:43 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:43 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af45cbb62c3c6bcff4a806a424542132fa12269ab7f92bf7e25f48d7b64abac`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e73352fccabd33b4f6e59e94c7ada1147072d3e899f9fe46c93b190e5780087`  
		Last Modified: Tue, 17 Feb 2026 20:28:03 GMT  
		Size: 88.0 MB (88011049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b6dc2550f8d275d1b8a2972d99eb7864e1484626d1705284e7a43110b14f18`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:a24bb9b53295e1f8931cd3878a74eaa4649000f82c62b43ec32c3ec784ffed0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8769ae7ac5dcb9743fbdafb0e203fa4880e4bff80edfc4cda391740b9cbdaa`

```dockerfile
```

-	Layers:
	-	`sha256:639fd74429e9187d057bed665cf1779a7b3652b24426242c497ddb45b29aaa9b`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be79e71e22990f85135cd8e5d6a99590d1175a7791655e3c74369b1172e44046`  
		Last Modified: Tue, 17 Feb 2026 20:28:00 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:969b45dfc7b131986778d2b8652115839096d9ad5a5d4d250195d617ccd238b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114675877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8088cd01488abd4a3f17d881a56d67d888e966f7fdb76c26f8b535db49fd7d2c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:05 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:05 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:05 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:05 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:05 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:05 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Feb 2026 20:26:05 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Feb 2026 20:26:33 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:33 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:33 GMT
USER kong
# Tue, 17 Feb 2026 20:26:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:33 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:33 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cf886d8a9811672edc5df676258379ed76526e78d6fa62a30e7f5a14685f9a`  
		Last Modified: Tue, 17 Feb 2026 20:26:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d21de19eac50bf166665423e2a2951b89b8ae81452f8796b8736eb5832e1bac`  
		Last Modified: Tue, 17 Feb 2026 20:26:52 GMT  
		Size: 87.3 MB (87289649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4be0bbdb1e5f747b026137c7677055ff3093884d4549083606a2789c16f807`  
		Last Modified: Tue, 17 Feb 2026 20:26:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:579d0d9d92bda0273b8c568691e6f3f96c077c7048a233a93fe3bad6393bd55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9951e6920d7b862455bb5763f74674963408ba20921f6cc4d25f0dfffa891628`

```dockerfile
```

-	Layers:
	-	`sha256:3dab3b9e8a828ae66ea1e2bab4c56cbfa3f6a16ea3b32ae3bc9a8f341e202cec`  
		Last Modified: Tue, 17 Feb 2026 20:26:51 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702a74df9c1bc6802f98f10f33b9f636fb030dbfd896f38acb64b3304cad5de5`  
		Last Modified: Tue, 17 Feb 2026 20:26:50 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:a4b9d61bec6563758acec108f5f9cd5d70dd3c90d73e663b04c021847a9a5f44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:05f39a6524ada9de672457837d782139b12a323cc3714655fbfe26ee55b38960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120416812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f331b97f150aef35a5a7246352d04dabf1694c957380ed309f8a5ecad13c6a89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:44 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:44 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:27:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
USER kong
# Tue, 17 Feb 2026 20:27:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a09760e339f51685ad58d90c9fa039ecabfdfdb0d580da80c5c6802ed29ad`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3439955f3b3fa77448790033fe53fa33b0db8937f61d8b378f2f81d58027f`  
		Last Modified: Tue, 17 Feb 2026 20:27:27 GMT  
		Size: 90.7 MB (90687917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca4f682b27bd913c5921b3306b8601c519f1179a6701a0faff1c6a28401256`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:7f20d7a32163ce18251231ffb76431fe7a76ccb125eb494883c96f964af8ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e33ed7b3d97dc7a16fca550e3a99a92b19063ae6afa12408bac813047f7a3c`

```dockerfile
```

-	Layers:
	-	`sha256:dc6a5566b66dab90dd178fd3d4138b42a77a6403d56890c2382545f051c7af88`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 5.4 MB (5421142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a558597074af99e79d3886a9b95094e63c96941dc9b35f4334a9e88ff11b6e78`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b599c361c53fb2ff57ccd03afaa0fd5a5e3a0c717d719155dda57bf00edf91cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118870191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef7534ea867288cd3f038ca4d945bf051e0a3d9aa28fa5b25bee1910392d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:25:59 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:25:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:26:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
USER kong
# Tue, 17 Feb 2026 20:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee99ec660cb97b75d0d5ab7125b75553d0e2e843dbbab29c99509902623e266b`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9282049c3210691a34ed0130307d3233df5a90b7c10165b99a190a9b8292e2`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 90.0 MB (90003781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434a120f9dcc7db6edabd21ad55231f977ea265d723d113b420aa105b748fde8`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:92bbbdc98c77df23b62b092d8c4d58f9a1f9e814531aba6694478fe5b4903428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b489fc02e26b037e8c29d9e1b5a666667ad0c23204fb16a5cdc0a58ffb6f6c2`

```dockerfile
```

-	Layers:
	-	`sha256:e98cfdc0ba28ab9eabb6bf149e4fad6acd32723c7bef036a25182f59054a46c9`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 5.4 MB (5428309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934b8384220e0b0161eeca5ab48b20d619940bfd8583310d540a0b6530d94da5`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:a4b9d61bec6563758acec108f5f9cd5d70dd3c90d73e663b04c021847a9a5f44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:05f39a6524ada9de672457837d782139b12a323cc3714655fbfe26ee55b38960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120416812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f331b97f150aef35a5a7246352d04dabf1694c957380ed309f8a5ecad13c6a89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:44 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:44 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:27:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
USER kong
# Tue, 17 Feb 2026 20:27:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a09760e339f51685ad58d90c9fa039ecabfdfdb0d580da80c5c6802ed29ad`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3439955f3b3fa77448790033fe53fa33b0db8937f61d8b378f2f81d58027f`  
		Last Modified: Tue, 17 Feb 2026 20:27:27 GMT  
		Size: 90.7 MB (90687917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca4f682b27bd913c5921b3306b8601c519f1179a6701a0faff1c6a28401256`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:7f20d7a32163ce18251231ffb76431fe7a76ccb125eb494883c96f964af8ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e33ed7b3d97dc7a16fca550e3a99a92b19063ae6afa12408bac813047f7a3c`

```dockerfile
```

-	Layers:
	-	`sha256:dc6a5566b66dab90dd178fd3d4138b42a77a6403d56890c2382545f051c7af88`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 5.4 MB (5421142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a558597074af99e79d3886a9b95094e63c96941dc9b35f4334a9e88ff11b6e78`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b599c361c53fb2ff57ccd03afaa0fd5a5e3a0c717d719155dda57bf00edf91cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118870191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef7534ea867288cd3f038ca4d945bf051e0a3d9aa28fa5b25bee1910392d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:25:59 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:25:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:26:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
USER kong
# Tue, 17 Feb 2026 20:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee99ec660cb97b75d0d5ab7125b75553d0e2e843dbbab29c99509902623e266b`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9282049c3210691a34ed0130307d3233df5a90b7c10165b99a190a9b8292e2`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 90.0 MB (90003781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434a120f9dcc7db6edabd21ad55231f977ea265d723d113b420aa105b748fde8`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:92bbbdc98c77df23b62b092d8c4d58f9a1f9e814531aba6694478fe5b4903428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b489fc02e26b037e8c29d9e1b5a666667ad0c23204fb16a5cdc0a58ffb6f6c2`

```dockerfile
```

-	Layers:
	-	`sha256:e98cfdc0ba28ab9eabb6bf149e4fad6acd32723c7bef036a25182f59054a46c9`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 5.4 MB (5428309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934b8384220e0b0161eeca5ab48b20d619940bfd8583310d540a0b6530d94da5`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:a4b9d61bec6563758acec108f5f9cd5d70dd3c90d73e663b04c021847a9a5f44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:05f39a6524ada9de672457837d782139b12a323cc3714655fbfe26ee55b38960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120416812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f331b97f150aef35a5a7246352d04dabf1694c957380ed309f8a5ecad13c6a89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:44 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:44 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:27:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
USER kong
# Tue, 17 Feb 2026 20:27:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a09760e339f51685ad58d90c9fa039ecabfdfdb0d580da80c5c6802ed29ad`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3439955f3b3fa77448790033fe53fa33b0db8937f61d8b378f2f81d58027f`  
		Last Modified: Tue, 17 Feb 2026 20:27:27 GMT  
		Size: 90.7 MB (90687917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca4f682b27bd913c5921b3306b8601c519f1179a6701a0faff1c6a28401256`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:7f20d7a32163ce18251231ffb76431fe7a76ccb125eb494883c96f964af8ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e33ed7b3d97dc7a16fca550e3a99a92b19063ae6afa12408bac813047f7a3c`

```dockerfile
```

-	Layers:
	-	`sha256:dc6a5566b66dab90dd178fd3d4138b42a77a6403d56890c2382545f051c7af88`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 5.4 MB (5421142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a558597074af99e79d3886a9b95094e63c96941dc9b35f4334a9e88ff11b6e78`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b599c361c53fb2ff57ccd03afaa0fd5a5e3a0c717d719155dda57bf00edf91cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118870191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef7534ea867288cd3f038ca4d945bf051e0a3d9aa28fa5b25bee1910392d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:25:59 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:25:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:26:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
USER kong
# Tue, 17 Feb 2026 20:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee99ec660cb97b75d0d5ab7125b75553d0e2e843dbbab29c99509902623e266b`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9282049c3210691a34ed0130307d3233df5a90b7c10165b99a190a9b8292e2`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 90.0 MB (90003781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434a120f9dcc7db6edabd21ad55231f977ea265d723d113b420aa105b748fde8`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:92bbbdc98c77df23b62b092d8c4d58f9a1f9e814531aba6694478fe5b4903428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b489fc02e26b037e8c29d9e1b5a666667ad0c23204fb16a5cdc0a58ffb6f6c2`

```dockerfile
```

-	Layers:
	-	`sha256:e98cfdc0ba28ab9eabb6bf149e4fad6acd32723c7bef036a25182f59054a46c9`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 5.4 MB (5428309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934b8384220e0b0161eeca5ab48b20d619940bfd8583310d540a0b6530d94da5`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:a4b9d61bec6563758acec108f5f9cd5d70dd3c90d73e663b04c021847a9a5f44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:05f39a6524ada9de672457837d782139b12a323cc3714655fbfe26ee55b38960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120416812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f331b97f150aef35a5a7246352d04dabf1694c957380ed309f8a5ecad13c6a89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:44 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:44 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:27:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
USER kong
# Tue, 17 Feb 2026 20:27:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a09760e339f51685ad58d90c9fa039ecabfdfdb0d580da80c5c6802ed29ad`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3439955f3b3fa77448790033fe53fa33b0db8937f61d8b378f2f81d58027f`  
		Last Modified: Tue, 17 Feb 2026 20:27:27 GMT  
		Size: 90.7 MB (90687917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca4f682b27bd913c5921b3306b8601c519f1179a6701a0faff1c6a28401256`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:7f20d7a32163ce18251231ffb76431fe7a76ccb125eb494883c96f964af8ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e33ed7b3d97dc7a16fca550e3a99a92b19063ae6afa12408bac813047f7a3c`

```dockerfile
```

-	Layers:
	-	`sha256:dc6a5566b66dab90dd178fd3d4138b42a77a6403d56890c2382545f051c7af88`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 5.4 MB (5421142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a558597074af99e79d3886a9b95094e63c96941dc9b35f4334a9e88ff11b6e78`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b599c361c53fb2ff57ccd03afaa0fd5a5e3a0c717d719155dda57bf00edf91cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118870191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef7534ea867288cd3f038ca4d945bf051e0a3d9aa28fa5b25bee1910392d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:25:59 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:25:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:26:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
USER kong
# Tue, 17 Feb 2026 20:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee99ec660cb97b75d0d5ab7125b75553d0e2e843dbbab29c99509902623e266b`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9282049c3210691a34ed0130307d3233df5a90b7c10165b99a190a9b8292e2`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 90.0 MB (90003781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434a120f9dcc7db6edabd21ad55231f977ea265d723d113b420aa105b748fde8`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:92bbbdc98c77df23b62b092d8c4d58f9a1f9e814531aba6694478fe5b4903428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b489fc02e26b037e8c29d9e1b5a666667ad0c23204fb16a5cdc0a58ffb6f6c2`

```dockerfile
```

-	Layers:
	-	`sha256:e98cfdc0ba28ab9eabb6bf149e4fad6acd32723c7bef036a25182f59054a46c9`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 5.4 MB (5428309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934b8384220e0b0161eeca5ab48b20d619940bfd8583310d540a0b6530d94da5`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:a4b9d61bec6563758acec108f5f9cd5d70dd3c90d73e663b04c021847a9a5f44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:05f39a6524ada9de672457837d782139b12a323cc3714655fbfe26ee55b38960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120416812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f331b97f150aef35a5a7246352d04dabf1694c957380ed309f8a5ecad13c6a89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:44 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:44 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:27:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
USER kong
# Tue, 17 Feb 2026 20:27:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a09760e339f51685ad58d90c9fa039ecabfdfdb0d580da80c5c6802ed29ad`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3439955f3b3fa77448790033fe53fa33b0db8937f61d8b378f2f81d58027f`  
		Last Modified: Tue, 17 Feb 2026 20:27:27 GMT  
		Size: 90.7 MB (90687917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca4f682b27bd913c5921b3306b8601c519f1179a6701a0faff1c6a28401256`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:7f20d7a32163ce18251231ffb76431fe7a76ccb125eb494883c96f964af8ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e33ed7b3d97dc7a16fca550e3a99a92b19063ae6afa12408bac813047f7a3c`

```dockerfile
```

-	Layers:
	-	`sha256:dc6a5566b66dab90dd178fd3d4138b42a77a6403d56890c2382545f051c7af88`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 5.4 MB (5421142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a558597074af99e79d3886a9b95094e63c96941dc9b35f4334a9e88ff11b6e78`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b599c361c53fb2ff57ccd03afaa0fd5a5e3a0c717d719155dda57bf00edf91cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118870191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef7534ea867288cd3f038ca4d945bf051e0a3d9aa28fa5b25bee1910392d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:25:59 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:25:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:26:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
USER kong
# Tue, 17 Feb 2026 20:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee99ec660cb97b75d0d5ab7125b75553d0e2e843dbbab29c99509902623e266b`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9282049c3210691a34ed0130307d3233df5a90b7c10165b99a190a9b8292e2`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 90.0 MB (90003781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434a120f9dcc7db6edabd21ad55231f977ea265d723d113b420aa105b748fde8`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:92bbbdc98c77df23b62b092d8c4d58f9a1f9e814531aba6694478fe5b4903428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b489fc02e26b037e8c29d9e1b5a666667ad0c23204fb16a5cdc0a58ffb6f6c2`

```dockerfile
```

-	Layers:
	-	`sha256:e98cfdc0ba28ab9eabb6bf149e4fad6acd32723c7bef036a25182f59054a46c9`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 5.4 MB (5428309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934b8384220e0b0161eeca5ab48b20d619940bfd8583310d540a0b6530d94da5`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:a4b9d61bec6563758acec108f5f9cd5d70dd3c90d73e663b04c021847a9a5f44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:05f39a6524ada9de672457837d782139b12a323cc3714655fbfe26ee55b38960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120416812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f331b97f150aef35a5a7246352d04dabf1694c957380ed309f8a5ecad13c6a89`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:26:44 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:26:44 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:26:44 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:26:44 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:26:44 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:27:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:27:09 GMT
USER kong
# Tue, 17 Feb 2026 20:27:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:27:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:27:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:27:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:27:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959a09760e339f51685ad58d90c9fa039ecabfdfdb0d580da80c5c6802ed29ad`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3439955f3b3fa77448790033fe53fa33b0db8937f61d8b378f2f81d58027f`  
		Last Modified: Tue, 17 Feb 2026 20:27:27 GMT  
		Size: 90.7 MB (90687917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca4f682b27bd913c5921b3306b8601c519f1179a6701a0faff1c6a28401256`  
		Last Modified: Tue, 17 Feb 2026 20:27:24 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:7f20d7a32163ce18251231ffb76431fe7a76ccb125eb494883c96f964af8ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e33ed7b3d97dc7a16fca550e3a99a92b19063ae6afa12408bac813047f7a3c`

```dockerfile
```

-	Layers:
	-	`sha256:dc6a5566b66dab90dd178fd3d4138b42a77a6403d56890c2382545f051c7af88`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 5.4 MB (5421142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a558597074af99e79d3886a9b95094e63c96941dc9b35f4334a9e88ff11b6e78`  
		Last Modified: Tue, 17 Feb 2026 20:27:25 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b599c361c53fb2ff57ccd03afaa0fd5a5e3a0c717d719155dda57bf00edf91cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118870191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742ef7534ea867288cd3f038ca4d945bf051e0a3d9aa28fa5b25bee1910392d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:25:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Feb 2026 20:25:59 GMT
ARG ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ENV ASSET=ce
# Tue, 17 Feb 2026 20:25:59 GMT
ARG EE_PORTS
# Tue, 17 Feb 2026 20:25:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Feb 2026 20:25:59 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Feb 2026 20:26:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:26:25 GMT
USER kong
# Tue, 17 Feb 2026 20:26:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Feb 2026 20:26:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Feb 2026 20:26:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Feb 2026 20:26:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Feb 2026 20:26:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee99ec660cb97b75d0d5ab7125b75553d0e2e843dbbab29c99509902623e266b`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9282049c3210691a34ed0130307d3233df5a90b7c10165b99a190a9b8292e2`  
		Last Modified: Tue, 17 Feb 2026 20:26:45 GMT  
		Size: 90.0 MB (90003781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434a120f9dcc7db6edabd21ad55231f977ea265d723d113b420aa105b748fde8`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:92bbbdc98c77df23b62b092d8c4d58f9a1f9e814531aba6694478fe5b4903428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b489fc02e26b037e8c29d9e1b5a666667ad0c23204fb16a5cdc0a58ffb6f6c2`

```dockerfile
```

-	Layers:
	-	`sha256:e98cfdc0ba28ab9eabb6bf149e4fad6acd32723c7bef036a25182f59054a46c9`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 5.4 MB (5428309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934b8384220e0b0161eeca5ab48b20d619940bfd8583310d540a0b6530d94da5`  
		Last Modified: Tue, 17 Feb 2026 20:26:43 GMT  
		Size: 16.4 KB (16357 bytes)  
		MIME: application/vnd.in-toto+json
