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
$ docker pull kong@sha256:b4dca11c0e12d0a861bda09d62f76702e70a9a90c711534b6215c5035763b928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2a342f95d416c811f6cf721e3c5faca03051391aed7a0c8758e73408a716ca0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185248654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d96eaca8abd4656493e155644814ae00bcb2159c732ebd368a6c1f05c8fd97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ARG RELEASE
# Mon, 01 Jul 2024 13:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 01 Jul 2024 13:31:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 01 Jul 2024 13:31:38 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 01 Jul 2024 13:31:38 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/bash"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=ce
# Mon, 01 Jul 2024 13:31:38 GMT
ENV ASSET=ce
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b826be5ae7155e3571c1d4c147715aafc92946a7aece2c802756443b816fbd`  
		Last Modified: Thu, 02 Oct 2025 05:10:03 GMT  
		Size: 25.1 MB (25081972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a3b6acd22a7defdf373ba3b2e05bf8a38b2e3732aabb46180a0a05b108f8d`  
		Last Modified: Thu, 02 Oct 2025 06:16:39 GMT  
		Size: 130.6 MB (130628981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6b0e0362e81b56cafa76219b22fdbb886d4d0908cf24e166586cb562b753bc`  
		Last Modified: Thu, 02 Oct 2025 05:10:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c138c44b65a118b01ee258c29145703f3decf41043fb34989c2b13038a533a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854f803eaa052fa98723697e94d05a86f38071b9ce2a5c329030e606383cca24`

```dockerfile
```

-	Layers:
	-	`sha256:462163e3abf6c01e1e3e343649e86497ea6889ac22f70500094140a49f7db693`  
		Last Modified: Thu, 02 Oct 2025 08:51:16 GMT  
		Size: 7.3 MB (7347718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0fa93f559cb313a2c74c3422ffb11ba0ac17f56a1c702d804c825e91535cef`  
		Last Modified: Thu, 02 Oct 2025 08:51:17 GMT  
		Size: 14.5 KB (14486 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:2.8.5-ubuntu`

```console
$ docker pull kong@sha256:b4dca11c0e12d0a861bda09d62f76702e70a9a90c711534b6215c5035763b928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kong:2.8.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2a342f95d416c811f6cf721e3c5faca03051391aed7a0c8758e73408a716ca0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185248654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d96eaca8abd4656493e155644814ae00bcb2159c732ebd368a6c1f05c8fd97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 01 Jul 2024 13:31:38 GMT
ARG RELEASE
# Mon, 01 Jul 2024 13:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 01 Jul 2024 13:31:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 01 Jul 2024 13:31:38 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 01 Jul 2024 13:31:38 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["/bin/bash"]
# Mon, 01 Jul 2024 13:31:38 GMT
ARG ASSET=ce
# Mon, 01 Jul 2024 13:31:38 GMT
ENV ASSET=ce
# Mon, 01 Jul 2024 13:31:38 GMT
ARG EE_PORTS
# Mon, 01 Jul 2024 13:31:38 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ENV KONG_VERSION=2.8.5
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3
# Mon, 01 Jul 2024 13:31:38 GMT
ARG KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
# Mon, 01 Jul 2024 13:31:38 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=2.8.5 KONG_AMD64_SHA=efba2bb8b1cb567bc90cc371e80503c558cbc74377b34609552ae2273def3fe3 KONG_ARM64_SHA=4fff44f9a0c7b06469591b7d1499a99a100109bc3f08dc412dd0eb38ff383d35
RUN set -ex;     arch=$(dpkg --print-architecture);     major_minor="$(echo "${KONG_VERSION%.*}" | tr -d '.')";     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       CODENAME=$(grep -m1 VERSION_CODENAME /etc/os-release | cut -d = -f 2);       apt-get install -y curl       && curl -fL "https://packages.konghq.com/public/gateway-${major_minor}/deb/ubuntu/pool/${CODENAME}/main/k/ko/kong_${KONG_VERSION}/kong_${KONG_VERSION}_${arch}.deb" -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi     && apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb luarocks    && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 01 Jul 2024 13:31:38 GMT
USER kong
# Mon, 01 Jul 2024 13:31:38 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 01 Jul 2024 13:31:38 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Mon, 01 Jul 2024 13:31:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 01 Jul 2024 13:31:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "1m0s" "10s" "0s" "0s" '\n'}
# Mon, 01 Jul 2024 13:31:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b826be5ae7155e3571c1d4c147715aafc92946a7aece2c802756443b816fbd`  
		Last Modified: Thu, 02 Oct 2025 05:10:03 GMT  
		Size: 25.1 MB (25081972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8a3b6acd22a7defdf373ba3b2e05bf8a38b2e3732aabb46180a0a05b108f8d`  
		Last Modified: Thu, 02 Oct 2025 06:16:39 GMT  
		Size: 130.6 MB (130628981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6b0e0362e81b56cafa76219b22fdbb886d4d0908cf24e166586cb562b753bc`  
		Last Modified: Thu, 02 Oct 2025 05:10:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:2.8.5-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:c138c44b65a118b01ee258c29145703f3decf41043fb34989c2b13038a533a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854f803eaa052fa98723697e94d05a86f38071b9ce2a5c329030e606383cca24`

```dockerfile
```

-	Layers:
	-	`sha256:462163e3abf6c01e1e3e343649e86497ea6889ac22f70500094140a49f7db693`  
		Last Modified: Thu, 02 Oct 2025 08:51:16 GMT  
		Size: 7.3 MB (7347718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e0fa93f559cb313a2c74c3422ffb11ba0ac17f56a1c702d804c825e91535cef`  
		Last Modified: Thu, 02 Oct 2025 08:51:17 GMT  
		Size: 14.5 KB (14486 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3`

```console
$ docker pull kong@sha256:196c6f3e21eee65fe3da143b346500eb1b6907fefa0765436d648df938435574
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3` - linux; amd64

```console
$ docker pull kong@sha256:5e17ae8909bed4f95a1eaf7182822a69672832db197595ed8daa42e171f1e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21043cc7bfb62f7f81970174a51dbf5825464690beea06d25c207bf89da0e0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7d307f3abc925483a65ef770cd272880e2fac6b35323aede27d0de2ce62e1`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fedccbb468196e14232c2f39d03cdfe8cbae74d85c538fc9891872fa8fce9f`  
		Last Modified: Thu, 09 Oct 2025 21:19:09 GMT  
		Size: 90.7 MB (90683560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022bc559edac70a31d4e5e5aaddc3aa4fe548a70f6ec082e8e6054d1ff529931`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:b7401b878d5632fea83751e47af112636a8b89dd5ea98b157296bc7f53810a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46547620b90b44204493120e82f506226045c40a04e98ea35be88ad63ed24663`

```dockerfile
```

-	Layers:
	-	`sha256:87b97efac41e7719b85ca5633595f0a195842a27e1a438d8acfd39553ef53103`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d09d6fc6c9f141d5b7c92662a4a3b970eeaa5081bc59b67ea10ffe2ebe47d`  
		Last Modified: Thu, 09 Oct 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a858aea36d8afe6c2942fe27a66bd6eb330593a256bf45b711f211725e3efae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419f568a65a7caee67f58d0af1e5398e6bd3361722c85209d12a20e261e77a4`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1ab19a979641e1e808a9dba5c0c068990f2a523a4a2e6ed046cdead66a1f3`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28e95f7059d80486f7319141729c2c3337392b401bda25f230e7989543dbc3`  
		Last Modified: Thu, 09 Oct 2025 21:20:40 GMT  
		Size: 90.0 MB (90002331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a38b6b99fad558995048694d3e51808a3d05c0b55643bd298b65fc9fd2004`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3` - unknown; unknown

```console
$ docker pull kong@sha256:771f9ee8c446d83fe5d225324b0f481ecff4fa9833ff664e49842a1ebb515731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627ff01600b96c4290d0b878a24185e5918b29bfbc13cb089fdd7087c8fbcc2`

```dockerfile
```

-	Layers:
	-	`sha256:d28acb78a58ef23da9eb7b999cb4e323d73642d962c85ecd0d4b935a67959a05`  
		Last Modified: Thu, 09 Oct 2025 23:51:50 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffb7998e5620230fd753960603a61368605eebadd9ebddf54c0e1eaf9f0c1cf`  
		Last Modified: Thu, 09 Oct 2025 23:51:51 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4`

```console
$ docker pull kong@sha256:16309f7355826116f2596512560401225e0006befa0ba986a88f665dff099d9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4` - linux; amd64

```console
$ docker pull kong@sha256:c25f6a1c07f9d2186889848da0467e13770b9d9d4e366b353a94a8ea356b31df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92281528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58915133f8a8fbe4effdd257817abdc656e37566f134e46f4a8fcf63ff33f7b`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997aa621eff05a6551bdfc57c3d996d1446906ce95cb3540646585a7e72847f6`  
		Last Modified: Thu, 02 Oct 2025 05:09:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd68cad16941c15651aa632e2b134c6053b395468f9161273c05a7d9ee280ee`  
		Last Modified: Thu, 02 Oct 2025 05:09:31 GMT  
		Size: 62.7 MB (62743429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa6e9f59bcda820f9f0f6f21926951d9da215769eba0a01b111fae0bc8fc25f`  
		Last Modified: Thu, 02 Oct 2025 05:09:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:fdbf9328bd450eabeb577be194e689c1561b2412cf88225034ad346eec2ed22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabc0abfbc212a30d572ef14cada5a181fed02941966414a4b45104e5c667111`

```dockerfile
```

-	Layers:
	-	`sha256:e852588406a25d7bb1da71b72bbcb2584c21c2b4a6328cc9ba64517124b6fcc4`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4211524832851b8d01e9d33e2d67d1921eedb2d594b74de947b896854957cb3`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3559030056713a6abeada341445c7c199caa7052bf65b9bc49ada1803b913d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88584268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ce4925c088aee491fd91540a540b5c30d9e6bade5b06dbb8ac3249962e0e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47434bf502c669d95107dc51c5c58d0f0f64ab263e9456c9a6fe5f2ab6f3b593`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72784660d74ec50ce0ce1416474fb1f51ee94bd9e297cef3179e252ba625aeb`  
		Last Modified: Thu, 02 Oct 2025 01:25:03 GMT  
		Size: 61.2 MB (61199879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86ca58e35b8411a2c9b00b6dc47832491f7d3a873d08e7fd8a240293552748`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4` - unknown; unknown

```console
$ docker pull kong@sha256:6ff25837c352f4acabefd68a435270685c3a597a7252e0df88444206c4071e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb497b36ae7f60ff96c58dda0229e90708c32d490b62791525177b51ed957cd`

```dockerfile
```

-	Layers:
	-	`sha256:1296d7d4ff88a0ef15e4a013c6d8ade66c8e2013b3d34fc27e5d5d1d2f1d8425`  
		Last Modified: Thu, 02 Oct 2025 02:51:27 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929a8f45e069d23a4b8e515dddfe3a1112519c598718920b00e188eac58dd1c`  
		Last Modified: Thu, 02 Oct 2025 02:51:28 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4-ubuntu`

```console
$ docker pull kong@sha256:16309f7355826116f2596512560401225e0006befa0ba986a88f665dff099d9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c25f6a1c07f9d2186889848da0467e13770b9d9d4e366b353a94a8ea356b31df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92281528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58915133f8a8fbe4effdd257817abdc656e37566f134e46f4a8fcf63ff33f7b`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997aa621eff05a6551bdfc57c3d996d1446906ce95cb3540646585a7e72847f6`  
		Last Modified: Thu, 02 Oct 2025 05:09:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd68cad16941c15651aa632e2b134c6053b395468f9161273c05a7d9ee280ee`  
		Last Modified: Thu, 02 Oct 2025 05:09:31 GMT  
		Size: 62.7 MB (62743429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa6e9f59bcda820f9f0f6f21926951d9da215769eba0a01b111fae0bc8fc25f`  
		Last Modified: Thu, 02 Oct 2025 05:09:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:fdbf9328bd450eabeb577be194e689c1561b2412cf88225034ad346eec2ed22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabc0abfbc212a30d572ef14cada5a181fed02941966414a4b45104e5c667111`

```dockerfile
```

-	Layers:
	-	`sha256:e852588406a25d7bb1da71b72bbcb2584c21c2b4a6328cc9ba64517124b6fcc4`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4211524832851b8d01e9d33e2d67d1921eedb2d594b74de947b896854957cb3`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3559030056713a6abeada341445c7c199caa7052bf65b9bc49ada1803b913d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88584268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ce4925c088aee491fd91540a540b5c30d9e6bade5b06dbb8ac3249962e0e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47434bf502c669d95107dc51c5c58d0f0f64ab263e9456c9a6fe5f2ab6f3b593`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72784660d74ec50ce0ce1416474fb1f51ee94bd9e297cef3179e252ba625aeb`  
		Last Modified: Thu, 02 Oct 2025 01:25:03 GMT  
		Size: 61.2 MB (61199879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86ca58e35b8411a2c9b00b6dc47832491f7d3a873d08e7fd8a240293552748`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:6ff25837c352f4acabefd68a435270685c3a597a7252e0df88444206c4071e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb497b36ae7f60ff96c58dda0229e90708c32d490b62791525177b51ed957cd`

```dockerfile
```

-	Layers:
	-	`sha256:1296d7d4ff88a0ef15e4a013c6d8ade66c8e2013b3d34fc27e5d5d1d2f1d8425`  
		Last Modified: Thu, 02 Oct 2025 02:51:27 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929a8f45e069d23a4b8e515dddfe3a1112519c598718920b00e188eac58dd1c`  
		Last Modified: Thu, 02 Oct 2025 02:51:28 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2`

```console
$ docker pull kong@sha256:16309f7355826116f2596512560401225e0006befa0ba986a88f665dff099d9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2` - linux; amd64

```console
$ docker pull kong@sha256:c25f6a1c07f9d2186889848da0467e13770b9d9d4e366b353a94a8ea356b31df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92281528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58915133f8a8fbe4effdd257817abdc656e37566f134e46f4a8fcf63ff33f7b`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997aa621eff05a6551bdfc57c3d996d1446906ce95cb3540646585a7e72847f6`  
		Last Modified: Thu, 02 Oct 2025 05:09:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd68cad16941c15651aa632e2b134c6053b395468f9161273c05a7d9ee280ee`  
		Last Modified: Thu, 02 Oct 2025 05:09:31 GMT  
		Size: 62.7 MB (62743429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa6e9f59bcda820f9f0f6f21926951d9da215769eba0a01b111fae0bc8fc25f`  
		Last Modified: Thu, 02 Oct 2025 05:09:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:fdbf9328bd450eabeb577be194e689c1561b2412cf88225034ad346eec2ed22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabc0abfbc212a30d572ef14cada5a181fed02941966414a4b45104e5c667111`

```dockerfile
```

-	Layers:
	-	`sha256:e852588406a25d7bb1da71b72bbcb2584c21c2b4a6328cc9ba64517124b6fcc4`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4211524832851b8d01e9d33e2d67d1921eedb2d594b74de947b896854957cb3`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3559030056713a6abeada341445c7c199caa7052bf65b9bc49ada1803b913d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88584268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ce4925c088aee491fd91540a540b5c30d9e6bade5b06dbb8ac3249962e0e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47434bf502c669d95107dc51c5c58d0f0f64ab263e9456c9a6fe5f2ab6f3b593`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72784660d74ec50ce0ce1416474fb1f51ee94bd9e297cef3179e252ba625aeb`  
		Last Modified: Thu, 02 Oct 2025 01:25:03 GMT  
		Size: 61.2 MB (61199879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86ca58e35b8411a2c9b00b6dc47832491f7d3a873d08e7fd8a240293552748`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2` - unknown; unknown

```console
$ docker pull kong@sha256:6ff25837c352f4acabefd68a435270685c3a597a7252e0df88444206c4071e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb497b36ae7f60ff96c58dda0229e90708c32d490b62791525177b51ed957cd`

```dockerfile
```

-	Layers:
	-	`sha256:1296d7d4ff88a0ef15e4a013c6d8ade66c8e2013b3d34fc27e5d5d1d2f1d8425`  
		Last Modified: Thu, 02 Oct 2025 02:51:27 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929a8f45e069d23a4b8e515dddfe3a1112519c598718920b00e188eac58dd1c`  
		Last Modified: Thu, 02 Oct 2025 02:51:28 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.4.2-ubuntu`

```console
$ docker pull kong@sha256:16309f7355826116f2596512560401225e0006befa0ba986a88f665dff099d9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.4.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c25f6a1c07f9d2186889848da0467e13770b9d9d4e366b353a94a8ea356b31df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92281528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58915133f8a8fbe4effdd257817abdc656e37566f134e46f4a8fcf63ff33f7b`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997aa621eff05a6551bdfc57c3d996d1446906ce95cb3540646585a7e72847f6`  
		Last Modified: Thu, 02 Oct 2025 05:09:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd68cad16941c15651aa632e2b134c6053b395468f9161273c05a7d9ee280ee`  
		Last Modified: Thu, 02 Oct 2025 05:09:31 GMT  
		Size: 62.7 MB (62743429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa6e9f59bcda820f9f0f6f21926951d9da215769eba0a01b111fae0bc8fc25f`  
		Last Modified: Thu, 02 Oct 2025 05:09:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:fdbf9328bd450eabeb577be194e689c1561b2412cf88225034ad346eec2ed22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6078296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabc0abfbc212a30d572ef14cada5a181fed02941966414a4b45104e5c667111`

```dockerfile
```

-	Layers:
	-	`sha256:e852588406a25d7bb1da71b72bbcb2584c21c2b4a6328cc9ba64517124b6fcc4`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 6.1 MB (6062907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4211524832851b8d01e9d33e2d67d1921eedb2d594b74de947b896854957cb3`  
		Last Modified: Thu, 02 Oct 2025 08:51:28 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.4.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:3559030056713a6abeada341445c7c199caa7052bf65b9bc49ada1803b913d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88584268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3ce4925c088aee491fd91540a540b5c30d9e6bade5b06dbb8ac3249962e0e7`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47434bf502c669d95107dc51c5c58d0f0f64ab263e9456c9a6fe5f2ab6f3b593`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72784660d74ec50ce0ce1416474fb1f51ee94bd9e297cef3179e252ba625aeb`  
		Last Modified: Thu, 02 Oct 2025 01:25:03 GMT  
		Size: 61.2 MB (61199879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a86ca58e35b8411a2c9b00b6dc47832491f7d3a873d08e7fd8a240293552748`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.4.2-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:6ff25837c352f4acabefd68a435270685c3a597a7252e0df88444206c4071e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6056477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb497b36ae7f60ff96c58dda0229e90708c32d490b62791525177b51ed957cd`

```dockerfile
```

-	Layers:
	-	`sha256:1296d7d4ff88a0ef15e4a013c6d8ade66c8e2013b3d34fc27e5d5d1d2f1d8425`  
		Last Modified: Thu, 02 Oct 2025 02:51:27 GMT  
		Size: 6.0 MB (6040986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a929a8f45e069d23a4b8e515dddfe3a1112519c598718920b00e188eac58dd1c`  
		Last Modified: Thu, 02 Oct 2025 02:51:28 GMT  
		Size: 15.5 KB (15491 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8`

```console
$ docker pull kong@sha256:28c4ac43a7ede00b4d95f1409f0ec7eb348b9033006a3a8634333a067bd70166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8` - linux; amd64

```console
$ docker pull kong@sha256:34cc9d3942760044fe15d226a64873141a2ca288601eabe056a1315272566365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9958b1a1a0ac3f46d218cd0906631689bb3f97117717677cc53d6c52d9c0d9b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7db39ec03cc8e9875f6be4c89aec5f9d2223d31fc91395e0373ec60a127b67`  
		Last Modified: Thu, 02 Oct 2025 05:09:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b945128b0301155928bd84f0d8ebc0e9744377ebb63f7066a0a4f69c9305c`  
		Last Modified: Thu, 02 Oct 2025 05:10:10 GMT  
		Size: 88.0 MB (88009768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4082438c142661fc0c2fed1f037624811939195ccce4045dd621ad762ce8648f`  
		Last Modified: Thu, 02 Oct 2025 05:09:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:75f54ae98a702eee87112579c54a7ce7f6a78eb7d79a19f0e2b6536638647d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcc91d9766928dfa68c9777de719da3ae6ca9ccdd19e9fc5aaa07e26a0cba3f`

```dockerfile
```

-	Layers:
	-	`sha256:d4c4cb03c3da42baadb7d9731f0e28d943cf79cd7e07d1a72491cf4b0463292e`  
		Last Modified: Thu, 02 Oct 2025 08:51:40 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1adb4f248210be5d08cfc025ef95193c4595dceffce26183b57ddbf8ee5d8497`  
		Last Modified: Thu, 02 Oct 2025 08:51:42 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:00bcb1d6d2387431b80bc9ba15750b62a9c71dcfb4c366d9ebd1f15a1241fb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377e4a788ccecb7ffce6de75d6515dae4882073788e3e4d6708014c8af3b17f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949273f4e970672a127ace61c92f81f44dbffdf72658e45fc61f400f7faf13ed`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b4c898a3fe17a62b9b6b98c16d71d79afc21b938a4542c199ee07831a2e72`  
		Last Modified: Thu, 02 Oct 2025 03:00:19 GMT  
		Size: 87.3 MB (87288753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43350dce70d6057816696573088ffbbf7ad09dad213b371045e682e018aecdc7`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8` - unknown; unknown

```console
$ docker pull kong@sha256:9637d8a6e47598df42c530d9291cdd295e00ad01db774cf9d0329f64d43e8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d3442492c15262e8c4b84bd8c5cd55e98a611e2122cb56bcf5fca115b22de`

```dockerfile
```

-	Layers:
	-	`sha256:cce72a388571b32b0aa26b8069576ecbc150345bd022f9b785166139ef67b445`  
		Last Modified: Thu, 02 Oct 2025 02:51:41 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79166d0edf21eb7ab069f03a3db3b98582e00959a53b1c880a367ca14c63db03`  
		Last Modified: Thu, 02 Oct 2025 02:51:42 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8-ubuntu`

```console
$ docker pull kong@sha256:28c4ac43a7ede00b4d95f1409f0ec7eb348b9033006a3a8634333a067bd70166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:34cc9d3942760044fe15d226a64873141a2ca288601eabe056a1315272566365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9958b1a1a0ac3f46d218cd0906631689bb3f97117717677cc53d6c52d9c0d9b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7db39ec03cc8e9875f6be4c89aec5f9d2223d31fc91395e0373ec60a127b67`  
		Last Modified: Thu, 02 Oct 2025 05:09:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b945128b0301155928bd84f0d8ebc0e9744377ebb63f7066a0a4f69c9305c`  
		Last Modified: Thu, 02 Oct 2025 05:10:10 GMT  
		Size: 88.0 MB (88009768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4082438c142661fc0c2fed1f037624811939195ccce4045dd621ad762ce8648f`  
		Last Modified: Thu, 02 Oct 2025 05:09:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:75f54ae98a702eee87112579c54a7ce7f6a78eb7d79a19f0e2b6536638647d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcc91d9766928dfa68c9777de719da3ae6ca9ccdd19e9fc5aaa07e26a0cba3f`

```dockerfile
```

-	Layers:
	-	`sha256:d4c4cb03c3da42baadb7d9731f0e28d943cf79cd7e07d1a72491cf4b0463292e`  
		Last Modified: Thu, 02 Oct 2025 08:51:40 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1adb4f248210be5d08cfc025ef95193c4595dceffce26183b57ddbf8ee5d8497`  
		Last Modified: Thu, 02 Oct 2025 08:51:42 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:00bcb1d6d2387431b80bc9ba15750b62a9c71dcfb4c366d9ebd1f15a1241fb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377e4a788ccecb7ffce6de75d6515dae4882073788e3e4d6708014c8af3b17f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949273f4e970672a127ace61c92f81f44dbffdf72658e45fc61f400f7faf13ed`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b4c898a3fe17a62b9b6b98c16d71d79afc21b938a4542c199ee07831a2e72`  
		Last Modified: Thu, 02 Oct 2025 03:00:19 GMT  
		Size: 87.3 MB (87288753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43350dce70d6057816696573088ffbbf7ad09dad213b371045e682e018aecdc7`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9637d8a6e47598df42c530d9291cdd295e00ad01db774cf9d0329f64d43e8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d3442492c15262e8c4b84bd8c5cd55e98a611e2122cb56bcf5fca115b22de`

```dockerfile
```

-	Layers:
	-	`sha256:cce72a388571b32b0aa26b8069576ecbc150345bd022f9b785166139ef67b445`  
		Last Modified: Thu, 02 Oct 2025 02:51:41 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79166d0edf21eb7ab069f03a3db3b98582e00959a53b1c880a367ca14c63db03`  
		Last Modified: Thu, 02 Oct 2025 02:51:42 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0`

```console
$ docker pull kong@sha256:28c4ac43a7ede00b4d95f1409f0ec7eb348b9033006a3a8634333a067bd70166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0` - linux; amd64

```console
$ docker pull kong@sha256:34cc9d3942760044fe15d226a64873141a2ca288601eabe056a1315272566365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9958b1a1a0ac3f46d218cd0906631689bb3f97117717677cc53d6c52d9c0d9b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7db39ec03cc8e9875f6be4c89aec5f9d2223d31fc91395e0373ec60a127b67`  
		Last Modified: Thu, 02 Oct 2025 05:09:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b945128b0301155928bd84f0d8ebc0e9744377ebb63f7066a0a4f69c9305c`  
		Last Modified: Thu, 02 Oct 2025 05:10:10 GMT  
		Size: 88.0 MB (88009768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4082438c142661fc0c2fed1f037624811939195ccce4045dd621ad762ce8648f`  
		Last Modified: Thu, 02 Oct 2025 05:09:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:75f54ae98a702eee87112579c54a7ce7f6a78eb7d79a19f0e2b6536638647d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcc91d9766928dfa68c9777de719da3ae6ca9ccdd19e9fc5aaa07e26a0cba3f`

```dockerfile
```

-	Layers:
	-	`sha256:d4c4cb03c3da42baadb7d9731f0e28d943cf79cd7e07d1a72491cf4b0463292e`  
		Last Modified: Thu, 02 Oct 2025 08:51:40 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1adb4f248210be5d08cfc025ef95193c4595dceffce26183b57ddbf8ee5d8497`  
		Last Modified: Thu, 02 Oct 2025 08:51:42 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:00bcb1d6d2387431b80bc9ba15750b62a9c71dcfb4c366d9ebd1f15a1241fb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377e4a788ccecb7ffce6de75d6515dae4882073788e3e4d6708014c8af3b17f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949273f4e970672a127ace61c92f81f44dbffdf72658e45fc61f400f7faf13ed`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b4c898a3fe17a62b9b6b98c16d71d79afc21b938a4542c199ee07831a2e72`  
		Last Modified: Thu, 02 Oct 2025 03:00:19 GMT  
		Size: 87.3 MB (87288753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43350dce70d6057816696573088ffbbf7ad09dad213b371045e682e018aecdc7`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0` - unknown; unknown

```console
$ docker pull kong@sha256:9637d8a6e47598df42c530d9291cdd295e00ad01db774cf9d0329f64d43e8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d3442492c15262e8c4b84bd8c5cd55e98a611e2122cb56bcf5fca115b22de`

```dockerfile
```

-	Layers:
	-	`sha256:cce72a388571b32b0aa26b8069576ecbc150345bd022f9b785166139ef67b445`  
		Last Modified: Thu, 02 Oct 2025 02:51:41 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79166d0edf21eb7ab069f03a3db3b98582e00959a53b1c880a367ca14c63db03`  
		Last Modified: Thu, 02 Oct 2025 02:51:42 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.8.0-ubuntu`

```console
$ docker pull kong@sha256:28c4ac43a7ede00b4d95f1409f0ec7eb348b9033006a3a8634333a067bd70166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:34cc9d3942760044fe15d226a64873141a2ca288601eabe056a1315272566365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117547867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9958b1a1a0ac3f46d218cd0906631689bb3f97117717677cc53d6c52d9c0d9b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7db39ec03cc8e9875f6be4c89aec5f9d2223d31fc91395e0373ec60a127b67`  
		Last Modified: Thu, 02 Oct 2025 05:09:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b945128b0301155928bd84f0d8ebc0e9744377ebb63f7066a0a4f69c9305c`  
		Last Modified: Thu, 02 Oct 2025 05:10:10 GMT  
		Size: 88.0 MB (88009768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4082438c142661fc0c2fed1f037624811939195ccce4045dd621ad762ce8648f`  
		Last Modified: Thu, 02 Oct 2025 05:09:59 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:75f54ae98a702eee87112579c54a7ce7f6a78eb7d79a19f0e2b6536638647d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5378093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcc91d9766928dfa68c9777de719da3ae6ca9ccdd19e9fc5aaa07e26a0cba3f`

```dockerfile
```

-	Layers:
	-	`sha256:d4c4cb03c3da42baadb7d9731f0e28d943cf79cd7e07d1a72491cf4b0463292e`  
		Last Modified: Thu, 02 Oct 2025 08:51:40 GMT  
		Size: 5.4 MB (5362704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1adb4f248210be5d08cfc025ef95193c4595dceffce26183b57ddbf8ee5d8497`  
		Last Modified: Thu, 02 Oct 2025 08:51:42 GMT  
		Size: 15.4 KB (15389 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.8.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:00bcb1d6d2387431b80bc9ba15750b62a9c71dcfb4c366d9ebd1f15a1241fb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114673142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e377e4a788ccecb7ffce6de75d6515dae4882073788e3e4d6708014c8af3b17f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 12 Sep 2024 15:56:21 GMT
ARG RELEASE
# Thu, 12 Sep 2024 15:56:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 12 Sep 2024 15:56:21 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["/bin/bash"]
# Thu, 12 Sep 2024 15:56:21 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 12 Sep 2024 15:56:21 GMT
ARG ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ENV ASSET=ce
# Thu, 12 Sep 2024 15:56:21 GMT
ARG EE_PORTS
# Thu, 12 Sep 2024 15:56:21 GMT
COPY kong.deb /tmp/kong.deb # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ENV KONG_VERSION=3.8.0
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987
# Thu, 12 Sep 2024 15:56:21 GMT
ARG KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
# Thu, 12 Sep 2024 15:56:21 GMT
# ARGS: ASSET=ce EE_PORTS= KONG_VERSION=3.8.0 KONG_AMD64_SHA=d7f3bb1b34128ebefc7c1dadf552b88903631d33e479715545c1e1b8f9468987 KONG_ARM64_SHA=21a35f15c1ee96996da8739c9bcc937e164b5a075db64c0a7e17b5443af458bf
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y --no-install-recommends curl ca-certificates       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && KONG_REPO=$(echo ${KONG_VERSION%.*} | sed 's/\.//')       && curl -fL https://packages.konghq.com/public/gateway-$KONG_REPO/deb/ubuntu/pool/$UBUNTU_CODENAME/main/k/ko/kong_$KONG_VERSION/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes --no-install-recommends /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Sep 2024 15:56:21 GMT
USER kong
# Thu, 12 Sep 2024 15:56:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Sep 2024 15:56:21 GMT
EXPOSE map[8000/tcp:{} 8001/tcp:{} 8443/tcp:{} 8444/tcp:{}]
# Thu, 12 Sep 2024 15:56:21 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 15:56:21 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" "0s" '\n'}
# Thu, 12 Sep 2024 15:56:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949273f4e970672a127ace61c92f81f44dbffdf72658e45fc61f400f7faf13ed`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980b4c898a3fe17a62b9b6b98c16d71d79afc21b938a4542c199ee07831a2e72`  
		Last Modified: Thu, 02 Oct 2025 03:00:19 GMT  
		Size: 87.3 MB (87288753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43350dce70d6057816696573088ffbbf7ad09dad213b371045e682e018aecdc7`  
		Last Modified: Thu, 02 Oct 2025 01:24:59 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.8.0-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:9637d8a6e47598df42c530d9291cdd295e00ad01db774cf9d0329f64d43e8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05d3442492c15262e8c4b84bd8c5cd55e98a611e2122cb56bcf5fca115b22de`

```dockerfile
```

-	Layers:
	-	`sha256:cce72a388571b32b0aa26b8069576ecbc150345bd022f9b785166139ef67b445`  
		Last Modified: Thu, 02 Oct 2025 02:51:41 GMT  
		Size: 5.4 MB (5369030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79166d0edf21eb7ab069f03a3db3b98582e00959a53b1c880a367ca14c63db03`  
		Last Modified: Thu, 02 Oct 2025 02:51:42 GMT  
		Size: 15.5 KB (15493 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9`

```console
$ docker pull kong@sha256:196c6f3e21eee65fe3da143b346500eb1b6907fefa0765436d648df938435574
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9` - linux; amd64

```console
$ docker pull kong@sha256:5e17ae8909bed4f95a1eaf7182822a69672832db197595ed8daa42e171f1e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21043cc7bfb62f7f81970174a51dbf5825464690beea06d25c207bf89da0e0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7d307f3abc925483a65ef770cd272880e2fac6b35323aede27d0de2ce62e1`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fedccbb468196e14232c2f39d03cdfe8cbae74d85c538fc9891872fa8fce9f`  
		Last Modified: Thu, 09 Oct 2025 21:19:09 GMT  
		Size: 90.7 MB (90683560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022bc559edac70a31d4e5e5aaddc3aa4fe548a70f6ec082e8e6054d1ff529931`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:b7401b878d5632fea83751e47af112636a8b89dd5ea98b157296bc7f53810a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46547620b90b44204493120e82f506226045c40a04e98ea35be88ad63ed24663`

```dockerfile
```

-	Layers:
	-	`sha256:87b97efac41e7719b85ca5633595f0a195842a27e1a438d8acfd39553ef53103`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d09d6fc6c9f141d5b7c92662a4a3b970eeaa5081bc59b67ea10ffe2ebe47d`  
		Last Modified: Thu, 09 Oct 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a858aea36d8afe6c2942fe27a66bd6eb330593a256bf45b711f211725e3efae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419f568a65a7caee67f58d0af1e5398e6bd3361722c85209d12a20e261e77a4`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1ab19a979641e1e808a9dba5c0c068990f2a523a4a2e6ed046cdead66a1f3`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28e95f7059d80486f7319141729c2c3337392b401bda25f230e7989543dbc3`  
		Last Modified: Thu, 09 Oct 2025 21:20:40 GMT  
		Size: 90.0 MB (90002331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a38b6b99fad558995048694d3e51808a3d05c0b55643bd298b65fc9fd2004`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9` - unknown; unknown

```console
$ docker pull kong@sha256:771f9ee8c446d83fe5d225324b0f481ecff4fa9833ff664e49842a1ebb515731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627ff01600b96c4290d0b878a24185e5918b29bfbc13cb089fdd7087c8fbcc2`

```dockerfile
```

-	Layers:
	-	`sha256:d28acb78a58ef23da9eb7b999cb4e323d73642d962c85ecd0d4b935a67959a05`  
		Last Modified: Thu, 09 Oct 2025 23:51:50 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffb7998e5620230fd753960603a61368605eebadd9ebddf54c0e1eaf9f0c1cf`  
		Last Modified: Thu, 09 Oct 2025 23:51:51 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9-ubuntu`

```console
$ docker pull kong@sha256:196c6f3e21eee65fe3da143b346500eb1b6907fefa0765436d648df938435574
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5e17ae8909bed4f95a1eaf7182822a69672832db197595ed8daa42e171f1e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21043cc7bfb62f7f81970174a51dbf5825464690beea06d25c207bf89da0e0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7d307f3abc925483a65ef770cd272880e2fac6b35323aede27d0de2ce62e1`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fedccbb468196e14232c2f39d03cdfe8cbae74d85c538fc9891872fa8fce9f`  
		Last Modified: Thu, 09 Oct 2025 21:19:09 GMT  
		Size: 90.7 MB (90683560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022bc559edac70a31d4e5e5aaddc3aa4fe548a70f6ec082e8e6054d1ff529931`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:b7401b878d5632fea83751e47af112636a8b89dd5ea98b157296bc7f53810a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46547620b90b44204493120e82f506226045c40a04e98ea35be88ad63ed24663`

```dockerfile
```

-	Layers:
	-	`sha256:87b97efac41e7719b85ca5633595f0a195842a27e1a438d8acfd39553ef53103`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d09d6fc6c9f141d5b7c92662a4a3b970eeaa5081bc59b67ea10ffe2ebe47d`  
		Last Modified: Thu, 09 Oct 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a858aea36d8afe6c2942fe27a66bd6eb330593a256bf45b711f211725e3efae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419f568a65a7caee67f58d0af1e5398e6bd3361722c85209d12a20e261e77a4`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1ab19a979641e1e808a9dba5c0c068990f2a523a4a2e6ed046cdead66a1f3`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28e95f7059d80486f7319141729c2c3337392b401bda25f230e7989543dbc3`  
		Last Modified: Thu, 09 Oct 2025 21:20:40 GMT  
		Size: 90.0 MB (90002331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a38b6b99fad558995048694d3e51808a3d05c0b55643bd298b65fc9fd2004`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:771f9ee8c446d83fe5d225324b0f481ecff4fa9833ff664e49842a1ebb515731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627ff01600b96c4290d0b878a24185e5918b29bfbc13cb089fdd7087c8fbcc2`

```dockerfile
```

-	Layers:
	-	`sha256:d28acb78a58ef23da9eb7b999cb4e323d73642d962c85ecd0d4b935a67959a05`  
		Last Modified: Thu, 09 Oct 2025 23:51:50 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffb7998e5620230fd753960603a61368605eebadd9ebddf54c0e1eaf9f0c1cf`  
		Last Modified: Thu, 09 Oct 2025 23:51:51 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1`

```console
$ docker pull kong@sha256:196c6f3e21eee65fe3da143b346500eb1b6907fefa0765436d648df938435574
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1` - linux; amd64

```console
$ docker pull kong@sha256:5e17ae8909bed4f95a1eaf7182822a69672832db197595ed8daa42e171f1e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21043cc7bfb62f7f81970174a51dbf5825464690beea06d25c207bf89da0e0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7d307f3abc925483a65ef770cd272880e2fac6b35323aede27d0de2ce62e1`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fedccbb468196e14232c2f39d03cdfe8cbae74d85c538fc9891872fa8fce9f`  
		Last Modified: Thu, 09 Oct 2025 21:19:09 GMT  
		Size: 90.7 MB (90683560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022bc559edac70a31d4e5e5aaddc3aa4fe548a70f6ec082e8e6054d1ff529931`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:b7401b878d5632fea83751e47af112636a8b89dd5ea98b157296bc7f53810a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46547620b90b44204493120e82f506226045c40a04e98ea35be88ad63ed24663`

```dockerfile
```

-	Layers:
	-	`sha256:87b97efac41e7719b85ca5633595f0a195842a27e1a438d8acfd39553ef53103`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d09d6fc6c9f141d5b7c92662a4a3b970eeaa5081bc59b67ea10ffe2ebe47d`  
		Last Modified: Thu, 09 Oct 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a858aea36d8afe6c2942fe27a66bd6eb330593a256bf45b711f211725e3efae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419f568a65a7caee67f58d0af1e5398e6bd3361722c85209d12a20e261e77a4`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1ab19a979641e1e808a9dba5c0c068990f2a523a4a2e6ed046cdead66a1f3`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28e95f7059d80486f7319141729c2c3337392b401bda25f230e7989543dbc3`  
		Last Modified: Thu, 09 Oct 2025 21:20:40 GMT  
		Size: 90.0 MB (90002331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a38b6b99fad558995048694d3e51808a3d05c0b55643bd298b65fc9fd2004`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1` - unknown; unknown

```console
$ docker pull kong@sha256:771f9ee8c446d83fe5d225324b0f481ecff4fa9833ff664e49842a1ebb515731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627ff01600b96c4290d0b878a24185e5918b29bfbc13cb089fdd7087c8fbcc2`

```dockerfile
```

-	Layers:
	-	`sha256:d28acb78a58ef23da9eb7b999cb4e323d73642d962c85ecd0d4b935a67959a05`  
		Last Modified: Thu, 09 Oct 2025 23:51:50 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffb7998e5620230fd753960603a61368605eebadd9ebddf54c0e1eaf9f0c1cf`  
		Last Modified: Thu, 09 Oct 2025 23:51:51 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:3.9.1-ubuntu`

```console
$ docker pull kong@sha256:196c6f3e21eee65fe3da143b346500eb1b6907fefa0765436d648df938435574
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:3.9.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5e17ae8909bed4f95a1eaf7182822a69672832db197595ed8daa42e171f1e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21043cc7bfb62f7f81970174a51dbf5825464690beea06d25c207bf89da0e0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7d307f3abc925483a65ef770cd272880e2fac6b35323aede27d0de2ce62e1`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fedccbb468196e14232c2f39d03cdfe8cbae74d85c538fc9891872fa8fce9f`  
		Last Modified: Thu, 09 Oct 2025 21:19:09 GMT  
		Size: 90.7 MB (90683560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022bc559edac70a31d4e5e5aaddc3aa4fe548a70f6ec082e8e6054d1ff529931`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:b7401b878d5632fea83751e47af112636a8b89dd5ea98b157296bc7f53810a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46547620b90b44204493120e82f506226045c40a04e98ea35be88ad63ed24663`

```dockerfile
```

-	Layers:
	-	`sha256:87b97efac41e7719b85ca5633595f0a195842a27e1a438d8acfd39553ef53103`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d09d6fc6c9f141d5b7c92662a4a3b970eeaa5081bc59b67ea10ffe2ebe47d`  
		Last Modified: Thu, 09 Oct 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:3.9.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a858aea36d8afe6c2942fe27a66bd6eb330593a256bf45b711f211725e3efae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419f568a65a7caee67f58d0af1e5398e6bd3361722c85209d12a20e261e77a4`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1ab19a979641e1e808a9dba5c0c068990f2a523a4a2e6ed046cdead66a1f3`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28e95f7059d80486f7319141729c2c3337392b401bda25f230e7989543dbc3`  
		Last Modified: Thu, 09 Oct 2025 21:20:40 GMT  
		Size: 90.0 MB (90002331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a38b6b99fad558995048694d3e51808a3d05c0b55643bd298b65fc9fd2004`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:3.9.1-ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:771f9ee8c446d83fe5d225324b0f481ecff4fa9833ff664e49842a1ebb515731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627ff01600b96c4290d0b878a24185e5918b29bfbc13cb089fdd7087c8fbcc2`

```dockerfile
```

-	Layers:
	-	`sha256:d28acb78a58ef23da9eb7b999cb4e323d73642d962c85ecd0d4b935a67959a05`  
		Last Modified: Thu, 09 Oct 2025 23:51:50 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffb7998e5620230fd753960603a61368605eebadd9ebddf54c0e1eaf9f0c1cf`  
		Last Modified: Thu, 09 Oct 2025 23:51:51 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:latest`

```console
$ docker pull kong@sha256:196c6f3e21eee65fe3da143b346500eb1b6907fefa0765436d648df938435574
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:5e17ae8909bed4f95a1eaf7182822a69672832db197595ed8daa42e171f1e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21043cc7bfb62f7f81970174a51dbf5825464690beea06d25c207bf89da0e0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7d307f3abc925483a65ef770cd272880e2fac6b35323aede27d0de2ce62e1`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fedccbb468196e14232c2f39d03cdfe8cbae74d85c538fc9891872fa8fce9f`  
		Last Modified: Thu, 09 Oct 2025 21:19:09 GMT  
		Size: 90.7 MB (90683560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022bc559edac70a31d4e5e5aaddc3aa4fe548a70f6ec082e8e6054d1ff529931`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:b7401b878d5632fea83751e47af112636a8b89dd5ea98b157296bc7f53810a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46547620b90b44204493120e82f506226045c40a04e98ea35be88ad63ed24663`

```dockerfile
```

-	Layers:
	-	`sha256:87b97efac41e7719b85ca5633595f0a195842a27e1a438d8acfd39553ef53103`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d09d6fc6c9f141d5b7c92662a4a3b970eeaa5081bc59b67ea10ffe2ebe47d`  
		Last Modified: Thu, 09 Oct 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a858aea36d8afe6c2942fe27a66bd6eb330593a256bf45b711f211725e3efae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419f568a65a7caee67f58d0af1e5398e6bd3361722c85209d12a20e261e77a4`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1ab19a979641e1e808a9dba5c0c068990f2a523a4a2e6ed046cdead66a1f3`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28e95f7059d80486f7319141729c2c3337392b401bda25f230e7989543dbc3`  
		Last Modified: Thu, 09 Oct 2025 21:20:40 GMT  
		Size: 90.0 MB (90002331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a38b6b99fad558995048694d3e51808a3d05c0b55643bd298b65fc9fd2004`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:latest` - unknown; unknown

```console
$ docker pull kong@sha256:771f9ee8c446d83fe5d225324b0f481ecff4fa9833ff664e49842a1ebb515731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627ff01600b96c4290d0b878a24185e5918b29bfbc13cb089fdd7087c8fbcc2`

```dockerfile
```

-	Layers:
	-	`sha256:d28acb78a58ef23da9eb7b999cb4e323d73642d962c85ecd0d4b935a67959a05`  
		Last Modified: Thu, 09 Oct 2025 23:51:50 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffb7998e5620230fd753960603a61368605eebadd9ebddf54c0e1eaf9f0c1cf`  
		Last Modified: Thu, 09 Oct 2025 23:51:51 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

## `kong:ubuntu`

```console
$ docker pull kong@sha256:196c6f3e21eee65fe3da143b346500eb1b6907fefa0765436d648df938435574
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5e17ae8909bed4f95a1eaf7182822a69672832db197595ed8daa42e171f1e914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120407993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21043cc7bfb62f7f81970174a51dbf5825464690beea06d25c207bf89da0e0`
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
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
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
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf7d307f3abc925483a65ef770cd272880e2fac6b35323aede27d0de2ce62e1`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fedccbb468196e14232c2f39d03cdfe8cbae74d85c538fc9891872fa8fce9f`  
		Last Modified: Thu, 09 Oct 2025 21:19:09 GMT  
		Size: 90.7 MB (90683560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022bc559edac70a31d4e5e5aaddc3aa4fe548a70f6ec082e8e6054d1ff529931`  
		Last Modified: Thu, 09 Oct 2025 21:19:01 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:b7401b878d5632fea83751e47af112636a8b89dd5ea98b157296bc7f53810a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46547620b90b44204493120e82f506226045c40a04e98ea35be88ad63ed24663`

```dockerfile
```

-	Layers:
	-	`sha256:87b97efac41e7719b85ca5633595f0a195842a27e1a438d8acfd39553ef53103`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 5.4 MB (5421134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d09d6fc6c9f141d5b7c92662a4a3b970eeaa5081bc59b67ea10ffe2ebe47d`  
		Last Modified: Thu, 09 Oct 2025 23:51:23 GMT  
		Size: 16.3 KB (16261 bytes)  
		MIME: application/vnd.in-toto+json

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a858aea36d8afe6c2942fe27a66bd6eb330593a256bf45b711f211725e3efae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118865330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7419f568a65a7caee67f58d0af1e5398e6bd3361722c85209d12a20e261e77a4`
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
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
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
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e1ab19a979641e1e808a9dba5c0c068990f2a523a4a2e6ed046cdead66a1f3`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef28e95f7059d80486f7319141729c2c3337392b401bda25f230e7989543dbc3`  
		Last Modified: Thu, 09 Oct 2025 21:20:40 GMT  
		Size: 90.0 MB (90002331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a38b6b99fad558995048694d3e51808a3d05c0b55643bd298b65fc9fd2004`  
		Last Modified: Thu, 09 Oct 2025 21:20:28 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kong:ubuntu` - unknown; unknown

```console
$ docker pull kong@sha256:771f9ee8c446d83fe5d225324b0f481ecff4fa9833ff664e49842a1ebb515731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b627ff01600b96c4290d0b878a24185e5918b29bfbc13cb089fdd7087c8fbcc2`

```dockerfile
```

-	Layers:
	-	`sha256:d28acb78a58ef23da9eb7b999cb4e323d73642d962c85ecd0d4b935a67959a05`  
		Last Modified: Thu, 09 Oct 2025 23:51:50 GMT  
		Size: 5.4 MB (5428301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffb7998e5620230fd753960603a61368605eebadd9ebddf54c0e1eaf9f0c1cf`  
		Last Modified: Thu, 09 Oct 2025 23:51:51 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json
