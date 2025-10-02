## `kong:latest`

```console
$ docker pull kong@sha256:30597ffe2fc98160b979311d18f7649edd1ed3bf145063e99b1ef89775a668d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:4c19d5e04a76d2ae7df943a376ace1c3e23beaed5236adc4c0e87aac1c665d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120408151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38930d56606d4e6c271cce8c63b4bf401a728c8887517ebb0ea15823411cd51b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a737aeb4167a859699887d661b37d589e3912ec02074d61c9874d05dffce9`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbd7d3d0fb9226e4d5f77687f5c6ff36bb9dd1d1add48fa190ab6aa5f66926f`  
		Last Modified: Mon, 15 Sep 2025 22:20:01 GMT  
		Size: 90.7 MB (90683414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df30bba013e8ad37a8eefab77989731e08963276c2b67790edf321591f2a25ae`  
		Last Modified: Mon, 15 Sep 2025 22:19:52 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:2fef901c98c46906a1354c398f4bac15fd535f413fb1b7fb1226964801e2c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900359cfd9dd50cf616c65d415c62228193851fd8b3ccbc50ca6fe9af4e39654`

```dockerfile
```

-	Layers:
	-	`sha256:7aab9f71b6b92b83016eba41bc8aebad9641898b5bfa9989d6d7de910cf6198b`  
		Last Modified: Mon, 15 Sep 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0125d3b6f729fe5019e34209322e91d0ab2f975dcc3c4fb9533f757fc115d36`  
		Last Modified: Mon, 15 Sep 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d86a6b9a4b3faec087553390345c2031dea5cb9debcf932f5e43faee0beb97bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121092354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9c7a014f198480b766b5ce5ed41186b357e2e5c60c94c8b3929484850d2e9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 05 Jun 2025 09:03:49 GMT
ARG RELEASE
# Thu, 05 Jun 2025 09:03:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 05 Jun 2025 09:03:49 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["/bin/bash"]
# Thu, 05 Jun 2025 09:03:49 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 05 Jun 2025 09:03:49 GMT
ARG ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ENV ASSET=ce
# Thu, 05 Jun 2025 09:03:49 GMT
ARG EE_PORTS
# Thu, 05 Jun 2025 09:03:49 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ENV KONG_VERSION=3.9.1
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac
# Thu, 05 Jun 2025 09:03:49 GMT
ARG KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
# Thu, 05 Jun 2025 09:03:49 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.9.1 KONG_AMD64_SHA=8f493149bfc321d3108e5031f5008dd1511aed166fb0d4673916577d04c63eac KONG_ARM64_SHA=87f9c971d232c71fcd21808c65082cdd9ded3441950c00d2718206b6438c7cd8
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 05 Jun 2025 09:03:49 GMT
USER kong
# Thu, 05 Jun 2025 09:03:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Jun 2025 09:03:49 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 05 Jun 2025 09:03:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Jun 2025 09:03:49 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 05 Jun 2025 09:03:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f086a091e2e1c2a02d87a8e877d82423698cec857fbbdeb1da6d5228b8855c00`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6068b25573db1ae2c976e98bf35c9a3842e28bbee1cc9c62896d24e5f642e5c`  
		Last Modified: Thu, 02 Oct 2025 01:25:06 GMT  
		Size: 92.2 MB (92229492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78f0ef82511f19628f19bacaba5f2349580bd3e55ace63e3ab4e0a217d45860`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:82df75418b58a6cb1e5047fea79d2f2cad8cd772e74a2d38148c590fc0beffc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd82f42126f80f41756ee10d8dfb7eeae8cc26af48eddb9fe7c045baeb88a55`

```dockerfile
```

-	Layers:
	-	`sha256:a064f1c26d8055f0cb3784ccf93a4954f27f39da3d9329d9c2a498c39e67172f`  
		Last Modified: Thu, 02 Oct 2025 02:51:22 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:429a20f1215dd81cf6717a62dc17d3a905ac39afcd1c1d61e0484eefd645cbcd`  
		Last Modified: Thu, 02 Oct 2025 02:51:23 GMT  
		Size: 16.4 KB (16401 bytes)  
		MIME: application/vnd.in-toto+json
