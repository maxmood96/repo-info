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
$ docker pull kong@sha256:cfcd1f275211f6032bad2ba02942c8f436236871a58b1634e0d53e2d30aded85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:16304b1903b65110713ce0ec19541de506d5d26984792029eda699e0ab4bf41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185242268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af88bddc079f9bb19d6cafac95d04505c7b62a77416808921bbe909813cd8b77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Jun 2024 13:23:47 GMT
ARG RELEASE
# Tue, 25 Jun 2024 13:23:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 13:23:47 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 25 Jun 2024 13:23:47 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea313535d8947df695bef88d40d2b7bc832e3ef21f2bb2b50c17579798942b6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0b22310f7f18eb5cc81cdc44fe002df75b4038a20d82539ac127871847e79`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 130.6 MB (130625365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f58e46a42f4a2b191eaf47e5f833e24cd34d1a655ac036fc17e1c75301de10`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2` - unknown; unknown

```console
$ docker pull kong@sha256:23a81e0836f93ae3f5a1cd252b4828386fcf5d7f6c83645a80923be21f05d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb95afc43fe547cf45603bd59872834a34e93de756b71c786937506a9ca757ae`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ad016dab488a39338097c9145435fdb0b395ba40b3e763b2748f115cc0c20`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 7.1 MB (7062725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1123f64ab7fd01f733f914e45ca6059bcaa17aaf5ecc56fdcd44d102aa00ba27`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8`

```console
$ docker pull kong@sha256:cfcd1f275211f6032bad2ba02942c8f436236871a58b1634e0d53e2d30aded85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:16304b1903b65110713ce0ec19541de506d5d26984792029eda699e0ab4bf41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185242268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af88bddc079f9bb19d6cafac95d04505c7b62a77416808921bbe909813cd8b77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Jun 2024 13:23:47 GMT
ARG RELEASE
# Tue, 25 Jun 2024 13:23:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 13:23:47 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 25 Jun 2024 13:23:47 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea313535d8947df695bef88d40d2b7bc832e3ef21f2bb2b50c17579798942b6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0b22310f7f18eb5cc81cdc44fe002df75b4038a20d82539ac127871847e79`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 130.6 MB (130625365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f58e46a42f4a2b191eaf47e5f833e24cd34d1a655ac036fc17e1c75301de10`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8` - unknown; unknown

```console
$ docker pull kong@sha256:23a81e0836f93ae3f5a1cd252b4828386fcf5d7f6c83645a80923be21f05d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb95afc43fe547cf45603bd59872834a34e93de756b71c786937506a9ca757ae`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ad016dab488a39338097c9145435fdb0b395ba40b3e763b2748f115cc0c20`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 7.1 MB (7062725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1123f64ab7fd01f733f914e45ca6059bcaa17aaf5ecc56fdcd44d102aa00ba27`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:cfcd1f275211f6032bad2ba02942c8f436236871a58b1634e0d53e2d30aded85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:16304b1903b65110713ce0ec19541de506d5d26984792029eda699e0ab4bf41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185242268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af88bddc079f9bb19d6cafac95d04505c7b62a77416808921bbe909813cd8b77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Jun 2024 13:23:47 GMT
ARG RELEASE
# Tue, 25 Jun 2024 13:23:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 13:23:47 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 25 Jun 2024 13:23:47 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea313535d8947df695bef88d40d2b7bc832e3ef21f2bb2b50c17579798942b6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0b22310f7f18eb5cc81cdc44fe002df75b4038a20d82539ac127871847e79`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 130.6 MB (130625365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f58e46a42f4a2b191eaf47e5f833e24cd34d1a655ac036fc17e1c75301de10`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:23a81e0836f93ae3f5a1cd252b4828386fcf5d7f6c83645a80923be21f05d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb95afc43fe547cf45603bd59872834a34e93de756b71c786937506a9ca757ae`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ad016dab488a39338097c9145435fdb0b395ba40b3e763b2748f115cc0c20`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 7.1 MB (7062725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1123f64ab7fd01f733f914e45ca6059bcaa17aaf5ecc56fdcd44d102aa00ba27`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5`

```console
$ docker pull kong@sha256:cfcd1f275211f6032bad2ba02942c8f436236871a58b1634e0d53e2d30aded85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5` - linux; amd64

