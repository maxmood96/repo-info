<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

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
-	[`kong:3.9.3`](#kong393)
-	[`kong:3.9.3-ubuntu`](#kong393-ubuntu)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:3`

```console
$ docker pull kong@sha256:8a6a7a48af3161ec0ac2ee909e5f94dd83ad7d8668479da620ee85046c5b266e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:476c99dc77ee32867547188015e7b3e3bb4a2a94847fbe64f0b5ba5a23649c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122824648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f047bc123120f40c0d563f87ff934673033175b277528401899485e6a5e5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:49 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
USER kong
# Wed, 17 Jun 2026 21:53:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2c50624783cdc4dba30e087715d002012a972e8dd67356315b83ee23456c95`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1926f0f3104f2b63195d737e9d94b27facb50becfa254a37fd455884a5aa7cf`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 93.1 MB (93090550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536147b95eab04fdc424b6411d89ca89d6e97aa778ceed60f9be003fcd436316`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:d2787b5ebb11a611c10a5b283279ee2214d1d0be5569c10f2dd2569339903bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c3b990ce3c1efc4ddc398ff78b4490ae9526727e199709bc941c7af95bd503`

```dockerfile
```

-	Layers:
	-	`sha256:d6ff8eab5ab73a0c852c34fbbe332d4c26fb94b25c3c5c131ffe94ce7cb308d7`  
		Last Modified: Wed, 17 Jun 2026 21:53:25 GMT  
		Size: 5.4 MB (5448561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d827abda2e7f600552e445b160ed038f68f9dc2d296d4bd547a8bf9f54e2622`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:547dc796172917644af167b3e32ec4815e8ce685f1316d8a009a48a30d416728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121090970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c6402c136fab7b18179d52a70cfd52bf2367365d6ee9185656c1c735a5d56f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:46 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
USER kong
# Wed, 17 Jun 2026 21:53:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75928a78297abbfc30d516c90561170c45e32f258534a23545a4f8d72a9e0b59`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6f091c6d3c7f0f3d6fd4549927177662ea698e5043d2efcd210e224689aaf`  
		Last Modified: Wed, 17 Jun 2026 21:53:30 GMT  
		Size: 92.2 MB (92213275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e7b8ab7a887f7333cf5a5cc48fa1dd333fda2b6e6fa8b20d2719a6541a926d`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:09cb1678fdb985cc60d21fc2de0e0b488de889ea41e962737052677bd82ac63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ace6c42a2ba6ff528665cf53a06260b6f81b6946f69314d8d2477bdbd9a5ea`

```dockerfile
```

-	Layers:
	-	`sha256:0ac77c25678154d78fa0e08cd6af256ada5c0b45bf09ddae2085d2167b3f8a81`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 5.5 MB (5455728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70384f08cf37dfbcc303041c2339971991ae0ba8f57759c1402f9e649f8b5f5`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:cf571f0d57662aa2a933142d630b626a11249a11b7ce6d4a64d32205927b7603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:3c06f70cf02480a83ca57ef9b50ab22e6bcd8837bc95f465bbb96f6c8f229717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92469328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45d72a9d675bc89936200fc42dd3169a45350a0a50a5bfc5e1b432c259fe17e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:40 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:40 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:40 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:40 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:40 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:40 GMT
ENV KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 15 May 2026 21:19:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:57 GMT
USER kong
# Fri, 15 May 2026 21:19:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3437dcbc128c7197e153f29e93fd11a32387b6dc9c60e34bd1d8e279576334fd`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b8616a3280161328b97dedb042c55afc2633ec14e86849f0a63312654a69d3`  
		Last Modified: Fri, 15 May 2026 21:20:14 GMT  
		Size: 62.7 MB (62731362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda3b21115709f0c372c28c5417c83842fa76434d152e69e29e58c087add5c49`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:875566543c4e71e7a8b4d6caeddec35fd5cce94ddfe952ac135cb3074ec89e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a662938b3349555325698d87bfc181c4e485928094fe696daa872dd726b0d955`

```dockerfile
```

-	Layers:
	-	`sha256:9e89369e9e68675ebbceea2b0e2d0b9001768a135afa3558ff9435cd2a632ffc`  
		Last Modified: Fri, 15 May 2026 21:20:12 GMT  
		Size: 6.1 MB (6062911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8497040ba0b7f6867afd82fc2e84c6f49c3d1e2fc728035ec486e62b44fd4b5c`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2d568b7e29e915e7b9ab59260a3e74cdb6b5ac75516daad6a0caa2624f5de594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88802004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bb7cf50486615e198fd45c6ae8407e3aeb3d01f4f79f0c22b9fac62b1ba526`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:23 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:23 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:23 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:23 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:23 GMT
ENV KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 15 May 2026 21:19:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:47 GMT
USER kong
# Fri, 15 May 2026 21:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f2fbe2d4b4f98b72a91571d444ecc52e7841747ae5f84eb033d62fac304580`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725a18df0d88c8d2671a27417b1e215b5d9fe993e87bb3e540b7d45d498b8f5c`  
		Last Modified: Fri, 15 May 2026 21:20:04 GMT  
		Size: 61.2 MB (61194099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f49a7e46d8fec9345e2adc493e30a68810ae228d67e5c819b9e0580a1d9e0c`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:73835d5c26cf480128c57156027b972b1864a73668de13f2e5bb311d5b648eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b40fe70dfa55a67a1eed222811a846ba7f37dca65edc964997a1b69256969a9`

```dockerfile
```

-	Layers:
	-	`sha256:53c803698abe1f0f3ee0a9e691bc1ba7943c1d555a33a3baa5f1c2b4b60ac32f`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 6.0 MB (6040990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d968d3d5a469baa407829fd003b1a1cbc0b2834c071d9b2e43dce66d1ec15848`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:cf571f0d57662aa2a933142d630b626a11249a11b7ce6d4a64d32205927b7603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3c06f70cf02480a83ca57ef9b50ab22e6bcd8837bc95f465bbb96f6c8f229717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92469328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45d72a9d675bc89936200fc42dd3169a45350a0a50a5bfc5e1b432c259fe17e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:40 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:40 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:40 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:40 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:40 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:40 GMT
ENV KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 15 May 2026 21:19:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:57 GMT
USER kong
# Fri, 15 May 2026 21:19:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3437dcbc128c7197e153f29e93fd11a32387b6dc9c60e34bd1d8e279576334fd`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b8616a3280161328b97dedb042c55afc2633ec14e86849f0a63312654a69d3`  
		Last Modified: Fri, 15 May 2026 21:20:14 GMT  
		Size: 62.7 MB (62731362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda3b21115709f0c372c28c5417c83842fa76434d152e69e29e58c087add5c49`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:875566543c4e71e7a8b4d6caeddec35fd5cce94ddfe952ac135cb3074ec89e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a662938b3349555325698d87bfc181c4e485928094fe696daa872dd726b0d955`

```dockerfile
```

-	Layers:
	-	`sha256:9e89369e9e68675ebbceea2b0e2d0b9001768a135afa3558ff9435cd2a632ffc`  
		Last Modified: Fri, 15 May 2026 21:20:12 GMT  
		Size: 6.1 MB (6062911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8497040ba0b7f6867afd82fc2e84c6f49c3d1e2fc728035ec486e62b44fd4b5c`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2d568b7e29e915e7b9ab59260a3e74cdb6b5ac75516daad6a0caa2624f5de594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88802004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bb7cf50486615e198fd45c6ae8407e3aeb3d01f4f79f0c22b9fac62b1ba526`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:23 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:23 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:23 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:23 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:23 GMT
ENV KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 15 May 2026 21:19:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:47 GMT
USER kong
# Fri, 15 May 2026 21:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f2fbe2d4b4f98b72a91571d444ecc52e7841747ae5f84eb033d62fac304580`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725a18df0d88c8d2671a27417b1e215b5d9fe993e87bb3e540b7d45d498b8f5c`  
		Last Modified: Fri, 15 May 2026 21:20:04 GMT  
		Size: 61.2 MB (61194099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f49a7e46d8fec9345e2adc493e30a68810ae228d67e5c819b9e0580a1d9e0c`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:73835d5c26cf480128c57156027b972b1864a73668de13f2e5bb311d5b648eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b40fe70dfa55a67a1eed222811a846ba7f37dca65edc964997a1b69256969a9`

```dockerfile
```

-	Layers:
	-	`sha256:53c803698abe1f0f3ee0a9e691bc1ba7943c1d555a33a3baa5f1c2b4b60ac32f`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 6.0 MB (6040990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d968d3d5a469baa407829fd003b1a1cbc0b2834c071d9b2e43dce66d1ec15848`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:cf571f0d57662aa2a933142d630b626a11249a11b7ce6d4a64d32205927b7603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:3c06f70cf02480a83ca57ef9b50ab22e6bcd8837bc95f465bbb96f6c8f229717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92469328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45d72a9d675bc89936200fc42dd3169a45350a0a50a5bfc5e1b432c259fe17e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:40 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:40 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:40 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:40 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:40 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:40 GMT
ENV KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 15 May 2026 21:19:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:57 GMT
USER kong
# Fri, 15 May 2026 21:19:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3437dcbc128c7197e153f29e93fd11a32387b6dc9c60e34bd1d8e279576334fd`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b8616a3280161328b97dedb042c55afc2633ec14e86849f0a63312654a69d3`  
		Last Modified: Fri, 15 May 2026 21:20:14 GMT  
		Size: 62.7 MB (62731362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda3b21115709f0c372c28c5417c83842fa76434d152e69e29e58c087add5c49`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:875566543c4e71e7a8b4d6caeddec35fd5cce94ddfe952ac135cb3074ec89e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a662938b3349555325698d87bfc181c4e485928094fe696daa872dd726b0d955`

```dockerfile
```

-	Layers:
	-	`sha256:9e89369e9e68675ebbceea2b0e2d0b9001768a135afa3558ff9435cd2a632ffc`  
		Last Modified: Fri, 15 May 2026 21:20:12 GMT  
		Size: 6.1 MB (6062911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8497040ba0b7f6867afd82fc2e84c6f49c3d1e2fc728035ec486e62b44fd4b5c`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2d568b7e29e915e7b9ab59260a3e74cdb6b5ac75516daad6a0caa2624f5de594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88802004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bb7cf50486615e198fd45c6ae8407e3aeb3d01f4f79f0c22b9fac62b1ba526`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:23 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:23 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:23 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:23 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:23 GMT
ENV KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 15 May 2026 21:19:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:47 GMT
USER kong
# Fri, 15 May 2026 21:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f2fbe2d4b4f98b72a91571d444ecc52e7841747ae5f84eb033d62fac304580`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725a18df0d88c8d2671a27417b1e215b5d9fe993e87bb3e540b7d45d498b8f5c`  
		Last Modified: Fri, 15 May 2026 21:20:04 GMT  
		Size: 61.2 MB (61194099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f49a7e46d8fec9345e2adc493e30a68810ae228d67e5c819b9e0580a1d9e0c`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:73835d5c26cf480128c57156027b972b1864a73668de13f2e5bb311d5b648eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b40fe70dfa55a67a1eed222811a846ba7f37dca65edc964997a1b69256969a9`

```dockerfile
```

-	Layers:
	-	`sha256:53c803698abe1f0f3ee0a9e691bc1ba7943c1d555a33a3baa5f1c2b4b60ac32f`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 6.0 MB (6040990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d968d3d5a469baa407829fd003b1a1cbc0b2834c071d9b2e43dce66d1ec15848`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:cf571f0d57662aa2a933142d630b626a11249a11b7ce6d4a64d32205927b7603
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:3c06f70cf02480a83ca57ef9b50ab22e6bcd8837bc95f465bbb96f6c8f229717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92469328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45d72a9d675bc89936200fc42dd3169a45350a0a50a5bfc5e1b432c259fe17e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:40 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:40 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:40 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:40 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:40 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:40 GMT
ENV KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 15 May 2026 21:19:40 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 15 May 2026 21:19:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:57 GMT
USER kong
# Fri, 15 May 2026 21:19:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3437dcbc128c7197e153f29e93fd11a32387b6dc9c60e34bd1d8e279576334fd`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b8616a3280161328b97dedb042c55afc2633ec14e86849f0a63312654a69d3`  
		Last Modified: Fri, 15 May 2026 21:20:14 GMT  
		Size: 62.7 MB (62731362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda3b21115709f0c372c28c5417c83842fa76434d152e69e29e58c087add5c49`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:875566543c4e71e7a8b4d6caeddec35fd5cce94ddfe952ac135cb3074ec89e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a662938b3349555325698d87bfc181c4e485928094fe696daa872dd726b0d955`

```dockerfile
```

-	Layers:
	-	`sha256:9e89369e9e68675ebbceea2b0e2d0b9001768a135afa3558ff9435cd2a632ffc`  
		Last Modified: Fri, 15 May 2026 21:20:12 GMT  
		Size: 6.1 MB (6062911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8497040ba0b7f6867afd82fc2e84c6f49c3d1e2fc728035ec486e62b44fd4b5c`  
		Last Modified: Fri, 15 May 2026 21:20:11 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2d568b7e29e915e7b9ab59260a3e74cdb6b5ac75516daad6a0caa2624f5de594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88802004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1bb7cf50486615e198fd45c6ae8407e3aeb3d01f4f79f0c22b9fac62b1ba526`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:23 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:23 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:23 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:23 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:23 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:23 GMT
ENV KONG_VERSION=3.4.2
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2
# Fri, 15 May 2026 21:19:23 GMT
ARG KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
# Fri, 15 May 2026 21:19:47 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.4.2 KONG_AMD64_SHA=b6bf56a5088660e7cac748a005af8d977be7177e64b0abfe1e7f77d797cdc0e2 KONG_ARM64_SHA=8bca79a6337a6299316cca4e2f9a766df09268359292686498db18a48d883689
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:47 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:47 GMT
USER kong
# Fri, 15 May 2026 21:19:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:47 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:47 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:47 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f2fbe2d4b4f98b72a91571d444ecc52e7841747ae5f84eb033d62fac304580`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725a18df0d88c8d2671a27417b1e215b5d9fe993e87bb3e540b7d45d498b8f5c`  
		Last Modified: Fri, 15 May 2026 21:20:04 GMT  
		Size: 61.2 MB (61194099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f49a7e46d8fec9345e2adc493e30a68810ae228d67e5c819b9e0580a1d9e0c`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:73835d5c26cf480128c57156027b972b1864a73668de13f2e5bb311d5b648eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b40fe70dfa55a67a1eed222811a846ba7f37dca65edc964997a1b69256969a9`

```dockerfile
```

-	Layers:
	-	`sha256:53c803698abe1f0f3ee0a9e691bc1ba7943c1d555a33a3baa5f1c2b4b60ac32f`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 6.0 MB (6040990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d968d3d5a469baa407829fd003b1a1cbc0b2834c071d9b2e43dce66d1ec15848`  
		Last Modified: Fri, 15 May 2026 21:20:02 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:1b1bb63e2fe89cee660a288b3a4982bdb1a128e65fa5f90312bcc279966a5f78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:e5dd0ff7309317a2e6bb320b89eebe3a12b46f357e7f85133030e19981c06c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117755320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4033d29b65deed6726d11af689f2cea9dd1aa2feac8db18f21018a08864bcc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:19 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:19 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:19 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:19 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:19 GMT
ENV KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Fri, 15 May 2026 21:19:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:38 GMT
USER kong
# Fri, 15 May 2026 21:19:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a389eceae841b92576806e7998faa5409f5027f3f6c5d124349f41f6d11dfd09`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776bc9808a17a9be01011c02ee461d624d1cde1c036ce76c2d7d3d3e5e01c153`  
		Last Modified: Fri, 15 May 2026 21:19:56 GMT  
		Size: 88.0 MB (88017355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95159b3e3246abaeb80e63fb61e7a44584c598c0fd0ca66443972b96a2fba115`  
		Last Modified: Fri, 15 May 2026 21:19:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:1e4cdace50ec2c82ef875a41d71f01f32c0c5f3a98333d70f6d421cdc5f3d194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eadd7980d06cbfd496df08763b76f0c6eb3029605e126faf02f25e40674871f`

```dockerfile
```

-	Layers:
	-	`sha256:f1441aa0f1ad0825c84933ac800a325f2fdd46a7ac7ebcf78141d0df14d73030`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 5.4 MB (5362708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be2d9d2aec91a8b050bb0ca4cdcf33aeaad387f5d8b5f7efd2ec00b5cb037fe6`  
		Last Modified: Fri, 15 May 2026 21:19:53 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4ee51fdf23cf9cc8adbfc3ff9b82538a6586760a7dc71a8ea597c37f4a4a7eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114932786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960c181b66040c438bb54208f25a310175c69faa6cc18e6fc8c52411275107f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:07 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:07 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:07 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:07 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:07 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:07 GMT
ENV KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Fri, 15 May 2026 21:19:37 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:37 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:37 GMT
USER kong
# Fri, 15 May 2026 21:19:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:37 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9268a3f59ae6309ead5863f96cab25f59cb57ab020456795da1269c172fd6523`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe6b50a28e61b3d2d21322b9d90ed6d5dbf0e7160c5d282020f78351384092f`  
		Last Modified: Fri, 15 May 2026 21:19:57 GMT  
		Size: 87.3 MB (87324884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480d76ff373792296c6334a0dee881c8d26241c770dee9e4202263035e43849`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:733dfcec5cc4028509f9de1955f415c80282528500bd10340a7f6dbd5a3ca941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae2bc062472df7dd7d404d4a9a728173fb6a9f9b1c341adfc9bee280867276d`

```dockerfile
```

-	Layers:
	-	`sha256:1e2c2e86c356aed75f129cc2349567e223a43f899f81cf296cdf26ee7a45723e`  
		Last Modified: Fri, 15 May 2026 21:19:55 GMT  
		Size: 5.4 MB (5369034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194b4bbe88f60725ccfe0d8aa3ef08d40c394e973c8c3affc4713e7ca7a2f4d6`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:1b1bb63e2fe89cee660a288b3a4982bdb1a128e65fa5f90312bcc279966a5f78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e5dd0ff7309317a2e6bb320b89eebe3a12b46f357e7f85133030e19981c06c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117755320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4033d29b65deed6726d11af689f2cea9dd1aa2feac8db18f21018a08864bcc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:19 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:19 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:19 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:19 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:19 GMT
ENV KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Fri, 15 May 2026 21:19:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:38 GMT
USER kong
# Fri, 15 May 2026 21:19:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a389eceae841b92576806e7998faa5409f5027f3f6c5d124349f41f6d11dfd09`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776bc9808a17a9be01011c02ee461d624d1cde1c036ce76c2d7d3d3e5e01c153`  
		Last Modified: Fri, 15 May 2026 21:19:56 GMT  
		Size: 88.0 MB (88017355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95159b3e3246abaeb80e63fb61e7a44584c598c0fd0ca66443972b96a2fba115`  
		Last Modified: Fri, 15 May 2026 21:19:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1e4cdace50ec2c82ef875a41d71f01f32c0c5f3a98333d70f6d421cdc5f3d194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eadd7980d06cbfd496df08763b76f0c6eb3029605e126faf02f25e40674871f`

```dockerfile
```

-	Layers:
	-	`sha256:f1441aa0f1ad0825c84933ac800a325f2fdd46a7ac7ebcf78141d0df14d73030`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 5.4 MB (5362708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be2d9d2aec91a8b050bb0ca4cdcf33aeaad387f5d8b5f7efd2ec00b5cb037fe6`  
		Last Modified: Fri, 15 May 2026 21:19:53 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4ee51fdf23cf9cc8adbfc3ff9b82538a6586760a7dc71a8ea597c37f4a4a7eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114932786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960c181b66040c438bb54208f25a310175c69faa6cc18e6fc8c52411275107f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:07 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:07 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:07 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:07 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:07 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:07 GMT
ENV KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Fri, 15 May 2026 21:19:37 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:37 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:37 GMT
USER kong
# Fri, 15 May 2026 21:19:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:37 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9268a3f59ae6309ead5863f96cab25f59cb57ab020456795da1269c172fd6523`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe6b50a28e61b3d2d21322b9d90ed6d5dbf0e7160c5d282020f78351384092f`  
		Last Modified: Fri, 15 May 2026 21:19:57 GMT  
		Size: 87.3 MB (87324884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480d76ff373792296c6334a0dee881c8d26241c770dee9e4202263035e43849`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:733dfcec5cc4028509f9de1955f415c80282528500bd10340a7f6dbd5a3ca941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae2bc062472df7dd7d404d4a9a728173fb6a9f9b1c341adfc9bee280867276d`

```dockerfile
```

-	Layers:
	-	`sha256:1e2c2e86c356aed75f129cc2349567e223a43f899f81cf296cdf26ee7a45723e`  
		Last Modified: Fri, 15 May 2026 21:19:55 GMT  
		Size: 5.4 MB (5369034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194b4bbe88f60725ccfe0d8aa3ef08d40c394e973c8c3affc4713e7ca7a2f4d6`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:1b1bb63e2fe89cee660a288b3a4982bdb1a128e65fa5f90312bcc279966a5f78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:e5dd0ff7309317a2e6bb320b89eebe3a12b46f357e7f85133030e19981c06c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117755320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4033d29b65deed6726d11af689f2cea9dd1aa2feac8db18f21018a08864bcc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:19 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:19 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:19 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:19 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:19 GMT
ENV KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Fri, 15 May 2026 21:19:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:38 GMT
USER kong
# Fri, 15 May 2026 21:19:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a389eceae841b92576806e7998faa5409f5027f3f6c5d124349f41f6d11dfd09`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776bc9808a17a9be01011c02ee461d624d1cde1c036ce76c2d7d3d3e5e01c153`  
		Last Modified: Fri, 15 May 2026 21:19:56 GMT  
		Size: 88.0 MB (88017355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95159b3e3246abaeb80e63fb61e7a44584c598c0fd0ca66443972b96a2fba115`  
		Last Modified: Fri, 15 May 2026 21:19:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:1e4cdace50ec2c82ef875a41d71f01f32c0c5f3a98333d70f6d421cdc5f3d194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eadd7980d06cbfd496df08763b76f0c6eb3029605e126faf02f25e40674871f`

```dockerfile
```

-	Layers:
	-	`sha256:f1441aa0f1ad0825c84933ac800a325f2fdd46a7ac7ebcf78141d0df14d73030`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 5.4 MB (5362708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be2d9d2aec91a8b050bb0ca4cdcf33aeaad387f5d8b5f7efd2ec00b5cb037fe6`  
		Last Modified: Fri, 15 May 2026 21:19:53 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4ee51fdf23cf9cc8adbfc3ff9b82538a6586760a7dc71a8ea597c37f4a4a7eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114932786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960c181b66040c438bb54208f25a310175c69faa6cc18e6fc8c52411275107f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:07 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:07 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:07 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:07 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:07 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:07 GMT
ENV KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Fri, 15 May 2026 21:19:37 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:37 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:37 GMT
USER kong
# Fri, 15 May 2026 21:19:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:37 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9268a3f59ae6309ead5863f96cab25f59cb57ab020456795da1269c172fd6523`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe6b50a28e61b3d2d21322b9d90ed6d5dbf0e7160c5d282020f78351384092f`  
		Last Modified: Fri, 15 May 2026 21:19:57 GMT  
		Size: 87.3 MB (87324884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480d76ff373792296c6334a0dee881c8d26241c770dee9e4202263035e43849`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:733dfcec5cc4028509f9de1955f415c80282528500bd10340a7f6dbd5a3ca941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae2bc062472df7dd7d404d4a9a728173fb6a9f9b1c341adfc9bee280867276d`

```dockerfile
```

-	Layers:
	-	`sha256:1e2c2e86c356aed75f129cc2349567e223a43f899f81cf296cdf26ee7a45723e`  
		Last Modified: Fri, 15 May 2026 21:19:55 GMT  
		Size: 5.4 MB (5369034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194b4bbe88f60725ccfe0d8aa3ef08d40c394e973c8c3affc4713e7ca7a2f4d6`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:1b1bb63e2fe89cee660a288b3a4982bdb1a128e65fa5f90312bcc279966a5f78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e5dd0ff7309317a2e6bb320b89eebe3a12b46f357e7f85133030e19981c06c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117755320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4033d29b65deed6726d11af689f2cea9dd1aa2feac8db18f21018a08864bcc92`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:19 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:19 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:19 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:19 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:19 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:19 GMT
ENV KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Fri, 15 May 2026 21:19:19 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Fri, 15 May 2026 21:19:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:38 GMT
USER kong
# Fri, 15 May 2026 21:19:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a389eceae841b92576806e7998faa5409f5027f3f6c5d124349f41f6d11dfd09`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776bc9808a17a9be01011c02ee461d624d1cde1c036ce76c2d7d3d3e5e01c153`  
		Last Modified: Fri, 15 May 2026 21:19:56 GMT  
		Size: 88.0 MB (88017355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95159b3e3246abaeb80e63fb61e7a44584c598c0fd0ca66443972b96a2fba115`  
		Last Modified: Fri, 15 May 2026 21:19:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:1e4cdace50ec2c82ef875a41d71f01f32c0c5f3a98333d70f6d421cdc5f3d194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eadd7980d06cbfd496df08763b76f0c6eb3029605e126faf02f25e40674871f`

```dockerfile
```

-	Layers:
	-	`sha256:f1441aa0f1ad0825c84933ac800a325f2fdd46a7ac7ebcf78141d0df14d73030`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 5.4 MB (5362708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be2d9d2aec91a8b050bb0ca4cdcf33aeaad387f5d8b5f7efd2ec00b5cb037fe6`  
		Last Modified: Fri, 15 May 2026 21:19:53 GMT  
		Size: 15.3 KB (15346 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4ee51fdf23cf9cc8adbfc3ff9b82538a6586760a7dc71a8ea597c37f4a4a7eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.9 MB (114932786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960c181b66040c438bb54208f25a310175c69faa6cc18e6fc8c52411275107f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:19:07 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Fri, 15 May 2026 21:19:07 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:07 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:07 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:07 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:07 GMT
ENV KONG_VERSION=3.8.0
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Fri, 15 May 2026 21:19:07 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Fri, 15 May 2026 21:19:37 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:19:37 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:19:37 GMT
USER kong
# Fri, 15 May 2026 21:19:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:19:37 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:19:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:19:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:19:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9268a3f59ae6309ead5863f96cab25f59cb57ab020456795da1269c172fd6523`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe6b50a28e61b3d2d21322b9d90ed6d5dbf0e7160c5d282020f78351384092f`  
		Last Modified: Fri, 15 May 2026 21:19:57 GMT  
		Size: 87.3 MB (87324884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0480d76ff373792296c6334a0dee881c8d26241c770dee9e4202263035e43849`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:733dfcec5cc4028509f9de1955f415c80282528500bd10340a7f6dbd5a3ca941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae2bc062472df7dd7d404d4a9a728173fb6a9f9b1c341adfc9bee280867276d`

```dockerfile
```

-	Layers:
	-	`sha256:1e2c2e86c356aed75f129cc2349567e223a43f899f81cf296cdf26ee7a45723e`  
		Last Modified: Fri, 15 May 2026 21:19:55 GMT  
		Size: 5.4 MB (5369034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194b4bbe88f60725ccfe0d8aa3ef08d40c394e973c8c3affc4713e7ca7a2f4d6`  
		Last Modified: Fri, 15 May 2026 21:19:54 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:8a6a7a48af3161ec0ac2ee909e5f94dd83ad7d8668479da620ee85046c5b266e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:476c99dc77ee32867547188015e7b3e3bb4a2a94847fbe64f0b5ba5a23649c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122824648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f047bc123120f40c0d563f87ff934673033175b277528401899485e6a5e5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:49 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
USER kong
# Wed, 17 Jun 2026 21:53:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2c50624783cdc4dba30e087715d002012a972e8dd67356315b83ee23456c95`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1926f0f3104f2b63195d737e9d94b27facb50becfa254a37fd455884a5aa7cf`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 93.1 MB (93090550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536147b95eab04fdc424b6411d89ca89d6e97aa778ceed60f9be003fcd436316`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:d2787b5ebb11a611c10a5b283279ee2214d1d0be5569c10f2dd2569339903bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c3b990ce3c1efc4ddc398ff78b4490ae9526727e199709bc941c7af95bd503`

```dockerfile
```

-	Layers:
	-	`sha256:d6ff8eab5ab73a0c852c34fbbe332d4c26fb94b25c3c5c131ffe94ce7cb308d7`  
		Last Modified: Wed, 17 Jun 2026 21:53:25 GMT  
		Size: 5.4 MB (5448561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d827abda2e7f600552e445b160ed038f68f9dc2d296d4bd547a8bf9f54e2622`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:547dc796172917644af167b3e32ec4815e8ce685f1316d8a009a48a30d416728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121090970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c6402c136fab7b18179d52a70cfd52bf2367365d6ee9185656c1c735a5d56f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:46 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
USER kong
# Wed, 17 Jun 2026 21:53:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75928a78297abbfc30d516c90561170c45e32f258534a23545a4f8d72a9e0b59`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6f091c6d3c7f0f3d6fd4549927177662ea698e5043d2efcd210e224689aaf`  
		Last Modified: Wed, 17 Jun 2026 21:53:30 GMT  
		Size: 92.2 MB (92213275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e7b8ab7a887f7333cf5a5cc48fa1dd333fda2b6e6fa8b20d2719a6541a926d`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:09cb1678fdb985cc60d21fc2de0e0b488de889ea41e962737052677bd82ac63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ace6c42a2ba6ff528665cf53a06260b6f81b6946f69314d8d2477bdbd9a5ea`

```dockerfile
```

-	Layers:
	-	`sha256:0ac77c25678154d78fa0e08cd6af256ada5c0b45bf09ddae2085d2167b3f8a81`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 5.5 MB (5455728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70384f08cf37dfbcc303041c2339971991ae0ba8f57759c1402f9e649f8b5f5`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:8a6a7a48af3161ec0ac2ee909e5f94dd83ad7d8668479da620ee85046c5b266e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:476c99dc77ee32867547188015e7b3e3bb4a2a94847fbe64f0b5ba5a23649c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122824648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f047bc123120f40c0d563f87ff934673033175b277528401899485e6a5e5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:49 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
USER kong
# Wed, 17 Jun 2026 21:53:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2c50624783cdc4dba30e087715d002012a972e8dd67356315b83ee23456c95`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1926f0f3104f2b63195d737e9d94b27facb50becfa254a37fd455884a5aa7cf`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 93.1 MB (93090550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536147b95eab04fdc424b6411d89ca89d6e97aa778ceed60f9be003fcd436316`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d2787b5ebb11a611c10a5b283279ee2214d1d0be5569c10f2dd2569339903bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c3b990ce3c1efc4ddc398ff78b4490ae9526727e199709bc941c7af95bd503`

```dockerfile
```

-	Layers:
	-	`sha256:d6ff8eab5ab73a0c852c34fbbe332d4c26fb94b25c3c5c131ffe94ce7cb308d7`  
		Last Modified: Wed, 17 Jun 2026 21:53:25 GMT  
		Size: 5.4 MB (5448561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d827abda2e7f600552e445b160ed038f68f9dc2d296d4bd547a8bf9f54e2622`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:547dc796172917644af167b3e32ec4815e8ce685f1316d8a009a48a30d416728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121090970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c6402c136fab7b18179d52a70cfd52bf2367365d6ee9185656c1c735a5d56f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:46 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
USER kong
# Wed, 17 Jun 2026 21:53:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75928a78297abbfc30d516c90561170c45e32f258534a23545a4f8d72a9e0b59`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6f091c6d3c7f0f3d6fd4549927177662ea698e5043d2efcd210e224689aaf`  
		Last Modified: Wed, 17 Jun 2026 21:53:30 GMT  
		Size: 92.2 MB (92213275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e7b8ab7a887f7333cf5a5cc48fa1dd333fda2b6e6fa8b20d2719a6541a926d`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:09cb1678fdb985cc60d21fc2de0e0b488de889ea41e962737052677bd82ac63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ace6c42a2ba6ff528665cf53a06260b6f81b6946f69314d8d2477bdbd9a5ea`

```dockerfile
```

-	Layers:
	-	`sha256:0ac77c25678154d78fa0e08cd6af256ada5c0b45bf09ddae2085d2167b3f8a81`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 5.5 MB (5455728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70384f08cf37dfbcc303041c2339971991ae0ba8f57759c1402f9e649f8b5f5`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.3`

```console
$ docker pull kong@sha256:8a6a7a48af3161ec0ac2ee909e5f94dd83ad7d8668479da620ee85046c5b266e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.3` - linux; amd64

```console
$ docker pull kong@sha256:476c99dc77ee32867547188015e7b3e3bb4a2a94847fbe64f0b5ba5a23649c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122824648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f047bc123120f40c0d563f87ff934673033175b277528401899485e6a5e5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:49 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
USER kong
# Wed, 17 Jun 2026 21:53:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2c50624783cdc4dba30e087715d002012a972e8dd67356315b83ee23456c95`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1926f0f3104f2b63195d737e9d94b27facb50becfa254a37fd455884a5aa7cf`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 93.1 MB (93090550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536147b95eab04fdc424b6411d89ca89d6e97aa778ceed60f9be003fcd436316`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.3` - unknown; unknown

```console
$ docker pull kong@sha256:d2787b5ebb11a611c10a5b283279ee2214d1d0be5569c10f2dd2569339903bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c3b990ce3c1efc4ddc398ff78b4490ae9526727e199709bc941c7af95bd503`

```dockerfile
```

-	Layers:
	-	`sha256:d6ff8eab5ab73a0c852c34fbbe332d4c26fb94b25c3c5c131ffe94ce7cb308d7`  
		Last Modified: Wed, 17 Jun 2026 21:53:25 GMT  
		Size: 5.4 MB (5448561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d827abda2e7f600552e445b160ed038f68f9dc2d296d4bd547a8bf9f54e2622`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:547dc796172917644af167b3e32ec4815e8ce685f1316d8a009a48a30d416728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121090970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c6402c136fab7b18179d52a70cfd52bf2367365d6ee9185656c1c735a5d56f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:46 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
USER kong
# Wed, 17 Jun 2026 21:53:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75928a78297abbfc30d516c90561170c45e32f258534a23545a4f8d72a9e0b59`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6f091c6d3c7f0f3d6fd4549927177662ea698e5043d2efcd210e224689aaf`  
		Last Modified: Wed, 17 Jun 2026 21:53:30 GMT  
		Size: 92.2 MB (92213275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e7b8ab7a887f7333cf5a5cc48fa1dd333fda2b6e6fa8b20d2719a6541a926d`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.3` - unknown; unknown

```console
$ docker pull kong@sha256:09cb1678fdb985cc60d21fc2de0e0b488de889ea41e962737052677bd82ac63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ace6c42a2ba6ff528665cf53a06260b6f81b6946f69314d8d2477bdbd9a5ea`

```dockerfile
```

-	Layers:
	-	`sha256:0ac77c25678154d78fa0e08cd6af256ada5c0b45bf09ddae2085d2167b3f8a81`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 5.5 MB (5455728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70384f08cf37dfbcc303041c2339971991ae0ba8f57759c1402f9e649f8b5f5`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.3-ubuntu`

```console
$ docker pull kong@sha256:8a6a7a48af3161ec0ac2ee909e5f94dd83ad7d8668479da620ee85046c5b266e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:476c99dc77ee32867547188015e7b3e3bb4a2a94847fbe64f0b5ba5a23649c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122824648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f047bc123120f40c0d563f87ff934673033175b277528401899485e6a5e5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:49 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
USER kong
# Wed, 17 Jun 2026 21:53:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2c50624783cdc4dba30e087715d002012a972e8dd67356315b83ee23456c95`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1926f0f3104f2b63195d737e9d94b27facb50becfa254a37fd455884a5aa7cf`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 93.1 MB (93090550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536147b95eab04fdc424b6411d89ca89d6e97aa778ceed60f9be003fcd436316`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.3-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d2787b5ebb11a611c10a5b283279ee2214d1d0be5569c10f2dd2569339903bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c3b990ce3c1efc4ddc398ff78b4490ae9526727e199709bc941c7af95bd503`

```dockerfile
```

-	Layers:
	-	`sha256:d6ff8eab5ab73a0c852c34fbbe332d4c26fb94b25c3c5c131ffe94ce7cb308d7`  
		Last Modified: Wed, 17 Jun 2026 21:53:25 GMT  
		Size: 5.4 MB (5448561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d827abda2e7f600552e445b160ed038f68f9dc2d296d4bd547a8bf9f54e2622`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:547dc796172917644af167b3e32ec4815e8ce685f1316d8a009a48a30d416728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121090970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c6402c136fab7b18179d52a70cfd52bf2367365d6ee9185656c1c735a5d56f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:46 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
USER kong
# Wed, 17 Jun 2026 21:53:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75928a78297abbfc30d516c90561170c45e32f258534a23545a4f8d72a9e0b59`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6f091c6d3c7f0f3d6fd4549927177662ea698e5043d2efcd210e224689aaf`  
		Last Modified: Wed, 17 Jun 2026 21:53:30 GMT  
		Size: 92.2 MB (92213275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e7b8ab7a887f7333cf5a5cc48fa1dd333fda2b6e6fa8b20d2719a6541a926d`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.3-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:09cb1678fdb985cc60d21fc2de0e0b488de889ea41e962737052677bd82ac63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ace6c42a2ba6ff528665cf53a06260b6f81b6946f69314d8d2477bdbd9a5ea`

```dockerfile
```

-	Layers:
	-	`sha256:0ac77c25678154d78fa0e08cd6af256ada5c0b45bf09ddae2085d2167b3f8a81`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 5.5 MB (5455728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70384f08cf37dfbcc303041c2339971991ae0ba8f57759c1402f9e649f8b5f5`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:8a6a7a48af3161ec0ac2ee909e5f94dd83ad7d8668479da620ee85046c5b266e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:476c99dc77ee32867547188015e7b3e3bb4a2a94847fbe64f0b5ba5a23649c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122824648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f047bc123120f40c0d563f87ff934673033175b277528401899485e6a5e5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:49 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
USER kong
# Wed, 17 Jun 2026 21:53:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2c50624783cdc4dba30e087715d002012a972e8dd67356315b83ee23456c95`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1926f0f3104f2b63195d737e9d94b27facb50becfa254a37fd455884a5aa7cf`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 93.1 MB (93090550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536147b95eab04fdc424b6411d89ca89d6e97aa778ceed60f9be003fcd436316`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:d2787b5ebb11a611c10a5b283279ee2214d1d0be5569c10f2dd2569339903bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c3b990ce3c1efc4ddc398ff78b4490ae9526727e199709bc941c7af95bd503`

```dockerfile
```

-	Layers:
	-	`sha256:d6ff8eab5ab73a0c852c34fbbe332d4c26fb94b25c3c5c131ffe94ce7cb308d7`  
		Last Modified: Wed, 17 Jun 2026 21:53:25 GMT  
		Size: 5.4 MB (5448561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d827abda2e7f600552e445b160ed038f68f9dc2d296d4bd547a8bf9f54e2622`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:547dc796172917644af167b3e32ec4815e8ce685f1316d8a009a48a30d416728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121090970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c6402c136fab7b18179d52a70cfd52bf2367365d6ee9185656c1c735a5d56f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:46 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
USER kong
# Wed, 17 Jun 2026 21:53:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75928a78297abbfc30d516c90561170c45e32f258534a23545a4f8d72a9e0b59`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6f091c6d3c7f0f3d6fd4549927177662ea698e5043d2efcd210e224689aaf`  
		Last Modified: Wed, 17 Jun 2026 21:53:30 GMT  
		Size: 92.2 MB (92213275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e7b8ab7a887f7333cf5a5cc48fa1dd333fda2b6e6fa8b20d2719a6541a926d`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:09cb1678fdb985cc60d21fc2de0e0b488de889ea41e962737052677bd82ac63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ace6c42a2ba6ff528665cf53a06260b6f81b6946f69314d8d2477bdbd9a5ea`

```dockerfile
```

-	Layers:
	-	`sha256:0ac77c25678154d78fa0e08cd6af256ada5c0b45bf09ddae2085d2167b3f8a81`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 5.5 MB (5455728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70384f08cf37dfbcc303041c2339971991ae0ba8f57759c1402f9e649f8b5f5`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:8a6a7a48af3161ec0ac2ee909e5f94dd83ad7d8668479da620ee85046c5b266e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:476c99dc77ee32867547188015e7b3e3bb4a2a94847fbe64f0b5ba5a23649c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122824648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1f047bc123120f40c0d563f87ff934673033175b277528401899485e6a5e5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:49 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:49 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:49 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:08 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:08 GMT
USER kong
# Wed, 17 Jun 2026 21:53:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:08 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:08 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2c50624783cdc4dba30e087715d002012a972e8dd67356315b83ee23456c95`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1926f0f3104f2b63195d737e9d94b27facb50becfa254a37fd455884a5aa7cf`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 93.1 MB (93090550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536147b95eab04fdc424b6411d89ca89d6e97aa778ceed60f9be003fcd436316`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:d2787b5ebb11a611c10a5b283279ee2214d1d0be5569c10f2dd2569339903bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c3b990ce3c1efc4ddc398ff78b4490ae9526727e199709bc941c7af95bd503`

```dockerfile
```

-	Layers:
	-	`sha256:d6ff8eab5ab73a0c852c34fbbe332d4c26fb94b25c3c5c131ffe94ce7cb308d7`  
		Last Modified: Wed, 17 Jun 2026 21:53:25 GMT  
		Size: 5.4 MB (5448561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d827abda2e7f600552e445b160ed038f68f9dc2d296d4bd547a8bf9f54e2622`  
		Last Modified: Wed, 17 Jun 2026 21:53:24 GMT  
		Size: 16.2 KB (16217 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:547dc796172917644af167b3e32ec4815e8ce685f1316d8a009a48a30d416728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121090970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c6402c136fab7b18179d52a70cfd52bf2367365d6ee9185656c1c735a5d56f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Jun 2026 21:52:46 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 17 Jun 2026 21:52:46 GMT
ARG ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ENV ASSET=ce
# Wed, 17 Jun 2026 21:52:46 GMT
ARG EE_PORTS
# Wed, 17 Jun 2026 21:52:46 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ENV KONG_VERSION=3.9.3
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872
# Wed, 17 Jun 2026 21:52:46 GMT
ARG KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
# Wed, 17 Jun 2026 21:53:09 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.3 KONG_AMD64_SHA=3b0bcaf6701b02c10fc2afd692f8e4411b981f0ed1b765f3c3b0f036fe373872 KONG_ARM64_SHA=fd62644015296c70f29802da287dec8f7d46ac0715f844e52c84a0df6b479763
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Wed, 17 Jun 2026 21:53:09 GMT
USER kong
# Wed, 17 Jun 2026 21:53:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 21:53:09 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Wed, 17 Jun 2026 21:53:09 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 21:53:09 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Wed, 17 Jun 2026 21:53:09 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75928a78297abbfc30d516c90561170c45e32f258534a23545a4f8d72a9e0b59`  
		Last Modified: Wed, 17 Jun 2026 21:53:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c6f091c6d3c7f0f3d6fd4549927177662ea698e5043d2efcd210e224689aaf`  
		Last Modified: Wed, 17 Jun 2026 21:53:30 GMT  
		Size: 92.2 MB (92213275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e7b8ab7a887f7333cf5a5cc48fa1dd333fda2b6e6fa8b20d2719a6541a926d`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:09cb1678fdb985cc60d21fc2de0e0b488de889ea41e962737052677bd82ac63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ace6c42a2ba6ff528665cf53a06260b6f81b6946f69314d8d2477bdbd9a5ea`

```dockerfile
```

-	Layers:
	-	`sha256:0ac77c25678154d78fa0e08cd6af256ada5c0b45bf09ddae2085d2167b3f8a81`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 5.5 MB (5455728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70384f08cf37dfbcc303041c2339971991ae0ba8f57759c1402f9e649f8b5f5`  
		Last Modified: Wed, 17 Jun 2026 21:53:28 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json
