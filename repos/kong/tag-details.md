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
$ docker pull kong@sha256:6fffef4db83e7560db7969f05b804fa4602be257d6843736e0e366582e64844d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:263368f4dd1ae6a9cc4a9ef05fc0f8d3ec05a01f01a909ac109bd50885059b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186583068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4f6cf86e85552c0ab6f91b76eb7b75a9edde897726cd1460b36b00315ef2a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:49 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:49 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:49 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
ARG KONG_VERSION=2.8.5
# Tue, 17 Mar 2026 01:39:49 GMT
ENV KONG_VERSION=2.8.5
# Tue, 17 Mar 2026 01:39:49 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 17 Mar 2026 01:39:49 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 17 Mar 2026 01:40:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:40:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:25 GMT
USER kong
# Tue, 17 Mar 2026 01:40:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:40:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:40:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:40:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec507a0702e9298a409770cea7c5662dcfab9fd7b0533a596203b7320297cde4`  
		Last Modified: Tue, 17 Mar 2026 01:40:47 GMT  
		Size: 25.1 MB (25081974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d002de6689abcbe5d92ac5055a78714895cc373cab999146e93c4f7d392646b5`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 132.0 MB (131961692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc5ddf8300917fc3902bd067ea46ec96fb8f7b512ee08beaadaf0cc1eb76c36`  
		Last Modified: Tue, 17 Mar 2026 01:40:45 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d2f65417276a0d8c42355d5304f07e2faadeac3edbd9d761d6459b89a827fe98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd7093a4dab50111bbc43bfed58c1ae448bb849a41722d3e7c724e31b53f978`

```dockerfile
```

-	Layers:
	-	`sha256:e5ce5022d2e1b915ad990f3d185222aced17c079de55646b590d45fdf81abf88`  
		Last Modified: Tue, 17 Mar 2026 01:40:46 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:346fdef571473196fc4e7e642ade0a3402adb5cf982b12e5c8f6c0c2831f44b2`  
		Last Modified: Tue, 17 Mar 2026 01:40:45 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:6fffef4db83e7560db7969f05b804fa4602be257d6843736e0e366582e64844d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:263368f4dd1ae6a9cc4a9ef05fc0f8d3ec05a01f01a909ac109bd50885059b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186583068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4f6cf86e85552c0ab6f91b76eb7b75a9edde897726cd1460b36b00315ef2a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:49 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:49 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:49 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
ARG KONG_VERSION=2.8.5
# Tue, 17 Mar 2026 01:39:49 GMT
ENV KONG_VERSION=2.8.5
# Tue, 17 Mar 2026 01:39:49 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 17 Mar 2026 01:39:49 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 17 Mar 2026 01:40:25 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:40:25 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:25 GMT
USER kong
# Tue, 17 Mar 2026 01:40:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:25 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:40:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:40:25 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:40:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec507a0702e9298a409770cea7c5662dcfab9fd7b0533a596203b7320297cde4`  
		Last Modified: Tue, 17 Mar 2026 01:40:47 GMT  
		Size: 25.1 MB (25081974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d002de6689abcbe5d92ac5055a78714895cc373cab999146e93c4f7d392646b5`  
		Last Modified: Tue, 17 Mar 2026 01:40:49 GMT  
		Size: 132.0 MB (131961692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc5ddf8300917fc3902bd067ea46ec96fb8f7b512ee08beaadaf0cc1eb76c36`  
		Last Modified: Tue, 17 Mar 2026 01:40:45 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d2f65417276a0d8c42355d5304f07e2faadeac3edbd9d761d6459b89a827fe98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd7093a4dab50111bbc43bfed58c1ae448bb849a41722d3e7c724e31b53f978`

```dockerfile
```

-	Layers:
	-	`sha256:e5ce5022d2e1b915ad990f3d185222aced17c079de55646b590d45fdf81abf88`  
		Last Modified: Tue, 17 Mar 2026 01:40:46 GMT  
		Size: 7.3 MB (7347744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:346fdef571473196fc4e7e642ade0a3402adb5cf982b12e5c8f6c0c2831f44b2`  
		Last Modified: Tue, 17 Mar 2026 01:40:45 GMT  
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
$ docker pull kong@sha256:df947d7d10e16f321fd26fbed37836a162bd6a9168bd0e506f20e67411fdf01e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:59a37ca18d2580ad047bd91265e249c4145ed9df7ff1814707f2dc6b5a7fa51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92284121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f1f8afc56d793451170ef194b4c3b6391cb446777e4840b0deb3b6f90a3265`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:46 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:46 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:46 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:39:46 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Mar 2026 01:40:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:40:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:11 GMT
USER kong
# Tue, 17 Mar 2026 01:40:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:40:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:40:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:40:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8798b747f4662ab7b471f489fec0262fb1e6b6258b7f6c70d05b57cce1403d6d`  
		Last Modified: Tue, 17 Mar 2026 01:40:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bddbdf567adebb032ef05ceea3b332d66c4e780f9c41234817c4e018628a6ce`  
		Last Modified: Tue, 17 Mar 2026 01:40:27 GMT  
		Size: 62.7 MB (62744319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e358a1746fc119756cc6a7fb7d8fc91b2d9f9bc2d3a3c5eecad70ae509b3c`  
		Last Modified: Tue, 17 Mar 2026 01:40:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:131d60110ea24ab11e51389a4520edfcdbfe47a2701a508353961fe8281e3ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e54723fec1d1c04b22e1b2cd02e24c949e61f633d93b72f88cf9f22cb0c283`

```dockerfile
```

-	Layers:
	-	`sha256:b50f3b5a967f74d738b1849ddc97991e6bceee8282d734cb910d02a51ca6b9bd`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4ad318ba820c49d5443e152d95ca7d5cd66dbf801b20907b771852bd97e8ac`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:15b42219be422c2ac9ef163ae3f48f1caf47bc73f275ce4e84a98ed824402551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88600414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2c0c36f2067152969e4b33c308fa6c1ffb003a2a083f6227b715ccb2686228`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:49 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:49 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:49 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:40:49 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Mar 2026 01:41:23 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:23 GMT
USER kong
# Tue, 17 Mar 2026 01:41:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:23 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c161866d3e42bffbb83e4753ddfc391f58417a705ebcaf382a2e15e3fd3f37f`  
		Last Modified: Tue, 17 Mar 2026 01:41:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535161047479c5e046db48b280484c29233148bbdc0e11b2b81c5c715c49808f`  
		Last Modified: Tue, 17 Mar 2026 01:41:39 GMT  
		Size: 61.2 MB (61210109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e66ec645227bb9cb719d763ae4dc1a800e8343e765e4bcd99c89bf69f03fd`  
		Last Modified: Tue, 17 Mar 2026 01:41:37 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:271f9794c497bdaf632628a0f68e2060e7dbc8378b2402808f7999a5e1da9149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c53c2057a51d08cbad93abfb41d2462332ae5e64601feb7022cec9fd4abba9`

```dockerfile
```

-	Layers:
	-	`sha256:e0ce7d028e7cab7c5932e6df020ad4469e33ab5b0c60ca7b4242ec92a0fddd32`  
		Last Modified: Tue, 17 Mar 2026 01:41:38 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e425e3266060ba53ae33efc4412d6b29c084d8fdb13766212aea2ef4ba4f7a8e`  
		Last Modified: Tue, 17 Mar 2026 01:41:38 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:df947d7d10e16f321fd26fbed37836a162bd6a9168bd0e506f20e67411fdf01e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:59a37ca18d2580ad047bd91265e249c4145ed9df7ff1814707f2dc6b5a7fa51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92284121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f1f8afc56d793451170ef194b4c3b6391cb446777e4840b0deb3b6f90a3265`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:46 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:46 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:46 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:39:46 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Mar 2026 01:40:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:40:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:11 GMT
USER kong
# Tue, 17 Mar 2026 01:40:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:40:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:40:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:40:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8798b747f4662ab7b471f489fec0262fb1e6b6258b7f6c70d05b57cce1403d6d`  
		Last Modified: Tue, 17 Mar 2026 01:40:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bddbdf567adebb032ef05ceea3b332d66c4e780f9c41234817c4e018628a6ce`  
		Last Modified: Tue, 17 Mar 2026 01:40:27 GMT  
		Size: 62.7 MB (62744319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e358a1746fc119756cc6a7fb7d8fc91b2d9f9bc2d3a3c5eecad70ae509b3c`  
		Last Modified: Tue, 17 Mar 2026 01:40:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:131d60110ea24ab11e51389a4520edfcdbfe47a2701a508353961fe8281e3ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e54723fec1d1c04b22e1b2cd02e24c949e61f633d93b72f88cf9f22cb0c283`

```dockerfile
```

-	Layers:
	-	`sha256:b50f3b5a967f74d738b1849ddc97991e6bceee8282d734cb910d02a51ca6b9bd`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4ad318ba820c49d5443e152d95ca7d5cd66dbf801b20907b771852bd97e8ac`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:15b42219be422c2ac9ef163ae3f48f1caf47bc73f275ce4e84a98ed824402551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88600414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2c0c36f2067152969e4b33c308fa6c1ffb003a2a083f6227b715ccb2686228`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:49 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:49 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:49 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:40:49 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Mar 2026 01:41:23 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:23 GMT
USER kong
# Tue, 17 Mar 2026 01:41:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:23 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c161866d3e42bffbb83e4753ddfc391f58417a705ebcaf382a2e15e3fd3f37f`  
		Last Modified: Tue, 17 Mar 2026 01:41:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535161047479c5e046db48b280484c29233148bbdc0e11b2b81c5c715c49808f`  
		Last Modified: Tue, 17 Mar 2026 01:41:39 GMT  
		Size: 61.2 MB (61210109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e66ec645227bb9cb719d763ae4dc1a800e8343e765e4bcd99c89bf69f03fd`  
		Last Modified: Tue, 17 Mar 2026 01:41:37 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:271f9794c497bdaf632628a0f68e2060e7dbc8378b2402808f7999a5e1da9149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c53c2057a51d08cbad93abfb41d2462332ae5e64601feb7022cec9fd4abba9`

```dockerfile
```

-	Layers:
	-	`sha256:e0ce7d028e7cab7c5932e6df020ad4469e33ab5b0c60ca7b4242ec92a0fddd32`  
		Last Modified: Tue, 17 Mar 2026 01:41:38 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e425e3266060ba53ae33efc4412d6b29c084d8fdb13766212aea2ef4ba4f7a8e`  
		Last Modified: Tue, 17 Mar 2026 01:41:38 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:df947d7d10e16f321fd26fbed37836a162bd6a9168bd0e506f20e67411fdf01e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:59a37ca18d2580ad047bd91265e249c4145ed9df7ff1814707f2dc6b5a7fa51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92284121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f1f8afc56d793451170ef194b4c3b6391cb446777e4840b0deb3b6f90a3265`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:46 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:46 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:46 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:39:46 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Mar 2026 01:40:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:40:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:11 GMT
USER kong
# Tue, 17 Mar 2026 01:40:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:40:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:40:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:40:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8798b747f4662ab7b471f489fec0262fb1e6b6258b7f6c70d05b57cce1403d6d`  
		Last Modified: Tue, 17 Mar 2026 01:40:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bddbdf567adebb032ef05ceea3b332d66c4e780f9c41234817c4e018628a6ce`  
		Last Modified: Tue, 17 Mar 2026 01:40:27 GMT  
		Size: 62.7 MB (62744319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e358a1746fc119756cc6a7fb7d8fc91b2d9f9bc2d3a3c5eecad70ae509b3c`  
		Last Modified: Tue, 17 Mar 2026 01:40:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:131d60110ea24ab11e51389a4520edfcdbfe47a2701a508353961fe8281e3ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e54723fec1d1c04b22e1b2cd02e24c949e61f633d93b72f88cf9f22cb0c283`

```dockerfile
```

-	Layers:
	-	`sha256:b50f3b5a967f74d738b1849ddc97991e6bceee8282d734cb910d02a51ca6b9bd`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4ad318ba820c49d5443e152d95ca7d5cd66dbf801b20907b771852bd97e8ac`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:15b42219be422c2ac9ef163ae3f48f1caf47bc73f275ce4e84a98ed824402551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88600414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2c0c36f2067152969e4b33c308fa6c1ffb003a2a083f6227b715ccb2686228`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:49 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:49 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:49 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:40:49 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Mar 2026 01:41:23 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:23 GMT
USER kong
# Tue, 17 Mar 2026 01:41:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:23 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c161866d3e42bffbb83e4753ddfc391f58417a705ebcaf382a2e15e3fd3f37f`  
		Last Modified: Tue, 17 Mar 2026 01:41:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535161047479c5e046db48b280484c29233148bbdc0e11b2b81c5c715c49808f`  
		Last Modified: Tue, 17 Mar 2026 01:41:39 GMT  
		Size: 61.2 MB (61210109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e66ec645227bb9cb719d763ae4dc1a800e8343e765e4bcd99c89bf69f03fd`  
		Last Modified: Tue, 17 Mar 2026 01:41:37 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:271f9794c497bdaf632628a0f68e2060e7dbc8378b2402808f7999a5e1da9149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c53c2057a51d08cbad93abfb41d2462332ae5e64601feb7022cec9fd4abba9`

```dockerfile
```

-	Layers:
	-	`sha256:e0ce7d028e7cab7c5932e6df020ad4469e33ab5b0c60ca7b4242ec92a0fddd32`  
		Last Modified: Tue, 17 Mar 2026 01:41:38 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e425e3266060ba53ae33efc4412d6b29c084d8fdb13766212aea2ef4ba4f7a8e`  
		Last Modified: Tue, 17 Mar 2026 01:41:38 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:df947d7d10e16f321fd26fbed37836a162bd6a9168bd0e506f20e67411fdf01e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:59a37ca18d2580ad047bd91265e249c4145ed9df7ff1814707f2dc6b5a7fa51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92284121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f1f8afc56d793451170ef194b4c3b6391cb446777e4840b0deb3b6f90a3265`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:46 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:46 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:46 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:39:46 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Mar 2026 01:39:46 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Mar 2026 01:40:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:40:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:40:11 GMT
USER kong
# Tue, 17 Mar 2026 01:40:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:40:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:40:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:40:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8798b747f4662ab7b471f489fec0262fb1e6b6258b7f6c70d05b57cce1403d6d`  
		Last Modified: Tue, 17 Mar 2026 01:40:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bddbdf567adebb032ef05ceea3b332d66c4e780f9c41234817c4e018628a6ce`  
		Last Modified: Tue, 17 Mar 2026 01:40:27 GMT  
		Size: 62.7 MB (62744319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238e358a1746fc119756cc6a7fb7d8fc91b2d9f9bc2d3a3c5eecad70ae509b3c`  
		Last Modified: Tue, 17 Mar 2026 01:40:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:131d60110ea24ab11e51389a4520edfcdbfe47a2701a508353961fe8281e3ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e54723fec1d1c04b22e1b2cd02e24c949e61f633d93b72f88cf9f22cb0c283`

```dockerfile
```

-	Layers:
	-	`sha256:b50f3b5a967f74d738b1849ddc97991e6bceee8282d734cb910d02a51ca6b9bd`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4ad318ba820c49d5443e152d95ca7d5cd66dbf801b20907b771852bd97e8ac`  
		Last Modified: Tue, 17 Mar 2026 01:40:26 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:15b42219be422c2ac9ef163ae3f48f1caf47bc73f275ce4e84a98ed824402551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88600414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2c0c36f2067152969e4b33c308fa6c1ffb003a2a083f6227b715ccb2686228`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:49 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:49 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:49 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:40:49 GMT
ENV KONG_VERSION=3.4.2
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Tue, 17 Mar 2026 01:40:49 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Tue, 17 Mar 2026 01:41:23 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:23 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:23 GMT
USER kong
# Tue, 17 Mar 2026 01:41:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:23 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:23 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c161866d3e42bffbb83e4753ddfc391f58417a705ebcaf382a2e15e3fd3f37f`  
		Last Modified: Tue, 17 Mar 2026 01:41:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535161047479c5e046db48b280484c29233148bbdc0e11b2b81c5c715c49808f`  
		Last Modified: Tue, 17 Mar 2026 01:41:39 GMT  
		Size: 61.2 MB (61210109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606e66ec645227bb9cb719d763ae4dc1a800e8343e765e4bcd99c89bf69f03fd`  
		Last Modified: Tue, 17 Mar 2026 01:41:37 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:271f9794c497bdaf632628a0f68e2060e7dbc8378b2402808f7999a5e1da9149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c53c2057a51d08cbad93abfb41d2462332ae5e64601feb7022cec9fd4abba9`

```dockerfile
```

-	Layers:
	-	`sha256:e0ce7d028e7cab7c5932e6df020ad4469e33ab5b0c60ca7b4242ec92a0fddd32`  
		Last Modified: Tue, 17 Mar 2026 01:41:38 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e425e3266060ba53ae33efc4412d6b29c084d8fdb13766212aea2ef4ba4f7a8e`  
		Last Modified: Tue, 17 Mar 2026 01:41:38 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:2da0e3e9407b14c3e5ed8c583d2c6257aa53871ccb9e2c12c4224db10e0c43c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:62fad54c77acdcebd15d462d152a0b3752ce1089bb68f387620c95fcab9e99fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117555769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ff7bfdfff1587838ee678a0736349cf9d58e8fe3b84f6d4d51fc6ccf44e79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:24 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:24 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:24 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:24 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:39:24 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Mar 2026 01:39:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
USER kong
# Tue, 17 Mar 2026 01:39:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c3523f85b3365db1c5538b753dbb4deb9faf6a8bbcc4391c4cf582394d582d`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c3f85c7b8eb226a6d6830e31596d859aabf780c03ab001d4a25ba789833fbd`  
		Last Modified: Tue, 17 Mar 2026 01:40:07 GMT  
		Size: 88.0 MB (88015968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bcbcc79501ea543b4bcbc839863e05303b5a7bcdb7c4d1ae404205ff3745a8`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:193a55ccf914a45b73ffaa86d4aba3f2a63a0096e3fb1660304c6e0957efb48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d10c5b08cbb757742e6fc82b6c53eea146d78685482fa147c8f1799bd4ccec3`

```dockerfile
```

-	Layers:
	-	`sha256:8c00f816950a0d7f8f6e139be974dccf12141d190af59ebc46fa34d0c3885112`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375ff7a9fe430c515c653b15f21a3c19bf94f3b13a788eeed9b2d49f32f67fa2`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d3fdcf9639871ae939ff3bd57ef25dfd4e3625fc86dcb00faab3ad0e3b8e8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114713498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6862fb4322c145998df0eb23243da848bbe6dd4fa7a367c857ca21c182cb37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:57 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:57 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:57 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:57 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:57 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:40:57 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Mar 2026 01:41:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:27 GMT
USER kong
# Tue, 17 Mar 2026 01:41:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cf4ec3123086df947247599fd5b957fea3d1357c841a31ab41f918d84445c9`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0073bfd855b22260d99fa35f746dd9480ced2400d3585b2f722f524073dec950`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 87.3 MB (87323189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a666f2478ba2d953d13d2b2bba808817eabf9c1beb719c7a2d72b45f13b36f1`  
		Last Modified: Tue, 17 Mar 2026 01:41:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:633f4904c735f57e5584aa428a2a11f19688accc1f52c7e6c88041573d5b4078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efed52cca14e2343301a8391c909ab717b38d48fcada51221f9b680640b01754`

```dockerfile
```

-	Layers:
	-	`sha256:e0c9ff174c2ffbc77b4009619f9763eb7bc8c26b7a87d0d0a1fadf6198d2c7fa`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f8f953bff7d20b2bdb9ef2c7bef03748c1c2fa77e76c4f772676d2a1dd889e`  
		Last Modified: Tue, 17 Mar 2026 01:41:43 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:2da0e3e9407b14c3e5ed8c583d2c6257aa53871ccb9e2c12c4224db10e0c43c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:62fad54c77acdcebd15d462d152a0b3752ce1089bb68f387620c95fcab9e99fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117555769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ff7bfdfff1587838ee678a0736349cf9d58e8fe3b84f6d4d51fc6ccf44e79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:24 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:24 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:24 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:24 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:39:24 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Mar 2026 01:39:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
USER kong
# Tue, 17 Mar 2026 01:39:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c3523f85b3365db1c5538b753dbb4deb9faf6a8bbcc4391c4cf582394d582d`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c3f85c7b8eb226a6d6830e31596d859aabf780c03ab001d4a25ba789833fbd`  
		Last Modified: Tue, 17 Mar 2026 01:40:07 GMT  
		Size: 88.0 MB (88015968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bcbcc79501ea543b4bcbc839863e05303b5a7bcdb7c4d1ae404205ff3745a8`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:193a55ccf914a45b73ffaa86d4aba3f2a63a0096e3fb1660304c6e0957efb48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d10c5b08cbb757742e6fc82b6c53eea146d78685482fa147c8f1799bd4ccec3`

```dockerfile
```

-	Layers:
	-	`sha256:8c00f816950a0d7f8f6e139be974dccf12141d190af59ebc46fa34d0c3885112`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375ff7a9fe430c515c653b15f21a3c19bf94f3b13a788eeed9b2d49f32f67fa2`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d3fdcf9639871ae939ff3bd57ef25dfd4e3625fc86dcb00faab3ad0e3b8e8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114713498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6862fb4322c145998df0eb23243da848bbe6dd4fa7a367c857ca21c182cb37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:57 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:57 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:57 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:57 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:57 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:40:57 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Mar 2026 01:41:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:27 GMT
USER kong
# Tue, 17 Mar 2026 01:41:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cf4ec3123086df947247599fd5b957fea3d1357c841a31ab41f918d84445c9`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0073bfd855b22260d99fa35f746dd9480ced2400d3585b2f722f524073dec950`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 87.3 MB (87323189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a666f2478ba2d953d13d2b2bba808817eabf9c1beb719c7a2d72b45f13b36f1`  
		Last Modified: Tue, 17 Mar 2026 01:41:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:633f4904c735f57e5584aa428a2a11f19688accc1f52c7e6c88041573d5b4078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efed52cca14e2343301a8391c909ab717b38d48fcada51221f9b680640b01754`

```dockerfile
```

-	Layers:
	-	`sha256:e0c9ff174c2ffbc77b4009619f9763eb7bc8c26b7a87d0d0a1fadf6198d2c7fa`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f8f953bff7d20b2bdb9ef2c7bef03748c1c2fa77e76c4f772676d2a1dd889e`  
		Last Modified: Tue, 17 Mar 2026 01:41:43 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:2da0e3e9407b14c3e5ed8c583d2c6257aa53871ccb9e2c12c4224db10e0c43c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:62fad54c77acdcebd15d462d152a0b3752ce1089bb68f387620c95fcab9e99fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117555769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ff7bfdfff1587838ee678a0736349cf9d58e8fe3b84f6d4d51fc6ccf44e79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:24 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:24 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:24 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:24 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:39:24 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Mar 2026 01:39:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
USER kong
# Tue, 17 Mar 2026 01:39:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c3523f85b3365db1c5538b753dbb4deb9faf6a8bbcc4391c4cf582394d582d`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c3f85c7b8eb226a6d6830e31596d859aabf780c03ab001d4a25ba789833fbd`  
		Last Modified: Tue, 17 Mar 2026 01:40:07 GMT  
		Size: 88.0 MB (88015968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bcbcc79501ea543b4bcbc839863e05303b5a7bcdb7c4d1ae404205ff3745a8`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:193a55ccf914a45b73ffaa86d4aba3f2a63a0096e3fb1660304c6e0957efb48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d10c5b08cbb757742e6fc82b6c53eea146d78685482fa147c8f1799bd4ccec3`

```dockerfile
```

-	Layers:
	-	`sha256:8c00f816950a0d7f8f6e139be974dccf12141d190af59ebc46fa34d0c3885112`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375ff7a9fe430c515c653b15f21a3c19bf94f3b13a788eeed9b2d49f32f67fa2`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d3fdcf9639871ae939ff3bd57ef25dfd4e3625fc86dcb00faab3ad0e3b8e8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114713498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6862fb4322c145998df0eb23243da848bbe6dd4fa7a367c857ca21c182cb37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:57 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:57 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:57 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:57 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:57 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:40:57 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Mar 2026 01:41:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:27 GMT
USER kong
# Tue, 17 Mar 2026 01:41:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cf4ec3123086df947247599fd5b957fea3d1357c841a31ab41f918d84445c9`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0073bfd855b22260d99fa35f746dd9480ced2400d3585b2f722f524073dec950`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 87.3 MB (87323189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a666f2478ba2d953d13d2b2bba808817eabf9c1beb719c7a2d72b45f13b36f1`  
		Last Modified: Tue, 17 Mar 2026 01:41:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:633f4904c735f57e5584aa428a2a11f19688accc1f52c7e6c88041573d5b4078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efed52cca14e2343301a8391c909ab717b38d48fcada51221f9b680640b01754`

```dockerfile
```

-	Layers:
	-	`sha256:e0c9ff174c2ffbc77b4009619f9763eb7bc8c26b7a87d0d0a1fadf6198d2c7fa`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f8f953bff7d20b2bdb9ef2c7bef03748c1c2fa77e76c4f772676d2a1dd889e`  
		Last Modified: Tue, 17 Mar 2026 01:41:43 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:2da0e3e9407b14c3e5ed8c583d2c6257aa53871ccb9e2c12c4224db10e0c43c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:62fad54c77acdcebd15d462d152a0b3752ce1089bb68f387620c95fcab9e99fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117555769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ff7bfdfff1587838ee678a0736349cf9d58e8fe3b84f6d4d51fc6ccf44e79e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:24 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:39:24 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:39:24 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:39:24 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:39:24 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:39:24 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Mar 2026 01:39:24 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Mar 2026 01:39:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:39:49 GMT
USER kong
# Tue, 17 Mar 2026 01:39:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:39:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:39:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:39:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:39:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c3523f85b3365db1c5538b753dbb4deb9faf6a8bbcc4391c4cf582394d582d`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c3f85c7b8eb226a6d6830e31596d859aabf780c03ab001d4a25ba789833fbd`  
		Last Modified: Tue, 17 Mar 2026 01:40:07 GMT  
		Size: 88.0 MB (88015968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bcbcc79501ea543b4bcbc839863e05303b5a7bcdb7c4d1ae404205ff3745a8`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:193a55ccf914a45b73ffaa86d4aba3f2a63a0096e3fb1660304c6e0957efb48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d10c5b08cbb757742e6fc82b6c53eea146d78685482fa147c8f1799bd4ccec3`

```dockerfile
```

-	Layers:
	-	`sha256:8c00f816950a0d7f8f6e139be974dccf12141d190af59ebc46fa34d0c3885112`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375ff7a9fe430c515c653b15f21a3c19bf94f3b13a788eeed9b2d49f32f67fa2`  
		Last Modified: Tue, 17 Mar 2026 01:40:05 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d3fdcf9639871ae939ff3bd57ef25dfd4e3625fc86dcb00faab3ad0e3b8e8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114713498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6862fb4322c145998df0eb23243da848bbe6dd4fa7a367c857ca21c182cb37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:57 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 17 Mar 2026 01:40:57 GMT
ARG ASSET=ce
# Tue, 17 Mar 2026 01:40:57 GMT
ENV ASSET=ce
# Tue, 17 Mar 2026 01:40:57 GMT
ARG EE_PORTS
# Tue, 17 Mar 2026 01:40:57 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:40:57 GMT
ENV KONG_VERSION=3.8.0
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Tue, 17 Mar 2026 01:40:57 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Tue, 17 Mar 2026 01:41:27 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 17 Mar 2026 01:41:27 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 01:41:27 GMT
USER kong
# Tue, 17 Mar 2026 01:41:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:41:27 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 17 Mar 2026 01:41:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 01:41:27 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 17 Mar 2026 01:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cf4ec3123086df947247599fd5b957fea3d1357c841a31ab41f918d84445c9`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0073bfd855b22260d99fa35f746dd9480ced2400d3585b2f722f524073dec950`  
		Last Modified: Tue, 17 Mar 2026 01:41:46 GMT  
		Size: 87.3 MB (87323189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a666f2478ba2d953d13d2b2bba808817eabf9c1beb719c7a2d72b45f13b36f1`  
		Last Modified: Tue, 17 Mar 2026 01:41:43 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:633f4904c735f57e5584aa428a2a11f19688accc1f52c7e6c88041573d5b4078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efed52cca14e2343301a8391c909ab717b38d48fcada51221f9b680640b01754`

```dockerfile
```

-	Layers:
	-	`sha256:e0c9ff174c2ffbc77b4009619f9763eb7bc8c26b7a87d0d0a1fadf6198d2c7fa`  
		Last Modified: Tue, 17 Mar 2026 01:41:44 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f8f953bff7d20b2bdb9ef2c7bef03748c1c2fa77e76c4f772676d2a1dd889e`  
		Last Modified: Tue, 17 Mar 2026 01:41:43 GMT  
		Size: 15.4 KB (15450 bytes)  
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