```console
$ docker pull kong@sha256:16304b1903b65110713ce0ec19541de506d5d26984792029eda699e0ab4bf41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185242268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af88bddc079f9bb19d6cafac95d04505c7b62a77416808921bbe909813cd8b77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Jun 2024 13:23:47 GMT
ARG RELEASE
# Tue, 25 Jun 2024 13:23:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 13:23:47 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 25 Jun 2024 13:23:47 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea313535d8947df695bef88d40d2b7bc832e3ef21f2bb2b50c17579798942b6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0b22310f7f18eb5cc81cdc44fe002df75b4038a20d82539ac127871847e79`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 130.6 MB (130625365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f58e46a42f4a2b191eaf47e5f833e24cd34d1a655ac036fc17e1c75301de10`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5` - unknown; unknown

```console
$ docker pull kong@sha256:23a81e0836f93ae3f5a1cd252b4828386fcf5d7f6c83645a80923be21f05d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb95afc43fe547cf45603bd59872834a34e93de756b71c786937506a9ca757ae`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ad016dab488a39338097c9145435fdb0b395ba40b3e763b2748f115cc0c20`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 7.1 MB (7062725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1123f64ab7fd01f733f914e45ca6059bcaa17aaf5ecc56fdcd44d102aa00ba27`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:cfcd1f275211f6032bad2ba02942c8f436236871a58b1634e0d53e2d30aded85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:16304b1903b65110713ce0ec19541de506d5d26984792029eda699e0ab4bf41d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185242268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af88bddc079f9bb19d6cafac95d04505c7b62a77416808921bbe909813cd8b77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 25 Jun 2024 13:23:47 GMT
ARG RELEASE
# Tue, 25 Jun 2024 13:23:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Jun 2024 13:23:47 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Jun 2024 13:23:47 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 25 Jun 2024 13:23:47 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea313535d8947df695bef88d40d2b7bc832e3ef21f2bb2b50c17579798942b6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 25.1 MB (25081965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0b22310f7f18eb5cc81cdc44fe002df75b4038a20d82539ac127871847e79`  
		Last Modified: Tue, 02 Jul 2024 03:04:12 GMT  
		Size: 130.6 MB (130625365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f58e46a42f4a2b191eaf47e5f833e24cd34d1a655ac036fc17e1c75301de10`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:23a81e0836f93ae3f5a1cd252b4828386fcf5d7f6c83645a80923be21f05d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb95afc43fe547cf45603bd59872834a34e93de756b71c786937506a9ca757ae`

```dockerfile
```

-	Layers:
	-	`sha256:7e8ad016dab488a39338097c9145435fdb0b395ba40b3e763b2748f115cc0c20`  
		Last Modified: Tue, 02 Jul 2024 03:04:10 GMT  
		Size: 7.1 MB (7062725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1123f64ab7fd01f733f914e45ca6059bcaa17aaf5ecc56fdcd44d102aa00ba27`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 15.1 KB (15096 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:2799758c97191e22b84d88d611387f21fc4503c186a8029621c41658d2469e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:2fe48406624ba014286502e71912663c57b05e663e6863389e92c6d01a3c2102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8047104cfac02de210edac6773b1072736c8dc3caf6d220e939760fa5c0aeda5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea0c3e76a3b5827ab771114ec792b49b7673d063ccf35d5ef374f57af60ab42`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc789aa436d5f3ae6e1d1d0a57aa5f543bd7ff7a0dd5d2fca51b2e9335fd3de`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 67.7 MB (67710110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf088c8a9d718696c3a6aa9c88bd905040f8d0bc18397ab016ded447517c1a6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:e39f49ea77f7f75248f0f556936df8d72c14d20ec6fb51bc8651f0b113ccace6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17501e767e6400dd5f28991966cd06f12fddb029b6f07b054ed881c9249b3fd1`

```dockerfile
```

-	Layers:
	-	`sha256:59d0fe55fd07a1ebeaec261834e9ea2d9e63d94f149fd4a81bdd8835776ff214`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d195a25a0cba96c6815b22d0bed6c6afa3539bafad4deeb8290db3238d762256`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
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
$ docker pull kong@sha256:d4b478d5f4848a6b0b2936b1ee81a32a05239864abcca69a47b878983f043638
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:bc03006f1f727d856718a8d365b330379911fc44372522de6bbd1ff8e5ca4a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92280858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dab8e0a98a4cb6963efe79c6bbf6583dd19e554f6ffc08cf7aea35d60252f38`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1e0be55f81745a5ef671894eabd74a8c9d8f77fa96d6d230faa9ea516f31f7`  
		Last Modified: Tue, 02 Jul 2024 03:04:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ce972fa3c27f5a20faa527320f53524d5e2d884768a587af1021c900c99bab`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 62.7 MB (62745515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a3ebf2da8713bc7787acb7e3ed9e731ebb685dd8f264b11c24739b95cd17e`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:be551a3096b84637237754be9480d434d7447b30d84839f0316aeea3143f3e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5889852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce46f6abe9969d4147de55a94cd5294635c3171985f631788a6a1bab62c905d7`

```dockerfile
```

-	Layers:
	-	`sha256:2e5cf2b3d742a96987601e7c7e1f3f8df76908aa465fe104c3e59ef6d9a9e259`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 5.9 MB (5874718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2df2190021f0ae8f06c1b1df87148ad87ed7694187d898dfbf96335a28a85e`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:16aedba05be887abbec7cc8fd111d043a2f2bccf8bd23aaa64b1b391c903fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88531646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7fee897d4b79e298c8e33b5b9bfad65ca6a916336dd1e95f42776448b65f2b`
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a96bd4da9fba6fd270c17eaf0ffcf82c63dd7c18438ede411f14561a16ef4fd`  
		Last Modified: Wed, 26 Jun 2024 17:01:09 GMT  
		Size: 61.2 MB (61168581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116a5e0e9418e0fb6a179376d0d40c3a50ec9d0f30e996f1cc83800544306400`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:106a77d6bcccd9b60dea2ba177cafb3d3d562c6ee49157e6c9eb945bff4d9b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5868203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8880aca7fcd24eb87384a93f3de03b3176f2a5bae451ed013b13de1248b220`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2e7082f0c10db884a5841981c8bca5eedc8d2b4e1599da7d535548ae5c3b0`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 5.9 MB (5852767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:409e658d423e1a8f163df497f0e3e9e72d792bf27831938134dc1653c82288b3`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:d4b478d5f4848a6b0b2936b1ee81a32a05239864abcca69a47b878983f043638
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:bc03006f1f727d856718a8d365b330379911fc44372522de6bbd1ff8e5ca4a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92280858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dab8e0a98a4cb6963efe79c6bbf6583dd19e554f6ffc08cf7aea35d60252f38`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1e0be55f81745a5ef671894eabd74a8c9d8f77fa96d6d230faa9ea516f31f7`  
		Last Modified: Tue, 02 Jul 2024 03:04:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ce972fa3c27f5a20faa527320f53524d5e2d884768a587af1021c900c99bab`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 62.7 MB (62745515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a3ebf2da8713bc7787acb7e3ed9e731ebb685dd8f264b11c24739b95cd17e`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:be551a3096b84637237754be9480d434d7447b30d84839f0316aeea3143f3e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5889852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce46f6abe9969d4147de55a94cd5294635c3171985f631788a6a1bab62c905d7`

```dockerfile
```

-	Layers:
	-	`sha256:2e5cf2b3d742a96987601e7c7e1f3f8df76908aa465fe104c3e59ef6d9a9e259`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 5.9 MB (5874718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2df2190021f0ae8f06c1b1df87148ad87ed7694187d898dfbf96335a28a85e`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:16aedba05be887abbec7cc8fd111d043a2f2bccf8bd23aaa64b1b391c903fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88531646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7fee897d4b79e298c8e33b5b9bfad65ca6a916336dd1e95f42776448b65f2b`
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a96bd4da9fba6fd270c17eaf0ffcf82c63dd7c18438ede411f14561a16ef4fd`  
		Last Modified: Wed, 26 Jun 2024 17:01:09 GMT  
		Size: 61.2 MB (61168581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116a5e0e9418e0fb6a179376d0d40c3a50ec9d0f30e996f1cc83800544306400`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:106a77d6bcccd9b60dea2ba177cafb3d3d562c6ee49157e6c9eb945bff4d9b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5868203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8880aca7fcd24eb87384a93f3de03b3176f2a5bae451ed013b13de1248b220`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2e7082f0c10db884a5841981c8bca5eedc8d2b4e1599da7d535548ae5c3b0`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 5.9 MB (5852767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:409e658d423e1a8f163df497f0e3e9e72d792bf27831938134dc1653c82288b3`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:d4b478d5f4848a6b0b2936b1ee81a32a05239864abcca69a47b878983f043638
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:bc03006f1f727d856718a8d365b330379911fc44372522de6bbd1ff8e5ca4a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92280858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dab8e0a98a4cb6963efe79c6bbf6583dd19e554f6ffc08cf7aea35d60252f38`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1e0be55f81745a5ef671894eabd74a8c9d8f77fa96d6d230faa9ea516f31f7`  
		Last Modified: Tue, 02 Jul 2024 03:04:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ce972fa3c27f5a20faa527320f53524d5e2d884768a587af1021c900c99bab`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 62.7 MB (62745515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a3ebf2da8713bc7787acb7e3ed9e731ebb685dd8f264b11c24739b95cd17e`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:be551a3096b84637237754be9480d434d7447b30d84839f0316aeea3143f3e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5889852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce46f6abe9969d4147de55a94cd5294635c3171985f631788a6a1bab62c905d7`

```dockerfile
```

-	Layers:
	-	`sha256:2e5cf2b3d742a96987601e7c7e1f3f8df76908aa465fe104c3e59ef6d9a9e259`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 5.9 MB (5874718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2df2190021f0ae8f06c1b1df87148ad87ed7694187d898dfbf96335a28a85e`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:16aedba05be887abbec7cc8fd111d043a2f2bccf8bd23aaa64b1b391c903fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88531646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7fee897d4b79e298c8e33b5b9bfad65ca6a916336dd1e95f42776448b65f2b`
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a96bd4da9fba6fd270c17eaf0ffcf82c63dd7c18438ede411f14561a16ef4fd`  
		Last Modified: Wed, 26 Jun 2024 17:01:09 GMT  
		Size: 61.2 MB (61168581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116a5e0e9418e0fb6a179376d0d40c3a50ec9d0f30e996f1cc83800544306400`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:106a77d6bcccd9b60dea2ba177cafb3d3d562c6ee49157e6c9eb945bff4d9b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5868203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8880aca7fcd24eb87384a93f3de03b3176f2a5bae451ed013b13de1248b220`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2e7082f0c10db884a5841981c8bca5eedc8d2b4e1599da7d535548ae5c3b0`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 5.9 MB (5852767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:409e658d423e1a8f163df497f0e3e9e72d792bf27831938134dc1653c82288b3`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:d4b478d5f4848a6b0b2936b1ee81a32a05239864abcca69a47b878983f043638
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:bc03006f1f727d856718a8d365b330379911fc44372522de6bbd1ff8e5ca4a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92280858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dab8e0a98a4cb6963efe79c6bbf6583dd19e554f6ffc08cf7aea35d60252f38`
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
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1e0be55f81745a5ef671894eabd74a8c9d8f77fa96d6d230faa9ea516f31f7`  
		Last Modified: Tue, 02 Jul 2024 03:04:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ce972fa3c27f5a20faa527320f53524d5e2d884768a587af1021c900c99bab`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 62.7 MB (62745515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a3ebf2da8713bc7787acb7e3ed9e731ebb685dd8f264b11c24739b95cd17e`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:be551a3096b84637237754be9480d434d7447b30d84839f0316aeea3143f3e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5889852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce46f6abe9969d4147de55a94cd5294635c3171985f631788a6a1bab62c905d7`

```dockerfile
```

-	Layers:
	-	`sha256:2e5cf2b3d742a96987601e7c7e1f3f8df76908aa465fe104c3e59ef6d9a9e259`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 5.9 MB (5874718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b2df2190021f0ae8f06c1b1df87148ad87ed7694187d898dfbf96335a28a85e`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 15.1 KB (15134 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:16aedba05be887abbec7cc8fd111d043a2f2bccf8bd23aaa64b1b391c903fc63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88531646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7fee897d4b79e298c8e33b5b9bfad65ca6a916336dd1e95f42776448b65f2b`
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee58e65c61f38e8b9d03bf4607c9d4c619ca530e0d2c7502ffbd5d67f16fd0d2`  
		Last Modified: Fri, 21 Jun 2024 07:30:45 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a96bd4da9fba6fd270c17eaf0ffcf82c63dd7c18438ede411f14561a16ef4fd`  
		Last Modified: Wed, 26 Jun 2024 17:01:09 GMT  
		Size: 61.2 MB (61168581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116a5e0e9418e0fb6a179376d0d40c3a50ec9d0f30e996f1cc83800544306400`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:106a77d6bcccd9b60dea2ba177cafb3d3d562c6ee49157e6c9eb945bff4d9b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5868203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8880aca7fcd24eb87384a93f3de03b3176f2a5bae451ed013b13de1248b220`

```dockerfile
```

-	Layers:
	-	`sha256:e6e2e7082f0c10db884a5841981c8bca5eedc8d2b4e1599da7d535548ae5c3b0`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 5.9 MB (5852767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:409e658d423e1a8f163df497f0e3e9e72d792bf27831938134dc1653c82288b3`  
		Last Modified: Wed, 26 Jun 2024 17:01:07 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.5`

```console
$ docker pull kong@sha256:7f3309070e36c7057eb88e538323bca006021e762419e815bb784249e261dd56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.5` - linux; amd64

```console
$ docker pull kong@sha256:8ef188005bff1197ca0428d5191d11f9d317ef4779d2261179917acd91b32f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93497217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc158c98b2df2f0b840be255872ade612fd623cee5221889f778d5b4d6d9fcb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:29 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:29 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 14 Jun 2024 20:58:29 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:29 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ENV KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 14 Jun 2024 20:58:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.5.0 KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
USER kong
# Fri, 14 Jun 2024 20:58:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e72e64e716ca59fdced8d3a6b81f6968051d95623e6ded5407ffbf6f50bc`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3922a7100147513f153fda04c766d121396993cee75c76e3b11bbe10acdce134`  
		Last Modified: Tue, 02 Jul 2024 03:04:08 GMT  
		Size: 64.0 MB (63961874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f15e0a49ac6f3d6669dbbd67e34da7def932a3741c00c57388fa4ebb4774e7`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.5` - unknown; unknown

```console
$ docker pull kong@sha256:e1cddd6780b31b6d825eb0a2d195fe44faf154fee171be901108b1b52c4e093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4877968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d748bd1ad061e675661774b70ed224fffe8dd607aa1595b3caebda2303dcd`

```dockerfile
```

-	Layers:
	-	`sha256:0aea6129930d9b10e8730a97fa426518db6866ee0c39874f5f6a50fe6d19a29a`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 4.9 MB (4862833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1333f356003ff87af8199c8869b7d962ea7dc5e59ac4b859866f98faae3fc748`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2c93119914fad3f261fc8716960fbb3088cdbcb0b4c2df26864946f8d0195046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90844319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cf346b9d3532707a59d2c94827adfb5b739c8d9d189174106e2a93f327002`
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
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:29 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ENV KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 14 Jun 2024 20:58:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.5.0 KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
USER kong
# Fri, 14 Jun 2024 20:58:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:29 GMT
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
	-	`sha256:bde9317874925d662facc431af8bf7809b452e7f9d3db75aa5f9d9dd606fa032`  
		Last Modified: Wed, 26 Jun 2024 16:59:53 GMT  
		Size: 63.5 MB (63481253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fd9c751afc9f44db027a482e80cc70158c1c5526468287a25f0d530439b511`  
		Last Modified: Wed, 26 Jun 2024 16:59:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.5` - unknown; unknown

```console
$ docker pull kong@sha256:67c9581ecc0d72917ffeeb542e4897d93b0f45155bdefc16e0980dd8bfb71a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4884601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf784837f2a7020f526c5a7fac24f9147228928c90a9c6553359c19df2eb94c`

```dockerfile
```

-	Layers:
	-	`sha256:92f7a86a9d4c35ca766cf0fd59829a0b0d33fd829dfedca3e40376726086e56e`  
		Last Modified: Wed, 26 Jun 2024 16:59:51 GMT  
		Size: 4.9 MB (4869165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845d103b458c8ea1cad6c825acdcc512fb03579f2b2e49abb3714da0aac934b9`  
		Last Modified: Wed, 26 Jun 2024 16:59:50 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.5-ubuntu`

```console
$ docker pull kong@sha256:7f3309070e36c7057eb88e538323bca006021e762419e815bb784249e261dd56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8ef188005bff1197ca0428d5191d11f9d317ef4779d2261179917acd91b32f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93497217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc158c98b2df2f0b840be255872ade612fd623cee5221889f778d5b4d6d9fcb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:29 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:29 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 14 Jun 2024 20:58:29 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:29 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ENV KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 14 Jun 2024 20:58:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.5.0 KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
USER kong
# Fri, 14 Jun 2024 20:58:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e72e64e716ca59fdced8d3a6b81f6968051d95623e6ded5407ffbf6f50bc`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3922a7100147513f153fda04c766d121396993cee75c76e3b11bbe10acdce134`  
		Last Modified: Tue, 02 Jul 2024 03:04:08 GMT  
		Size: 64.0 MB (63961874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f15e0a49ac6f3d6669dbbd67e34da7def932a3741c00c57388fa4ebb4774e7`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e1cddd6780b31b6d825eb0a2d195fe44faf154fee171be901108b1b52c4e093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4877968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d748bd1ad061e675661774b70ed224fffe8dd607aa1595b3caebda2303dcd`

```dockerfile
```

-	Layers:
	-	`sha256:0aea6129930d9b10e8730a97fa426518db6866ee0c39874f5f6a50fe6d19a29a`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 4.9 MB (4862833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1333f356003ff87af8199c8869b7d962ea7dc5e59ac4b859866f98faae3fc748`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2c93119914fad3f261fc8716960fbb3088cdbcb0b4c2df26864946f8d0195046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90844319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cf346b9d3532707a59d2c94827adfb5b739c8d9d189174106e2a93f327002`
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
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:29 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ENV KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 14 Jun 2024 20:58:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.5.0 KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
USER kong
# Fri, 14 Jun 2024 20:58:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:29 GMT
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
	-	`sha256:bde9317874925d662facc431af8bf7809b452e7f9d3db75aa5f9d9dd606fa032`  
		Last Modified: Wed, 26 Jun 2024 16:59:53 GMT  
		Size: 63.5 MB (63481253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fd9c751afc9f44db027a482e80cc70158c1c5526468287a25f0d530439b511`  
		Last Modified: Wed, 26 Jun 2024 16:59:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:67c9581ecc0d72917ffeeb542e4897d93b0f45155bdefc16e0980dd8bfb71a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4884601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf784837f2a7020f526c5a7fac24f9147228928c90a9c6553359c19df2eb94c`

```dockerfile
```

-	Layers:
	-	`sha256:92f7a86a9d4c35ca766cf0fd59829a0b0d33fd829dfedca3e40376726086e56e`  
		Last Modified: Wed, 26 Jun 2024 16:59:51 GMT  
		Size: 4.9 MB (4869165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845d103b458c8ea1cad6c825acdcc512fb03579f2b2e49abb3714da0aac934b9`  
		Last Modified: Wed, 26 Jun 2024 16:59:50 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.5.0`

```console
$ docker pull kong@sha256:7f3309070e36c7057eb88e538323bca006021e762419e815bb784249e261dd56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.5.0` - linux; amd64

```console
$ docker pull kong@sha256:8ef188005bff1197ca0428d5191d11f9d317ef4779d2261179917acd91b32f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93497217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc158c98b2df2f0b840be255872ade612fd623cee5221889f778d5b4d6d9fcb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:29 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:29 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 14 Jun 2024 20:58:29 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:29 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ENV KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 14 Jun 2024 20:58:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.5.0 KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
USER kong
# Fri, 14 Jun 2024 20:58:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e72e64e716ca59fdced8d3a6b81f6968051d95623e6ded5407ffbf6f50bc`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3922a7100147513f153fda04c766d121396993cee75c76e3b11bbe10acdce134`  
		Last Modified: Tue, 02 Jul 2024 03:04:08 GMT  
		Size: 64.0 MB (63961874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f15e0a49ac6f3d6669dbbd67e34da7def932a3741c00c57388fa4ebb4774e7`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.5.0` - unknown; unknown

```console
$ docker pull kong@sha256:e1cddd6780b31b6d825eb0a2d195fe44faf154fee171be901108b1b52c4e093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4877968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d748bd1ad061e675661774b70ed224fffe8dd607aa1595b3caebda2303dcd`

```dockerfile
```

-	Layers:
	-	`sha256:0aea6129930d9b10e8730a97fa426518db6866ee0c39874f5f6a50fe6d19a29a`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 4.9 MB (4862833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1333f356003ff87af8199c8869b7d962ea7dc5e59ac4b859866f98faae3fc748`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.5.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2c93119914fad3f261fc8716960fbb3088cdbcb0b4c2df26864946f8d0195046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90844319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cf346b9d3532707a59d2c94827adfb5b739c8d9d189174106e2a93f327002`
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
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:29 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ENV KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 14 Jun 2024 20:58:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.5.0 KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
USER kong
# Fri, 14 Jun 2024 20:58:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:29 GMT
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
	-	`sha256:bde9317874925d662facc431af8bf7809b452e7f9d3db75aa5f9d9dd606fa032`  
		Last Modified: Wed, 26 Jun 2024 16:59:53 GMT  
		Size: 63.5 MB (63481253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fd9c751afc9f44db027a482e80cc70158c1c5526468287a25f0d530439b511`  
		Last Modified: Wed, 26 Jun 2024 16:59:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.5.0` - unknown; unknown

```console
$ docker pull kong@sha256:67c9581ecc0d72917ffeeb542e4897d93b0f45155bdefc16e0980dd8bfb71a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4884601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf784837f2a7020f526c5a7fac24f9147228928c90a9c6553359c19df2eb94c`

```dockerfile
```

-	Layers:
	-	`sha256:92f7a86a9d4c35ca766cf0fd59829a0b0d33fd829dfedca3e40376726086e56e`  
		Last Modified: Wed, 26 Jun 2024 16:59:51 GMT  
		Size: 4.9 MB (4869165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845d103b458c8ea1cad6c825acdcc512fb03579f2b2e49abb3714da0aac934b9`  
		Last Modified: Wed, 26 Jun 2024 16:59:50 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.5.0-ubuntu`

```console
$ docker pull kong@sha256:7f3309070e36c7057eb88e538323bca006021e762419e815bb784249e261dd56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.5.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8ef188005bff1197ca0428d5191d11f9d317ef4779d2261179917acd91b32f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93497217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc158c98b2df2f0b840be255872ade612fd623cee5221889f778d5b4d6d9fcb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:58:29 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:58:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:58:29 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 14 Jun 2024 20:58:29 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:29 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ENV KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 14 Jun 2024 20:58:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.5.0 KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
USER kong
# Fri, 14 Jun 2024 20:58:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e72e64e716ca59fdced8d3a6b81f6968051d95623e6ded5407ffbf6f50bc`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3922a7100147513f153fda04c766d121396993cee75c76e3b11bbe10acdce134`  
		Last Modified: Tue, 02 Jul 2024 03:04:08 GMT  
		Size: 64.0 MB (63961874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f15e0a49ac6f3d6669dbbd67e34da7def932a3741c00c57388fa4ebb4774e7`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.5.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e1cddd6780b31b6d825eb0a2d195fe44faf154fee171be901108b1b52c4e093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4877968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d748bd1ad061e675661774b70ed224fffe8dd607aa1595b3caebda2303dcd`

```dockerfile
```

-	Layers:
	-	`sha256:0aea6129930d9b10e8730a97fa426518db6866ee0c39874f5f6a50fe6d19a29a`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 4.9 MB (4862833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1333f356003ff87af8199c8869b7d962ea7dc5e59ac4b859866f98faae3fc748`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.5.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2c93119914fad3f261fc8716960fbb3088cdbcb0b4c2df26864946f8d0195046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90844319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cf346b9d3532707a59d2c94827adfb5b739c8d9d189174106e2a93f327002`
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
# Fri, 14 Jun 2024 20:58:29 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:58:29 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:58:29 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:58:29 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ENV KONG_VERSION=3.5.0
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d
# Fri, 14 Jun 2024 20:58:29 GMT
ARG KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
# Fri, 14 Jun 2024 20:58:29 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.5.0 KONG_AMD64_SHA=ad00de50a799f533e0e88d10063022b41e52bc50fa3c9169ce451c9561e2cd5d KONG_ARM64_SHA=d34c29ba688986f2bb23e118478f450d8a49755d1178ecc5d7184e46944b4881
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:58:29 GMT
USER kong
# Fri, 14 Jun 2024 20:58:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:58:29 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:58:29 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:58:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:58:29 GMT
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
	-	`sha256:bde9317874925d662facc431af8bf7809b452e7f9d3db75aa5f9d9dd606fa032`  
		Last Modified: Wed, 26 Jun 2024 16:59:53 GMT  
		Size: 63.5 MB (63481253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fd9c751afc9f44db027a482e80cc70158c1c5526468287a25f0d530439b511`  
		Last Modified: Wed, 26 Jun 2024 16:59:50 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.5.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:67c9581ecc0d72917ffeeb542e4897d93b0f45155bdefc16e0980dd8bfb71a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4884601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf784837f2a7020f526c5a7fac24f9147228928c90a9c6553359c19df2eb94c`

```dockerfile
```

-	Layers:
	-	`sha256:92f7a86a9d4c35ca766cf0fd59829a0b0d33fd829dfedca3e40376726086e56e`  
		Last Modified: Wed, 26 Jun 2024 16:59:51 GMT  
		Size: 4.9 MB (4869165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:845d103b458c8ea1cad6c825acdcc512fb03579f2b2e49abb3714da0aac934b9`  
		Last Modified: Wed, 26 Jun 2024 16:59:50 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6`

```console
$ docker pull kong@sha256:1e20f713f8c64bd19aebf1dcf4e6249e6985f01353d047b6438efc0ac5e5d698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6` - linux; amd64

```console
$ docker pull kong@sha256:9020aa8ba901210f51d2b2a3452f245a2733bb120cfb1ea701202c2acdc46363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97207603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5caf7cdcaca51c3183d1b7ab6e7073cd7317e31a4e868afe799365eadb2b919`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e72e64e716ca59fdced8d3a6b81f6968051d95623e6ded5407ffbf6f50bc`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eb602a30a3cc237e21a749b77c8b010bfae3cf50a2d637e3ebe69bcc27c4a1`  
		Last Modified: Tue, 02 Jul 2024 03:04:08 GMT  
		Size: 67.7 MB (67672260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f15e0a49ac6f3d6669dbbd67e34da7def932a3741c00c57388fa4ebb4774e7`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:e14776380baf5054f5e13565c13d8826af1e9afc9e953600d68235c5f7dd8125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d44ea0ce0ceb8b373c7934508eb986c1d69f0dcc48830cde4113369b76a4cf8`

```dockerfile
```

-	Layers:
	-	`sha256:ae88c05ee4d394fcce8d5aebc8fa24b2c4f768b66dbeccdfc284a4fb50be049e`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 4.9 MB (4905266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07b8d2ffb76a26caf00b5ad24c4d6d837580a525422c3680d1418fa2eb8a9b0`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40ff25f8550f7cb4efab721d6364270a846a40f1e844aaff569b4013a0159e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94588256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f303a21e31799e3cd77b5bd712076050ee9fc5073a5fc1d5e0b2fc9f0cf423`
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
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
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
	-	`sha256:e0b39fb67d651276a4d94d94ee3982d275ba566a848847ad3076a363d8f11fdc`  
		Last Modified: Wed, 26 Jun 2024 16:58:58 GMT  
		Size: 67.2 MB (67225189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79ff05e556d68ee630399eb3badd226b08a98e9808bffc2b68c67fed08ce8a5`  
		Last Modified: Wed, 26 Jun 2024 16:58:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6` - unknown; unknown

```console
$ docker pull kong@sha256:1b056341629c0056bacd27cc6fb5bb70d066be2a53fde471c5b38d015dfb7c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa00184a6564c67781046bb4bcc8bced799c3644b1808040b43f1c62f481b6b4`

```dockerfile
```

-	Layers:
	-	`sha256:24cafb285797b15fd78b10da624cc17c412cba61952d349ac5ba5023fe420778`  
		Last Modified: Wed, 26 Jun 2024 16:58:56 GMT  
		Size: 4.9 MB (4911598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbbab9a07df77fef4a13d73192c611fb63ce9dd32158b3ac8d05dffffb690e43`  
		Last Modified: Wed, 26 Jun 2024 16:58:55 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6-ubuntu`

```console
$ docker pull kong@sha256:1e20f713f8c64bd19aebf1dcf4e6249e6985f01353d047b6438efc0ac5e5d698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9020aa8ba901210f51d2b2a3452f245a2733bb120cfb1ea701202c2acdc46363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97207603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5caf7cdcaca51c3183d1b7ab6e7073cd7317e31a4e868afe799365eadb2b919`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e72e64e716ca59fdced8d3a6b81f6968051d95623e6ded5407ffbf6f50bc`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eb602a30a3cc237e21a749b77c8b010bfae3cf50a2d637e3ebe69bcc27c4a1`  
		Last Modified: Tue, 02 Jul 2024 03:04:08 GMT  
		Size: 67.7 MB (67672260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f15e0a49ac6f3d6669dbbd67e34da7def932a3741c00c57388fa4ebb4774e7`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e14776380baf5054f5e13565c13d8826af1e9afc9e953600d68235c5f7dd8125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d44ea0ce0ceb8b373c7934508eb986c1d69f0dcc48830cde4113369b76a4cf8`

```dockerfile
```

-	Layers:
	-	`sha256:ae88c05ee4d394fcce8d5aebc8fa24b2c4f768b66dbeccdfc284a4fb50be049e`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 4.9 MB (4905266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07b8d2ffb76a26caf00b5ad24c4d6d837580a525422c3680d1418fa2eb8a9b0`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40ff25f8550f7cb4efab721d6364270a846a40f1e844aaff569b4013a0159e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94588256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f303a21e31799e3cd77b5bd712076050ee9fc5073a5fc1d5e0b2fc9f0cf423`
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
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
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
	-	`sha256:e0b39fb67d651276a4d94d94ee3982d275ba566a848847ad3076a363d8f11fdc`  
		Last Modified: Wed, 26 Jun 2024 16:58:58 GMT  
		Size: 67.2 MB (67225189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79ff05e556d68ee630399eb3badd226b08a98e9808bffc2b68c67fed08ce8a5`  
		Last Modified: Wed, 26 Jun 2024 16:58:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1b056341629c0056bacd27cc6fb5bb70d066be2a53fde471c5b38d015dfb7c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa00184a6564c67781046bb4bcc8bced799c3644b1808040b43f1c62f481b6b4`

```dockerfile
```

-	Layers:
	-	`sha256:24cafb285797b15fd78b10da624cc17c412cba61952d349ac5ba5023fe420778`  
		Last Modified: Wed, 26 Jun 2024 16:58:56 GMT  
		Size: 4.9 MB (4911598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbbab9a07df77fef4a13d73192c611fb63ce9dd32158b3ac8d05dffffb690e43`  
		Last Modified: Wed, 26 Jun 2024 16:58:55 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6.1`

```console
$ docker pull kong@sha256:1e20f713f8c64bd19aebf1dcf4e6249e6985f01353d047b6438efc0ac5e5d698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1` - linux; amd64

```console
$ docker pull kong@sha256:9020aa8ba901210f51d2b2a3452f245a2733bb120cfb1ea701202c2acdc46363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97207603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5caf7cdcaca51c3183d1b7ab6e7073cd7317e31a4e868afe799365eadb2b919`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e72e64e716ca59fdced8d3a6b81f6968051d95623e6ded5407ffbf6f50bc`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eb602a30a3cc237e21a749b77c8b010bfae3cf50a2d637e3ebe69bcc27c4a1`  
		Last Modified: Tue, 02 Jul 2024 03:04:08 GMT  
		Size: 67.7 MB (67672260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f15e0a49ac6f3d6669dbbd67e34da7def932a3741c00c57388fa4ebb4774e7`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:e14776380baf5054f5e13565c13d8826af1e9afc9e953600d68235c5f7dd8125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d44ea0ce0ceb8b373c7934508eb986c1d69f0dcc48830cde4113369b76a4cf8`

```dockerfile
```

-	Layers:
	-	`sha256:ae88c05ee4d394fcce8d5aebc8fa24b2c4f768b66dbeccdfc284a4fb50be049e`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 4.9 MB (4905266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07b8d2ffb76a26caf00b5ad24c4d6d837580a525422c3680d1418fa2eb8a9b0`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40ff25f8550f7cb4efab721d6364270a846a40f1e844aaff569b4013a0159e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94588256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f303a21e31799e3cd77b5bd712076050ee9fc5073a5fc1d5e0b2fc9f0cf423`
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
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
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
	-	`sha256:e0b39fb67d651276a4d94d94ee3982d275ba566a848847ad3076a363d8f11fdc`  
		Last Modified: Wed, 26 Jun 2024 16:58:58 GMT  
		Size: 67.2 MB (67225189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79ff05e556d68ee630399eb3badd226b08a98e9808bffc2b68c67fed08ce8a5`  
		Last Modified: Wed, 26 Jun 2024 16:58:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1` - unknown; unknown

```console
$ docker pull kong@sha256:1b056341629c0056bacd27cc6fb5bb70d066be2a53fde471c5b38d015dfb7c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa00184a6564c67781046bb4bcc8bced799c3644b1808040b43f1c62f481b6b4`

```dockerfile
```

-	Layers:
	-	`sha256:24cafb285797b15fd78b10da624cc17c412cba61952d349ac5ba5023fe420778`  
		Last Modified: Wed, 26 Jun 2024 16:58:56 GMT  
		Size: 4.9 MB (4911598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbbab9a07df77fef4a13d73192c611fb63ce9dd32158b3ac8d05dffffb690e43`  
		Last Modified: Wed, 26 Jun 2024 16:58:55 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.6.1-ubuntu`

```console
$ docker pull kong@sha256:1e20f713f8c64bd19aebf1dcf4e6249e6985f01353d047b6438efc0ac5e5d698
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.6.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9020aa8ba901210f51d2b2a3452f245a2733bb120cfb1ea701202c2acdc46363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97207603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5caf7cdcaca51c3183d1b7ab6e7073cd7317e31a4e868afe799365eadb2b919`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 14 Jun 2024 20:57:56 GMT
ARG RELEASE
# Fri, 14 Jun 2024 20:57:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 14 Jun 2024 20:57:56 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["/bin/bash"]
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4e72e64e716ca59fdced8d3a6b81f6968051d95623e6ded5407ffbf6f50bc`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eb602a30a3cc237e21a749b77c8b010bfae3cf50a2d637e3ebe69bcc27c4a1`  
		Last Modified: Tue, 02 Jul 2024 03:04:08 GMT  
		Size: 67.7 MB (67672260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f15e0a49ac6f3d6669dbbd67e34da7def932a3741c00c57388fa4ebb4774e7`  
		Last Modified: Tue, 02 Jul 2024 03:04:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e14776380baf5054f5e13565c13d8826af1e9afc9e953600d68235c5f7dd8125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d44ea0ce0ceb8b373c7934508eb986c1d69f0dcc48830cde4113369b76a4cf8`

```dockerfile
```

-	Layers:
	-	`sha256:ae88c05ee4d394fcce8d5aebc8fa24b2c4f768b66dbeccdfc284a4fb50be049e`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 4.9 MB (4905266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07b8d2ffb76a26caf00b5ad24c4d6d837580a525422c3680d1418fa2eb8a9b0`  
		Last Modified: Tue, 02 Jul 2024 03:04:05 GMT  
		Size: 15.1 KB (15135 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.6.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40ff25f8550f7cb4efab721d6364270a846a40f1e844aaff569b4013a0159e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94588256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f303a21e31799e3cd77b5bd712076050ee9fc5073a5fc1d5e0b2fc9f0cf423`
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
# Fri, 14 Jun 2024 20:57:56 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 14 Jun 2024 20:57:56 GMT
ARG ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ENV ASSET=ce
# Fri, 14 Jun 2024 20:57:56 GMT
ARG EE_PORTS
# Fri, 14 Jun 2024 20:57:56 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ENV KONG_VERSION=3.6.1
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd
# Fri, 14 Jun 2024 20:57:56 GMT
ARG KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
# Fri, 14 Jun 2024 20:57:56 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.6.1 KONG_AMD64_SHA=03b2aca93fd41b8dc0908754cef815433c1d3069ac842a1d078ca98105b230fd KONG_ARM64_SHA=b544bfe2ba4109335d26efb5e59029450f823c3a19b6aef77f6c93d5850142b0
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 14 Jun 2024 20:57:56 GMT
USER kong
# Fri, 14 Jun 2024 20:57:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 14 Jun 2024 20:57:56 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 14 Jun 2024 20:57:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 14 Jun 2024 20:57:56 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 14 Jun 2024 20:57:56 GMT
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
	-	`sha256:e0b39fb67d651276a4d94d94ee3982d275ba566a848847ad3076a363d8f11fdc`  
		Last Modified: Wed, 26 Jun 2024 16:58:58 GMT  
		Size: 67.2 MB (67225189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79ff05e556d68ee630399eb3badd226b08a98e9808bffc2b68c67fed08ce8a5`  
		Last Modified: Wed, 26 Jun 2024 16:58:55 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.6.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1b056341629c0056bacd27cc6fb5bb70d066be2a53fde471c5b38d015dfb7c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa00184a6564c67781046bb4bcc8bced799c3644b1808040b43f1c62f481b6b4`

```dockerfile
```

-	Layers:
	-	`sha256:24cafb285797b15fd78b10da624cc17c412cba61952d349ac5ba5023fe420778`  
		Last Modified: Wed, 26 Jun 2024 16:58:56 GMT  
		Size: 4.9 MB (4911598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbbab9a07df77fef4a13d73192c611fb63ce9dd32158b3ac8d05dffffb690e43`  
		Last Modified: Wed, 26 Jun 2024 16:58:55 GMT  
		Size: 15.4 KB (15436 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.7`

```console
$ docker pull kong@sha256:2799758c97191e22b84d88d611387f21fc4503c186a8029621c41658d2469e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7` - linux; amd64

```console
$ docker pull kong@sha256:2fe48406624ba014286502e71912663c57b05e663e6863389e92c6d01a3c2102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8047104cfac02de210edac6773b1072736c8dc3caf6d220e939760fa5c0aeda5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea0c3e76a3b5827ab771114ec792b49b7673d063ccf35d5ef374f57af60ab42`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc789aa436d5f3ae6e1d1d0a57aa5f543bd7ff7a0dd5d2fca51b2e9335fd3de`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 67.7 MB (67710110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf088c8a9d718696c3a6aa9c88bd905040f8d0bc18397ab016ded447517c1a6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7` - unknown; unknown

```console
$ docker pull kong@sha256:e39f49ea77f7f75248f0f556936df8d72c14d20ec6fb51bc8651f0b113ccace6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17501e767e6400dd5f28991966cd06f12fddb029b6f07b054ed881c9249b3fd1`

```dockerfile
```

-	Layers:
	-	`sha256:59d0fe55fd07a1ebeaec261834e9ea2d9e63d94f149fd4a81bdd8835776ff214`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d195a25a0cba96c6815b22d0bed6c6afa3539bafad4deeb8290db3238d762256`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
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
$ docker pull kong@sha256:2799758c97191e22b84d88d611387f21fc4503c186a8029621c41658d2469e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2fe48406624ba014286502e71912663c57b05e663e6863389e92c6d01a3c2102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8047104cfac02de210edac6773b1072736c8dc3caf6d220e939760fa5c0aeda5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea0c3e76a3b5827ab771114ec792b49b7673d063ccf35d5ef374f57af60ab42`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc789aa436d5f3ae6e1d1d0a57aa5f543bd7ff7a0dd5d2fca51b2e9335fd3de`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 67.7 MB (67710110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf088c8a9d718696c3a6aa9c88bd905040f8d0bc18397ab016ded447517c1a6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e39f49ea77f7f75248f0f556936df8d72c14d20ec6fb51bc8651f0b113ccace6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17501e767e6400dd5f28991966cd06f12fddb029b6f07b054ed881c9249b3fd1`

```dockerfile
```

-	Layers:
	-	`sha256:59d0fe55fd07a1ebeaec261834e9ea2d9e63d94f149fd4a81bdd8835776ff214`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d195a25a0cba96c6815b22d0bed6c6afa3539bafad4deeb8290db3238d762256`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
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
$ docker pull kong@sha256:2799758c97191e22b84d88d611387f21fc4503c186a8029621c41658d2469e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1` - linux; amd64

```console
$ docker pull kong@sha256:2fe48406624ba014286502e71912663c57b05e663e6863389e92c6d01a3c2102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8047104cfac02de210edac6773b1072736c8dc3caf6d220e939760fa5c0aeda5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea0c3e76a3b5827ab771114ec792b49b7673d063ccf35d5ef374f57af60ab42`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc789aa436d5f3ae6e1d1d0a57aa5f543bd7ff7a0dd5d2fca51b2e9335fd3de`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 67.7 MB (67710110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf088c8a9d718696c3a6aa9c88bd905040f8d0bc18397ab016ded447517c1a6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1` - unknown; unknown

```console
$ docker pull kong@sha256:e39f49ea77f7f75248f0f556936df8d72c14d20ec6fb51bc8651f0b113ccace6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17501e767e6400dd5f28991966cd06f12fddb029b6f07b054ed881c9249b3fd1`

```dockerfile
```

-	Layers:
	-	`sha256:59d0fe55fd07a1ebeaec261834e9ea2d9e63d94f149fd4a81bdd8835776ff214`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d195a25a0cba96c6815b22d0bed6c6afa3539bafad4deeb8290db3238d762256`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
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
$ docker pull kong@sha256:2799758c97191e22b84d88d611387f21fc4503c186a8029621c41658d2469e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2fe48406624ba014286502e71912663c57b05e663e6863389e92c6d01a3c2102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8047104cfac02de210edac6773b1072736c8dc3caf6d220e939760fa5c0aeda5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea0c3e76a3b5827ab771114ec792b49b7673d063ccf35d5ef374f57af60ab42`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc789aa436d5f3ae6e1d1d0a57aa5f543bd7ff7a0dd5d2fca51b2e9335fd3de`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 67.7 MB (67710110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf088c8a9d718696c3a6aa9c88bd905040f8d0bc18397ab016ded447517c1a6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.7.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e39f49ea77f7f75248f0f556936df8d72c14d20ec6fb51bc8651f0b113ccace6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17501e767e6400dd5f28991966cd06f12fddb029b6f07b054ed881c9249b3fd1`

```dockerfile
```

-	Layers:
	-	`sha256:59d0fe55fd07a1ebeaec261834e9ea2d9e63d94f149fd4a81bdd8835776ff214`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d195a25a0cba96c6815b22d0bed6c6afa3539bafad4deeb8290db3238d762256`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
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
$ docker pull kong@sha256:2799758c97191e22b84d88d611387f21fc4503c186a8029621c41658d2469e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:2fe48406624ba014286502e71912663c57b05e663e6863389e92c6d01a3c2102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8047104cfac02de210edac6773b1072736c8dc3caf6d220e939760fa5c0aeda5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea0c3e76a3b5827ab771114ec792b49b7673d063ccf35d5ef374f57af60ab42`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc789aa436d5f3ae6e1d1d0a57aa5f543bd7ff7a0dd5d2fca51b2e9335fd3de`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 67.7 MB (67710110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf088c8a9d718696c3a6aa9c88bd905040f8d0bc18397ab016ded447517c1a6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:e39f49ea77f7f75248f0f556936df8d72c14d20ec6fb51bc8651f0b113ccace6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17501e767e6400dd5f28991966cd06f12fddb029b6f07b054ed881c9249b3fd1`

```dockerfile
```

-	Layers:
	-	`sha256:59d0fe55fd07a1ebeaec261834e9ea2d9e63d94f149fd4a81bdd8835776ff214`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d195a25a0cba96c6815b22d0bed6c6afa3539bafad4deeb8290db3238d762256`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
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
$ docker pull kong@sha256:2799758c97191e22b84d88d611387f21fc4503c186a8029621c41658d2469e0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2fe48406624ba014286502e71912663c57b05e663e6863389e92c6d01a3c2102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97245451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8047104cfac02de210edac6773b1072736c8dc3caf6d220e939760fa5c0aeda5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 21 Jun 2024 16:03:55 GMT
ARG RELEASE
# Fri, 21 Jun 2024 16:03:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 16:03:55 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 16:03:55 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Fri, 21 Jun 2024 16:03:55 GMT
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea0c3e76a3b5827ab771114ec792b49b7673d063ccf35d5ef374f57af60ab42`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc789aa436d5f3ae6e1d1d0a57aa5f543bd7ff7a0dd5d2fca51b2e9335fd3de`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 67.7 MB (67710110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf088c8a9d718696c3a6aa9c88bd905040f8d0bc18397ab016ded447517c1a6b`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:e39f49ea77f7f75248f0f556936df8d72c14d20ec6fb51bc8651f0b113ccace6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17501e767e6400dd5f28991966cd06f12fddb029b6f07b054ed881c9249b3fd1`

```dockerfile
```

-	Layers:
	-	`sha256:59d0fe55fd07a1ebeaec261834e9ea2d9e63d94f149fd4a81bdd8835776ff214`  
		Last Modified: Tue, 02 Jul 2024 03:04:02 GMT  
		Size: 5.0 MB (4984579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d195a25a0cba96c6815b22d0bed6c6afa3539bafad4deeb8290db3238d762256`  
		Last Modified: Tue, 02 Jul 2024 03:04:01 GMT  
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
