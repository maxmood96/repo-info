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
$ docker pull kong@sha256:a2b02d517849d74f861cf001ac72e1775549bcac0e95d85ed45593390d516a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8c4bda3fc0610fcd500c0c5fb1c6e01cc3730346ef70381ed5c26b4b2eb81940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185638925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789f1792a1304ae1090c147f58fb6ff85311aacd01a7d7f2cde5e2364875d3a5`
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
# Fri, 15 May 2026 21:19:45 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:45 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:45 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:45 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:45 GMT
ARG KONG_VERSION=2.8.5
# Fri, 15 May 2026 21:19:45 GMT
ENV KONG_VERSION=2.8.5
# Fri, 15 May 2026 21:19:45 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Fri, 15 May 2026 21:19:45 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 15 May 2026 21:20:16 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:20:16 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:20:16 GMT
USER kong
# Fri, 15 May 2026 21:20:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:20:16 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:20:16 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:20:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:20:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b4d7dbe018824334b8e135e2e09450208c2b239f23032491fd312627bdbeb3`  
		Last Modified: Fri, 15 May 2026 21:20:40 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c780c38bc6386a577f30708d22f0f67a91e5cf90e0db5ef56da78c181b7b72`  
		Last Modified: Fri, 15 May 2026 21:20:47 GMT  
		Size: 130.8 MB (130819393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94feb8a5e7434baabbaa4efecfd425aba1e826738be99eac5aad8ac52746e74`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:4fc5f56ffd04a56e87561bade2b5b9123071b47ddddaf0b590a0d037965e76be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55dc6e881048d274bdf852fa767525cfd8ce63cc7feebbdb2439bc5ee04826a`

```dockerfile
```

-	Layers:
	-	`sha256:64e2d9831fbb1ecc697b462273f559d93287d2d15180482216932e97c6137293`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 7.3 MB (7347748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29490dd90d0d0850bd780c88f7c58da35e07f2871755698ce06aa487ebcb8ae`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:a2b02d517849d74f861cf001ac72e1775549bcac0e95d85ed45593390d516a5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:8c4bda3fc0610fcd500c0c5fb1c6e01cc3730346ef70381ed5c26b4b2eb81940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185638925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789f1792a1304ae1090c147f58fb6ff85311aacd01a7d7f2cde5e2364875d3a5`
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
# Fri, 15 May 2026 21:19:45 GMT
ARG ASSET=ce
# Fri, 15 May 2026 21:19:45 GMT
ENV ASSET=ce
# Fri, 15 May 2026 21:19:45 GMT
ARG EE_PORTS
# Fri, 15 May 2026 21:19:45 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Fri, 15 May 2026 21:19:45 GMT
ARG KONG_VERSION=2.8.5
# Fri, 15 May 2026 21:19:45 GMT
ENV KONG_VERSION=2.8.5
# Fri, 15 May 2026 21:19:45 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Fri, 15 May 2026 21:19:45 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Fri, 15 May 2026 21:20:16 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Fri, 15 May 2026 21:20:16 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 15 May 2026 21:20:16 GMT
USER kong
# Fri, 15 May 2026 21:20:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 15 May 2026 21:20:16 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Fri, 15 May 2026 21:20:16 GMT
STOPSIGNAL SIGQUIT
# Fri, 15 May 2026 21:20:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Fri, 15 May 2026 21:20:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b4d7dbe018824334b8e135e2e09450208c2b239f23032491fd312627bdbeb3`  
		Last Modified: Fri, 15 May 2026 21:20:40 GMT  
		Size: 25.1 MB (25081967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c780c38bc6386a577f30708d22f0f67a91e5cf90e0db5ef56da78c181b7b72`  
		Last Modified: Fri, 15 May 2026 21:20:47 GMT  
		Size: 130.8 MB (130819393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94feb8a5e7434baabbaa4efecfd425aba1e826738be99eac5aad8ac52746e74`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:4fc5f56ffd04a56e87561bade2b5b9123071b47ddddaf0b590a0d037965e76be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55dc6e881048d274bdf852fa767525cfd8ce63cc7feebbdb2439bc5ee04826a`

```dockerfile
```

-	Layers:
	-	`sha256:64e2d9831fbb1ecc697b462273f559d93287d2d15180482216932e97c6137293`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 7.3 MB (7347748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c29490dd90d0d0850bd780c88f7c58da35e07f2871755698ce06aa487ebcb8ae`  
		Last Modified: Fri, 15 May 2026 21:20:38 GMT  
		Size: 14.4 KB (14443 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:76c14b93e989f7f4418039f7f9789ca32564016211c86ac1a18022f4788e7b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:9f749b03265c67476119cbaae3966bb61beb3c1e474d9ba5aa2c1d6d4c28a66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120428709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c3d7f0e740c7797e066e357360edb4fcba1d084d34a02ed30271d03cf14a4`
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
# Tue, 02 Jun 2026 08:18:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:36 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:36 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:18:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
USER kong
# Tue, 02 Jun 2026 08:18:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:18:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:18:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:18:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c50d4d5acfb66154ee918bd062a98f61ccaae3d5666394983282597191a922`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ab210ff1d911c416f671eca9d48ae5fecf4835361a65a1ee7293b0fd543c71`  
		Last Modified: Tue, 02 Jun 2026 08:19:17 GMT  
		Size: 90.7 MB (90694619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae500fe64d1ab1a86893be2364c944fec4890fb5e90e294ff9df4f46f60e6eb3`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:af1f485671a04c40761e5ff679322f44856333e2ed9f89aee8ade49ab45668ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5566b599c9878771c451e87f418566eeab5e94d99ea3a4458fbbf2b424b93e90`

```dockerfile
```

-	Layers:
	-	`sha256:13e0c4276fc74f7807bdf161f036a928d60ca1677ce5fc151d564561a0a08fcd`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 5.4 MB (5421176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a901b6b04ad0e90056ce2dbf05d533a77bfd29a4651999b7d3bb60f5cd275f5e`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0964be0d4523faafcf51f73760521509fa74e1ce9dac74f02b1c3f05e0b89082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118883873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dae4eb58a95201712f886f3299a98dcf7c094597c170380f66fee69c34aed00`
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
# Tue, 02 Jun 2026 08:18:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:47 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:19:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
USER kong
# Tue, 02 Jun 2026 08:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:19:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:19:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:19:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0567ee103ba485041fa7d423a5d763f8deed0a5810a5d2ba3f67afb031f70`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14964c990086dc128b359ff523267f3560d4bb68a42575ab111624996c1a702`  
		Last Modified: Tue, 02 Jun 2026 08:19:31 GMT  
		Size: 90.0 MB (90006182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d655b49f6c3be4733181121ae37a5a692d655ae8577845ea32bd9fdd5eb36`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:9bce4ad9042ae059a95fa67647b4b13b0842d11a7f0e473669c3b29cbcdf86ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdf761e7c5e44fcab37277d1154ea52caef24c8f13fec81f1bc6e0b52d6c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f255e86e8d75f5bf91cce923a5a7ee1cd43adcdc1847076df1cce60639d3e9d0`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 5.4 MB (5428343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98d0e7ed0628754d4c2a5d61841762c18a52a45fbc85265599c610287a25524`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
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
$ docker pull kong@sha256:76c14b93e989f7f4418039f7f9789ca32564016211c86ac1a18022f4788e7b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:9f749b03265c67476119cbaae3966bb61beb3c1e474d9ba5aa2c1d6d4c28a66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120428709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c3d7f0e740c7797e066e357360edb4fcba1d084d34a02ed30271d03cf14a4`
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
# Tue, 02 Jun 2026 08:18:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:36 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:36 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:18:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
USER kong
# Tue, 02 Jun 2026 08:18:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:18:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:18:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:18:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c50d4d5acfb66154ee918bd062a98f61ccaae3d5666394983282597191a922`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ab210ff1d911c416f671eca9d48ae5fecf4835361a65a1ee7293b0fd543c71`  
		Last Modified: Tue, 02 Jun 2026 08:19:17 GMT  
		Size: 90.7 MB (90694619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae500fe64d1ab1a86893be2364c944fec4890fb5e90e294ff9df4f46f60e6eb3`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:af1f485671a04c40761e5ff679322f44856333e2ed9f89aee8ade49ab45668ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5566b599c9878771c451e87f418566eeab5e94d99ea3a4458fbbf2b424b93e90`

```dockerfile
```

-	Layers:
	-	`sha256:13e0c4276fc74f7807bdf161f036a928d60ca1677ce5fc151d564561a0a08fcd`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 5.4 MB (5421176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a901b6b04ad0e90056ce2dbf05d533a77bfd29a4651999b7d3bb60f5cd275f5e`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0964be0d4523faafcf51f73760521509fa74e1ce9dac74f02b1c3f05e0b89082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118883873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dae4eb58a95201712f886f3299a98dcf7c094597c170380f66fee69c34aed00`
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
# Tue, 02 Jun 2026 08:18:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:47 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:19:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
USER kong
# Tue, 02 Jun 2026 08:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:19:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:19:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:19:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0567ee103ba485041fa7d423a5d763f8deed0a5810a5d2ba3f67afb031f70`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14964c990086dc128b359ff523267f3560d4bb68a42575ab111624996c1a702`  
		Last Modified: Tue, 02 Jun 2026 08:19:31 GMT  
		Size: 90.0 MB (90006182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d655b49f6c3be4733181121ae37a5a692d655ae8577845ea32bd9fdd5eb36`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:9bce4ad9042ae059a95fa67647b4b13b0842d11a7f0e473669c3b29cbcdf86ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdf761e7c5e44fcab37277d1154ea52caef24c8f13fec81f1bc6e0b52d6c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f255e86e8d75f5bf91cce923a5a7ee1cd43adcdc1847076df1cce60639d3e9d0`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 5.4 MB (5428343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98d0e7ed0628754d4c2a5d61841762c18a52a45fbc85265599c610287a25524`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:76c14b93e989f7f4418039f7f9789ca32564016211c86ac1a18022f4788e7b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9f749b03265c67476119cbaae3966bb61beb3c1e474d9ba5aa2c1d6d4c28a66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120428709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c3d7f0e740c7797e066e357360edb4fcba1d084d34a02ed30271d03cf14a4`
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
# Tue, 02 Jun 2026 08:18:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:36 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:36 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:18:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
USER kong
# Tue, 02 Jun 2026 08:18:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:18:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:18:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:18:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c50d4d5acfb66154ee918bd062a98f61ccaae3d5666394983282597191a922`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ab210ff1d911c416f671eca9d48ae5fecf4835361a65a1ee7293b0fd543c71`  
		Last Modified: Tue, 02 Jun 2026 08:19:17 GMT  
		Size: 90.7 MB (90694619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae500fe64d1ab1a86893be2364c944fec4890fb5e90e294ff9df4f46f60e6eb3`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:af1f485671a04c40761e5ff679322f44856333e2ed9f89aee8ade49ab45668ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5566b599c9878771c451e87f418566eeab5e94d99ea3a4458fbbf2b424b93e90`

```dockerfile
```

-	Layers:
	-	`sha256:13e0c4276fc74f7807bdf161f036a928d60ca1677ce5fc151d564561a0a08fcd`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 5.4 MB (5421176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a901b6b04ad0e90056ce2dbf05d533a77bfd29a4651999b7d3bb60f5cd275f5e`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0964be0d4523faafcf51f73760521509fa74e1ce9dac74f02b1c3f05e0b89082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118883873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dae4eb58a95201712f886f3299a98dcf7c094597c170380f66fee69c34aed00`
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
# Tue, 02 Jun 2026 08:18:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:47 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:19:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
USER kong
# Tue, 02 Jun 2026 08:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:19:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:19:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:19:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0567ee103ba485041fa7d423a5d763f8deed0a5810a5d2ba3f67afb031f70`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14964c990086dc128b359ff523267f3560d4bb68a42575ab111624996c1a702`  
		Last Modified: Tue, 02 Jun 2026 08:19:31 GMT  
		Size: 90.0 MB (90006182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d655b49f6c3be4733181121ae37a5a692d655ae8577845ea32bd9fdd5eb36`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9bce4ad9042ae059a95fa67647b4b13b0842d11a7f0e473669c3b29cbcdf86ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdf761e7c5e44fcab37277d1154ea52caef24c8f13fec81f1bc6e0b52d6c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f255e86e8d75f5bf91cce923a5a7ee1cd43adcdc1847076df1cce60639d3e9d0`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 5.4 MB (5428343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98d0e7ed0628754d4c2a5d61841762c18a52a45fbc85265599c610287a25524`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:76c14b93e989f7f4418039f7f9789ca32564016211c86ac1a18022f4788e7b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:9f749b03265c67476119cbaae3966bb61beb3c1e474d9ba5aa2c1d6d4c28a66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120428709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c3d7f0e740c7797e066e357360edb4fcba1d084d34a02ed30271d03cf14a4`
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
# Tue, 02 Jun 2026 08:18:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:36 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:36 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:18:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
USER kong
# Tue, 02 Jun 2026 08:18:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:18:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:18:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:18:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c50d4d5acfb66154ee918bd062a98f61ccaae3d5666394983282597191a922`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ab210ff1d911c416f671eca9d48ae5fecf4835361a65a1ee7293b0fd543c71`  
		Last Modified: Tue, 02 Jun 2026 08:19:17 GMT  
		Size: 90.7 MB (90694619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae500fe64d1ab1a86893be2364c944fec4890fb5e90e294ff9df4f46f60e6eb3`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:af1f485671a04c40761e5ff679322f44856333e2ed9f89aee8ade49ab45668ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5566b599c9878771c451e87f418566eeab5e94d99ea3a4458fbbf2b424b93e90`

```dockerfile
```

-	Layers:
	-	`sha256:13e0c4276fc74f7807bdf161f036a928d60ca1677ce5fc151d564561a0a08fcd`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 5.4 MB (5421176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a901b6b04ad0e90056ce2dbf05d533a77bfd29a4651999b7d3bb60f5cd275f5e`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0964be0d4523faafcf51f73760521509fa74e1ce9dac74f02b1c3f05e0b89082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118883873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dae4eb58a95201712f886f3299a98dcf7c094597c170380f66fee69c34aed00`
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
# Tue, 02 Jun 2026 08:18:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:47 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:19:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
USER kong
# Tue, 02 Jun 2026 08:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:19:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:19:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:19:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0567ee103ba485041fa7d423a5d763f8deed0a5810a5d2ba3f67afb031f70`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14964c990086dc128b359ff523267f3560d4bb68a42575ab111624996c1a702`  
		Last Modified: Tue, 02 Jun 2026 08:19:31 GMT  
		Size: 90.0 MB (90006182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d655b49f6c3be4733181121ae37a5a692d655ae8577845ea32bd9fdd5eb36`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:9bce4ad9042ae059a95fa67647b4b13b0842d11a7f0e473669c3b29cbcdf86ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdf761e7c5e44fcab37277d1154ea52caef24c8f13fec81f1bc6e0b52d6c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f255e86e8d75f5bf91cce923a5a7ee1cd43adcdc1847076df1cce60639d3e9d0`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 5.4 MB (5428343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98d0e7ed0628754d4c2a5d61841762c18a52a45fbc85265599c610287a25524`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:76c14b93e989f7f4418039f7f9789ca32564016211c86ac1a18022f4788e7b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9f749b03265c67476119cbaae3966bb61beb3c1e474d9ba5aa2c1d6d4c28a66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120428709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c3d7f0e740c7797e066e357360edb4fcba1d084d34a02ed30271d03cf14a4`
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
# Tue, 02 Jun 2026 08:18:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:36 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:36 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:18:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
USER kong
# Tue, 02 Jun 2026 08:18:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:18:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:18:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:18:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c50d4d5acfb66154ee918bd062a98f61ccaae3d5666394983282597191a922`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ab210ff1d911c416f671eca9d48ae5fecf4835361a65a1ee7293b0fd543c71`  
		Last Modified: Tue, 02 Jun 2026 08:19:17 GMT  
		Size: 90.7 MB (90694619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae500fe64d1ab1a86893be2364c944fec4890fb5e90e294ff9df4f46f60e6eb3`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:af1f485671a04c40761e5ff679322f44856333e2ed9f89aee8ade49ab45668ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5566b599c9878771c451e87f418566eeab5e94d99ea3a4458fbbf2b424b93e90`

```dockerfile
```

-	Layers:
	-	`sha256:13e0c4276fc74f7807bdf161f036a928d60ca1677ce5fc151d564561a0a08fcd`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 5.4 MB (5421176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a901b6b04ad0e90056ce2dbf05d533a77bfd29a4651999b7d3bb60f5cd275f5e`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0964be0d4523faafcf51f73760521509fa74e1ce9dac74f02b1c3f05e0b89082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118883873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dae4eb58a95201712f886f3299a98dcf7c094597c170380f66fee69c34aed00`
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
# Tue, 02 Jun 2026 08:18:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:47 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:19:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
USER kong
# Tue, 02 Jun 2026 08:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:19:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:19:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:19:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0567ee103ba485041fa7d423a5d763f8deed0a5810a5d2ba3f67afb031f70`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14964c990086dc128b359ff523267f3560d4bb68a42575ab111624996c1a702`  
		Last Modified: Tue, 02 Jun 2026 08:19:31 GMT  
		Size: 90.0 MB (90006182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d655b49f6c3be4733181121ae37a5a692d655ae8577845ea32bd9fdd5eb36`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9bce4ad9042ae059a95fa67647b4b13b0842d11a7f0e473669c3b29cbcdf86ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdf761e7c5e44fcab37277d1154ea52caef24c8f13fec81f1bc6e0b52d6c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f255e86e8d75f5bf91cce923a5a7ee1cd43adcdc1847076df1cce60639d3e9d0`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 5.4 MB (5428343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98d0e7ed0628754d4c2a5d61841762c18a52a45fbc85265599c610287a25524`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:76c14b93e989f7f4418039f7f9789ca32564016211c86ac1a18022f4788e7b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:9f749b03265c67476119cbaae3966bb61beb3c1e474d9ba5aa2c1d6d4c28a66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120428709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c3d7f0e740c7797e066e357360edb4fcba1d084d34a02ed30271d03cf14a4`
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
# Tue, 02 Jun 2026 08:18:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:36 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:36 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:18:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
USER kong
# Tue, 02 Jun 2026 08:18:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:18:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:18:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:18:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c50d4d5acfb66154ee918bd062a98f61ccaae3d5666394983282597191a922`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ab210ff1d911c416f671eca9d48ae5fecf4835361a65a1ee7293b0fd543c71`  
		Last Modified: Tue, 02 Jun 2026 08:19:17 GMT  
		Size: 90.7 MB (90694619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae500fe64d1ab1a86893be2364c944fec4890fb5e90e294ff9df4f46f60e6eb3`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:af1f485671a04c40761e5ff679322f44856333e2ed9f89aee8ade49ab45668ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5566b599c9878771c451e87f418566eeab5e94d99ea3a4458fbbf2b424b93e90`

```dockerfile
```

-	Layers:
	-	`sha256:13e0c4276fc74f7807bdf161f036a928d60ca1677ce5fc151d564561a0a08fcd`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 5.4 MB (5421176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a901b6b04ad0e90056ce2dbf05d533a77bfd29a4651999b7d3bb60f5cd275f5e`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0964be0d4523faafcf51f73760521509fa74e1ce9dac74f02b1c3f05e0b89082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118883873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dae4eb58a95201712f886f3299a98dcf7c094597c170380f66fee69c34aed00`
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
# Tue, 02 Jun 2026 08:18:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:47 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:19:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
USER kong
# Tue, 02 Jun 2026 08:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:19:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:19:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:19:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0567ee103ba485041fa7d423a5d763f8deed0a5810a5d2ba3f67afb031f70`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14964c990086dc128b359ff523267f3560d4bb68a42575ab111624996c1a702`  
		Last Modified: Tue, 02 Jun 2026 08:19:31 GMT  
		Size: 90.0 MB (90006182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d655b49f6c3be4733181121ae37a5a692d655ae8577845ea32bd9fdd5eb36`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:9bce4ad9042ae059a95fa67647b4b13b0842d11a7f0e473669c3b29cbcdf86ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdf761e7c5e44fcab37277d1154ea52caef24c8f13fec81f1bc6e0b52d6c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f255e86e8d75f5bf91cce923a5a7ee1cd43adcdc1847076df1cce60639d3e9d0`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 5.4 MB (5428343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98d0e7ed0628754d4c2a5d61841762c18a52a45fbc85265599c610287a25524`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:76c14b93e989f7f4418039f7f9789ca32564016211c86ac1a18022f4788e7b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9f749b03265c67476119cbaae3966bb61beb3c1e474d9ba5aa2c1d6d4c28a66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120428709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5c3d7f0e740c7797e066e357360edb4fcba1d084d34a02ed30271d03cf14a4`
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
# Tue, 02 Jun 2026 08:18:36 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:36 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:36 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:36 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:36 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:18:57 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:18:57 GMT
USER kong
# Tue, 02 Jun 2026 08:18:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:18:57 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:18:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:18:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:18:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c50d4d5acfb66154ee918bd062a98f61ccaae3d5666394983282597191a922`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ab210ff1d911c416f671eca9d48ae5fecf4835361a65a1ee7293b0fd543c71`  
		Last Modified: Tue, 02 Jun 2026 08:19:17 GMT  
		Size: 90.7 MB (90694619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae500fe64d1ab1a86893be2364c944fec4890fb5e90e294ff9df4f46f60e6eb3`  
		Last Modified: Tue, 02 Jun 2026 08:19:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:af1f485671a04c40761e5ff679322f44856333e2ed9f89aee8ade49ab45668ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5566b599c9878771c451e87f418566eeab5e94d99ea3a4458fbbf2b424b93e90`

```dockerfile
```

-	Layers:
	-	`sha256:13e0c4276fc74f7807bdf161f036a928d60ca1677ce5fc151d564561a0a08fcd`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 5.4 MB (5421176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a901b6b04ad0e90056ce2dbf05d533a77bfd29a4651999b7d3bb60f5cd275f5e`  
		Last Modified: Tue, 02 Jun 2026 08:19:15 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:0964be0d4523faafcf51f73760521509fa74e1ce9dac74f02b1c3f05e0b89082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118883873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dae4eb58a95201712f886f3299a98dcf7c094597c170380f66fee69c34aed00`
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
# Tue, 02 Jun 2026 08:18:47 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 02 Jun 2026 08:18:47 GMT
ARG ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ENV ASSET=ce
# Tue, 02 Jun 2026 08:18:47 GMT
ARG EE_PORTS
# Tue, 02 Jun 2026 08:18:47 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ENV KONG_VERSION=3.9.1
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Tue, 02 Jun 2026 08:18:47 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Tue, 02 Jun 2026 08:19:11 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 08:19:11 GMT
USER kong
# Tue, 02 Jun 2026 08:19:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Jun 2026 08:19:11 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Tue, 02 Jun 2026 08:19:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jun 2026 08:19:11 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Tue, 02 Jun 2026 08:19:11 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c0567ee103ba485041fa7d423a5d763f8deed0a5810a5d2ba3f67afb031f70`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14964c990086dc128b359ff523267f3560d4bb68a42575ab111624996c1a702`  
		Last Modified: Tue, 02 Jun 2026 08:19:31 GMT  
		Size: 90.0 MB (90006182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6d655b49f6c3be4733181121ae37a5a692d655ae8577845ea32bd9fdd5eb36`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9bce4ad9042ae059a95fa67647b4b13b0842d11a7f0e473669c3b29cbcdf86ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afdf761e7c5e44fcab37277d1154ea52caef24c8f13fec81f1bc6e0b52d6c1b`

```dockerfile
```

-	Layers:
	-	`sha256:f255e86e8d75f5bf91cce923a5a7ee1cd43adcdc1847076df1cce60639d3e9d0`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 5.4 MB (5428343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98d0e7ed0628754d4c2a5d61841762c18a52a45fbc85265599c610287a25524`  
		Last Modified: Tue, 02 Jun 2026 08:19:29 GMT  
		Size: 16.4 KB (16358 bytes)  
		MIME: application/vnd.in-toto+json
