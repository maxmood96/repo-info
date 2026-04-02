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
$ docker pull kong@sha256:c8f75f6d7f594bfaf73846cf0a8f9a1dc8325b445997a1b41a022942e83c0cc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:aa2f31d0ed7d317a7abeb14bf7b615366199e1afbc1883057c60af85e0a6bde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185646691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228770c4b90b53601b881cc872797a21501e11a5eaa9daab0eff7bcc32ae9df5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:18 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:14:18 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:14:18 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:14:18 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:14:18 GMT
ARG KONG_VERSION=2.8.5
# Wed, 01 Apr 2026 20:14:18 GMT
ENV KONG_VERSION=2.8.5
# Wed, 01 Apr 2026 20:14:18 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Wed, 01 Apr 2026 20:14:18 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Wed, 01 Apr 2026 20:14:58 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:58 GMT
USER kong
# Wed, 01 Apr 2026 20:14:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:58 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:58 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:58 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80d3f250ff1e3860e441dddd12734e0271099d71375bf9763b6375aa0eb4a4c`  
		Last Modified: Wed, 01 Apr 2026 20:15:21 GMT  
		Size: 25.1 MB (25081972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f482abbc902c7fbc74dcc5343ff6c7610746ca4a28f4fdd27fb28f283cb2cdd9`  
		Last Modified: Wed, 01 Apr 2026 20:15:23 GMT  
		Size: 130.8 MB (130827423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da05b411db154fef96c3325589783832a7f1bf16ddcff09cf596fc26c7479a0d`  
		Last Modified: Wed, 01 Apr 2026 20:15:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:b99047097b72d2649b2ebc6e227b37142709fcc41ed4578af1bfefaefec9b720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cc31fb24442a8084a70d192f3fcbefda1b7f7d6691a54b135723f9f1271644`

```dockerfile
```

-	Layers:
	-	`sha256:18b5c23040971e807b4fc897a1395ace2a6b02290114c33a3da5d86ddf57af67`  
		Last Modified: Wed, 01 Apr 2026 20:15:20 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01c7d4043da5b46ddf561bf4330454171d0ca5f5e3b1ab430e6d71de9ee7c96`  
		Last Modified: Wed, 01 Apr 2026 20:15:20 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:c8f75f6d7f594bfaf73846cf0a8f9a1dc8325b445997a1b41a022942e83c0cc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:aa2f31d0ed7d317a7abeb14bf7b615366199e1afbc1883057c60af85e0a6bde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185646691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228770c4b90b53601b881cc872797a21501e11a5eaa9daab0eff7bcc32ae9df5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:18 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:14:18 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:14:18 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:14:18 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:14:18 GMT
ARG KONG_VERSION=2.8.5
# Wed, 01 Apr 2026 20:14:18 GMT
ENV KONG_VERSION=2.8.5
# Wed, 01 Apr 2026 20:14:18 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Wed, 01 Apr 2026 20:14:18 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Wed, 01 Apr 2026 20:14:58 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:58 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:58 GMT
USER kong
# Wed, 01 Apr 2026 20:14:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:58 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:58 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:58 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:58 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80d3f250ff1e3860e441dddd12734e0271099d71375bf9763b6375aa0eb4a4c`  
		Last Modified: Wed, 01 Apr 2026 20:15:21 GMT  
		Size: 25.1 MB (25081972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f482abbc902c7fbc74dcc5343ff6c7610746ca4a28f4fdd27fb28f283cb2cdd9`  
		Last Modified: Wed, 01 Apr 2026 20:15:23 GMT  
		Size: 130.8 MB (130827423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da05b411db154fef96c3325589783832a7f1bf16ddcff09cf596fc26c7479a0d`  
		Last Modified: Wed, 01 Apr 2026 20:15:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:b99047097b72d2649b2ebc6e227b37142709fcc41ed4578af1bfefaefec9b720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cc31fb24442a8084a70d192f3fcbefda1b7f7d6691a54b135723f9f1271644`

```dockerfile
```

-	Layers:
	-	`sha256:18b5c23040971e807b4fc897a1395ace2a6b02290114c33a3da5d86ddf57af67`  
		Last Modified: Wed, 01 Apr 2026 20:15:20 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01c7d4043da5b46ddf561bf4330454171d0ca5f5e3b1ab430e6d71de9ee7c96`  
		Last Modified: Wed, 01 Apr 2026 20:15:20 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:7512bfa30d96709a9dede46c723b2c57b6fa61f4cbb797adf20f531d3e0266dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:7563df2ddf4938b826c8828da28572f7b9357cfb3e8607b36a15cc35b856aca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2620abfb8871e7741f3e10db56b83cd5866367f45e243bc97c8f022e6c0c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:20 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:20 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:20 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:39:48 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
USER kong
# Tue, 17 Mar 2026 01:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:48 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b43afd99cb1203273e3bf6cf9b42857ba2355f5218c924a310bb7cc21184d`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66038258e40a0a1302df60f6410f0c82d3c0a43ccdba69f6950f09b7b7183de`  
		Last Modified: Tue, 17 Mar 2026 01:40:06 GMT  
		Size: 90.7 MB (90692231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba581d5adf0d98b835dd239b1c96ffdd837857bf5edb85cded35a47599956b73`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:979493665a8c528d1ac6d8b09d4615e29ea99d54c8095f1dde79d97f4c23bf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032be33683199b1c6e5692ccc4a41859009748bdf9b2c2f1161e87f6b87cb78c`

```dockerfile
```

-	Layers:
	-	`sha256:a04da651e31999b82bc9ff0460696c27e540ff645a7a286aa79d22963a043a23`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f3b4a93fdf3e687cc0a5905662a0d66a4e3bacd30e4a3255d9bb1790ab74d2`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1aaf7b21ff8387489cf1b23d764542096d331bd4ee7b2f350c738f9f36a33f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118874339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f61ecab8cf35cae09475709dc7ce6868ce664b44dff3ca7a3773a024d79c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:54 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:54 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:41:26 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
USER kong
# Tue, 17 Mar 2026 01:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:26 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b0661171bf34ea182c4e15a6bb8a7d6d1ef8274654ab456a592bf8d0e3f86`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a2506e0b2a1fe740de635e019f70b67d1450fed67c72860d884dbdcfc9390`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 90.0 MB (90003339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19699203c06695b4414f10615cc9237f953cc008b634e414a6f7def3263272d1`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:e6595103d2d89e7d0d86dd80de606a32733854c43355997e16831f6ad77f4d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5124e3c50603a880744ccf9b4cb8457613d76b8a1abaad819fc4dca2ad9180`

```dockerfile
```

-	Layers:
	-	`sha256:d167aca56ef2576e465b7aae50c65e6a10e1cb455246a1804140c6d76477a4ec`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a4032d566877433146b7ecd07c9f2f4a77e4789acaf445e036761d56a1108c`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:ba47cd06209799c05d98c18c0b35259bc7d8debf48b303dfe8866670aef93963
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:916d8e66c48938a02ca197163ead84108eae0719f1521d9708f05f00f62745d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92477799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cd4d6ff51b583cdf2bd8ab6042b7dfe1a1010de22943e44d1090a5a7025005`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:14:09 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:14:09 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:14:09 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:14:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:14:09 GMT
ENV KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 01 Apr 2026 20:14:30 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:30 GMT
USER kong
# Wed, 01 Apr 2026 20:14:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:30 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:30 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0f93b1600f51f35d2e4f16f435c0eae991ae3207099f32944f1a59eca3f02`  
		Last Modified: Wed, 01 Apr 2026 20:14:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03345cb8ad5a1b9dba9c17f18121108fd767403cb32c794498814456bc5f44`  
		Last Modified: Wed, 01 Apr 2026 20:14:44 GMT  
		Size: 62.7 MB (62740103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf31bee8faee2e311ae8d8d4cd90e193cb51041b05429732e08a3b5e12831f2`  
		Last Modified: Wed, 01 Apr 2026 20:14:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:3b5c35531c54934e1f8b676a22f259a9afd755accb23936ea3a04c499f63a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a39359cd7dccddd0d7e1d2c9827d0002588ccc29437f6d4a07afaafeb44e9f`

```dockerfile
```

-	Layers:
	-	`sha256:325ec8256a448659f0d7e504c80b61251f05d51f05c322af75225bf79ece857f`  
		Last Modified: Wed, 01 Apr 2026 20:14:43 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48480493ef513f5de975459bb0a1696beca604ffbb2dbba8c79bc26c1607b14f`  
		Last Modified: Wed, 01 Apr 2026 20:14:42 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:30ea8c38f2e23f0a96052e14cf7141502728af07be960605a5ccf1069d45ba8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88813294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514d239172b1fe4d5f871680264b1d8cda1deb2a127040ba62348393c94187c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:25 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:25 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:25 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:13:25 GMT
ENV KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 01 Apr 2026 20:13:53 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:13:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:53 GMT
USER kong
# Wed, 01 Apr 2026 20:13:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:53 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:13:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:13:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:13:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ff1f4ee4387a15937f4e200d6df6d164a58c0c80114d771d6cbbf85cf5c36`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46366e7b6a4b14e50f10b43f6384ba846d357e0614de0b5f51a71ce274092e`  
		Last Modified: Wed, 01 Apr 2026 20:14:11 GMT  
		Size: 61.2 MB (61205069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70aa1f5dad893096b75b3008765cdb8521730ab1cb9fba10a4a25ff2fe5e2db`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:e21bbaa7ff4516c0aa2eb5c28827eccf499dd61fda903003e2051f0b765930b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efd1e3056b158957fe7e7a3aa72a13528715dae7c6a01dac18b840e31c77d36`

```dockerfile
```

-	Layers:
	-	`sha256:eb4849b97c13ccd56ff776bf4b171cc7a8eb6cbb1fb2de0f1fa091cf15443c06`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d10b52305ebd2a220f7ae09f2645ecf249a543f4180cc1eb5ab73ec80810a29`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:ba47cd06209799c05d98c18c0b35259bc7d8debf48b303dfe8866670aef93963
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:916d8e66c48938a02ca197163ead84108eae0719f1521d9708f05f00f62745d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92477799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cd4d6ff51b583cdf2bd8ab6042b7dfe1a1010de22943e44d1090a5a7025005`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:14:09 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:14:09 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:14:09 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:14:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:14:09 GMT
ENV KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 01 Apr 2026 20:14:30 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:30 GMT
USER kong
# Wed, 01 Apr 2026 20:14:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:30 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:30 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0f93b1600f51f35d2e4f16f435c0eae991ae3207099f32944f1a59eca3f02`  
		Last Modified: Wed, 01 Apr 2026 20:14:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03345cb8ad5a1b9dba9c17f18121108fd767403cb32c794498814456bc5f44`  
		Last Modified: Wed, 01 Apr 2026 20:14:44 GMT  
		Size: 62.7 MB (62740103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf31bee8faee2e311ae8d8d4cd90e193cb51041b05429732e08a3b5e12831f2`  
		Last Modified: Wed, 01 Apr 2026 20:14:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:3b5c35531c54934e1f8b676a22f259a9afd755accb23936ea3a04c499f63a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a39359cd7dccddd0d7e1d2c9827d0002588ccc29437f6d4a07afaafeb44e9f`

```dockerfile
```

-	Layers:
	-	`sha256:325ec8256a448659f0d7e504c80b61251f05d51f05c322af75225bf79ece857f`  
		Last Modified: Wed, 01 Apr 2026 20:14:43 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48480493ef513f5de975459bb0a1696beca604ffbb2dbba8c79bc26c1607b14f`  
		Last Modified: Wed, 01 Apr 2026 20:14:42 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:30ea8c38f2e23f0a96052e14cf7141502728af07be960605a5ccf1069d45ba8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88813294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514d239172b1fe4d5f871680264b1d8cda1deb2a127040ba62348393c94187c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:25 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:25 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:25 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:13:25 GMT
ENV KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 01 Apr 2026 20:13:53 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:13:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:53 GMT
USER kong
# Wed, 01 Apr 2026 20:13:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:53 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:13:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:13:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:13:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ff1f4ee4387a15937f4e200d6df6d164a58c0c80114d771d6cbbf85cf5c36`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46366e7b6a4b14e50f10b43f6384ba846d357e0614de0b5f51a71ce274092e`  
		Last Modified: Wed, 01 Apr 2026 20:14:11 GMT  
		Size: 61.2 MB (61205069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70aa1f5dad893096b75b3008765cdb8521730ab1cb9fba10a4a25ff2fe5e2db`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e21bbaa7ff4516c0aa2eb5c28827eccf499dd61fda903003e2051f0b765930b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efd1e3056b158957fe7e7a3aa72a13528715dae7c6a01dac18b840e31c77d36`

```dockerfile
```

-	Layers:
	-	`sha256:eb4849b97c13ccd56ff776bf4b171cc7a8eb6cbb1fb2de0f1fa091cf15443c06`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d10b52305ebd2a220f7ae09f2645ecf249a543f4180cc1eb5ab73ec80810a29`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:ba47cd06209799c05d98c18c0b35259bc7d8debf48b303dfe8866670aef93963
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:916d8e66c48938a02ca197163ead84108eae0719f1521d9708f05f00f62745d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92477799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cd4d6ff51b583cdf2bd8ab6042b7dfe1a1010de22943e44d1090a5a7025005`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:14:09 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:14:09 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:14:09 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:14:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:14:09 GMT
ENV KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 01 Apr 2026 20:14:30 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:30 GMT
USER kong
# Wed, 01 Apr 2026 20:14:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:30 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:30 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0f93b1600f51f35d2e4f16f435c0eae991ae3207099f32944f1a59eca3f02`  
		Last Modified: Wed, 01 Apr 2026 20:14:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03345cb8ad5a1b9dba9c17f18121108fd767403cb32c794498814456bc5f44`  
		Last Modified: Wed, 01 Apr 2026 20:14:44 GMT  
		Size: 62.7 MB (62740103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf31bee8faee2e311ae8d8d4cd90e193cb51041b05429732e08a3b5e12831f2`  
		Last Modified: Wed, 01 Apr 2026 20:14:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:3b5c35531c54934e1f8b676a22f259a9afd755accb23936ea3a04c499f63a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a39359cd7dccddd0d7e1d2c9827d0002588ccc29437f6d4a07afaafeb44e9f`

```dockerfile
```

-	Layers:
	-	`sha256:325ec8256a448659f0d7e504c80b61251f05d51f05c322af75225bf79ece857f`  
		Last Modified: Wed, 01 Apr 2026 20:14:43 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48480493ef513f5de975459bb0a1696beca604ffbb2dbba8c79bc26c1607b14f`  
		Last Modified: Wed, 01 Apr 2026 20:14:42 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:30ea8c38f2e23f0a96052e14cf7141502728af07be960605a5ccf1069d45ba8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88813294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514d239172b1fe4d5f871680264b1d8cda1deb2a127040ba62348393c94187c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:25 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:25 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:25 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:13:25 GMT
ENV KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 01 Apr 2026 20:13:53 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:13:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:53 GMT
USER kong
# Wed, 01 Apr 2026 20:13:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:53 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:13:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:13:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:13:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ff1f4ee4387a15937f4e200d6df6d164a58c0c80114d771d6cbbf85cf5c36`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46366e7b6a4b14e50f10b43f6384ba846d357e0614de0b5f51a71ce274092e`  
		Last Modified: Wed, 01 Apr 2026 20:14:11 GMT  
		Size: 61.2 MB (61205069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70aa1f5dad893096b75b3008765cdb8521730ab1cb9fba10a4a25ff2fe5e2db`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:e21bbaa7ff4516c0aa2eb5c28827eccf499dd61fda903003e2051f0b765930b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efd1e3056b158957fe7e7a3aa72a13528715dae7c6a01dac18b840e31c77d36`

```dockerfile
```

-	Layers:
	-	`sha256:eb4849b97c13ccd56ff776bf4b171cc7a8eb6cbb1fb2de0f1fa091cf15443c06`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d10b52305ebd2a220f7ae09f2645ecf249a543f4180cc1eb5ab73ec80810a29`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:ba47cd06209799c05d98c18c0b35259bc7d8debf48b303dfe8866670aef93963
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:916d8e66c48938a02ca197163ead84108eae0719f1521d9708f05f00f62745d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92477799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75cd4d6ff51b583cdf2bd8ab6042b7dfe1a1010de22943e44d1090a5a7025005`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:14:09 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:14:09 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:14:09 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:14:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:14:09 GMT
ENV KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 01 Apr 2026 20:14:09 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 01 Apr 2026 20:14:30 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:30 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:30 GMT
USER kong
# Wed, 01 Apr 2026 20:14:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:30 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:30 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0f93b1600f51f35d2e4f16f435c0eae991ae3207099f32944f1a59eca3f02`  
		Last Modified: Wed, 01 Apr 2026 20:14:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03345cb8ad5a1b9dba9c17f18121108fd767403cb32c794498814456bc5f44`  
		Last Modified: Wed, 01 Apr 2026 20:14:44 GMT  
		Size: 62.7 MB (62740103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf31bee8faee2e311ae8d8d4cd90e193cb51041b05429732e08a3b5e12831f2`  
		Last Modified: Wed, 01 Apr 2026 20:14:43 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:3b5c35531c54934e1f8b676a22f259a9afd755accb23936ea3a04c499f63a487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a39359cd7dccddd0d7e1d2c9827d0002588ccc29437f6d4a07afaafeb44e9f`

```dockerfile
```

-	Layers:
	-	`sha256:325ec8256a448659f0d7e504c80b61251f05d51f05c322af75225bf79ece857f`  
		Last Modified: Wed, 01 Apr 2026 20:14:43 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48480493ef513f5de975459bb0a1696beca604ffbb2dbba8c79bc26c1607b14f`  
		Last Modified: Wed, 01 Apr 2026 20:14:42 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:30ea8c38f2e23f0a96052e14cf7141502728af07be960605a5ccf1069d45ba8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88813294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f514d239172b1fe4d5f871680264b1d8cda1deb2a127040ba62348393c94187c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:25 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:25 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:25 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:25 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:25 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:13:25 GMT
ENV KONG_VERSION=3.4.2
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 01 Apr 2026 20:13:25 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Wed, 01 Apr 2026 20:13:53 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:13:53 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:53 GMT
USER kong
# Wed, 01 Apr 2026 20:13:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:53 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:13:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:13:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:13:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7ff1f4ee4387a15937f4e200d6df6d164a58c0c80114d771d6cbbf85cf5c36`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c46366e7b6a4b14e50f10b43f6384ba846d357e0614de0b5f51a71ce274092e`  
		Last Modified: Wed, 01 Apr 2026 20:14:11 GMT  
		Size: 61.2 MB (61205069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70aa1f5dad893096b75b3008765cdb8521730ab1cb9fba10a4a25ff2fe5e2db`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e21bbaa7ff4516c0aa2eb5c28827eccf499dd61fda903003e2051f0b765930b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9efd1e3056b158957fe7e7a3aa72a13528715dae7c6a01dac18b840e31c77d36`

```dockerfile
```

-	Layers:
	-	`sha256:eb4849b97c13ccd56ff776bf4b171cc7a8eb6cbb1fb2de0f1fa091cf15443c06`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d10b52305ebd2a220f7ae09f2645ecf249a543f4180cc1eb5ab73ec80810a29`  
		Last Modified: Wed, 01 Apr 2026 20:14:08 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:82ec6c65d9cc9a141edf6b495ff7fde1f59c8db8faf1735a7a2d281123cc1f98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:9b3cbd8cfa5b309a2948959f9ea90807130918bf9223ebaa6540f87d5ca5c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117753775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d244023f87306630b9c829bfaa4573d1fd90dcfbcc1acae8ad0b0a94aa10ba84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:59 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:59 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:59 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:59 GMT
ENV KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 01 Apr 2026 20:14:23 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:23 GMT
USER kong
# Wed, 01 Apr 2026 20:14:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:23 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296efd687e82e2f42d7c582cbe3bc5ecc1b517c0aa58c798bd212c2165dbe98a`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fb7d86b978f02000d1430b42a18ecdab3b8efc00133918be6e4fa84d858075`  
		Last Modified: Wed, 01 Apr 2026 20:14:49 GMT  
		Size: 88.0 MB (88016081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a7e32711b5e4d4d02976a78ef444e2e9b528ecef39b040368eb6c92f6fee0`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:11f49d94b5b490c1c60f4fe9b681ad5a3c3837faf16a6bcb934c946b143c8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1827beaf9065457177e62a941266786d0634340a16686cf57de5ba5cad88e212`

```dockerfile
```

-	Layers:
	-	`sha256:39491e022a2b04d09d589d466d15a564aedf1f89144e060c91394cbc0c0e0309`  
		Last Modified: Wed, 01 Apr 2026 20:14:41 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f74c5ba5d144f6d7a90fb7747429309b15c7781d33e39a1f318a2bc3a4f31d`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b31f375f49e750b3db1f4d69955950af12027969fbe218f47f32ecbdb92cb02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114931706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7508fc218b5f0c4211863ea84f2c2829aa41c6606bb2bbd7e226e118af25306`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:09 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:09 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:09 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:09 GMT
ENV KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 01 Apr 2026 20:13:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:13:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:38 GMT
USER kong
# Wed, 01 Apr 2026 20:13:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:13:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:13:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:13:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ba2cba94ce9a8cc3e6aeddc3e1cbc12fb81602ee981c8a4da20425e3f1c16d`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b94f0c6b61b2ea7db565b3971fb1faa978555cd9276008d53fe68e15e5a8f6`  
		Last Modified: Wed, 01 Apr 2026 20:13:59 GMT  
		Size: 87.3 MB (87323482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb807a01458454207135599d1181bec0b9ed0944c241239ead40e83dc7f545a9`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:1df75bc0eb2e44dccfd5263377eea232f147a968b81e18e914ad4b3264176fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94c7fb7a0d95e75c769cd027947a24a99334fdc48b0d31d70fc771095e9b871`

```dockerfile
```

-	Layers:
	-	`sha256:3cc8058d79c948d9e329aea62726509982d14b2c9993ef974bcfb6204fcae81f`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517a935b618392ae4bbd129431ac9f358aec54be4aff2d9ba83a706a6c8f892d`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 15.4 KB (15449 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:82ec6c65d9cc9a141edf6b495ff7fde1f59c8db8faf1735a7a2d281123cc1f98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9b3cbd8cfa5b309a2948959f9ea90807130918bf9223ebaa6540f87d5ca5c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117753775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d244023f87306630b9c829bfaa4573d1fd90dcfbcc1acae8ad0b0a94aa10ba84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:59 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:59 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:59 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:59 GMT
ENV KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 01 Apr 2026 20:14:23 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:23 GMT
USER kong
# Wed, 01 Apr 2026 20:14:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:23 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296efd687e82e2f42d7c582cbe3bc5ecc1b517c0aa58c798bd212c2165dbe98a`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fb7d86b978f02000d1430b42a18ecdab3b8efc00133918be6e4fa84d858075`  
		Last Modified: Wed, 01 Apr 2026 20:14:49 GMT  
		Size: 88.0 MB (88016081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a7e32711b5e4d4d02976a78ef444e2e9b528ecef39b040368eb6c92f6fee0`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:11f49d94b5b490c1c60f4fe9b681ad5a3c3837faf16a6bcb934c946b143c8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1827beaf9065457177e62a941266786d0634340a16686cf57de5ba5cad88e212`

```dockerfile
```

-	Layers:
	-	`sha256:39491e022a2b04d09d589d466d15a564aedf1f89144e060c91394cbc0c0e0309`  
		Last Modified: Wed, 01 Apr 2026 20:14:41 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f74c5ba5d144f6d7a90fb7747429309b15c7781d33e39a1f318a2bc3a4f31d`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b31f375f49e750b3db1f4d69955950af12027969fbe218f47f32ecbdb92cb02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114931706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7508fc218b5f0c4211863ea84f2c2829aa41c6606bb2bbd7e226e118af25306`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:09 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:09 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:09 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:09 GMT
ENV KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 01 Apr 2026 20:13:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:13:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:38 GMT
USER kong
# Wed, 01 Apr 2026 20:13:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:13:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:13:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:13:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ba2cba94ce9a8cc3e6aeddc3e1cbc12fb81602ee981c8a4da20425e3f1c16d`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b94f0c6b61b2ea7db565b3971fb1faa978555cd9276008d53fe68e15e5a8f6`  
		Last Modified: Wed, 01 Apr 2026 20:13:59 GMT  
		Size: 87.3 MB (87323482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb807a01458454207135599d1181bec0b9ed0944c241239ead40e83dc7f545a9`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1df75bc0eb2e44dccfd5263377eea232f147a968b81e18e914ad4b3264176fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94c7fb7a0d95e75c769cd027947a24a99334fdc48b0d31d70fc771095e9b871`

```dockerfile
```

-	Layers:
	-	`sha256:3cc8058d79c948d9e329aea62726509982d14b2c9993ef974bcfb6204fcae81f`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517a935b618392ae4bbd129431ac9f358aec54be4aff2d9ba83a706a6c8f892d`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 15.4 KB (15449 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:82ec6c65d9cc9a141edf6b495ff7fde1f59c8db8faf1735a7a2d281123cc1f98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:9b3cbd8cfa5b309a2948959f9ea90807130918bf9223ebaa6540f87d5ca5c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117753775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d244023f87306630b9c829bfaa4573d1fd90dcfbcc1acae8ad0b0a94aa10ba84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:59 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:59 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:59 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:59 GMT
ENV KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 01 Apr 2026 20:14:23 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:23 GMT
USER kong
# Wed, 01 Apr 2026 20:14:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:23 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296efd687e82e2f42d7c582cbe3bc5ecc1b517c0aa58c798bd212c2165dbe98a`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fb7d86b978f02000d1430b42a18ecdab3b8efc00133918be6e4fa84d858075`  
		Last Modified: Wed, 01 Apr 2026 20:14:49 GMT  
		Size: 88.0 MB (88016081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a7e32711b5e4d4d02976a78ef444e2e9b528ecef39b040368eb6c92f6fee0`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:11f49d94b5b490c1c60f4fe9b681ad5a3c3837faf16a6bcb934c946b143c8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1827beaf9065457177e62a941266786d0634340a16686cf57de5ba5cad88e212`

```dockerfile
```

-	Layers:
	-	`sha256:39491e022a2b04d09d589d466d15a564aedf1f89144e060c91394cbc0c0e0309`  
		Last Modified: Wed, 01 Apr 2026 20:14:41 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f74c5ba5d144f6d7a90fb7747429309b15c7781d33e39a1f318a2bc3a4f31d`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b31f375f49e750b3db1f4d69955950af12027969fbe218f47f32ecbdb92cb02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114931706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7508fc218b5f0c4211863ea84f2c2829aa41c6606bb2bbd7e226e118af25306`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:09 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:09 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:09 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:09 GMT
ENV KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 01 Apr 2026 20:13:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:13:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:38 GMT
USER kong
# Wed, 01 Apr 2026 20:13:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:13:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:13:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:13:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ba2cba94ce9a8cc3e6aeddc3e1cbc12fb81602ee981c8a4da20425e3f1c16d`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b94f0c6b61b2ea7db565b3971fb1faa978555cd9276008d53fe68e15e5a8f6`  
		Last Modified: Wed, 01 Apr 2026 20:13:59 GMT  
		Size: 87.3 MB (87323482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb807a01458454207135599d1181bec0b9ed0944c241239ead40e83dc7f545a9`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:1df75bc0eb2e44dccfd5263377eea232f147a968b81e18e914ad4b3264176fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94c7fb7a0d95e75c769cd027947a24a99334fdc48b0d31d70fc771095e9b871`

```dockerfile
```

-	Layers:
	-	`sha256:3cc8058d79c948d9e329aea62726509982d14b2c9993ef974bcfb6204fcae81f`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517a935b618392ae4bbd129431ac9f358aec54be4aff2d9ba83a706a6c8f892d`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 15.4 KB (15449 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:82ec6c65d9cc9a141edf6b495ff7fde1f59c8db8faf1735a7a2d281123cc1f98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9b3cbd8cfa5b309a2948959f9ea90807130918bf9223ebaa6540f87d5ca5c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117753775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d244023f87306630b9c829bfaa4573d1fd90dcfbcc1acae8ad0b0a94aa10ba84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:59 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:59 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:59 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:59 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:59 GMT
ENV KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 01 Apr 2026 20:13:59 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 01 Apr 2026 20:14:23 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:14:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:14:23 GMT
USER kong
# Wed, 01 Apr 2026 20:14:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:14:23 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:14:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:14:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:14:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296efd687e82e2f42d7c582cbe3bc5ecc1b517c0aa58c798bd212c2165dbe98a`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fb7d86b978f02000d1430b42a18ecdab3b8efc00133918be6e4fa84d858075`  
		Last Modified: Wed, 01 Apr 2026 20:14:49 GMT  
		Size: 88.0 MB (88016081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a7e32711b5e4d4d02976a78ef444e2e9b528ecef39b040368eb6c92f6fee0`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:11f49d94b5b490c1c60f4fe9b681ad5a3c3837faf16a6bcb934c946b143c8fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1827beaf9065457177e62a941266786d0634340a16686cf57de5ba5cad88e212`

```dockerfile
```

-	Layers:
	-	`sha256:39491e022a2b04d09d589d466d15a564aedf1f89144e060c91394cbc0c0e0309`  
		Last Modified: Wed, 01 Apr 2026 20:14:41 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9f74c5ba5d144f6d7a90fb7747429309b15c7781d33e39a1f318a2bc3a4f31d`  
		Last Modified: Wed, 01 Apr 2026 20:14:40 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b31f375f49e750b3db1f4d69955950af12027969fbe218f47f32ecbdb92cb02a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114931706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7508fc218b5f0c4211863ea84f2c2829aa41c6606bb2bbd7e226e118af25306`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:13:09 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Apr 2026 20:13:09 GMT
ARG ASSET=ce
# Wed, 01 Apr 2026 20:13:09 GMT
ENV ASSET=ce
# Wed, 01 Apr 2026 20:13:09 GMT
ARG EE_PORTS
# Wed, 01 Apr 2026 20:13:09 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:09 GMT
ENV KONG_VERSION=3.8.0
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Wed, 01 Apr 2026 20:13:09 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Wed, 01 Apr 2026 20:13:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 01 Apr 2026 20:13:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 01 Apr 2026 20:13:38 GMT
USER kong
# Wed, 01 Apr 2026 20:13:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Apr 2026 20:13:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 01 Apr 2026 20:13:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Apr 2026 20:13:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 01 Apr 2026 20:13:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ba2cba94ce9a8cc3e6aeddc3e1cbc12fb81602ee981c8a4da20425e3f1c16d`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b94f0c6b61b2ea7db565b3971fb1faa978555cd9276008d53fe68e15e5a8f6`  
		Last Modified: Wed, 01 Apr 2026 20:13:59 GMT  
		Size: 87.3 MB (87323482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb807a01458454207135599d1181bec0b9ed0944c241239ead40e83dc7f545a9`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1df75bc0eb2e44dccfd5263377eea232f147a968b81e18e914ad4b3264176fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94c7fb7a0d95e75c769cd027947a24a99334fdc48b0d31d70fc771095e9b871`

```dockerfile
```

-	Layers:
	-	`sha256:3cc8058d79c948d9e329aea62726509982d14b2c9993ef974bcfb6204fcae81f`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517a935b618392ae4bbd129431ac9f358aec54be4aff2d9ba83a706a6c8f892d`  
		Last Modified: Wed, 01 Apr 2026 20:13:55 GMT  
		Size: 15.4 KB (15449 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:7512bfa30d96709a9dede46c723b2c57b6fa61f4cbb797adf20f531d3e0266dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:7563df2ddf4938b826c8828da28572f7b9357cfb3e8607b36a15cc35b856aca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2620abfb8871e7741f3e10db56b83cd5866367f45e243bc97c8f022e6c0c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:20 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:20 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:20 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:39:48 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
USER kong
# Tue, 17 Mar 2026 01:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:48 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b43afd99cb1203273e3bf6cf9b42857ba2355f5218c924a310bb7cc21184d`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66038258e40a0a1302df60f6410f0c82d3c0a43ccdba69f6950f09b7b7183de`  
		Last Modified: Tue, 17 Mar 2026 01:40:06 GMT  
		Size: 90.7 MB (90692231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba581d5adf0d98b835dd239b1c96ffdd837857bf5edb85cded35a47599956b73`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:979493665a8c528d1ac6d8b09d4615e29ea99d54c8095f1dde79d97f4c23bf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032be33683199b1c6e5692ccc4a41859009748bdf9b2c2f1161e87f6b87cb78c`

```dockerfile
```

-	Layers:
	-	`sha256:a04da651e31999b82bc9ff0460696c27e540ff645a7a286aa79d22963a043a23`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f3b4a93fdf3e687cc0a5905662a0d66a4e3bacd30e4a3255d9bb1790ab74d2`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1aaf7b21ff8387489cf1b23d764542096d331bd4ee7b2f350c738f9f36a33f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118874339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f61ecab8cf35cae09475709dc7ce6868ce664b44dff3ca7a3773a024d79c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:54 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:54 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:41:26 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
USER kong
# Tue, 17 Mar 2026 01:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:26 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b0661171bf34ea182c4e15a6bb8a7d6d1ef8274654ab456a592bf8d0e3f86`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a2506e0b2a1fe740de635e019f70b67d1450fed67c72860d884dbdcfc9390`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 90.0 MB (90003339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19699203c06695b4414f10615cc9237f953cc008b634e414a6f7def3263272d1`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:e6595103d2d89e7d0d86dd80de606a32733854c43355997e16831f6ad77f4d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5124e3c50603a880744ccf9b4cb8457613d76b8a1abaad819fc4dca2ad9180`

```dockerfile
```

-	Layers:
	-	`sha256:d167aca56ef2576e465b7aae50c65e6a10e1cb455246a1804140c6d76477a4ec`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a4032d566877433146b7ecd07c9f2f4a77e4789acaf445e036761d56a1108c`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:7512bfa30d96709a9dede46c723b2c57b6fa61f4cbb797adf20f531d3e0266dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7563df2ddf4938b826c8828da28572f7b9357cfb3e8607b36a15cc35b856aca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2620abfb8871e7741f3e10db56b83cd5866367f45e243bc97c8f022e6c0c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:20 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:20 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:20 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:39:48 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
USER kong
# Tue, 17 Mar 2026 01:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:48 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b43afd99cb1203273e3bf6cf9b42857ba2355f5218c924a310bb7cc21184d`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66038258e40a0a1302df60f6410f0c82d3c0a43ccdba69f6950f09b7b7183de`  
		Last Modified: Tue, 17 Mar 2026 01:40:06 GMT  
		Size: 90.7 MB (90692231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba581d5adf0d98b835dd239b1c96ffdd837857bf5edb85cded35a47599956b73`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:979493665a8c528d1ac6d8b09d4615e29ea99d54c8095f1dde79d97f4c23bf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032be33683199b1c6e5692ccc4a41859009748bdf9b2c2f1161e87f6b87cb78c`

```dockerfile
```

-	Layers:
	-	`sha256:a04da651e31999b82bc9ff0460696c27e540ff645a7a286aa79d22963a043a23`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f3b4a93fdf3e687cc0a5905662a0d66a4e3bacd30e4a3255d9bb1790ab74d2`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1aaf7b21ff8387489cf1b23d764542096d331bd4ee7b2f350c738f9f36a33f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118874339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f61ecab8cf35cae09475709dc7ce6868ce664b44dff3ca7a3773a024d79c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:54 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:54 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:41:26 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
USER kong
# Tue, 17 Mar 2026 01:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:26 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b0661171bf34ea182c4e15a6bb8a7d6d1ef8274654ab456a592bf8d0e3f86`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a2506e0b2a1fe740de635e019f70b67d1450fed67c72860d884dbdcfc9390`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 90.0 MB (90003339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19699203c06695b4414f10615cc9237f953cc008b634e414a6f7def3263272d1`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e6595103d2d89e7d0d86dd80de606a32733854c43355997e16831f6ad77f4d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5124e3c50603a880744ccf9b4cb8457613d76b8a1abaad819fc4dca2ad9180`

```dockerfile
```

-	Layers:
	-	`sha256:d167aca56ef2576e465b7aae50c65e6a10e1cb455246a1804140c6d76477a4ec`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a4032d566877433146b7ecd07c9f2f4a77e4789acaf445e036761d56a1108c`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:7512bfa30d96709a9dede46c723b2c57b6fa61f4cbb797adf20f531d3e0266dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:7563df2ddf4938b826c8828da28572f7b9357cfb3e8607b36a15cc35b856aca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2620abfb8871e7741f3e10db56b83cd5866367f45e243bc97c8f022e6c0c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:20 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:20 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:20 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:39:48 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
USER kong
# Tue, 17 Mar 2026 01:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:48 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b43afd99cb1203273e3bf6cf9b42857ba2355f5218c924a310bb7cc21184d`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66038258e40a0a1302df60f6410f0c82d3c0a43ccdba69f6950f09b7b7183de`  
		Last Modified: Tue, 17 Mar 2026 01:40:06 GMT  
		Size: 90.7 MB (90692231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba581d5adf0d98b835dd239b1c96ffdd837857bf5edb85cded35a47599956b73`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:979493665a8c528d1ac6d8b09d4615e29ea99d54c8095f1dde79d97f4c23bf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032be33683199b1c6e5692ccc4a41859009748bdf9b2c2f1161e87f6b87cb78c`

```dockerfile
```

-	Layers:
	-	`sha256:a04da651e31999b82bc9ff0460696c27e540ff645a7a286aa79d22963a043a23`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f3b4a93fdf3e687cc0a5905662a0d66a4e3bacd30e4a3255d9bb1790ab74d2`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1aaf7b21ff8387489cf1b23d764542096d331bd4ee7b2f350c738f9f36a33f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118874339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f61ecab8cf35cae09475709dc7ce6868ce664b44dff3ca7a3773a024d79c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:54 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:54 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:41:26 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
USER kong
# Tue, 17 Mar 2026 01:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:26 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b0661171bf34ea182c4e15a6bb8a7d6d1ef8274654ab456a592bf8d0e3f86`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a2506e0b2a1fe740de635e019f70b67d1450fed67c72860d884dbdcfc9390`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 90.0 MB (90003339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19699203c06695b4414f10615cc9237f953cc008b634e414a6f7def3263272d1`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:e6595103d2d89e7d0d86dd80de606a32733854c43355997e16831f6ad77f4d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5124e3c50603a880744ccf9b4cb8457613d76b8a1abaad819fc4dca2ad9180`

```dockerfile
```

-	Layers:
	-	`sha256:d167aca56ef2576e465b7aae50c65e6a10e1cb455246a1804140c6d76477a4ec`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a4032d566877433146b7ecd07c9f2f4a77e4789acaf445e036761d56a1108c`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:7512bfa30d96709a9dede46c723b2c57b6fa61f4cbb797adf20f531d3e0266dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7563df2ddf4938b826c8828da28572f7b9357cfb3e8607b36a15cc35b856aca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2620abfb8871e7741f3e10db56b83cd5866367f45e243bc97c8f022e6c0c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:20 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:20 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:20 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:39:48 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
USER kong
# Tue, 17 Mar 2026 01:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:48 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b43afd99cb1203273e3bf6cf9b42857ba2355f5218c924a310bb7cc21184d`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66038258e40a0a1302df60f6410f0c82d3c0a43ccdba69f6950f09b7b7183de`  
		Last Modified: Tue, 17 Mar 2026 01:40:06 GMT  
		Size: 90.7 MB (90692231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba581d5adf0d98b835dd239b1c96ffdd837857bf5edb85cded35a47599956b73`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:979493665a8c528d1ac6d8b09d4615e29ea99d54c8095f1dde79d97f4c23bf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032be33683199b1c6e5692ccc4a41859009748bdf9b2c2f1161e87f6b87cb78c`

```dockerfile
```

-	Layers:
	-	`sha256:a04da651e31999b82bc9ff0460696c27e540ff645a7a286aa79d22963a043a23`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f3b4a93fdf3e687cc0a5905662a0d66a4e3bacd30e4a3255d9bb1790ab74d2`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1aaf7b21ff8387489cf1b23d764542096d331bd4ee7b2f350c738f9f36a33f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118874339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f61ecab8cf35cae09475709dc7ce6868ce664b44dff3ca7a3773a024d79c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:54 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:54 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:41:26 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
USER kong
# Tue, 17 Mar 2026 01:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:26 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b0661171bf34ea182c4e15a6bb8a7d6d1ef8274654ab456a592bf8d0e3f86`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a2506e0b2a1fe740de635e019f70b67d1450fed67c72860d884dbdcfc9390`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 90.0 MB (90003339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19699203c06695b4414f10615cc9237f953cc008b634e414a6f7def3263272d1`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e6595103d2d89e7d0d86dd80de606a32733854c43355997e16831f6ad77f4d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5124e3c50603a880744ccf9b4cb8457613d76b8a1abaad819fc4dca2ad9180`

```dockerfile
```

-	Layers:
	-	`sha256:d167aca56ef2576e465b7aae50c65e6a10e1cb455246a1804140c6d76477a4ec`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a4032d566877433146b7ecd07c9f2f4a77e4789acaf445e036761d56a1108c`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:7512bfa30d96709a9dede46c723b2c57b6fa61f4cbb797adf20f531d3e0266dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:7563df2ddf4938b826c8828da28572f7b9357cfb3e8607b36a15cc35b856aca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2620abfb8871e7741f3e10db56b83cd5866367f45e243bc97c8f022e6c0c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:20 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:20 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:20 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:39:48 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
USER kong
# Tue, 17 Mar 2026 01:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:48 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b43afd99cb1203273e3bf6cf9b42857ba2355f5218c924a310bb7cc21184d`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66038258e40a0a1302df60f6410f0c82d3c0a43ccdba69f6950f09b7b7183de`  
		Last Modified: Tue, 17 Mar 2026 01:40:06 GMT  
		Size: 90.7 MB (90692231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba581d5adf0d98b835dd239b1c96ffdd837857bf5edb85cded35a47599956b73`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:979493665a8c528d1ac6d8b09d4615e29ea99d54c8095f1dde79d97f4c23bf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032be33683199b1c6e5692ccc4a41859009748bdf9b2c2f1161e87f6b87cb78c`

```dockerfile
```

-	Layers:
	-	`sha256:a04da651e31999b82bc9ff0460696c27e540ff645a7a286aa79d22963a043a23`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f3b4a93fdf3e687cc0a5905662a0d66a4e3bacd30e4a3255d9bb1790ab74d2`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1aaf7b21ff8387489cf1b23d764542096d331bd4ee7b2f350c738f9f36a33f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118874339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f61ecab8cf35cae09475709dc7ce6868ce664b44dff3ca7a3773a024d79c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:54 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:54 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:41:26 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
USER kong
# Tue, 17 Mar 2026 01:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:26 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b0661171bf34ea182c4e15a6bb8a7d6d1ef8274654ab456a592bf8d0e3f86`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a2506e0b2a1fe740de635e019f70b67d1450fed67c72860d884dbdcfc9390`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 90.0 MB (90003339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19699203c06695b4414f10615cc9237f953cc008b634e414a6f7def3263272d1`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:e6595103d2d89e7d0d86dd80de606a32733854c43355997e16831f6ad77f4d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5124e3c50603a880744ccf9b4cb8457613d76b8a1abaad819fc4dca2ad9180`

```dockerfile
```

-	Layers:
	-	`sha256:d167aca56ef2576e465b7aae50c65e6a10e1cb455246a1804140c6d76477a4ec`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a4032d566877433146b7ecd07c9f2f4a77e4789acaf445e036761d56a1108c`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:7512bfa30d96709a9dede46c723b2c57b6fa61f4cbb797adf20f531d3e0266dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:7563df2ddf4938b826c8828da28572f7b9357cfb3e8607b36a15cc35b856aca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120425515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c2620abfb8871e7741f3e10db56b83cd5866367f45e243bc97c8f022e6c0c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:20 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:20 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:20 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:20 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:39:20 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:39:48 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:48 GMT
USER kong
# Tue, 17 Mar 2026 01:39:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:48 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:48 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b43afd99cb1203273e3bf6cf9b42857ba2355f5218c924a310bb7cc21184d`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66038258e40a0a1302df60f6410f0c82d3c0a43ccdba69f6950f09b7b7183de`  
		Last Modified: Tue, 17 Mar 2026 01:40:06 GMT  
		Size: 90.7 MB (90692231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba581d5adf0d98b835dd239b1c96ffdd837857bf5edb85cded35a47599956b73`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:979493665a8c528d1ac6d8b09d4615e29ea99d54c8095f1dde79d97f4c23bf13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032be33683199b1c6e5692ccc4a41859009748bdf9b2c2f1161e87f6b87cb78c`

```dockerfile
```

-	Layers:
	-	`sha256:a04da651e31999b82bc9ff0460696c27e540ff645a7a286aa79d22963a043a23`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 5.4 MB (5421158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5f3b4a93fdf3e687cc0a5905662a0d66a4e3bacd30e4a3255d9bb1790ab74d2`  
		Last Modified: Tue, 17 Mar 2026 01:40:04 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1aaf7b21ff8387489cf1b23d764542096d331bd4ee7b2f350c738f9f36a33f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118874339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257f61ecab8cf35cae09475709dc7ce6868ce664b44dff3ca7a3773a024d79c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:54 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:54 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:54 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:54 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ENV KONG_VERSION=3.9.1
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 17 Mar 2026 01:40:54 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 17 Mar 2026 01:41:26 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:26 GMT
USER kong
# Tue, 17 Mar 2026 01:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:26 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b0661171bf34ea182c4e15a6bb8a7d6d1ef8274654ab456a592bf8d0e3f86`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639a2506e0b2a1fe740de635e019f70b67d1450fed67c72860d884dbdcfc9390`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 90.0 MB (90003339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19699203c06695b4414f10615cc9237f953cc008b634e414a6f7def3263272d1`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e6595103d2d89e7d0d86dd80de606a32733854c43355997e16831f6ad77f4d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5124e3c50603a880744ccf9b4cb8457613d76b8a1abaad819fc4dca2ad9180`

```dockerfile
```

-	Layers:
	-	`sha256:d167aca56ef2576e465b7aae50c65e6a10e1cb455246a1804140c6d76477a4ec`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5428325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a4032d566877433146b7ecd07c9f2f4a77e4789acaf445e036761d56a1108c`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json
