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
$ docker pull kong@sha256:f3e1520cdddb6b9d5ab43fcc34bbeb43c0d6c22d8ea94455c11147dfde8fa7e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c9fd38babe3f1be76a8163c4d6bbf194feb8a45fff6e32ded35709eacfe2e90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185230220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd2703b92e9834a9be1e0da90e8898f84184eca798290fe1a4831c646b06d49`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:37 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:37 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:37 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:37 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:37 GMT
ARG KONG_VERSION=2.8.5
# Thu, 13 Nov 2025 23:28:37 GMT
ENV KONG_VERSION=2.8.5
# Thu, 13 Nov 2025 23:28:37 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Thu, 13 Nov 2025 23:28:37 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 13 Nov 2025 23:29:12 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:29:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:29:12 GMT
USER kong
# Thu, 13 Nov 2025 23:29:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:12 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:29:12 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:29:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:29:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5ffc6da68547f0c8858f58595d1d87cfbba7eaa59c699faaadbf9e486000e6`  
		Last Modified: Thu, 13 Nov 2025 23:29:43 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428613c4fd7abb4316edf11b7df45b21f7c8278678667a8b00dd5770ce620332`  
		Last Modified: Fri, 14 Nov 2025 02:07:55 GMT  
		Size: 130.6 MB (130610573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aac4f5cbb31821ac1aee107bfa5c9df03f300e23cf859fb80c8c64e3679fe59`  
		Last Modified: Thu, 13 Nov 2025 23:29:41 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:7a917d51b6276486449efc269255eb887d55a91dd621de18ae29fd4d2158c525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4527c9e5da85a3c126ce5aae588314cee20c1b2a75bba8c8796e825b5ced1ff2`

```dockerfile
```

-	Layers:
	-	`sha256:c98cfe5ecbe8bb6ee37540d5c27d1d2efcaf495d4b60497512f79b94a839ba41`  
		Last Modified: Fri, 14 Nov 2025 00:51:36 GMT  
		Size: 7.3 MB (7347732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26cba647684606d2047336e7370df8b31bceb5ac0c93f76e4c6cf57e4935abb5`  
		Last Modified: Fri, 14 Nov 2025 00:51:37 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:f3e1520cdddb6b9d5ab43fcc34bbeb43c0d6c22d8ea94455c11147dfde8fa7e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c9fd38babe3f1be76a8163c4d6bbf194feb8a45fff6e32ded35709eacfe2e90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185230220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd2703b92e9834a9be1e0da90e8898f84184eca798290fe1a4831c646b06d49`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:37 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:37 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:37 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:37 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:37 GMT
ARG KONG_VERSION=2.8.5
# Thu, 13 Nov 2025 23:28:37 GMT
ENV KONG_VERSION=2.8.5
# Thu, 13 Nov 2025 23:28:37 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Thu, 13 Nov 2025 23:28:37 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Thu, 13 Nov 2025 23:29:12 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:29:12 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:29:12 GMT
USER kong
# Thu, 13 Nov 2025 23:29:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:12 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:29:12 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:29:12 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:29:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5ffc6da68547f0c8858f58595d1d87cfbba7eaa59c699faaadbf9e486000e6`  
		Last Modified: Thu, 13 Nov 2025 23:29:43 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428613c4fd7abb4316edf11b7df45b21f7c8278678667a8b00dd5770ce620332`  
		Last Modified: Fri, 14 Nov 2025 02:07:55 GMT  
		Size: 130.6 MB (130610573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aac4f5cbb31821ac1aee107bfa5c9df03f300e23cf859fb80c8c64e3679fe59`  
		Last Modified: Thu, 13 Nov 2025 23:29:41 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:7a917d51b6276486449efc269255eb887d55a91dd621de18ae29fd4d2158c525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4527c9e5da85a3c126ce5aae588314cee20c1b2a75bba8c8796e825b5ced1ff2`

```dockerfile
```

-	Layers:
	-	`sha256:c98cfe5ecbe8bb6ee37540d5c27d1d2efcaf495d4b60497512f79b94a839ba41`  
		Last Modified: Fri, 14 Nov 2025 00:51:36 GMT  
		Size: 7.3 MB (7347732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26cba647684606d2047336e7370df8b31bceb5ac0c93f76e4c6cf57e4935abb5`  
		Last Modified: Fri, 14 Nov 2025 00:51:37 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:4379444ecfd82794b27de38a74ba540e8571683dfdfce74c8ecb4018f308fb29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:73ac10ce4d2c5b3b8b4acd6c8117b4e72d1a201d95be2d51aeae8324d776a108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a975970da2f5f3b909dec92b1a5ddc5e9299baee1442fb1a6986a8a120d5480`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:25 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:51 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
USER kong
# Thu, 13 Nov 2025 23:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:51 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:51 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5104131fbef7176e8cd24a2416bd30fc63327b0bc4e93f6e8c458a949643881b`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a179123cf6d8a29b35225250c7ef2422eb5e6662b5892c2afd6aacd9219e3`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 90.7 MB (90684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920d1873acc46a7f1f21afb90bee1d4a777bc5bb162d40955823be4f86d9111`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:91108241b0cc36c651a57aff8d1a75aee86c882de5b1b70d3e84fc5c9af5ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc818002c9463faf9fa84bdd7881afec502836e1f8d430ed9a85428a6a70cc4d`

```dockerfile
```

-	Layers:
	-	`sha256:74bc1f547d80da5da465fab4f853d5e7497626b68bccbaa91af57748e5c4ea63`  
		Last Modified: Fri, 14 Nov 2025 00:51:46 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49458e3133464aeee315cdb133807a4bb1eeb4fd78527fe5b43d5d343b9442c0`  
		Last Modified: Fri, 14 Nov 2025 00:51:47 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e392e72f7f8d4e25135721231cd84bca4d3997a53f448567ac14a141f62ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf86f243d2501de569559bf4860b3f80303583722d53ea1faf49066051de286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:01 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:01 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:01 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
