## `kong:latest`

```console
$ docker pull kong@sha256:829e1707149664d550c75551d357c7508e40a51af636f30a3613708cc5b4175b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:bf97c2dff2c1b26e40f9635a508b24a65a72985ff97af8b737ce045b4e3e15e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97790928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af41bd1970c551ebdff2aa1d21f9ec5bcae595cae26f673d22a5ec791f85b46`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:22:10 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 04 Jul 2023 18:22:10 GMT
ARG ASSET=ce
# Tue, 04 Jul 2023 18:22:10 GMT
ENV ASSET=ce
# Tue, 04 Jul 2023 18:22:10 GMT
ARG EE_PORTS
# Tue, 04 Jul 2023 18:22:11 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 11 Aug 2023 18:21:02 GMT
ARG KONG_VERSION=3.4.0
# Fri, 11 Aug 2023 18:21:02 GMT
ENV KONG_VERSION=3.4.0
# Fri, 11 Aug 2023 18:21:02 GMT
ARG KONG_AMD64_SHA=9a4203174a29895d5dd71092a05b15b26ee9644e068d14d970aed28461d358fa
# Fri, 11 Aug 2023 18:21:02 GMT
ARG KONG_ARM64_SHA=b64e19216ce125039a6a832dc93bf277e05f233a91f1647b351cad3f166edd81
# Fri, 11 Aug 2023 18:21:50 GMT
# ARGS: KONG_AMD64_SHA=9a4203174a29895d5dd71092a05b15b26ee9644e068d14d970aed28461d358fa KONG_ARM64_SHA=b64e19216ce125039a6a832dc93bf277e05f233a91f1647b351cad3f166edd81
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 11 Aug 2023 18:21:51 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 18:21:51 GMT
USER kong
# Fri, 11 Aug 2023 18:21:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 18:21:51 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 11 Aug 2023 18:21:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Aug 2023 18:21:51 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 11 Aug 2023 18:21:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95d715c451393bf53843bdb2d56f67f9228685e8a5467f1581eb7dbd1555e40`  
		Last Modified: Tue, 04 Jul 2023 18:25:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6b13e1b3b4d753a91a8a8dda1d6c352921eb4d6b7e466da53c9b63b65ef22`  
		Last Modified: Fri, 11 Aug 2023 18:22:53 GMT  
		Size: 67.4 MB (67358416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4458b6e54e52bfd922d8f6296516625ffd113d871f66aa5ff4e718f7a2c4a4a`  
		Last Modified: Fri, 11 Aug 2023 18:22:43 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2a04cc80d477942ba31fd6ffe0e946af936c851e34e1ca6b3e1de49bbe8e2675
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94149312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50474e375237b4bfee56a014cf61873f8a4b070fd82081b9e2536023557ebfec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:56:30 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Tue, 04 Jul 2023 15:56:30 GMT
ARG ASSET=ce
# Tue, 04 Jul 2023 15:56:30 GMT
ENV ASSET=ce
# Tue, 04 Jul 2023 15:56:31 GMT
ARG EE_PORTS
# Tue, 04 Jul 2023 15:56:31 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Fri, 11 Aug 2023 17:40:37 GMT
ARG KONG_VERSION=3.4.0
# Fri, 11 Aug 2023 17:40:37 GMT
ENV KONG_VERSION=3.4.0
# Fri, 11 Aug 2023 17:40:37 GMT
ARG KONG_AMD64_SHA=9a4203174a29895d5dd71092a05b15b26ee9644e068d14d970aed28461d358fa
# Fri, 11 Aug 2023 17:40:37 GMT
ARG KONG_ARM64_SHA=b64e19216ce125039a6a832dc93bf277e05f233a91f1647b351cad3f166edd81
# Fri, 11 Aug 2023 17:41:32 GMT
# ARGS: KONG_AMD64_SHA=9a4203174a29895d5dd71092a05b15b26ee9644e068d14d970aed28461d358fa KONG_ARM64_SHA=b64e19216ce125039a6a832dc93bf277e05f233a91f1647b351cad3f166edd81
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -sf /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -sf /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -sf /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Fri, 11 Aug 2023 17:41:33 GMT
COPY file:6bb80898c17e8239746044c0d891f54029077cb7b848c170e71b40f6e2243e33 in /docker-entrypoint.sh 
# Fri, 11 Aug 2023 17:41:33 GMT
USER kong
# Fri, 11 Aug 2023 17:41:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Aug 2023 17:41:34 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 11 Aug 2023 17:41:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Aug 2023 17:41:34 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Fri, 11 Aug 2023 17:41:34 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323749330ae28b00c28d5d9426a6340ac8c0950f884d5f86035845592177af50`  
		Last Modified: Tue, 04 Jul 2023 15:58:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f4fe723bb1123f4c74ce9ed7badfe06bc92ac0e73f4b2bc187084857d7245d`  
		Last Modified: Fri, 11 Aug 2023 17:42:23 GMT  
		Size: 65.8 MB (65757015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fad754d25dbaac9e870d6ca8a001c563311668540d8f256d44cd7b0c49c68e`  
		Last Modified: Fri, 11 Aug 2023 17:42:15 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
