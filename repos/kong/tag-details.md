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