USER kong
# Thu, 13 Nov 2025 23:28:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58fa5fef0221ddd66a522e1da28912b663369fd67055bf65780dc515c0d4980`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8382b8ad185c2d42050d0233cf7b15ced3f08a55a39460f866b3e0c62a67015`  
		Last Modified: Thu, 13 Nov 2025 23:29:06 GMT  
		Size: 90.0 MB (90002565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec291fa41f5c7aa3e8be31ddb4d16076756f60b2300135138b3c164348d73`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:9f379e0f8ef07064b65f713115f8fb1ed892b9fb704ae3dcbe7265bae23e13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc24390b67e128a3e9069676e64c69bd3dd6b32a0a7e816a90628a1ce7d5d34`

```dockerfile
```

-	Layers:
	-	`sha256:aa5304c177397dc7e34bbc372c3cea99528641db0beeb1d5bcc1de2d950d0947`  
		Last Modified: Fri, 14 Nov 2025 00:51:52 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba0d53888268fb2259f1c1b4ff934a69b6b5cdf16736557448980133d16f080`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:384807eefaaeca0c45a6cb73d5419f97c79cd749dba93475a389b0f131fa5bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:821d40e189cf19dca1b1f569d15a78f161a1b033e5faf66dad62522cd65650ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92259642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383cf45eb973c8129348d3b75ab68b87b15c49e84f1ba805442a88be2a9bde2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:40 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:40 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:40 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:40 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:40 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:40 GMT
ENV KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 13 Nov 2025 23:29:03 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:29:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:29:03 GMT
USER kong
# Thu, 13 Nov 2025 23:29:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:03 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:29:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:29:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:29:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e038756f99e05d29b01bb61e88559baa73060635ce49dfc589131b5a3921864a`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f06df743d9023e9a0d4aaccebdb73860c4c3bc672fc3a4ee0bb016f1dcf03`  
		Last Modified: Thu, 13 Nov 2025 23:29:38 GMT  
		Size: 62.7 MB (62721556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a82f4fc5d50c717eaf8c0ff319a0c4551b6ac99c5c58acbf9d27687a68600d`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:38cc27ca89d001fce8b842f2e0fab5278285d6cb37bd61732acab77043007fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2465d538b10ed580254b8362058d6115a67cdfe199a8f9781c4093bd61a3e563`

```dockerfile
```

-	Layers:
	-	`sha256:2ccbcc066600d2ab940163b34dc52a8db3277b1f8828d4ea53e6b5fa27058ada`  
		Last Modified: Fri, 14 Nov 2025 00:51:54 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a592a81f360d846a9d79e2c6df34071f2e424fbf4bc3035c7d3a4d3c890c9bb`  
		Last Modified: Fri, 14 Nov 2025 00:51:55 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf630a680384e5eea44299710902f717e38f2a03368d0f665762f27bb74de19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88566002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a03fab52c3f57f76520cfa61b70da17f5813b863ea0ff58868869184448af3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:09 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:09 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:09 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:09 GMT
ENV KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 13 Nov 2025 23:28:30 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
USER kong
# Thu, 13 Nov 2025 23:28:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:30 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:30 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd725214f38f58d638aae8bf31f08584a3984cb65d4592cb847fa25bc2d0b1d5`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c739e0291373d9f3a4dd3e8ec81269f4ed2c8af3c8f92e4984e82c4cc05030af`  
		Last Modified: Thu, 13 Nov 2025 23:28:56 GMT  
		Size: 61.2 MB (61180841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea979e4206cfce7cbfaf329018faa6b0290e6d0300b4f1fd5b2041f2fd39b94c`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:9635b48ee2950b5282a17c5ba96636cdef64beb6d53ab8e2f57b26df22e87788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15dce34d3d35ea12c5b29f3d25110b053d3f446d5f8020fcc6f013ec62ad9305`

```dockerfile
```

-	Layers:
	-	`sha256:96b64b0557e848fb36cf94d3dbf810e6d46036777a70a8a3b52e82e73db7ccc3`  
		Last Modified: Fri, 14 Nov 2025 00:52:01 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae7db4cf43d0a60d733d737d5991e0a99e23586e67ef01d7efc33ac19b2dec8`  
		Last Modified: Fri, 14 Nov 2025 00:52:02 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:384807eefaaeca0c45a6cb73d5419f97c79cd749dba93475a389b0f131fa5bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:821d40e189cf19dca1b1f569d15a78f161a1b033e5faf66dad62522cd65650ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92259642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383cf45eb973c8129348d3b75ab68b87b15c49e84f1ba805442a88be2a9bde2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:40 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:40 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:40 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:40 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:40 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:40 GMT
ENV KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 13 Nov 2025 23:29:03 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:29:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:29:03 GMT
USER kong
# Thu, 13 Nov 2025 23:29:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:03 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:29:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:29:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:29:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e038756f99e05d29b01bb61e88559baa73060635ce49dfc589131b5a3921864a`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f06df743d9023e9a0d4aaccebdb73860c4c3bc672fc3a4ee0bb016f1dcf03`  
		Last Modified: Thu, 13 Nov 2025 23:29:38 GMT  
		Size: 62.7 MB (62721556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a82f4fc5d50c717eaf8c0ff319a0c4551b6ac99c5c58acbf9d27687a68600d`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:38cc27ca89d001fce8b842f2e0fab5278285d6cb37bd61732acab77043007fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2465d538b10ed580254b8362058d6115a67cdfe199a8f9781c4093bd61a3e563`

```dockerfile
```

-	Layers:
	-	`sha256:2ccbcc066600d2ab940163b34dc52a8db3277b1f8828d4ea53e6b5fa27058ada`  
		Last Modified: Fri, 14 Nov 2025 00:51:54 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a592a81f360d846a9d79e2c6df34071f2e424fbf4bc3035c7d3a4d3c890c9bb`  
		Last Modified: Fri, 14 Nov 2025 00:51:55 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf630a680384e5eea44299710902f717e38f2a03368d0f665762f27bb74de19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88566002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a03fab52c3f57f76520cfa61b70da17f5813b863ea0ff58868869184448af3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:09 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:09 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:09 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:09 GMT
ENV KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 13 Nov 2025 23:28:30 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
USER kong
# Thu, 13 Nov 2025 23:28:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:30 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:30 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd725214f38f58d638aae8bf31f08584a3984cb65d4592cb847fa25bc2d0b1d5`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c739e0291373d9f3a4dd3e8ec81269f4ed2c8af3c8f92e4984e82c4cc05030af`  
		Last Modified: Thu, 13 Nov 2025 23:28:56 GMT  
		Size: 61.2 MB (61180841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea979e4206cfce7cbfaf329018faa6b0290e6d0300b4f1fd5b2041f2fd39b94c`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9635b48ee2950b5282a17c5ba96636cdef64beb6d53ab8e2f57b26df22e87788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15dce34d3d35ea12c5b29f3d25110b053d3f446d5f8020fcc6f013ec62ad9305`

```dockerfile
```

-	Layers:
	-	`sha256:96b64b0557e848fb36cf94d3dbf810e6d46036777a70a8a3b52e82e73db7ccc3`  
		Last Modified: Fri, 14 Nov 2025 00:52:01 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae7db4cf43d0a60d733d737d5991e0a99e23586e67ef01d7efc33ac19b2dec8`  
		Last Modified: Fri, 14 Nov 2025 00:52:02 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:384807eefaaeca0c45a6cb73d5419f97c79cd749dba93475a389b0f131fa5bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:821d40e189cf19dca1b1f569d15a78f161a1b033e5faf66dad62522cd65650ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92259642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383cf45eb973c8129348d3b75ab68b87b15c49e84f1ba805442a88be2a9bde2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:40 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:40 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:40 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:40 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:40 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:40 GMT
ENV KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 13 Nov 2025 23:29:03 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:29:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:29:03 GMT
USER kong
# Thu, 13 Nov 2025 23:29:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:03 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:29:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:29:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:29:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e038756f99e05d29b01bb61e88559baa73060635ce49dfc589131b5a3921864a`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f06df743d9023e9a0d4aaccebdb73860c4c3bc672fc3a4ee0bb016f1dcf03`  
		Last Modified: Thu, 13 Nov 2025 23:29:38 GMT  
		Size: 62.7 MB (62721556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a82f4fc5d50c717eaf8c0ff319a0c4551b6ac99c5c58acbf9d27687a68600d`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:38cc27ca89d001fce8b842f2e0fab5278285d6cb37bd61732acab77043007fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2465d538b10ed580254b8362058d6115a67cdfe199a8f9781c4093bd61a3e563`

```dockerfile
```

-	Layers:
	-	`sha256:2ccbcc066600d2ab940163b34dc52a8db3277b1f8828d4ea53e6b5fa27058ada`  
		Last Modified: Fri, 14 Nov 2025 00:51:54 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a592a81f360d846a9d79e2c6df34071f2e424fbf4bc3035c7d3a4d3c890c9bb`  
		Last Modified: Fri, 14 Nov 2025 00:51:55 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf630a680384e5eea44299710902f717e38f2a03368d0f665762f27bb74de19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88566002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a03fab52c3f57f76520cfa61b70da17f5813b863ea0ff58868869184448af3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:09 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:09 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:09 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:09 GMT
ENV KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 13 Nov 2025 23:28:30 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
USER kong
# Thu, 13 Nov 2025 23:28:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:30 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:30 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd725214f38f58d638aae8bf31f08584a3984cb65d4592cb847fa25bc2d0b1d5`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c739e0291373d9f3a4dd3e8ec81269f4ed2c8af3c8f92e4984e82c4cc05030af`  
		Last Modified: Thu, 13 Nov 2025 23:28:56 GMT  
		Size: 61.2 MB (61180841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea979e4206cfce7cbfaf329018faa6b0290e6d0300b4f1fd5b2041f2fd39b94c`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:9635b48ee2950b5282a17c5ba96636cdef64beb6d53ab8e2f57b26df22e87788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15dce34d3d35ea12c5b29f3d25110b053d3f446d5f8020fcc6f013ec62ad9305`

```dockerfile
```

-	Layers:
	-	`sha256:96b64b0557e848fb36cf94d3dbf810e6d46036777a70a8a3b52e82e73db7ccc3`  
		Last Modified: Fri, 14 Nov 2025 00:52:01 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae7db4cf43d0a60d733d737d5991e0a99e23586e67ef01d7efc33ac19b2dec8`  
		Last Modified: Fri, 14 Nov 2025 00:52:02 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:384807eefaaeca0c45a6cb73d5419f97c79cd749dba93475a389b0f131fa5bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:821d40e189cf19dca1b1f569d15a78f161a1b033e5faf66dad62522cd65650ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92259642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383cf45eb973c8129348d3b75ab68b87b15c49e84f1ba805442a88be2a9bde2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:40 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:40 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:40 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:40 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:40 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:40 GMT
ENV KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 13 Nov 2025 23:28:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 13 Nov 2025 23:29:03 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:29:03 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:29:03 GMT
USER kong
# Thu, 13 Nov 2025 23:29:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:03 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:29:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:29:03 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:29:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e038756f99e05d29b01bb61e88559baa73060635ce49dfc589131b5a3921864a`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4f06df743d9023e9a0d4aaccebdb73860c4c3bc672fc3a4ee0bb016f1dcf03`  
		Last Modified: Thu, 13 Nov 2025 23:29:38 GMT  
		Size: 62.7 MB (62721556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a82f4fc5d50c717eaf8c0ff319a0c4551b6ac99c5c58acbf9d27687a68600d`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:38cc27ca89d001fce8b842f2e0fab5278285d6cb37bd61732acab77043007fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2465d538b10ed580254b8362058d6115a67cdfe199a8f9781c4093bd61a3e563`

```dockerfile
```

-	Layers:
	-	`sha256:2ccbcc066600d2ab940163b34dc52a8db3277b1f8828d4ea53e6b5fa27058ada`  
		Last Modified: Fri, 14 Nov 2025 00:51:54 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a592a81f360d846a9d79e2c6df34071f2e424fbf4bc3035c7d3a4d3c890c9bb`  
		Last Modified: Fri, 14 Nov 2025 00:51:55 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf630a680384e5eea44299710902f717e38f2a03368d0f665762f27bb74de19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88566002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a03fab52c3f57f76520cfa61b70da17f5813b863ea0ff58868869184448af3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:09 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:09 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:09 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:09 GMT
ENV KONG_VERSION=3.4.2
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Thu, 13 Nov 2025 23:28:09 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Thu, 13 Nov 2025 23:28:30 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:30 GMT
USER kong
# Thu, 13 Nov 2025 23:28:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:30 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:30 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd725214f38f58d638aae8bf31f08584a3984cb65d4592cb847fa25bc2d0b1d5`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c739e0291373d9f3a4dd3e8ec81269f4ed2c8af3c8f92e4984e82c4cc05030af`  
		Last Modified: Thu, 13 Nov 2025 23:28:56 GMT  
		Size: 61.2 MB (61180841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea979e4206cfce7cbfaf329018faa6b0290e6d0300b4f1fd5b2041f2fd39b94c`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9635b48ee2950b5282a17c5ba96636cdef64beb6d53ab8e2f57b26df22e87788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15dce34d3d35ea12c5b29f3d25110b053d3f446d5f8020fcc6f013ec62ad9305`

```dockerfile
```

-	Layers:
	-	`sha256:96b64b0557e848fb36cf94d3dbf810e6d46036777a70a8a3b52e82e73db7ccc3`  
		Last Modified: Fri, 14 Nov 2025 00:52:01 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae7db4cf43d0a60d733d737d5991e0a99e23586e67ef01d7efc33ac19b2dec8`  
		Last Modified: Fri, 14 Nov 2025 00:52:02 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:a9130d1843e6740a33b7ea270f4b21e8adcbb0fb3041faefc2a226c74e6f80ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:e983f731c72a581092199532c3d8aa93d727056c5eb9005e9fd48c0d3ce7af11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac6f505e73f76948c3f35dca362ae6f7606cd2d49a4e206b49336dc9712b28e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:31 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:31 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:31 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:31 GMT
ENV KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 13 Nov 2025 23:28:53 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:54 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:54 GMT
USER kong
# Thu, 13 Nov 2025 23:28:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:54 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc5e80374a842b7d1d9a597ea1bbe24deba3ac18c36a9536459ca9bf72fd62d`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afea8f898d6069bfa9f6f0769f1e48eb5c1ec8ab7a1019a4c699d1662eca1e2`  
		Last Modified: Thu, 13 Nov 2025 23:29:25 GMT  
		Size: 88.0 MB (88009126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc449375376ccc21dde599bbe1355dc391a0a7d02c412fb904051b22a71e96`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:6795591ab91bb93b6508b898ab0cb5bc370db64a1afeb4016213d0bc60bddbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14df910dbc7eb44a35f4d971b4dc788c70737fb6694cf9a84c253f4469b6b884`

```dockerfile
```

-	Layers:
	-	`sha256:c9de1ffb8e98c75001b4c2bd80f0bf9a3f6bf9f684b0a3f3dacd8f06d3a272eb`  
		Last Modified: Fri, 14 Nov 2025 00:52:07 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44540453ec0d188a1f8a794b5a3954360ecf6baf576548b1383381e8e84c2d6`  
		Last Modified: Fri, 14 Nov 2025 00:52:08 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:19d6fe1897de5ca09110e4a7ce5057238581b8cfc1a249344912ea144870c272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114674147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b68dbcdc25cd4d782604ecc4bb9ec130f01e7629d777c9bfcae62a882b67a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:00 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:00 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:00 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:00 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:00 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:00 GMT
ENV KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 13 Nov 2025 23:28:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
USER kong
# Thu, 13 Nov 2025 23:28:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba0294c610db8b59caddaac863e761c82aff0f72ddab750315412b84c343417`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65005d4081173c68f42d18fab62ceca3551b30fc0f823190c3f55a4302fcf10`  
		Last Modified: Thu, 13 Nov 2025 23:28:59 GMT  
		Size: 87.3 MB (87288994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f644224532f324988ac41053675b2c8840b3afc3818c412ba55acb890a93ba`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:4d1c25476ae78733f08a7230ac432a2d35c5c0275867673ad0e92802cf96d1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972e7b4a122dd0784c844c0747f0a3b1b94b805c4a848b8112bb55831c8a96af`

```dockerfile
```

-	Layers:
	-	`sha256:c2d06932a15fb9817acb9d2b6c5013726d220c8002c712d74c2a0e86a47fb97c`  
		Last Modified: Fri, 14 Nov 2025 00:52:13 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d672cc5838c59cd1e1e32214d0481fd151bb4c71bf12333553f9eb70ec3515`  
		Last Modified: Fri, 14 Nov 2025 00:52:14 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:a9130d1843e6740a33b7ea270f4b21e8adcbb0fb3041faefc2a226c74e6f80ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e983f731c72a581092199532c3d8aa93d727056c5eb9005e9fd48c0d3ce7af11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac6f505e73f76948c3f35dca362ae6f7606cd2d49a4e206b49336dc9712b28e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:31 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:31 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:31 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:31 GMT
ENV KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 13 Nov 2025 23:28:53 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:54 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:54 GMT
USER kong
# Thu, 13 Nov 2025 23:28:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:54 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc5e80374a842b7d1d9a597ea1bbe24deba3ac18c36a9536459ca9bf72fd62d`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afea8f898d6069bfa9f6f0769f1e48eb5c1ec8ab7a1019a4c699d1662eca1e2`  
		Last Modified: Thu, 13 Nov 2025 23:29:25 GMT  
		Size: 88.0 MB (88009126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc449375376ccc21dde599bbe1355dc391a0a7d02c412fb904051b22a71e96`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:6795591ab91bb93b6508b898ab0cb5bc370db64a1afeb4016213d0bc60bddbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14df910dbc7eb44a35f4d971b4dc788c70737fb6694cf9a84c253f4469b6b884`

```dockerfile
```

-	Layers:
	-	`sha256:c9de1ffb8e98c75001b4c2bd80f0bf9a3f6bf9f684b0a3f3dacd8f06d3a272eb`  
		Last Modified: Fri, 14 Nov 2025 00:52:07 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44540453ec0d188a1f8a794b5a3954360ecf6baf576548b1383381e8e84c2d6`  
		Last Modified: Fri, 14 Nov 2025 00:52:08 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:19d6fe1897de5ca09110e4a7ce5057238581b8cfc1a249344912ea144870c272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114674147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b68dbcdc25cd4d782604ecc4bb9ec130f01e7629d777c9bfcae62a882b67a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:00 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:00 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:00 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:00 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:00 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:00 GMT
ENV KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 13 Nov 2025 23:28:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
USER kong
# Thu, 13 Nov 2025 23:28:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba0294c610db8b59caddaac863e761c82aff0f72ddab750315412b84c343417`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65005d4081173c68f42d18fab62ceca3551b30fc0f823190c3f55a4302fcf10`  
		Last Modified: Thu, 13 Nov 2025 23:28:59 GMT  
		Size: 87.3 MB (87288994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f644224532f324988ac41053675b2c8840b3afc3818c412ba55acb890a93ba`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:4d1c25476ae78733f08a7230ac432a2d35c5c0275867673ad0e92802cf96d1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972e7b4a122dd0784c844c0747f0a3b1b94b805c4a848b8112bb55831c8a96af`

```dockerfile
```

-	Layers:
	-	`sha256:c2d06932a15fb9817acb9d2b6c5013726d220c8002c712d74c2a0e86a47fb97c`  
		Last Modified: Fri, 14 Nov 2025 00:52:13 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d672cc5838c59cd1e1e32214d0481fd151bb4c71bf12333553f9eb70ec3515`  
		Last Modified: Fri, 14 Nov 2025 00:52:14 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:a9130d1843e6740a33b7ea270f4b21e8adcbb0fb3041faefc2a226c74e6f80ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:e983f731c72a581092199532c3d8aa93d727056c5eb9005e9fd48c0d3ce7af11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac6f505e73f76948c3f35dca362ae6f7606cd2d49a4e206b49336dc9712b28e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:31 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:31 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:31 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:31 GMT
ENV KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 13 Nov 2025 23:28:53 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:54 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:54 GMT
USER kong
# Thu, 13 Nov 2025 23:28:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:54 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc5e80374a842b7d1d9a597ea1bbe24deba3ac18c36a9536459ca9bf72fd62d`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afea8f898d6069bfa9f6f0769f1e48eb5c1ec8ab7a1019a4c699d1662eca1e2`  
		Last Modified: Thu, 13 Nov 2025 23:29:25 GMT  
		Size: 88.0 MB (88009126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc449375376ccc21dde599bbe1355dc391a0a7d02c412fb904051b22a71e96`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:6795591ab91bb93b6508b898ab0cb5bc370db64a1afeb4016213d0bc60bddbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14df910dbc7eb44a35f4d971b4dc788c70737fb6694cf9a84c253f4469b6b884`

```dockerfile
```

-	Layers:
	-	`sha256:c9de1ffb8e98c75001b4c2bd80f0bf9a3f6bf9f684b0a3f3dacd8f06d3a272eb`  
		Last Modified: Fri, 14 Nov 2025 00:52:07 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44540453ec0d188a1f8a794b5a3954360ecf6baf576548b1383381e8e84c2d6`  
		Last Modified: Fri, 14 Nov 2025 00:52:08 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:19d6fe1897de5ca09110e4a7ce5057238581b8cfc1a249344912ea144870c272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114674147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b68dbcdc25cd4d782604ecc4bb9ec130f01e7629d777c9bfcae62a882b67a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:00 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:00 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:00 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:00 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:00 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:00 GMT
ENV KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 13 Nov 2025 23:28:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
USER kong
# Thu, 13 Nov 2025 23:28:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba0294c610db8b59caddaac863e761c82aff0f72ddab750315412b84c343417`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65005d4081173c68f42d18fab62ceca3551b30fc0f823190c3f55a4302fcf10`  
		Last Modified: Thu, 13 Nov 2025 23:28:59 GMT  
		Size: 87.3 MB (87288994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f644224532f324988ac41053675b2c8840b3afc3818c412ba55acb890a93ba`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:4d1c25476ae78733f08a7230ac432a2d35c5c0275867673ad0e92802cf96d1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972e7b4a122dd0784c844c0747f0a3b1b94b805c4a848b8112bb55831c8a96af`

```dockerfile
```

-	Layers:
	-	`sha256:c2d06932a15fb9817acb9d2b6c5013726d220c8002c712d74c2a0e86a47fb97c`  
		Last Modified: Fri, 14 Nov 2025 00:52:13 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d672cc5838c59cd1e1e32214d0481fd151bb4c71bf12333553f9eb70ec3515`  
		Last Modified: Fri, 14 Nov 2025 00:52:14 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:a9130d1843e6740a33b7ea270f4b21e8adcbb0fb3041faefc2a226c74e6f80ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e983f731c72a581092199532c3d8aa93d727056c5eb9005e9fd48c0d3ce7af11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ac6f505e73f76948c3f35dca362ae6f7606cd2d49a4e206b49336dc9712b28e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:31 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:31 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:31 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:31 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:31 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:31 GMT
ENV KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 13 Nov 2025 23:28:31 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 13 Nov 2025 23:28:53 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:54 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:54 GMT
USER kong
# Thu, 13 Nov 2025 23:28:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:54 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:54 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc5e80374a842b7d1d9a597ea1bbe24deba3ac18c36a9536459ca9bf72fd62d`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afea8f898d6069bfa9f6f0769f1e48eb5c1ec8ab7a1019a4c699d1662eca1e2`  
		Last Modified: Thu, 13 Nov 2025 23:29:25 GMT  
		Size: 88.0 MB (88009126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc449375376ccc21dde599bbe1355dc391a0a7d02c412fb904051b22a71e96`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:6795591ab91bb93b6508b898ab0cb5bc370db64a1afeb4016213d0bc60bddbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14df910dbc7eb44a35f4d971b4dc788c70737fb6694cf9a84c253f4469b6b884`

```dockerfile
```

-	Layers:
	-	`sha256:c9de1ffb8e98c75001b4c2bd80f0bf9a3f6bf9f684b0a3f3dacd8f06d3a272eb`  
		Last Modified: Fri, 14 Nov 2025 00:52:07 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44540453ec0d188a1f8a794b5a3954360ecf6baf576548b1383381e8e84c2d6`  
		Last Modified: Fri, 14 Nov 2025 00:52:08 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:19d6fe1897de5ca09110e4a7ce5057238581b8cfc1a249344912ea144870c272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114674147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b68dbcdc25cd4d782604ecc4bb9ec130f01e7629d777c9bfcae62a882b67a4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:00 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:00 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:00 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:00 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:00 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:00 GMT
ENV KONG_VERSION=3.8.0
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 13 Nov 2025 23:28:00 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 13 Nov 2025 23:28:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:27 GMT
USER kong
# Thu, 13 Nov 2025 23:28:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba0294c610db8b59caddaac863e761c82aff0f72ddab750315412b84c343417`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65005d4081173c68f42d18fab62ceca3551b30fc0f823190c3f55a4302fcf10`  
		Last Modified: Thu, 13 Nov 2025 23:28:59 GMT  
		Size: 87.3 MB (87288994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f644224532f324988ac41053675b2c8840b3afc3818c412ba55acb890a93ba`  
		Last Modified: Thu, 13 Nov 2025 23:28:52 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:4d1c25476ae78733f08a7230ac432a2d35c5c0275867673ad0e92802cf96d1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972e7b4a122dd0784c844c0747f0a3b1b94b805c4a848b8112bb55831c8a96af`

```dockerfile
```

-	Layers:
	-	`sha256:c2d06932a15fb9817acb9d2b6c5013726d220c8002c712d74c2a0e86a47fb97c`  
		Last Modified: Fri, 14 Nov 2025 00:52:13 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d672cc5838c59cd1e1e32214d0481fd151bb4c71bf12333553f9eb70ec3515`  
		Last Modified: Fri, 14 Nov 2025 00:52:14 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:4379444ecfd82794b27de38a74ba540e8571683dfdfce74c8ecb4018f308fb29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:73ac10ce4d2c5b3b8b4acd6c8117b4e72d1a201d95be2d51aeae8324d776a108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a975970da2f5f3b909dec92b1a5ddc5e9299baee1442fb1a6986a8a120d5480`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:25 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:51 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
USER kong
# Thu, 13 Nov 2025 23:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:51 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:51 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5104131fbef7176e8cd24a2416bd30fc63327b0bc4e93f6e8c458a949643881b`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a179123cf6d8a29b35225250c7ef2422eb5e6662b5892c2afd6aacd9219e3`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 90.7 MB (90684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920d1873acc46a7f1f21afb90bee1d4a777bc5bb162d40955823be4f86d9111`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:91108241b0cc36c651a57aff8d1a75aee86c882de5b1b70d3e84fc5c9af5ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc818002c9463faf9fa84bdd7881afec502836e1f8d430ed9a85428a6a70cc4d`

```dockerfile
```

-	Layers:
	-	`sha256:74bc1f547d80da5da465fab4f853d5e7497626b68bccbaa91af57748e5c4ea63`  
		Last Modified: Fri, 14 Nov 2025 00:51:46 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49458e3133464aeee315cdb133807a4bb1eeb4fd78527fe5b43d5d343b9442c0`  
		Last Modified: Fri, 14 Nov 2025 00:51:47 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e392e72f7f8d4e25135721231cd84bca4d3997a53f448567ac14a141f62ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf86f243d2501de569559bf4860b3f80303583722d53ea1faf49066051de286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:01 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:01 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:01 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
USER kong
# Thu, 13 Nov 2025 23:28:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58fa5fef0221ddd66a522e1da28912b663369fd67055bf65780dc515c0d4980`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8382b8ad185c2d42050d0233cf7b15ced3f08a55a39460f866b3e0c62a67015`  
		Last Modified: Thu, 13 Nov 2025 23:29:06 GMT  
		Size: 90.0 MB (90002565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec291fa41f5c7aa3e8be31ddb4d16076756f60b2300135138b3c164348d73`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:9f379e0f8ef07064b65f713115f8fb1ed892b9fb704ae3dcbe7265bae23e13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc24390b67e128a3e9069676e64c69bd3dd6b32a0a7e816a90628a1ce7d5d34`

```dockerfile
```

-	Layers:
	-	`sha256:aa5304c177397dc7e34bbc372c3cea99528641db0beeb1d5bcc1de2d950d0947`  
		Last Modified: Fri, 14 Nov 2025 00:51:52 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba0d53888268fb2259f1c1b4ff934a69b6b5cdf16736557448980133d16f080`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:4379444ecfd82794b27de38a74ba540e8571683dfdfce74c8ecb4018f308fb29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:73ac10ce4d2c5b3b8b4acd6c8117b4e72d1a201d95be2d51aeae8324d776a108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a975970da2f5f3b909dec92b1a5ddc5e9299baee1442fb1a6986a8a120d5480`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:25 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:51 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
USER kong
# Thu, 13 Nov 2025 23:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:51 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:51 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5104131fbef7176e8cd24a2416bd30fc63327b0bc4e93f6e8c458a949643881b`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a179123cf6d8a29b35225250c7ef2422eb5e6662b5892c2afd6aacd9219e3`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 90.7 MB (90684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920d1873acc46a7f1f21afb90bee1d4a777bc5bb162d40955823be4f86d9111`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:91108241b0cc36c651a57aff8d1a75aee86c882de5b1b70d3e84fc5c9af5ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc818002c9463faf9fa84bdd7881afec502836e1f8d430ed9a85428a6a70cc4d`

```dockerfile
```

-	Layers:
	-	`sha256:74bc1f547d80da5da465fab4f853d5e7497626b68bccbaa91af57748e5c4ea63`  
		Last Modified: Fri, 14 Nov 2025 00:51:46 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49458e3133464aeee315cdb133807a4bb1eeb4fd78527fe5b43d5d343b9442c0`  
		Last Modified: Fri, 14 Nov 2025 00:51:47 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e392e72f7f8d4e25135721231cd84bca4d3997a53f448567ac14a141f62ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf86f243d2501de569559bf4860b3f80303583722d53ea1faf49066051de286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:01 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:01 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:01 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
USER kong
# Thu, 13 Nov 2025 23:28:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58fa5fef0221ddd66a522e1da28912b663369fd67055bf65780dc515c0d4980`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8382b8ad185c2d42050d0233cf7b15ced3f08a55a39460f866b3e0c62a67015`  
		Last Modified: Thu, 13 Nov 2025 23:29:06 GMT  
		Size: 90.0 MB (90002565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec291fa41f5c7aa3e8be31ddb4d16076756f60b2300135138b3c164348d73`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9f379e0f8ef07064b65f713115f8fb1ed892b9fb704ae3dcbe7265bae23e13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc24390b67e128a3e9069676e64c69bd3dd6b32a0a7e816a90628a1ce7d5d34`

```dockerfile
```

-	Layers:
	-	`sha256:aa5304c177397dc7e34bbc372c3cea99528641db0beeb1d5bcc1de2d950d0947`  
		Last Modified: Fri, 14 Nov 2025 00:51:52 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba0d53888268fb2259f1c1b4ff934a69b6b5cdf16736557448980133d16f080`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:4379444ecfd82794b27de38a74ba540e8571683dfdfce74c8ecb4018f308fb29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:73ac10ce4d2c5b3b8b4acd6c8117b4e72d1a201d95be2d51aeae8324d776a108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a975970da2f5f3b909dec92b1a5ddc5e9299baee1442fb1a6986a8a120d5480`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:25 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:51 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
USER kong
# Thu, 13 Nov 2025 23:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:51 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:51 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5104131fbef7176e8cd24a2416bd30fc63327b0bc4e93f6e8c458a949643881b`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a179123cf6d8a29b35225250c7ef2422eb5e6662b5892c2afd6aacd9219e3`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 90.7 MB (90684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920d1873acc46a7f1f21afb90bee1d4a777bc5bb162d40955823be4f86d9111`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:91108241b0cc36c651a57aff8d1a75aee86c882de5b1b70d3e84fc5c9af5ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc818002c9463faf9fa84bdd7881afec502836e1f8d430ed9a85428a6a70cc4d`

```dockerfile
```

-	Layers:
	-	`sha256:74bc1f547d80da5da465fab4f853d5e7497626b68bccbaa91af57748e5c4ea63`  
		Last Modified: Fri, 14 Nov 2025 00:51:46 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49458e3133464aeee315cdb133807a4bb1eeb4fd78527fe5b43d5d343b9442c0`  
		Last Modified: Fri, 14 Nov 2025 00:51:47 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e392e72f7f8d4e25135721231cd84bca4d3997a53f448567ac14a141f62ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf86f243d2501de569559bf4860b3f80303583722d53ea1faf49066051de286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:01 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:01 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:01 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
USER kong
# Thu, 13 Nov 2025 23:28:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58fa5fef0221ddd66a522e1da28912b663369fd67055bf65780dc515c0d4980`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8382b8ad185c2d42050d0233cf7b15ced3f08a55a39460f866b3e0c62a67015`  
		Last Modified: Thu, 13 Nov 2025 23:29:06 GMT  
		Size: 90.0 MB (90002565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec291fa41f5c7aa3e8be31ddb4d16076756f60b2300135138b3c164348d73`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:9f379e0f8ef07064b65f713115f8fb1ed892b9fb704ae3dcbe7265bae23e13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc24390b67e128a3e9069676e64c69bd3dd6b32a0a7e816a90628a1ce7d5d34`

```dockerfile
```

-	Layers:
	-	`sha256:aa5304c177397dc7e34bbc372c3cea99528641db0beeb1d5bcc1de2d950d0947`  
		Last Modified: Fri, 14 Nov 2025 00:51:52 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba0d53888268fb2259f1c1b4ff934a69b6b5cdf16736557448980133d16f080`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:4379444ecfd82794b27de38a74ba540e8571683dfdfce74c8ecb4018f308fb29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:73ac10ce4d2c5b3b8b4acd6c8117b4e72d1a201d95be2d51aeae8324d776a108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a975970da2f5f3b909dec92b1a5ddc5e9299baee1442fb1a6986a8a120d5480`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:25 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:51 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
USER kong
# Thu, 13 Nov 2025 23:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:51 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:51 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5104131fbef7176e8cd24a2416bd30fc63327b0bc4e93f6e8c458a949643881b`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a179123cf6d8a29b35225250c7ef2422eb5e6662b5892c2afd6aacd9219e3`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 90.7 MB (90684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920d1873acc46a7f1f21afb90bee1d4a777bc5bb162d40955823be4f86d9111`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:91108241b0cc36c651a57aff8d1a75aee86c882de5b1b70d3e84fc5c9af5ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc818002c9463faf9fa84bdd7881afec502836e1f8d430ed9a85428a6a70cc4d`

```dockerfile
```

-	Layers:
	-	`sha256:74bc1f547d80da5da465fab4f853d5e7497626b68bccbaa91af57748e5c4ea63`  
		Last Modified: Fri, 14 Nov 2025 00:51:46 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49458e3133464aeee315cdb133807a4bb1eeb4fd78527fe5b43d5d343b9442c0`  
		Last Modified: Fri, 14 Nov 2025 00:51:47 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e392e72f7f8d4e25135721231cd84bca4d3997a53f448567ac14a141f62ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf86f243d2501de569559bf4860b3f80303583722d53ea1faf49066051de286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:01 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:01 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:01 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
USER kong
# Thu, 13 Nov 2025 23:28:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58fa5fef0221ddd66a522e1da28912b663369fd67055bf65780dc515c0d4980`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8382b8ad185c2d42050d0233cf7b15ced3f08a55a39460f866b3e0c62a67015`  
		Last Modified: Thu, 13 Nov 2025 23:29:06 GMT  
		Size: 90.0 MB (90002565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec291fa41f5c7aa3e8be31ddb4d16076756f60b2300135138b3c164348d73`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9f379e0f8ef07064b65f713115f8fb1ed892b9fb704ae3dcbe7265bae23e13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc24390b67e128a3e9069676e64c69bd3dd6b32a0a7e816a90628a1ce7d5d34`

```dockerfile
```

-	Layers:
	-	`sha256:aa5304c177397dc7e34bbc372c3cea99528641db0beeb1d5bcc1de2d950d0947`  
		Last Modified: Fri, 14 Nov 2025 00:51:52 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba0d53888268fb2259f1c1b4ff934a69b6b5cdf16736557448980133d16f080`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:4379444ecfd82794b27de38a74ba540e8571683dfdfce74c8ecb4018f308fb29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:73ac10ce4d2c5b3b8b4acd6c8117b4e72d1a201d95be2d51aeae8324d776a108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a975970da2f5f3b909dec92b1a5ddc5e9299baee1442fb1a6986a8a120d5480`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:25 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:51 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
USER kong
# Thu, 13 Nov 2025 23:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:51 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:51 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5104131fbef7176e8cd24a2416bd30fc63327b0bc4e93f6e8c458a949643881b`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a179123cf6d8a29b35225250c7ef2422eb5e6662b5892c2afd6aacd9219e3`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 90.7 MB (90684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920d1873acc46a7f1f21afb90bee1d4a777bc5bb162d40955823be4f86d9111`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:91108241b0cc36c651a57aff8d1a75aee86c882de5b1b70d3e84fc5c9af5ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc818002c9463faf9fa84bdd7881afec502836e1f8d430ed9a85428a6a70cc4d`

```dockerfile
```

-	Layers:
	-	`sha256:74bc1f547d80da5da465fab4f853d5e7497626b68bccbaa91af57748e5c4ea63`  
		Last Modified: Fri, 14 Nov 2025 00:51:46 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49458e3133464aeee315cdb133807a4bb1eeb4fd78527fe5b43d5d343b9442c0`  
		Last Modified: Fri, 14 Nov 2025 00:51:47 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e392e72f7f8d4e25135721231cd84bca4d3997a53f448567ac14a141f62ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf86f243d2501de569559bf4860b3f80303583722d53ea1faf49066051de286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:01 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:01 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:01 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
USER kong
# Thu, 13 Nov 2025 23:28:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58fa5fef0221ddd66a522e1da28912b663369fd67055bf65780dc515c0d4980`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8382b8ad185c2d42050d0233cf7b15ced3f08a55a39460f866b3e0c62a67015`  
		Last Modified: Thu, 13 Nov 2025 23:29:06 GMT  
		Size: 90.0 MB (90002565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec291fa41f5c7aa3e8be31ddb4d16076756f60b2300135138b3c164348d73`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:9f379e0f8ef07064b65f713115f8fb1ed892b9fb704ae3dcbe7265bae23e13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc24390b67e128a3e9069676e64c69bd3dd6b32a0a7e816a90628a1ce7d5d34`

```dockerfile
```

-	Layers:
	-	`sha256:aa5304c177397dc7e34bbc372c3cea99528641db0beeb1d5bcc1de2d950d0947`  
		Last Modified: Fri, 14 Nov 2025 00:51:52 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba0d53888268fb2259f1c1b4ff934a69b6b5cdf16736557448980133d16f080`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:4379444ecfd82794b27de38a74ba540e8571683dfdfce74c8ecb4018f308fb29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:73ac10ce4d2c5b3b8b4acd6c8117b4e72d1a201d95be2d51aeae8324d776a108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120410007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a975970da2f5f3b909dec92b1a5ddc5e9299baee1442fb1a6986a8a120d5480`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:25 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:25 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:25 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:51 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:51 GMT
USER kong
# Thu, 13 Nov 2025 23:28:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:51 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:51 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5104131fbef7176e8cd24a2416bd30fc63327b0bc4e93f6e8c458a949643881b`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8a179123cf6d8a29b35225250c7ef2422eb5e6662b5892c2afd6aacd9219e3`  
		Last Modified: Thu, 13 Nov 2025 23:29:24 GMT  
		Size: 90.7 MB (90684034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e920d1873acc46a7f1f21afb90bee1d4a777bc5bb162d40955823be4f86d9111`  
		Last Modified: Thu, 13 Nov 2025 23:29:16 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:91108241b0cc36c651a57aff8d1a75aee86c882de5b1b70d3e84fc5c9af5ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc818002c9463faf9fa84bdd7881afec502836e1f8d430ed9a85428a6a70cc4d`

```dockerfile
```

-	Layers:
	-	`sha256:74bc1f547d80da5da465fab4f853d5e7497626b68bccbaa91af57748e5c4ea63`  
		Last Modified: Fri, 14 Nov 2025 00:51:46 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49458e3133464aeee315cdb133807a4bb1eeb4fd78527fe5b43d5d343b9442c0`  
		Last Modified: Fri, 14 Nov 2025 00:51:47 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e392e72f7f8d4e25135721231cd84bca4d3997a53f448567ac14a141f62ae5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf86f243d2501de569559bf4860b3f80303583722d53ea1faf49066051de286`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:28:01 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 13 Nov 2025 23:28:01 GMT
ARG ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ENV ASSET=ce
# Thu, 13 Nov 2025 23:28:01 GMT
ARG EE_PORTS
# Thu, 13 Nov 2025 23:28:01 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ENV KONG_VERSION=3.9.1
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 13 Nov 2025 23:28:01 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 13 Nov 2025 23:28:31 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:28:31 GMT
USER kong
# Thu, 13 Nov 2025 23:28:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:28:31 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 13 Nov 2025 23:28:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 13 Nov 2025 23:28:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 13 Nov 2025 23:28:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58fa5fef0221ddd66a522e1da28912b663369fd67055bf65780dc515c0d4980`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8382b8ad185c2d42050d0233cf7b15ced3f08a55a39460f866b3e0c62a67015`  
		Last Modified: Thu, 13 Nov 2025 23:29:06 GMT  
		Size: 90.0 MB (90002565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec291fa41f5c7aa3e8be31ddb4d16076756f60b2300135138b3c164348d73`  
		Last Modified: Thu, 13 Nov 2025 23:28:57 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9f379e0f8ef07064b65f713115f8fb1ed892b9fb704ae3dcbe7265bae23e13eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc24390b67e128a3e9069676e64c69bd3dd6b32a0a7e816a90628a1ce7d5d34`

```dockerfile
```

-	Layers:
	-	`sha256:aa5304c177397dc7e34bbc372c3cea99528641db0beeb1d5bcc1de2d950d0947`  
		Last Modified: Fri, 14 Nov 2025 00:51:52 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba0d53888268fb2259f1c1b4ff934a69b6b5cdf16736557448980133d16f080`  
		Last Modified: Fri, 14 Nov 2025 00:51:53 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json
