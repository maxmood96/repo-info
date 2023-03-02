## `kong:ubuntu`

```console
$ docker pull kong@sha256:5862338fb8f8e10cb10b4ba0884a0c9a1d4a5e7315b9f8cdda1155ae270031f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:2e482739b5155d63e1cf76e3d6a81909f323552693a36f85cc3033cf4892718b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101724911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65ea580c9b344f6392f645b956e1f7642e3e48bd0c110b6c0e11336ccce11d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Feb 2023 11:42:37 GMT
ARG RELEASE
# Wed, 01 Feb 2023 11:42:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Feb 2023 11:42:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Feb 2023 11:42:39 GMT
ADD file:8b180a9b4497de0c6e131d6b48cf5c69a885379e63033ab9639d1655991e626c in / 
# Wed, 01 Feb 2023 11:42:39 GMT
CMD ["/bin/bash"]
# Wed, 01 Feb 2023 19:13:51 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Wed, 01 Feb 2023 19:13:51 GMT
ARG ASSET=ce
# Wed, 01 Feb 2023 19:13:51 GMT
ENV ASSET=ce
# Wed, 01 Feb 2023 19:13:51 GMT
ARG EE_PORTS
# Wed, 01 Feb 2023 19:13:51 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Wed, 01 Feb 2023 19:13:51 GMT
ARG KONG_VERSION=3.1.1
# Wed, 01 Feb 2023 19:13:52 GMT
ENV KONG_VERSION=3.1.1
# Wed, 01 Feb 2023 19:13:52 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Wed, 01 Feb 2023 19:13:52 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Wed, 01 Feb 2023 19:14:28 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 01 Feb 2023 19:14:29 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 01 Feb 2023 19:14:29 GMT
USER kong
# Wed, 01 Feb 2023 19:14:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 01 Feb 2023 19:14:29 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 01 Feb 2023 19:14:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 01 Feb 2023 19:14:29 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 01 Feb 2023 19:14:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7608715873ec5c02d370e963aa9b19a149023ce218887221d93fe671b3abbf58`  
		Last Modified: Thu, 26 Jan 2023 17:04:53 GMT  
		Size: 28.6 MB (28577884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22125083e90234102050bb19d1918bdb2c3c04bea9c73a62fe9ccd73c83f60e`  
		Last Modified: Wed, 01 Feb 2023 19:17:08 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8dc9e1b22d6e7ad79f283f2ab4c4a807ed6e310a25f512783dfba9d33e0fbf`  
		Last Modified: Wed, 01 Feb 2023 19:17:21 GMT  
		Size: 73.1 MB (73146021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d523f9590e88b534d4ccca2f54947d36099583997a52ef86067e3a87de965ce`  
		Last Modified: Wed, 01 Feb 2023 19:17:09 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f37cdf0d55daae01c871ce3190bb98ee4ad1cf665a5d5908567ccc518a2343eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98967418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71af4a27e17d09b757d37e788f1396d8e93c875e4bba189e4e6247583f63e90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Mar 2023 05:24:53 GMT
ARG RELEASE
# Wed, 01 Mar 2023 05:24:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Mar 2023 05:24:53 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 01 Mar 2023 05:24:55 GMT
ADD file:110968e7ce1c893bcdf7597ece624ff881de3e1ee2c4e2b70dbc18c9a5271fc0 in / 
# Wed, 01 Mar 2023 05:24:55 GMT
CMD ["/bin/bash"]
# Thu, 02 Mar 2023 03:04:26 GMT
LABEL maintainer=Kong Docker Maintainers <docker@konghq.com> (@team-gateway-bot)
# Thu, 02 Mar 2023 03:04:26 GMT
ARG ASSET=ce
# Thu, 02 Mar 2023 03:04:26 GMT
ENV ASSET=ce
# Thu, 02 Mar 2023 03:04:27 GMT
ARG EE_PORTS
# Thu, 02 Mar 2023 03:04:27 GMT
COPY file:c24b3b9739a4614fa0679c1a90bac51eb61f9f84b2b02c5c24925e0c84878649 in /tmp/kong.deb 
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 03:04:27 GMT
ENV KONG_VERSION=3.1.1
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b
# Thu, 02 Mar 2023 03:04:27 GMT
ARG KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
# Thu, 02 Mar 2023 03:04:48 GMT
# ARGS: KONG_AMD64_SHA=39bbefa14d348dedf7734c742da46acf7777ff0018f2cad7961799ba4663277b KONG_ARM64_SHA=66c88430fb641ace356af55db4377a697a5ee5a63fbb243bcc8a4a90e3874f9f
RUN set -ex;     arch=$(dpkg --print-architecture);     case "${arch}" in       amd64) KONG_SHA256=$KONG_AMD64_SHA ;;       arm64) KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_$arch.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -       || exit 1;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Thu, 02 Mar 2023 03:04:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Thu, 02 Mar 2023 03:04:49 GMT
USER kong
# Thu, 02 Mar 2023 03:04:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 02 Mar 2023 03:04:49 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 02 Mar 2023 03:04:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 02 Mar 2023 03:04:50 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Thu, 02 Mar 2023 03:04:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:970e18d4d6e7e6f413a168be4dd550847bf3c325f54e7c69a5ad6435dfd1fe48`  
		Last Modified: Wed, 01 Mar 2023 10:21:59 GMT  
		Size: 27.2 MB (27194521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d0fbc8d9bf568f12a72ae3807d56d02d576297b3b60a7cb35c92037eed9cb7`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f420840a76159d996c9e294e0e41d81735ac1c72051f3338e7fc4441119b8b`  
		Last Modified: Thu, 02 Mar 2023 03:06:53 GMT  
		Size: 71.8 MB (71771888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eff32e2df689b166673a2995418859a7ba334495d8b03f94c502f2b6183fc1a`  
		Last Modified: Thu, 02 Mar 2023 03:06:43 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
