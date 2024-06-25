<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2`](#kong2)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.5`](#kong285)
-	[`kong:2.8.5-ubuntu`](#kong285-ubuntu)
-	[`kong:3`](#kong3)
-	[`kong:3.4`](#kong34)
-	[`kong:3.4-ubuntu`](#kong34-ubuntu)
-	[`kong:3.4.2`](#kong342)
-	[`kong:3.4.2-ubuntu`](#kong342-ubuntu)
-	[`kong:3.5`](#kong35)
-	[`kong:3.5-ubuntu`](#kong35-ubuntu)
-	[`kong:3.5.0`](#kong350)
-	[`kong:3.5.0-ubuntu`](#kong350-ubuntu)
-	[`kong:3.6`](#kong36)
-	[`kong:3.6-ubuntu`](#kong36-ubuntu)
-	[`kong:3.6.1`](#kong361)
-	[`kong:3.6.1-ubuntu`](#kong361-ubuntu)
-	[`kong:3.7`](#kong37)
-	[`kong:3.7-ubuntu`](#kong37-ubuntu)
-	[`kong:3.7.1`](#kong371)
-	[`kong:3.7.1-ubuntu`](#kong371-ubuntu)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2`

```console
$ docker pull kong@sha256:d3f2596d596283e3be2fd567cb83817a727ca1e90b531871496059aafe7e0c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:f98548d2b8582d9c70856111e074fa55923e5fb163474e74fc2ce87dd134dfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185280239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73926428358613c4d7b95a9eb203ad2be5a3d6c64175c3d40169bc65dfc2b0a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 13:23:47 GMT
ARG ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ENV ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ARG EE_PORTS
# Tue, 25 Jun 2024 13:23:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ENV KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 25 Jun 2024 13:23:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
USER kong
# Tue, 25 Jun 2024 13:23:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Jun 2024 13:23:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 25 Jun 2024 13:23:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Jun 2024 13:23:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 25 Jun 2024 13:23:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dd8b89c8df3f824f764c7440601666ab0813954a9eade81431a14166226582`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddd3791b5ba9334eb29ae0b2db07a41a4db4d20dcd26312a92a7abc0b8f05db`  
		Last Modified: Tue, 25 Jun 2024 18:54:02 GMT  
		Size: 130.7 MB (130663637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b54f864e4bb8acff9a0202bbf62ff1ead19d00cdacd1ffc1760fc07b086bc5e`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2` - unknown; unknown

```console
$ docker pull kong@sha256:c994e26976dbaf6230b4ad0abebe336e7ed016a35ced1138df66709d762a497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305f1a94df459eb7a1d01e2b0f1cf18396326203c6bee1ddbb302b26b1be25f`

```dockerfile
```

-	Layers:
	-	`sha256:82e6de502006a827a77ed09f6373c481595f154ff29b2ff6d6056235261392ee`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 7.1 MB (7062721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb0f5a7324d16c1758d274e3b67f810c66839872e37f6d2696cbcd98a514849`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8`

```console
$ docker pull kong@sha256:d3f2596d596283e3be2fd567cb83817a727ca1e90b531871496059aafe7e0c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:f98548d2b8582d9c70856111e074fa55923e5fb163474e74fc2ce87dd134dfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185280239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73926428358613c4d7b95a9eb203ad2be5a3d6c64175c3d40169bc65dfc2b0a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 13:23:47 GMT
ARG ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ENV ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ARG EE_PORTS
# Tue, 25 Jun 2024 13:23:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ENV KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 25 Jun 2024 13:23:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
USER kong
# Tue, 25 Jun 2024 13:23:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Jun 2024 13:23:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 25 Jun 2024 13:23:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Jun 2024 13:23:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 25 Jun 2024 13:23:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dd8b89c8df3f824f764c7440601666ab0813954a9eade81431a14166226582`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddd3791b5ba9334eb29ae0b2db07a41a4db4d20dcd26312a92a7abc0b8f05db`  
		Last Modified: Tue, 25 Jun 2024 18:54:02 GMT  
		Size: 130.7 MB (130663637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b54f864e4bb8acff9a0202bbf62ff1ead19d00cdacd1ffc1760fc07b086bc5e`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8` - unknown; unknown

```console
$ docker pull kong@sha256:c994e26976dbaf6230b4ad0abebe336e7ed016a35ced1138df66709d762a497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305f1a94df459eb7a1d01e2b0f1cf18396326203c6bee1ddbb302b26b1be25f`

```dockerfile
```

-	Layers:
	-	`sha256:82e6de502006a827a77ed09f6373c481595f154ff29b2ff6d6056235261392ee`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 7.1 MB (7062721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb0f5a7324d16c1758d274e3b67f810c66839872e37f6d2696cbcd98a514849`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:d3f2596d596283e3be2fd567cb83817a727ca1e90b531871496059aafe7e0c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f98548d2b8582d9c70856111e074fa55923e5fb163474e74fc2ce87dd134dfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185280239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73926428358613c4d7b95a9eb203ad2be5a3d6c64175c3d40169bc65dfc2b0a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 13:23:47 GMT
ARG ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ENV ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ARG EE_PORTS
# Tue, 25 Jun 2024 13:23:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ENV KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 25 Jun 2024 13:23:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
USER kong
# Tue, 25 Jun 2024 13:23:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Jun 2024 13:23:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 25 Jun 2024 13:23:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Jun 2024 13:23:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 25 Jun 2024 13:23:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dd8b89c8df3f824f764c7440601666ab0813954a9eade81431a14166226582`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddd3791b5ba9334eb29ae0b2db07a41a4db4d20dcd26312a92a7abc0b8f05db`  
		Last Modified: Tue, 25 Jun 2024 18:54:02 GMT  
		Size: 130.7 MB (130663637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b54f864e4bb8acff9a0202bbf62ff1ead19d00cdacd1ffc1760fc07b086bc5e`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c994e26976dbaf6230b4ad0abebe336e7ed016a35ced1138df66709d762a497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305f1a94df459eb7a1d01e2b0f1cf18396326203c6bee1ddbb302b26b1be25f`

```dockerfile
```

-	Layers:
	-	`sha256:82e6de502006a827a77ed09f6373c481595f154ff29b2ff6d6056235261392ee`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 7.1 MB (7062721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb0f5a7324d16c1758d274e3b67f810c66839872e37f6d2696cbcd98a514849`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5`

```console
$ docker pull kong@sha256:d3f2596d596283e3be2fd567cb83817a727ca1e90b531871496059aafe7e0c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5` - linux; amd64

```console
$ docker pull kong@sha256:f98548d2b8582d9c70856111e074fa55923e5fb163474e74fc2ce87dd134dfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185280239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73926428358613c4d7b95a9eb203ad2be5a3d6c64175c3d40169bc65dfc2b0a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 13:23:47 GMT
ARG ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ENV ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ARG EE_PORTS
# Tue, 25 Jun 2024 13:23:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ENV KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 25 Jun 2024 13:23:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
USER kong
# Tue, 25 Jun 2024 13:23:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Jun 2024 13:23:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 25 Jun 2024 13:23:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Jun 2024 13:23:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 25 Jun 2024 13:23:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dd8b89c8df3f824f764c7440601666ab0813954a9eade81431a14166226582`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddd3791b5ba9334eb29ae0b2db07a41a4db4d20dcd26312a92a7abc0b8f05db`  
		Last Modified: Tue, 25 Jun 2024 18:54:02 GMT  
		Size: 130.7 MB (130663637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b54f864e4bb8acff9a0202bbf62ff1ead19d00cdacd1ffc1760fc07b086bc5e`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5` - unknown; unknown

```console
$ docker pull kong@sha256:c994e26976dbaf6230b4ad0abebe336e7ed016a35ced1138df66709d762a497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305f1a94df459eb7a1d01e2b0f1cf18396326203c6bee1ddbb302b26b1be25f`

```dockerfile
```

-	Layers:
	-	`sha256:82e6de502006a827a77ed09f6373c481595f154ff29b2ff6d6056235261392ee`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 7.1 MB (7062721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb0f5a7324d16c1758d274e3b67f810c66839872e37f6d2696cbcd98a514849`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:d3f2596d596283e3be2fd567cb83817a727ca1e90b531871496059aafe7e0c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f98548d2b8582d9c70856111e074fa55923e5fb163474e74fc2ce87dd134dfbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.3 MB (185280239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73926428358613c4d7b95a9eb203ad2be5a3d6c64175c3d40169bc65dfc2b0a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 25 Jun 2024 13:23:47 GMT
ARG ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ENV ASSET=ce
# Tue, 25 Jun 2024 13:23:47 GMT
ARG EE_PORTS
# Tue, 25 Jun 2024 13:23:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ENV KONG_VERSION=2.8.5
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Tue, 25 Jun 2024 13:23:47 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Tue, 25 Jun 2024 13:23:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 25 Jun 2024 13:23:47 GMT
USER kong
# Tue, 25 Jun 2024 13:23:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 25 Jun 2024 13:23:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 25 Jun 2024 13:23:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Jun 2024 13:23:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Tue, 25 Jun 2024 13:23:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dd8b89c8df3f824f764c7440601666ab0813954a9eade81431a14166226582`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddd3791b5ba9334eb29ae0b2db07a41a4db4d20dcd26312a92a7abc0b8f05db`  
		Last Modified: Tue, 25 Jun 2024 18:54:02 GMT  
		Size: 130.7 MB (130663637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b54f864e4bb8acff9a0202bbf62ff1ead19d00cdacd1ffc1760fc07b086bc5e`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c994e26976dbaf6230b4ad0abebe336e7ed016a35ced1138df66709d762a497a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9305f1a94df459eb7a1d01e2b0f1cf18396326203c6bee1ddbb302b26b1be25f`

```dockerfile
```

-	Layers:
	-	`sha256:82e6de502006a827a77ed09f6373c481595f154ff29b2ff6d6056235261392ee`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 7.1 MB (7062721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb0f5a7324d16c1758d274e3b67f810c66839872e37f6d2696cbcd98a514849`  
		Last Modified: Tue, 25 Jun 2024 18:54:00 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:43b2e4e47b35deb698f9bb43d1e83a004f7bef9a4380d364bc4916f4751e410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:74e23e0146aaad4c1afc2e83d4338c9ea386d82b4cf45bafe8c93d4f0e53bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31619876e64e0de610faeb49dba552aa02be48954146ebbbd67694e16ae384f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17d22485ffe58f13f5431d630250008224700f70aa2b2125096dd2ec6f245cb`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36f7d7494853315d1200296062d6486f291641d53d3e1c1a6027c090df3538`  
		Last Modified: Fri, 21 Jun 2024 19:54:30 GMT  
		Size: 67.7 MB (67710059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e46b0537593126b5828f88b6b5d3f0b2e418d4ff9683f1ab6f589a125100b`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:31d6841f6ace121413bafc3e425f0488492a3ae7121d15255bf76d4b0b584bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae62db9ccad2118d424ff506befb470f935cc15ac773f4e94e8da230256ece0`

```dockerfile
```

-	Layers:
	-	`sha256:4c545e37b7f93cca1a63ef5fef8e76335d4f6ce0ffea01987d7aec4d2856c4cc`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81d2a8fdd06bc62afc631eb74c12dccb213bfbbdcea6cad26629a54c478a448`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:948e79d0db128b43cce68183f7b53c98a02ea4c8c12f903483d276b674431f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beed1c0805ca9dc8bbec7a0b810b325a24757d5db5882d58cb3c8f6ebe50cc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc34aa5b67fd3d5a20b6ac0e16b935abfa99e402f7517a4fa319f24093067d1`  
		Last Modified: Fri, 21 Jun 2024 19:55:27 GMT  
		Size: 67.7 MB (67652077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f358c419b9a726292ea393cd121c845aa14adede952a3b658e38fc6d19eb38e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:ab3fd8b5722491f7f4821bac6c67132221c70f85c7e3257bacae6b8c4877794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a610c77baabce0bb3510a6a6d57f1434906621adc965cb192c0760ea943e030`

```dockerfile
```

-	Layers:
	-	`sha256:377f85ee56ab1d04ea7a3501c02c9fad1b509c73763d922a1556af037285942e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77db0cc7f007a3b0c71b549771969f12712599a8f870a2b06920f00ab995864d`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:70f98f0d048c9d5f98c43c5fe4d2b916be27d774a0443b9e701c646dcb3ca4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:5f968967b941c60ef3143910ef26f78811fdbc79f19c7b10ee418d760ffd29e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794afc90787cfc3dad640b2a5b8f85b1835dd3f1649fca3e16aae0b99be9b123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:22:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:22:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:22:09 GMT
USER kong
# Sat, 15 Jun 2024 00:22:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:22:10 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a347fe47d68ffa81beab3d274caae8aab610627f58a546a75198efb9c11e070`  
		Last Modified: Sat, 15 Jun 2024 00:23:27 GMT  
		Size: 62.7 MB (62748133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61b3f40e2db198262e6bb9c1c6173fba253605c983cfa6dbbfd6285c26ac7b`  
		Last Modified: Sat, 15 Jun 2024 00:23:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bc2432c1fc70478be156c49eb2f3af1d6b686023e16e572056a6189ccf1d5abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89575599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c6f42ebe0af9280ccbda442f8ee1b6292c1766bcaedd4380d74732b567a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:41:14 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:41:15 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:41:15 GMT
USER kong
# Sat, 15 Jun 2024 00:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:41:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:41:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:41:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:41:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb5026d472701f71e6f3fb94dfb5d03622f307df72949ebd53d94984938e856`  
		Last Modified: Sat, 15 Jun 2024 00:42:18 GMT  
		Size: 61.2 MB (61172007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb5dd4a808f942e8072e8be104ee1a94133b3f1d4c667a1386f558b8a6ddd4`  
		Last Modified: Sat, 15 Jun 2024 00:42:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:70f98f0d048c9d5f98c43c5fe4d2b916be27d774a0443b9e701c646dcb3ca4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5f968967b941c60ef3143910ef26f78811fdbc79f19c7b10ee418d760ffd29e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794afc90787cfc3dad640b2a5b8f85b1835dd3f1649fca3e16aae0b99be9b123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:22:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:22:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:22:09 GMT
USER kong
# Sat, 15 Jun 2024 00:22:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:22:10 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a347fe47d68ffa81beab3d274caae8aab610627f58a546a75198efb9c11e070`  
		Last Modified: Sat, 15 Jun 2024 00:23:27 GMT  
		Size: 62.7 MB (62748133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61b3f40e2db198262e6bb9c1c6173fba253605c983cfa6dbbfd6285c26ac7b`  
		Last Modified: Sat, 15 Jun 2024 00:23:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bc2432c1fc70478be156c49eb2f3af1d6b686023e16e572056a6189ccf1d5abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89575599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c6f42ebe0af9280ccbda442f8ee1b6292c1766bcaedd4380d74732b567a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:41:14 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:41:15 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:41:15 GMT
USER kong
# Sat, 15 Jun 2024 00:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:41:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:41:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:41:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:41:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb5026d472701f71e6f3fb94dfb5d03622f307df72949ebd53d94984938e856`  
		Last Modified: Sat, 15 Jun 2024 00:42:18 GMT  
		Size: 61.2 MB (61172007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb5dd4a808f942e8072e8be104ee1a94133b3f1d4c667a1386f558b8a6ddd4`  
		Last Modified: Sat, 15 Jun 2024 00:42:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2`

```console
$ docker pull kong@sha256:70f98f0d048c9d5f98c43c5fe4d2b916be27d774a0443b9e701c646dcb3ca4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:5f968967b941c60ef3143910ef26f78811fdbc79f19c7b10ee418d760ffd29e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794afc90787cfc3dad640b2a5b8f85b1835dd3f1649fca3e16aae0b99be9b123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:22:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:22:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:22:09 GMT
USER kong
# Sat, 15 Jun 2024 00:22:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:22:10 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a347fe47d68ffa81beab3d274caae8aab610627f58a546a75198efb9c11e070`  
		Last Modified: Sat, 15 Jun 2024 00:23:27 GMT  
		Size: 62.7 MB (62748133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61b3f40e2db198262e6bb9c1c6173fba253605c983cfa6dbbfd6285c26ac7b`  
		Last Modified: Sat, 15 Jun 2024 00:23:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bc2432c1fc70478be156c49eb2f3af1d6b686023e16e572056a6189ccf1d5abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89575599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c6f42ebe0af9280ccbda442f8ee1b6292c1766bcaedd4380d74732b567a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:41:14 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:41:15 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:41:15 GMT
USER kong
# Sat, 15 Jun 2024 00:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:41:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:41:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:41:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:41:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb5026d472701f71e6f3fb94dfb5d03622f307df72949ebd53d94984938e856`  
		Last Modified: Sat, 15 Jun 2024 00:42:18 GMT  
		Size: 61.2 MB (61172007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb5dd4a808f942e8072e8be104ee1a94133b3f1d4c667a1386f558b8a6ddd4`  
		Last Modified: Sat, 15 Jun 2024 00:42:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:70f98f0d048c9d5f98c43c5fe4d2b916be27d774a0443b9e701c646dcb3ca4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5f968967b941c60ef3143910ef26f78811fdbc79f19c7b10ee418d760ffd29e4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93188701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794afc90787cfc3dad640b2a5b8f85b1835dd3f1649fca3e16aae0b99be9b123`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:30:38 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:22:09 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:22:09 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:22:09 GMT
USER kong
# Sat, 15 Jun 2024 00:22:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:22:10 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:22:10 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:22:10 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:22:10 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a347fe47d68ffa81beab3d274caae8aab610627f58a546a75198efb9c11e070`  
		Last Modified: Sat, 15 Jun 2024 00:23:27 GMT  
		Size: 62.7 MB (62748133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f61b3f40e2db198262e6bb9c1c6173fba253605c983cfa6dbbfd6285c26ac7b`  
		Last Modified: Sat, 15 Jun 2024 00:23:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bc2432c1fc70478be156c49eb2f3af1d6b686023e16e572056a6189ccf1d5abc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89575599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9c6f42ebe0af9280ccbda442f8ee1b6292c1766bcaedd4380d74732b567a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ENV KONG_VERSION=3.4.2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Wed, 05 Jun 2024 07:09:56 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Sat, 15 Jun 2024 00:41:14 GMT
# ARGS: KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:41:15 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:41:15 GMT
USER kong
# Sat, 15 Jun 2024 00:41:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:41:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:41:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:41:15 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:41:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb5026d472701f71e6f3fb94dfb5d03622f307df72949ebd53d94984938e856`  
		Last Modified: Sat, 15 Jun 2024 00:42:18 GMT  
		Size: 61.2 MB (61172007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bdb5dd4a808f942e8072e8be104ee1a94133b3f1d4c667a1386f558b8a6ddd4`  
		Last Modified: Sat, 15 Jun 2024 00:42:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5`

```console
$ docker pull kong@sha256:80695162a49f52a7f3284e11c86226b966c627c979b966ad4d12abad46efcb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5` - linux; amd64

```console
$ docker pull kong@sha256:9411fd86123391795f79d80f37dda9b14e769fd2800e9dc72d98359a3d66f9c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b605def7c3fee50f8798d6ad6d7bd1e852c0232a1eff8ca2249be020714a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:21:41 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:41 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:42 GMT
USER kong
# Sat, 15 Jun 2024 00:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:42 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8916e7036bb7e051f8b6c6f87ea74e5047cad1d9ca82626533470537f807cc8`  
		Last Modified: Sat, 15 Jun 2024 00:23:07 GMT  
		Size: 64.0 MB (63964608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9249b03ce187d409b282fd06a99e1a0eb8eea969209b029d5d9240c42228102c`  
		Last Modified: Sat, 15 Jun 2024 00:22:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e5e5b678f64a3dd2e8d10244195adaa1237b46b8a07f6bc133ae358539572d4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7271c81a1a45e919c608e0de23466b110af5284cf913d31a7b6fc71dc6854b7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:40:47 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:48 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:48 GMT
USER kong
# Sat, 15 Jun 2024 00:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:48 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f60e3de80db16b864444f80b19cc87ca2470443506ed93968cc66678762d2d`  
		Last Modified: Sat, 15 Jun 2024 00:41:59 GMT  
		Size: 63.5 MB (63484296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed3435482ab32691718553e82af2f33d52a726bb73bd0ba6f5eff665364ed2`  
		Last Modified: Sat, 15 Jun 2024 00:41:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5-ubuntu`

```console
$ docker pull kong@sha256:80695162a49f52a7f3284e11c86226b966c627c979b966ad4d12abad46efcb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9411fd86123391795f79d80f37dda9b14e769fd2800e9dc72d98359a3d66f9c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b605def7c3fee50f8798d6ad6d7bd1e852c0232a1eff8ca2249be020714a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:21:41 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:41 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:42 GMT
USER kong
# Sat, 15 Jun 2024 00:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:42 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8916e7036bb7e051f8b6c6f87ea74e5047cad1d9ca82626533470537f807cc8`  
		Last Modified: Sat, 15 Jun 2024 00:23:07 GMT  
		Size: 64.0 MB (63964608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9249b03ce187d409b282fd06a99e1a0eb8eea969209b029d5d9240c42228102c`  
		Last Modified: Sat, 15 Jun 2024 00:22:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e5e5b678f64a3dd2e8d10244195adaa1237b46b8a07f6bc133ae358539572d4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7271c81a1a45e919c608e0de23466b110af5284cf913d31a7b6fc71dc6854b7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:40:47 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:48 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:48 GMT
USER kong
# Sat, 15 Jun 2024 00:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:48 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f60e3de80db16b864444f80b19cc87ca2470443506ed93968cc66678762d2d`  
		Last Modified: Sat, 15 Jun 2024 00:41:59 GMT  
		Size: 63.5 MB (63484296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed3435482ab32691718553e82af2f33d52a726bb73bd0ba6f5eff665364ed2`  
		Last Modified: Sat, 15 Jun 2024 00:41:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0`

```console
$ docker pull kong@sha256:80695162a49f52a7f3284e11c86226b966c627c979b966ad4d12abad46efcb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0` - linux; amd64

```console
$ docker pull kong@sha256:9411fd86123391795f79d80f37dda9b14e769fd2800e9dc72d98359a3d66f9c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b605def7c3fee50f8798d6ad6d7bd1e852c0232a1eff8ca2249be020714a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:21:41 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:41 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:42 GMT
USER kong
# Sat, 15 Jun 2024 00:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:42 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8916e7036bb7e051f8b6c6f87ea74e5047cad1d9ca82626533470537f807cc8`  
		Last Modified: Sat, 15 Jun 2024 00:23:07 GMT  
		Size: 64.0 MB (63964608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9249b03ce187d409b282fd06a99e1a0eb8eea969209b029d5d9240c42228102c`  
		Last Modified: Sat, 15 Jun 2024 00:22:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e5e5b678f64a3dd2e8d10244195adaa1237b46b8a07f6bc133ae358539572d4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7271c81a1a45e919c608e0de23466b110af5284cf913d31a7b6fc71dc6854b7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:40:47 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:48 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:48 GMT
USER kong
# Sat, 15 Jun 2024 00:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:48 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f60e3de80db16b864444f80b19cc87ca2470443506ed93968cc66678762d2d`  
		Last Modified: Sat, 15 Jun 2024 00:41:59 GMT  
		Size: 63.5 MB (63484296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed3435482ab32691718553e82af2f33d52a726bb73bd0ba6f5eff665364ed2`  
		Last Modified: Sat, 15 Jun 2024 00:41:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.5.0-ubuntu`

```console
$ docker pull kong@sha256:80695162a49f52a7f3284e11c86226b966c627c979b966ad4d12abad46efcb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.5.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9411fd86123391795f79d80f37dda9b14e769fd2800e9dc72d98359a3d66f9c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94405177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b605def7c3fee50f8798d6ad6d7bd1e852c0232a1eff8ca2249be020714a06`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:30:13 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:21:41 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:41 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:42 GMT
USER kong
# Sat, 15 Jun 2024 00:21:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:42 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8916e7036bb7e051f8b6c6f87ea74e5047cad1d9ca82626533470537f807cc8`  
		Last Modified: Sat, 15 Jun 2024 00:23:07 GMT  
		Size: 64.0 MB (63964608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9249b03ce187d409b282fd06a99e1a0eb8eea969209b029d5d9240c42228102c`  
		Last Modified: Sat, 15 Jun 2024 00:22:58 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.5.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e5e5b678f64a3dd2e8d10244195adaa1237b46b8a07f6bc133ae358539572d4e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91887887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7271c81a1a45e919c608e0de23466b110af5284cf913d31a7b6fc71dc6854b7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ENV KONG_VERSION=3.5.0
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Wed, 05 Jun 2024 07:09:37 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Sat, 15 Jun 2024 00:40:47 GMT
# ARGS: KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:48 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:48 GMT
USER kong
# Sat, 15 Jun 2024 00:40:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:48 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:49 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f60e3de80db16b864444f80b19cc87ca2470443506ed93968cc66678762d2d`  
		Last Modified: Sat, 15 Jun 2024 00:41:59 GMT  
		Size: 63.5 MB (63484296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ed3435482ab32691718553e82af2f33d52a726bb73bd0ba6f5eff665364ed2`  
		Last Modified: Sat, 15 Jun 2024 00:41:51 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6`

```console
$ docker pull kong@sha256:a3d2c8699f5e864c916187424153b93135c2b4add8548e7675432bc53fd61807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6` - linux; amd64

```console
$ docker pull kong@sha256:aefc3b35390452620d257ac2dfa0a81133ae6d0f4c5abfc5df9cefe2417b1245
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b61bee6996c212d86bec55a46011d8dcd051c98ede6d5b64e8e17be28ab0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:21:16 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:17 GMT
USER kong
# Sat, 15 Jun 2024 00:21:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9750302f66dbbd904d68dc009bd096ae1e295fbcc60c062fca374ea83cb8d`  
		Last Modified: Sat, 15 Jun 2024 00:22:47 GMT  
		Size: 67.7 MB (67676065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395a55bfda51337af1c0622d33c891e9903f19de2dc2f4e50a960d5ce097fa`  
		Last Modified: Sat, 15 Jun 2024 00:22:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e388fdd07ab562a159e861687e7b61a2bf312175fd97cd9787070bf59808efee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95633709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77420d480b60404df779c63c7a33f101b72698933492269a17ec75717a5e0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:40:17 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:19 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:19 GMT
USER kong
# Sat, 15 Jun 2024 00:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:19 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f099f0061884274828d95293909d9c908211fbd97b94ca687f3311c80d0a59`  
		Last Modified: Sat, 15 Jun 2024 00:41:40 GMT  
		Size: 67.2 MB (67230117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdd9430c73a732aa248c466dff075f60e0673d76b5a7af2e7675c1f3a90669`  
		Last Modified: Sat, 15 Jun 2024 00:41:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:a3d2c8699f5e864c916187424153b93135c2b4add8548e7675432bc53fd61807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:aefc3b35390452620d257ac2dfa0a81133ae6d0f4c5abfc5df9cefe2417b1245
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b61bee6996c212d86bec55a46011d8dcd051c98ede6d5b64e8e17be28ab0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:21:16 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:17 GMT
USER kong
# Sat, 15 Jun 2024 00:21:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9750302f66dbbd904d68dc009bd096ae1e295fbcc60c062fca374ea83cb8d`  
		Last Modified: Sat, 15 Jun 2024 00:22:47 GMT  
		Size: 67.7 MB (67676065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395a55bfda51337af1c0622d33c891e9903f19de2dc2f4e50a960d5ce097fa`  
		Last Modified: Sat, 15 Jun 2024 00:22:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e388fdd07ab562a159e861687e7b61a2bf312175fd97cd9787070bf59808efee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95633709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77420d480b60404df779c63c7a33f101b72698933492269a17ec75717a5e0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:40:17 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:19 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:19 GMT
USER kong
# Sat, 15 Jun 2024 00:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:19 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f099f0061884274828d95293909d9c908211fbd97b94ca687f3311c80d0a59`  
		Last Modified: Sat, 15 Jun 2024 00:41:40 GMT  
		Size: 67.2 MB (67230117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdd9430c73a732aa248c466dff075f60e0673d76b5a7af2e7675c1f3a90669`  
		Last Modified: Sat, 15 Jun 2024 00:41:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1`

```console
$ docker pull kong@sha256:a3d2c8699f5e864c916187424153b93135c2b4add8548e7675432bc53fd61807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6.1` - linux; amd64

```console
$ docker pull kong@sha256:aefc3b35390452620d257ac2dfa0a81133ae6d0f4c5abfc5df9cefe2417b1245
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b61bee6996c212d86bec55a46011d8dcd051c98ede6d5b64e8e17be28ab0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:21:16 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:17 GMT
USER kong
# Sat, 15 Jun 2024 00:21:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9750302f66dbbd904d68dc009bd096ae1e295fbcc60c062fca374ea83cb8d`  
		Last Modified: Sat, 15 Jun 2024 00:22:47 GMT  
		Size: 67.7 MB (67676065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395a55bfda51337af1c0622d33c891e9903f19de2dc2f4e50a960d5ce097fa`  
		Last Modified: Sat, 15 Jun 2024 00:22:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e388fdd07ab562a159e861687e7b61a2bf312175fd97cd9787070bf59808efee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95633709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77420d480b60404df779c63c7a33f101b72698933492269a17ec75717a5e0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:40:17 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:19 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:19 GMT
USER kong
# Sat, 15 Jun 2024 00:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:19 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f099f0061884274828d95293909d9c908211fbd97b94ca687f3311c80d0a59`  
		Last Modified: Sat, 15 Jun 2024 00:41:40 GMT  
		Size: 67.2 MB (67230117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdd9430c73a732aa248c466dff075f60e0673d76b5a7af2e7675c1f3a90669`  
		Last Modified: Sat, 15 Jun 2024 00:41:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:a3d2c8699f5e864c916187424153b93135c2b4add8548e7675432bc53fd61807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:3.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:aefc3b35390452620d257ac2dfa0a81133ae6d0f4c5abfc5df9cefe2417b1245
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98116634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b61bee6996c212d86bec55a46011d8dcd051c98ede6d5b64e8e17be28ab0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:28:59 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:29:00 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:29:00 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:29:00 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:29:49 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:21:16 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:21:17 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:21:17 GMT
USER kong
# Sat, 15 Jun 2024 00:21:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:21:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:21:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:21:17 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:21:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eaeacb7d14fa5cd15dfc3bfee998b3fc1d5b7a679fe0b3ca64fb9fc5c1fc5f`  
		Last Modified: Wed, 05 Jun 2024 07:31:58 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d9750302f66dbbd904d68dc009bd096ae1e295fbcc60c062fca374ea83cb8d`  
		Last Modified: Sat, 15 Jun 2024 00:22:47 GMT  
		Size: 67.7 MB (67676065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07395a55bfda51337af1c0622d33c891e9903f19de2dc2f4e50a960d5ce097fa`  
		Last Modified: Sat, 15 Jun 2024 00:22:37 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:3.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e388fdd07ab562a159e861687e7b61a2bf312175fd97cd9787070bf59808efee
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95633709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77420d480b60404df779c63c7a33f101b72698933492269a17ec75717a5e0f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 07:08:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 05 Jun 2024 07:08:19 GMT
ARG ASSET=ce
# Wed, 05 Jun 2024 07:08:19 GMT
ENV ASSET=ce
# Wed, 05 Jun 2024 07:08:20 GMT
ARG EE_PORTS
# Wed, 05 Jun 2024 07:08:20 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ENV KONG_VERSION=3.6.1
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Wed, 05 Jun 2024 07:09:17 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Sat, 15 Jun 2024 00:40:17 GMT
# ARGS: KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 15 Jun 2024 00:40:19 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Sat, 15 Jun 2024 00:40:19 GMT
USER kong
# Sat, 15 Jun 2024 00:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 15 Jun 2024 00:40:19 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 15 Jun 2024 00:40:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 15 Jun 2024 00:40:19 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 15 Jun 2024 00:40:19 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcc96be7e4332061f97b8e507e761c542f3616a8d28c86a66b75181ccc819f2`  
		Last Modified: Wed, 05 Jun 2024 07:11:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f099f0061884274828d95293909d9c908211fbd97b94ca687f3311c80d0a59`  
		Last Modified: Sat, 15 Jun 2024 00:41:40 GMT  
		Size: 67.2 MB (67230117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdd9430c73a732aa248c466dff075f60e0673d76b5a7af2e7675c1f3a90669`  
		Last Modified: Sat, 15 Jun 2024 00:41:31 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:3.7`

```console
$ docker pull kong@sha256:43b2e4e47b35deb698f9bb43d1e83a004f7bef9a4380d364bc4916f4751e410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7` - linux; amd64

```console
$ docker pull kong@sha256:74e23e0146aaad4c1afc2e83d4338c9ea386d82b4cf45bafe8c93d4f0e53bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31619876e64e0de610faeb49dba552aa02be48954146ebbbd67694e16ae384f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17d22485ffe58f13f5431d630250008224700f70aa2b2125096dd2ec6f245cb`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36f7d7494853315d1200296062d6486f291641d53d3e1c1a6027c090df3538`  
		Last Modified: Fri, 21 Jun 2024 19:54:30 GMT  
		Size: 67.7 MB (67710059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e46b0537593126b5828f88b6b5d3f0b2e418d4ff9683f1ab6f589a125100b`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:31d6841f6ace121413bafc3e425f0488492a3ae7121d15255bf76d4b0b584bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae62db9ccad2118d424ff506befb470f935cc15ac773f4e94e8da230256ece0`

```dockerfile
```

-	Layers:
	-	`sha256:4c545e37b7f93cca1a63ef5fef8e76335d4f6ce0ffea01987d7aec4d2856c4cc`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81d2a8fdd06bc62afc631eb74c12dccb213bfbbdcea6cad26629a54c478a448`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:948e79d0db128b43cce68183f7b53c98a02ea4c8c12f903483d276b674431f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beed1c0805ca9dc8bbec7a0b810b325a24757d5db5882d58cb3c8f6ebe50cc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc34aa5b67fd3d5a20b6ac0e16b935abfa99e402f7517a4fa319f24093067d1`  
		Last Modified: Fri, 21 Jun 2024 19:55:27 GMT  
		Size: 67.7 MB (67652077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f358c419b9a726292ea393cd121c845aa14adede952a3b658e38fc6d19eb38e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:ab3fd8b5722491f7f4821bac6c67132221c70f85c7e3257bacae6b8c4877794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a610c77baabce0bb3510a6a6d57f1434906621adc965cb192c0760ea943e030`

```dockerfile
```

-	Layers:
	-	`sha256:377f85ee56ab1d04ea7a3501c02c9fad1b509c73763d922a1556af037285942e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77db0cc7f007a3b0c71b549771969f12712599a8f870a2b06920f00ab995864d`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7-ubuntu`

```console
$ docker pull kong@sha256:43b2e4e47b35deb698f9bb43d1e83a004f7bef9a4380d364bc4916f4751e410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:74e23e0146aaad4c1afc2e83d4338c9ea386d82b4cf45bafe8c93d4f0e53bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31619876e64e0de610faeb49dba552aa02be48954146ebbbd67694e16ae384f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17d22485ffe58f13f5431d630250008224700f70aa2b2125096dd2ec6f245cb`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36f7d7494853315d1200296062d6486f291641d53d3e1c1a6027c090df3538`  
		Last Modified: Fri, 21 Jun 2024 19:54:30 GMT  
		Size: 67.7 MB (67710059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e46b0537593126b5828f88b6b5d3f0b2e418d4ff9683f1ab6f589a125100b`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:31d6841f6ace121413bafc3e425f0488492a3ae7121d15255bf76d4b0b584bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae62db9ccad2118d424ff506befb470f935cc15ac773f4e94e8da230256ece0`

```dockerfile
```

-	Layers:
	-	`sha256:4c545e37b7f93cca1a63ef5fef8e76335d4f6ce0ffea01987d7aec4d2856c4cc`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81d2a8fdd06bc62afc631eb74c12dccb213bfbbdcea6cad26629a54c478a448`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:948e79d0db128b43cce68183f7b53c98a02ea4c8c12f903483d276b674431f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beed1c0805ca9dc8bbec7a0b810b325a24757d5db5882d58cb3c8f6ebe50cc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc34aa5b67fd3d5a20b6ac0e16b935abfa99e402f7517a4fa319f24093067d1`  
		Last Modified: Fri, 21 Jun 2024 19:55:27 GMT  
		Size: 67.7 MB (67652077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f358c419b9a726292ea393cd121c845aa14adede952a3b658e38fc6d19eb38e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:ab3fd8b5722491f7f4821bac6c67132221c70f85c7e3257bacae6b8c4877794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a610c77baabce0bb3510a6a6d57f1434906621adc965cb192c0760ea943e030`

```dockerfile
```

-	Layers:
	-	`sha256:377f85ee56ab1d04ea7a3501c02c9fad1b509c73763d922a1556af037285942e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77db0cc7f007a3b0c71b549771969f12712599a8f870a2b06920f00ab995864d`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.1`

```console
$ docker pull kong@sha256:43b2e4e47b35deb698f9bb43d1e83a004f7bef9a4380d364bc4916f4751e410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1` - linux; amd64

```console
$ docker pull kong@sha256:74e23e0146aaad4c1afc2e83d4338c9ea386d82b4cf45bafe8c93d4f0e53bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31619876e64e0de610faeb49dba552aa02be48954146ebbbd67694e16ae384f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17d22485ffe58f13f5431d630250008224700f70aa2b2125096dd2ec6f245cb`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36f7d7494853315d1200296062d6486f291641d53d3e1c1a6027c090df3538`  
		Last Modified: Fri, 21 Jun 2024 19:54:30 GMT  
		Size: 67.7 MB (67710059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e46b0537593126b5828f88b6b5d3f0b2e418d4ff9683f1ab6f589a125100b`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:31d6841f6ace121413bafc3e425f0488492a3ae7121d15255bf76d4b0b584bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae62db9ccad2118d424ff506befb470f935cc15ac773f4e94e8da230256ece0`

```dockerfile
```

-	Layers:
	-	`sha256:4c545e37b7f93cca1a63ef5fef8e76335d4f6ce0ffea01987d7aec4d2856c4cc`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81d2a8fdd06bc62afc631eb74c12dccb213bfbbdcea6cad26629a54c478a448`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:948e79d0db128b43cce68183f7b53c98a02ea4c8c12f903483d276b674431f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beed1c0805ca9dc8bbec7a0b810b325a24757d5db5882d58cb3c8f6ebe50cc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc34aa5b67fd3d5a20b6ac0e16b935abfa99e402f7517a4fa319f24093067d1`  
		Last Modified: Fri, 21 Jun 2024 19:55:27 GMT  
		Size: 67.7 MB (67652077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f358c419b9a726292ea393cd121c845aa14adede952a3b658e38fc6d19eb38e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:ab3fd8b5722491f7f4821bac6c67132221c70f85c7e3257bacae6b8c4877794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a610c77baabce0bb3510a6a6d57f1434906621adc965cb192c0760ea943e030`

```dockerfile
```

-	Layers:
	-	`sha256:377f85ee56ab1d04ea7a3501c02c9fad1b509c73763d922a1556af037285942e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77db0cc7f007a3b0c71b549771969f12712599a8f870a2b06920f00ab995864d`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7.1-ubuntu`

```console
$ docker pull kong@sha256:43b2e4e47b35deb698f9bb43d1e83a004f7bef9a4380d364bc4916f4751e410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:74e23e0146aaad4c1afc2e83d4338c9ea386d82b4cf45bafe8c93d4f0e53bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31619876e64e0de610faeb49dba552aa02be48954146ebbbd67694e16ae384f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17d22485ffe58f13f5431d630250008224700f70aa2b2125096dd2ec6f245cb`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36f7d7494853315d1200296062d6486f291641d53d3e1c1a6027c090df3538`  
		Last Modified: Fri, 21 Jun 2024 19:54:30 GMT  
		Size: 67.7 MB (67710059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e46b0537593126b5828f88b6b5d3f0b2e418d4ff9683f1ab6f589a125100b`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:31d6841f6ace121413bafc3e425f0488492a3ae7121d15255bf76d4b0b584bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae62db9ccad2118d424ff506befb470f935cc15ac773f4e94e8da230256ece0`

```dockerfile
```

-	Layers:
	-	`sha256:4c545e37b7f93cca1a63ef5fef8e76335d4f6ce0ffea01987d7aec4d2856c4cc`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81d2a8fdd06bc62afc631eb74c12dccb213bfbbdcea6cad26629a54c478a448`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.7.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:948e79d0db128b43cce68183f7b53c98a02ea4c8c12f903483d276b674431f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beed1c0805ca9dc8bbec7a0b810b325a24757d5db5882d58cb3c8f6ebe50cc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc34aa5b67fd3d5a20b6ac0e16b935abfa99e402f7517a4fa319f24093067d1`  
		Last Modified: Fri, 21 Jun 2024 19:55:27 GMT  
		Size: 67.7 MB (67652077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f358c419b9a726292ea393cd121c845aa14adede952a3b658e38fc6d19eb38e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:ab3fd8b5722491f7f4821bac6c67132221c70f85c7e3257bacae6b8c4877794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a610c77baabce0bb3510a6a6d57f1434906621adc965cb192c0760ea943e030`

```dockerfile
```

-	Layers:
	-	`sha256:377f85ee56ab1d04ea7a3501c02c9fad1b509c73763d922a1556af037285942e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77db0cc7f007a3b0c71b549771969f12712599a8f870a2b06920f00ab995864d`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:43b2e4e47b35deb698f9bb43d1e83a004f7bef9a4380d364bc4916f4751e410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:74e23e0146aaad4c1afc2e83d4338c9ea386d82b4cf45bafe8c93d4f0e53bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31619876e64e0de610faeb49dba552aa02be48954146ebbbd67694e16ae384f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17d22485ffe58f13f5431d630250008224700f70aa2b2125096dd2ec6f245cb`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36f7d7494853315d1200296062d6486f291641d53d3e1c1a6027c090df3538`  
		Last Modified: Fri, 21 Jun 2024 19:54:30 GMT  
		Size: 67.7 MB (67710059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e46b0537593126b5828f88b6b5d3f0b2e418d4ff9683f1ab6f589a125100b`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:31d6841f6ace121413bafc3e425f0488492a3ae7121d15255bf76d4b0b584bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae62db9ccad2118d424ff506befb470f935cc15ac773f4e94e8da230256ece0`

```dockerfile
```

-	Layers:
	-	`sha256:4c545e37b7f93cca1a63ef5fef8e76335d4f6ce0ffea01987d7aec4d2856c4cc`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81d2a8fdd06bc62afc631eb74c12dccb213bfbbdcea6cad26629a54c478a448`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:948e79d0db128b43cce68183f7b53c98a02ea4c8c12f903483d276b674431f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beed1c0805ca9dc8bbec7a0b810b325a24757d5db5882d58cb3c8f6ebe50cc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc34aa5b67fd3d5a20b6ac0e16b935abfa99e402f7517a4fa319f24093067d1`  
		Last Modified: Fri, 21 Jun 2024 19:55:27 GMT  
		Size: 67.7 MB (67652077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f358c419b9a726292ea393cd121c845aa14adede952a3b658e38fc6d19eb38e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:ab3fd8b5722491f7f4821bac6c67132221c70f85c7e3257bacae6b8c4877794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a610c77baabce0bb3510a6a6d57f1434906621adc965cb192c0760ea943e030`

```dockerfile
```

-	Layers:
	-	`sha256:377f85ee56ab1d04ea7a3501c02c9fad1b509c73763d922a1556af037285942e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77db0cc7f007a3b0c71b549771969f12712599a8f870a2b06920f00ab995864d`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:43b2e4e47b35deb698f9bb43d1e83a004f7bef9a4380d364bc4916f4751e410d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:74e23e0146aaad4c1afc2e83d4338c9ea386d82b4cf45bafe8c93d4f0e53bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31619876e64e0de610faeb49dba552aa02be48954146ebbbd67694e16ae384f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
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
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17d22485ffe58f13f5431d630250008224700f70aa2b2125096dd2ec6f245cb`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f36f7d7494853315d1200296062d6486f291641d53d3e1c1a6027c090df3538`  
		Last Modified: Fri, 21 Jun 2024 19:54:30 GMT  
		Size: 67.7 MB (67710059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e46b0537593126b5828f88b6b5d3f0b2e418d4ff9683f1ab6f589a125100b`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:31d6841f6ace121413bafc3e425f0488492a3ae7121d15255bf76d4b0b584bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae62db9ccad2118d424ff506befb470f935cc15ac773f4e94e8da230256ece0`

```dockerfile
```

-	Layers:
	-	`sha256:4c545e37b7f93cca1a63ef5fef8e76335d4f6ce0ffea01987d7aec4d2856c4cc`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81d2a8fdd06bc62afc631eb74c12dccb213bfbbdcea6cad26629a54c478a448`  
		Last Modified: Fri, 21 Jun 2024 19:54:29 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:948e79d0db128b43cce68183f7b53c98a02ea4c8c12f903483d276b674431f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95015143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beed1c0805ca9dc8bbec7a0b810b325a24757d5db5882d58cb3c8f6ebe50cc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc34aa5b67fd3d5a20b6ac0e16b935abfa99e402f7517a4fa319f24093067d1`  
		Last Modified: Fri, 21 Jun 2024 19:55:27 GMT  
		Size: 67.7 MB (67652077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f358c419b9a726292ea393cd121c845aa14adede952a3b658e38fc6d19eb38e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:ab3fd8b5722491f7f4821bac6c67132221c70f85c7e3257bacae6b8c4877794b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5007291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a610c77baabce0bb3510a6a6d57f1434906621adc965cb192c0760ea943e030`

```dockerfile
```

-	Layers:
	-	`sha256:377f85ee56ab1d04ea7a3501c02c9fad1b509c73763d922a1556af037285942e`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 5.0 MB (4990947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77db0cc7f007a3b0c71b549771969f12712599a8f870a2b06920f00ab995864d`  
		Last Modified: Fri, 21 Jun 2024 19:55:25 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
