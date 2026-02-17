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
