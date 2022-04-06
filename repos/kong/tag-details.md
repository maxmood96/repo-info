<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.5`](#kong25)
-	[`kong:2.5-ubuntu`](#kong25-ubuntu)
-	[`kong:2.5.1`](#kong251)
-	[`kong:2.5.1-alpine`](#kong251-alpine)
-	[`kong:2.5.1-ubuntu`](#kong251-ubuntu)
-	[`kong:2.6`](#kong26)
-	[`kong:2.6-ubuntu`](#kong26-ubuntu)
-	[`kong:2.6.0`](#kong260)
-	[`kong:2.6.0-alpine`](#kong260-alpine)
-	[`kong:2.6.0-ubuntu`](#kong260-ubuntu)
-	[`kong:2.7`](#kong27)
-	[`kong:2.7-ubuntu`](#kong27-ubuntu)
-	[`kong:2.7.1`](#kong271)
-	[`kong:2.7.1-alpine`](#kong271-alpine)
-	[`kong:2.7.1-ubuntu`](#kong271-ubuntu)
-	[`kong:2.8`](#kong28)
-	[`kong:2.8-ubuntu`](#kong28-ubuntu)
-	[`kong:2.8.0`](#kong280)
-	[`kong:2.8.0-alpine`](#kong280-alpine)
-	[`kong:2.8.0-ubuntu`](#kong280-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.5`

```console
$ docker pull kong@sha256:41e3edb43d99e58372ad516d02d7723dd4addfbb058cb0bc6f6f7ad224d4f383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:154142e5fd657d9db0e53d9c2f2bb9d3f8690754117153217c7e2c26daec1633
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4df8ab4c6b478a834567e91b0c4afaa8f612d2dd2ad82ef1638dffa8a1791`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:52 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:53 GMT
USER kong
# Tue, 05 Apr 2022 07:18:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e19ff8ee1a3d712fb5a9b15e5dc3975135eabb0db2bdc9d86987b1dc0ab312`  
		Last Modified: Tue, 05 Apr 2022 07:20:38 GMT  
		Size: 47.0 MB (47006838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca93a317bbe9559f2a86be6eb2d745765ebaf28fb2f60aa5c32f0fb28634f5`  
		Last Modified: Tue, 05 Apr 2022 07:20:30 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40bc1b80631be6572ebdd0b3297cf1b405d96eb55605a2843f7395d4c07bd914
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ef302d4e9c486b95849bf1d9380438c9704379c74b16ab5a1a2d9f26b4df54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:28:09 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:10 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:11 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:12 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:13 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:14 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:23 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:28:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:28:24 GMT
USER kong
# Tue, 05 Apr 2022 14:28:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:28:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:28:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:28:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:28:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099f94dcde963cbb40fd4c0b539ebda765c2a4ee6973d14bb0528df4fa3835`  
		Last Modified: Tue, 05 Apr 2022 14:32:09 GMT  
		Size: 46.5 MB (46519329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406022bc9bda03a0ac64449c49805df757f7800fc95c620c9ecc541d65b30820`  
		Last Modified: Tue, 05 Apr 2022 14:32:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:85942392940f2ac6c4ffae4805f9a90c9450c7515657856d2b753668795a430a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:46d0e251b3a8f7ea8747998a1f45fde84109c597d5c16c368d917a621b120f95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128035707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b963cc65711671160d3eaeaea802bb9f57a7e4e19055031f1031dc68b30f41c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:19:36 GMT
ARG KONG_VERSION=2.5.1
# Wed, 06 Apr 2022 04:19:36 GMT
ENV KONG_VERSION=2.5.1
# Wed, 06 Apr 2022 04:19:55 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:19:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:19:56 GMT
USER kong
# Wed, 06 Apr 2022 04:19:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:19:56 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:19:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:19:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:19:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58673de4b074856db413da93d798c5eadcd33db37fcb481dbab9357d6d15e02c`  
		Last Modified: Wed, 06 Apr 2022 04:21:46 GMT  
		Size: 74.4 MB (74386580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d5b3ddf5b84a57047c5fc73f3633d7323782e616dbfa26c0be2970e78f25e`  
		Last Modified: Wed, 06 Apr 2022 04:21:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7fb163125ba0769471c7adccc2609abcd37c3e58afcfb159ab99aa30f5ba58f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125879708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8100ea3c312d55c4a34fcf3706f2584737cc61f1662715a6dd709d77d3f79138`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:19 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Tue, 31 Aug 2021 01:41:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:41:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:41:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:41:21 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:13:00 GMT
ARG ASSET=ce
# Tue, 31 Aug 2021 03:13:00 GMT
ENV ASSET=ce
# Tue, 31 Aug 2021 03:13:00 GMT
ARG EE_PORTS
# Tue, 31 Aug 2021 03:13:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 31 Aug 2021 03:13:01 GMT
ARG KONG_VERSION=2.5.0
# Tue, 31 Aug 2021 03:13:01 GMT
ENV KONG_VERSION=2.5.0
# Tue, 31 Aug 2021 03:13:24 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 31 Aug 2021 03:13:25 GMT
COPY file:ae813ec19d3fef1de3793f6717c2aed3a9daa94e583e9e55448084541de3c5ff in /docker-entrypoint.sh 
# Tue, 31 Aug 2021 03:13:25 GMT
USER kong
# Tue, 31 Aug 2021 03:13:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Aug 2021 03:13:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 31 Aug 2021 03:13:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 31 Aug 2021 03:13:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 31 Aug 2021 03:13:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85569e0c17003d9cf46a8b94076418863e0abfc5474bb830403acf246947fea7`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32ca509d28808ab7c61361835292ee8eddecd0c0949d658bde0ab1a77ecbf6e`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8168af71f81f1ffa234c301e9cc2ee87b560ad8b74ef4100f8ab4a6abf3a8ad3`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee59a359925630cd377c9610b18f7d7797349cdbabeda7b8c8685852a5ff83`  
		Last Modified: Tue, 31 Aug 2021 03:14:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe71eb414d43ff3fbf75c0de9133ebafceaf672848c6e2c17e4ab47780e97b`  
		Last Modified: Tue, 31 Aug 2021 03:15:00 GMT  
		Size: 59.6 MB (59556314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a45ed64e5c35d56c7aafb050d22218142de8f6d3142eba9294d41638844747`  
		Last Modified: Tue, 31 Aug 2021 03:14:46 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1`

```console
$ docker pull kong@sha256:41e3edb43d99e58372ad516d02d7723dd4addfbb058cb0bc6f6f7ad224d4f383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1` - linux; amd64

```console
$ docker pull kong@sha256:154142e5fd657d9db0e53d9c2f2bb9d3f8690754117153217c7e2c26daec1633
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4df8ab4c6b478a834567e91b0c4afaa8f612d2dd2ad82ef1638dffa8a1791`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:52 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:53 GMT
USER kong
# Tue, 05 Apr 2022 07:18:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e19ff8ee1a3d712fb5a9b15e5dc3975135eabb0db2bdc9d86987b1dc0ab312`  
		Last Modified: Tue, 05 Apr 2022 07:20:38 GMT  
		Size: 47.0 MB (47006838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca93a317bbe9559f2a86be6eb2d745765ebaf28fb2f60aa5c32f0fb28634f5`  
		Last Modified: Tue, 05 Apr 2022 07:20:30 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40bc1b80631be6572ebdd0b3297cf1b405d96eb55605a2843f7395d4c07bd914
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ef302d4e9c486b95849bf1d9380438c9704379c74b16ab5a1a2d9f26b4df54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:28:09 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:10 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:11 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:12 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:13 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:14 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:23 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:28:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:28:24 GMT
USER kong
# Tue, 05 Apr 2022 14:28:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:28:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:28:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:28:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:28:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099f94dcde963cbb40fd4c0b539ebda765c2a4ee6973d14bb0528df4fa3835`  
		Last Modified: Tue, 05 Apr 2022 14:32:09 GMT  
		Size: 46.5 MB (46519329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406022bc9bda03a0ac64449c49805df757f7800fc95c620c9ecc541d65b30820`  
		Last Modified: Tue, 05 Apr 2022 14:32:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-alpine`

```console
$ docker pull kong@sha256:41e3edb43d99e58372ad516d02d7723dd4addfbb058cb0bc6f6f7ad224d4f383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:154142e5fd657d9db0e53d9c2f2bb9d3f8690754117153217c7e2c26daec1633
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e4df8ab4c6b478a834567e91b0c4afaa8f612d2dd2ad82ef1638dffa8a1791`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 07:18:45 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:45 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 07:18:52 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:53 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:53 GMT
USER kong
# Tue, 05 Apr 2022 07:18:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:53 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e19ff8ee1a3d712fb5a9b15e5dc3975135eabb0db2bdc9d86987b1dc0ab312`  
		Last Modified: Tue, 05 Apr 2022 07:20:38 GMT  
		Size: 47.0 MB (47006838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dca93a317bbe9559f2a86be6eb2d745765ebaf28fb2f60aa5c32f0fb28634f5`  
		Last Modified: Tue, 05 Apr 2022 07:20:30 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:40bc1b80631be6572ebdd0b3297cf1b405d96eb55605a2843f7395d4c07bd914
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49237732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ef302d4e9c486b95849bf1d9380438c9704379c74b16ab5a1a2d9f26b4df54`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:28:09 GMT
ARG KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:10 GMT
ENV KONG_VERSION=2.5.1
# Tue, 05 Apr 2022 14:28:11 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:12 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Tue, 05 Apr 2022 14:28:13 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:14 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Tue, 05 Apr 2022 14:28:23 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:28:24 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:28:24 GMT
USER kong
# Tue, 05 Apr 2022 14:28:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:28:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:28:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:28:28 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:28:29 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5099f94dcde963cbb40fd4c0b539ebda765c2a4ee6973d14bb0528df4fa3835`  
		Last Modified: Tue, 05 Apr 2022 14:32:09 GMT  
		Size: 46.5 MB (46519329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406022bc9bda03a0ac64449c49805df757f7800fc95c620c9ecc541d65b30820`  
		Last Modified: Tue, 05 Apr 2022 14:32:01 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-ubuntu`

```console
$ docker pull kong@sha256:fe524217d88915ef11ae4e7b561fb8b6e415a9a518a0bf17d979b4bb6a1afc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.5.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:46d0e251b3a8f7ea8747998a1f45fde84109c597d5c16c368d917a621b120f95
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128035707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b963cc65711671160d3eaeaea802bb9f57a7e4e19055031f1031dc68b30f41c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:19:36 GMT
ARG KONG_VERSION=2.5.1
# Wed, 06 Apr 2022 04:19:36 GMT
ENV KONG_VERSION=2.5.1
# Wed, 06 Apr 2022 04:19:55 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:19:56 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:19:56 GMT
USER kong
# Wed, 06 Apr 2022 04:19:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:19:56 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:19:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:19:57 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:19:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58673de4b074856db413da93d798c5eadcd33db37fcb481dbab9357d6d15e02c`  
		Last Modified: Wed, 06 Apr 2022 04:21:46 GMT  
		Size: 74.4 MB (74386580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347d5b3ddf5b84a57047c5fc73f3633d7323782e616dbfa26c0be2970e78f25e`  
		Last Modified: Wed, 06 Apr 2022 04:21:34 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:28f74e81f2d5eef6df34aaf806c177900be52bc2ac9e204c9545203d60ecf8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:c3d6a0453bca195a12b1e82a74afacecf5506a449492a3786b925cfb9ca4f3bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49851980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5640b9319c0ada43764602002fbe5122da3b9f35ac719498de95b87c39a6f7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:40 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:40 GMT
USER kong
# Tue, 05 Apr 2022 07:18:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:40 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77326087f7969514a492f9b51c9551af57cce74868e026bb20771e97b909ee61`  
		Last Modified: Tue, 05 Apr 2022 07:20:17 GMT  
		Size: 47.0 MB (47032599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e3fa1a6a1f75401c16c56dd497322a8801080e7e047952a17ee44d660848d`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf6164f986d92b75438706bf956f45eebb79f96532836b7a288ee069053f15db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49275254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b2de22d4ad9f1c985b93d3f0ca687a0bea88c9a09fc9d2137ff18dd557ecf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:26:09 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:10 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:11 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:12 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:13 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:14 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:33 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:26:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:26:34 GMT
USER kong
# Tue, 05 Apr 2022 14:26:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:26:36 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:26:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:26:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:26:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bf8e846a5b2efcef66530cbc0ac4c23db06f8e5c297227076ac2a714d14157`  
		Last Modified: Tue, 05 Apr 2022 14:31:47 GMT  
		Size: 46.6 MB (46556851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcf1b755d2953c1384dce92ef08cac677413d9b516f2f4a352825733c77b7bc`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:52ea5e6d792b4a5af623d08e28e85c014cbfe6fee03baca05a6cadfe04eddea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:a524347319306e2e649daa6c6a332a0baa8f55b3471bdc22aeb186188c726ecf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128080132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6674c4735ee598fd949ba7243cb5038cb36a12fa7a94a11222241f3b2559693b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:19:10 GMT
ARG KONG_VERSION=2.6.0
# Wed, 06 Apr 2022 04:19:10 GMT
ENV KONG_VERSION=2.6.0
# Wed, 06 Apr 2022 04:19:30 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:19:31 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:19:31 GMT
USER kong
# Wed, 06 Apr 2022 04:19:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:19:31 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:19:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:19:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:19:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d18e04fd6c6da1e66f0b32bd44c00ecea747d884b32e38d655bcbe1094f7e9`  
		Last Modified: Wed, 06 Apr 2022 04:21:23 GMT  
		Size: 74.4 MB (74431008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267fcb938e638b8d3e780f7211ddfccd8ff82cccc78e248b63c2b343a56bc405`  
		Last Modified: Wed, 06 Apr 2022 04:21:11 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0`

```console
$ docker pull kong@sha256:28f74e81f2d5eef6df34aaf806c177900be52bc2ac9e204c9545203d60ecf8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0` - linux; amd64

```console
$ docker pull kong@sha256:c3d6a0453bca195a12b1e82a74afacecf5506a449492a3786b925cfb9ca4f3bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49851980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5640b9319c0ada43764602002fbe5122da3b9f35ac719498de95b87c39a6f7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:40 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:40 GMT
USER kong
# Tue, 05 Apr 2022 07:18:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:40 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77326087f7969514a492f9b51c9551af57cce74868e026bb20771e97b909ee61`  
		Last Modified: Tue, 05 Apr 2022 07:20:17 GMT  
		Size: 47.0 MB (47032599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e3fa1a6a1f75401c16c56dd497322a8801080e7e047952a17ee44d660848d`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf6164f986d92b75438706bf956f45eebb79f96532836b7a288ee069053f15db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49275254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b2de22d4ad9f1c985b93d3f0ca687a0bea88c9a09fc9d2137ff18dd557ecf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:26:09 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:10 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:11 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:12 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:13 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:14 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:33 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:26:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:26:34 GMT
USER kong
# Tue, 05 Apr 2022 14:26:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:26:36 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:26:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:26:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:26:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bf8e846a5b2efcef66530cbc0ac4c23db06f8e5c297227076ac2a714d14157`  
		Last Modified: Tue, 05 Apr 2022 14:31:47 GMT  
		Size: 46.6 MB (46556851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcf1b755d2953c1384dce92ef08cac677413d9b516f2f4a352825733c77b7bc`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-alpine`

```console
$ docker pull kong@sha256:28f74e81f2d5eef6df34aaf806c177900be52bc2ac9e204c9545203d60ecf8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:c3d6a0453bca195a12b1e82a74afacecf5506a449492a3786b925cfb9ca4f3bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49851980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5640b9319c0ada43764602002fbe5122da3b9f35ac719498de95b87c39a6f7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:31 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:31 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:31 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:32 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:32 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 07:18:32 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:32 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 07:18:40 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:40 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:40 GMT
USER kong
# Tue, 05 Apr 2022 07:18:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:40 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:40 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:41 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65244e381d7e015a75f9b3d8df2a49f4170a38679e6c3c6b0a468205c1886b0`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77326087f7969514a492f9b51c9551af57cce74868e026bb20771e97b909ee61`  
		Last Modified: Tue, 05 Apr 2022 07:20:17 GMT  
		Size: 47.0 MB (47032599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e3fa1a6a1f75401c16c56dd497322a8801080e7e047952a17ee44d660848d`  
		Last Modified: Tue, 05 Apr 2022 07:20:10 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:cf6164f986d92b75438706bf956f45eebb79f96532836b7a288ee069053f15db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49275254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b2de22d4ad9f1c985b93d3f0ca687a0bea88c9a09fc9d2137ff18dd557ecf7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:26:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:26:05 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:26:06 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:26:07 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:26:09 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:26:09 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:10 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Apr 2022 14:26:11 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:12 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Tue, 05 Apr 2022 14:26:13 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:14 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Tue, 05 Apr 2022 14:26:33 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:26:34 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:26:34 GMT
USER kong
# Tue, 05 Apr 2022 14:26:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:26:36 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:26:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:26:38 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:26:39 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e35a40e16bf077293a403527df55332656538c7440f973ba718144ac6c49`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bf8e846a5b2efcef66530cbc0ac4c23db06f8e5c297227076ac2a714d14157`  
		Last Modified: Tue, 05 Apr 2022 14:31:47 GMT  
		Size: 46.6 MB (46556851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcf1b755d2953c1384dce92ef08cac677413d9b516f2f4a352825733c77b7bc`  
		Last Modified: Tue, 05 Apr 2022 14:31:38 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-ubuntu`

```console
$ docker pull kong@sha256:52ea5e6d792b4a5af623d08e28e85c014cbfe6fee03baca05a6cadfe04eddea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:a524347319306e2e649daa6c6a332a0baa8f55b3471bdc22aeb186188c726ecf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128080132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6674c4735ee598fd949ba7243cb5038cb36a12fa7a94a11222241f3b2559693b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:19:10 GMT
ARG KONG_VERSION=2.6.0
# Wed, 06 Apr 2022 04:19:10 GMT
ENV KONG_VERSION=2.6.0
# Wed, 06 Apr 2022 04:19:30 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:19:31 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:19:31 GMT
USER kong
# Wed, 06 Apr 2022 04:19:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:19:31 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:19:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:19:31 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:19:31 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d18e04fd6c6da1e66f0b32bd44c00ecea747d884b32e38d655bcbe1094f7e9`  
		Last Modified: Wed, 06 Apr 2022 04:21:23 GMT  
		Size: 74.4 MB (74431008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267fcb938e638b8d3e780f7211ddfccd8ff82cccc78e248b63c2b343a56bc405`  
		Last Modified: Wed, 06 Apr 2022 04:21:11 GMT  
		Size: 878.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7`

```console
$ docker pull kong@sha256:cceaaccdc162b184490a963558251e4d0b943b124f91afd60c039eacb2a6daeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7` - linux; amd64

```console
$ docker pull kong@sha256:1c16b62bbac29d34bb9d98b2c4086ddb5a7c4cb3f5894c49795ac937cd41212d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50072135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6a1882af7ab659ee01f9b685778fef813cee85a7cebbe4a830c75b881d585b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 07:18:26 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:26 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:26 GMT
USER kong
# Tue, 05 Apr 2022 07:18:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d4b98a2b936a3436c0d2da9470c9219252bfc027f7f9bb020b409209f7d8ea`  
		Last Modified: Tue, 05 Apr 2022 07:19:56 GMT  
		Size: 47.3 MB (47256562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73e510ff864bb33d132ecc03600e597b82440a30c0982c3af7020b51899b2bc`  
		Last Modified: Tue, 05 Apr 2022 07:19:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:aa319cc291ab93f3439ab314de844bf4372615469fe7882c052c09e4f03be863
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a5459f176100a3049e86076a607792a1785517d4940a00bb90d99ed5bcc0f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:23:50 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:51 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:52 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 14:23:53 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 14:24:08 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:24:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:24:09 GMT
USER kong
# Tue, 05 Apr 2022 14:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:24:11 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:24:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:24:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:24:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0d3010a5a0e66ff16384f855ef03ac57bd485603a15c2f679080e896c3eaae`  
		Last Modified: Tue, 05 Apr 2022 14:31:23 GMT  
		Size: 46.8 MB (46764090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8130dd0a7ba94337ce11c52ef6005a98a02c1200e2f85509a4777c4ee76664`  
		Last Modified: Tue, 05 Apr 2022 14:31:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7-ubuntu`

```console
$ docker pull kong@sha256:1c00e045228bdc9ce36b7ca8d32d527648b0627ab74e54faf56a68980c50751c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:afa50672746c3afe6c208cdab99d644e9f1d6bd9ab1ab1c7fab633d8d30ea070
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127991599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40fdf1d5dbdcad70b12d2fea8a66e791e8978a64bf8ec0d8c82f6f1bfa0a1b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:18:40 GMT
ARG KONG_VERSION=2.7.1
# Wed, 06 Apr 2022 04:18:40 GMT
ENV KONG_VERSION=2.7.1
# Wed, 06 Apr 2022 04:18:40 GMT
ARG KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
# Wed, 06 Apr 2022 04:19:00 GMT
# ARGS: KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:19:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:19:01 GMT
USER kong
# Wed, 06 Apr 2022 04:19:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:19:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:19:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:19:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:19:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed04d447cf03f9e74e8cffb7695159ea03226269560dc614d58ace407abb9ef`  
		Last Modified: Wed, 06 Apr 2022 04:21:00 GMT  
		Size: 74.3 MB (74342472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a647e96e8e2de99aee38e2cc6d1a1f1d16321350edcafece5169d285953082c2`  
		Last Modified: Wed, 06 Apr 2022 04:20:49 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1`

```console
$ docker pull kong@sha256:cceaaccdc162b184490a963558251e4d0b943b124f91afd60c039eacb2a6daeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.1` - linux; amd64

```console
$ docker pull kong@sha256:1c16b62bbac29d34bb9d98b2c4086ddb5a7c4cb3f5894c49795ac937cd41212d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50072135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6a1882af7ab659ee01f9b685778fef813cee85a7cebbe4a830c75b881d585b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 07:18:26 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:26 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:26 GMT
USER kong
# Tue, 05 Apr 2022 07:18:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d4b98a2b936a3436c0d2da9470c9219252bfc027f7f9bb020b409209f7d8ea`  
		Last Modified: Tue, 05 Apr 2022 07:19:56 GMT  
		Size: 47.3 MB (47256562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73e510ff864bb33d132ecc03600e597b82440a30c0982c3af7020b51899b2bc`  
		Last Modified: Tue, 05 Apr 2022 07:19:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:aa319cc291ab93f3439ab314de844bf4372615469fe7882c052c09e4f03be863
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a5459f176100a3049e86076a607792a1785517d4940a00bb90d99ed5bcc0f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:23:50 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:51 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:52 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 14:23:53 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 14:24:08 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:24:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:24:09 GMT
USER kong
# Tue, 05 Apr 2022 14:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:24:11 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:24:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:24:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:24:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0d3010a5a0e66ff16384f855ef03ac57bd485603a15c2f679080e896c3eaae`  
		Last Modified: Tue, 05 Apr 2022 14:31:23 GMT  
		Size: 46.8 MB (46764090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8130dd0a7ba94337ce11c52ef6005a98a02c1200e2f85509a4777c4ee76664`  
		Last Modified: Tue, 05 Apr 2022 14:31:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1-alpine`

```console
$ docker pull kong@sha256:cceaaccdc162b184490a963558251e4d0b943b124f91afd60c039eacb2a6daeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.7.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:1c16b62bbac29d34bb9d98b2c4086ddb5a7c4cb3f5894c49795ac937cd41212d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50072135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6a1882af7ab659ee01f9b685778fef813cee85a7cebbe4a830c75b881d585b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 07:18:18 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 07:18:26 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:26 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:26 GMT
USER kong
# Tue, 05 Apr 2022 07:18:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:26 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d4b98a2b936a3436c0d2da9470c9219252bfc027f7f9bb020b409209f7d8ea`  
		Last Modified: Tue, 05 Apr 2022 07:19:56 GMT  
		Size: 47.3 MB (47256562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73e510ff864bb33d132ecc03600e597b82440a30c0982c3af7020b51899b2bc`  
		Last Modified: Tue, 05 Apr 2022 07:19:48 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.7.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:aa319cc291ab93f3439ab314de844bf4372615469fe7882c052c09e4f03be863
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a5459f176100a3049e86076a607792a1785517d4940a00bb90d99ed5bcc0f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:23:50 GMT
ARG KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:51 GMT
ENV KONG_VERSION=2.7.1
# Tue, 05 Apr 2022 14:23:52 GMT
ARG KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4
# Tue, 05 Apr 2022 14:23:53 GMT
ARG KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
# Tue, 05 Apr 2022 14:24:08 GMT
# ARGS: KONG_AMD64_SHA=7ccd12a15f357dea4d9bea2a5c06c1efe05dcaa0bc8b937f00619e31634715c4 KONG_ARM64_SHA=00f6c3af15418af07d7429e15762db2355a5f9cdbf278f198c59b5fd34e80abc
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:24:09 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:24:09 GMT
USER kong
# Tue, 05 Apr 2022 14:24:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:24:11 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:24:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:24:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:24:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0d3010a5a0e66ff16384f855ef03ac57bd485603a15c2f679080e896c3eaae`  
		Last Modified: Tue, 05 Apr 2022 14:31:23 GMT  
		Size: 46.8 MB (46764090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c8130dd0a7ba94337ce11c52ef6005a98a02c1200e2f85509a4777c4ee76664`  
		Last Modified: Tue, 05 Apr 2022 14:31:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.7.1-ubuntu`

```console
$ docker pull kong@sha256:1c00e045228bdc9ce36b7ca8d32d527648b0627ab74e54faf56a68980c50751c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.7.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:afa50672746c3afe6c208cdab99d644e9f1d6bd9ab1ab1c7fab633d8d30ea070
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (127991599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40fdf1d5dbdcad70b12d2fea8a66e791e8978a64bf8ec0d8c82f6f1bfa0a1b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:18:40 GMT
ARG KONG_VERSION=2.7.1
# Wed, 06 Apr 2022 04:18:40 GMT
ENV KONG_VERSION=2.7.1
# Wed, 06 Apr 2022 04:18:40 GMT
ARG KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
# Wed, 06 Apr 2022 04:19:00 GMT
# ARGS: KONG_SHA256=feeee661bbe44cf3ca2d4b748291dd3f9153f355fbc13ffeccb6fbc036249a89
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:19:01 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:19:01 GMT
USER kong
# Wed, 06 Apr 2022 04:19:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:19:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:19:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:19:01 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:19:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed04d447cf03f9e74e8cffb7695159ea03226269560dc614d58ace407abb9ef`  
		Last Modified: Wed, 06 Apr 2022 04:21:00 GMT  
		Size: 74.3 MB (74342472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a647e96e8e2de99aee38e2cc6d1a1f1d16321350edcafece5169d285953082c2`  
		Last Modified: Wed, 06 Apr 2022 04:20:49 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8`

```console
$ docker pull kong@sha256:92e69c043806c7a77f07b3afa23335bd462fcfe4bcc6646b42527ae2e3682177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8` - linux; amd64

```console
$ docker pull kong@sha256:80ab9ea850626def46452d984e32d8a6cba057842e3002e03b83eabbf3b3e983
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49114128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abd56e893359a729325103065a1f6c2e004dec25e2ffc382016551372b6707`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 07:18:12 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:13 GMT
USER kong
# Tue, 05 Apr 2022 07:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c1f4c755850a2adc30b8cc2b020bfbee49e1a10fe126b299cfd80ffed685be`  
		Last Modified: Tue, 05 Apr 2022 07:19:30 GMT  
		Size: 46.3 MB (46298555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f270dea85947274c1da7de384551b7ab5514066ec071ab3d0ac1ca12004290`  
		Last Modified: Tue, 05 Apr 2022 07:19:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a1b94982b50727d67b57988efb863e3738e28f8f62851f5c0a8f4c8374476ed2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48306718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890c0a81ce116131f054213f59d76846afd1b9efd9893da6c58d37501d4a10c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:21:22 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:23 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:24 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 14:21:25 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 14:21:43 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:21:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:21:44 GMT
USER kong
# Tue, 05 Apr 2022 14:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:21:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:21:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:21:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:21:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab132370421ab09a7865a3492f2060ba102f456f0572e0b574d527ad0dd8f67`  
		Last Modified: Tue, 05 Apr 2022 14:30:34 GMT  
		Size: 45.6 MB (45589229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ab581ead9fa3c47fa83014394d89503e845d302567c5fe34b3282d2c15f90`  
		Last Modified: Tue, 05 Apr 2022 14:30:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8-ubuntu`

```console
$ docker pull kong@sha256:be63c6719492eb26dca9176bb5dfb454ab5dee8af0432e9d800e8755cbbb8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9300059a00436270edc60a8c123dbabfcc7707602436e80338edd62c502aef7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121206351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634e26875625abf55467c26fecc529e64d9d43d1ea4df09a5e6b0d318b4c06d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:18:15 GMT
ARG KONG_VERSION=2.8.0
# Wed, 06 Apr 2022 04:18:15 GMT
ENV KONG_VERSION=2.8.0
# Wed, 06 Apr 2022 04:18:15 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Wed, 06 Apr 2022 04:18:34 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:18:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:18:35 GMT
USER kong
# Wed, 06 Apr 2022 04:18:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:18:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:18:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:18:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:18:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c13a008561cf43e3826bc89a81951c725f75dbe6764471c74883592d6614b2`  
		Last Modified: Wed, 06 Apr 2022 04:20:36 GMT  
		Size: 67.6 MB (67557224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e08969d7f94992433e78e6c83b2d3a95c0f12295337b6a6b99bb61af19e0731`  
		Last Modified: Wed, 06 Apr 2022 04:20:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.0`

```console
$ docker pull kong@sha256:92e69c043806c7a77f07b3afa23335bd462fcfe4bcc6646b42527ae2e3682177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.0` - linux; amd64

```console
$ docker pull kong@sha256:80ab9ea850626def46452d984e32d8a6cba057842e3002e03b83eabbf3b3e983
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49114128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abd56e893359a729325103065a1f6c2e004dec25e2ffc382016551372b6707`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 07:18:12 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:13 GMT
USER kong
# Tue, 05 Apr 2022 07:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c1f4c755850a2adc30b8cc2b020bfbee49e1a10fe126b299cfd80ffed685be`  
		Last Modified: Tue, 05 Apr 2022 07:19:30 GMT  
		Size: 46.3 MB (46298555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f270dea85947274c1da7de384551b7ab5514066ec071ab3d0ac1ca12004290`  
		Last Modified: Tue, 05 Apr 2022 07:19:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a1b94982b50727d67b57988efb863e3738e28f8f62851f5c0a8f4c8374476ed2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48306718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890c0a81ce116131f054213f59d76846afd1b9efd9893da6c58d37501d4a10c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:21:22 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:23 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:24 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 14:21:25 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 14:21:43 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:21:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:21:44 GMT
USER kong
# Tue, 05 Apr 2022 14:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:21:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:21:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:21:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:21:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab132370421ab09a7865a3492f2060ba102f456f0572e0b574d527ad0dd8f67`  
		Last Modified: Tue, 05 Apr 2022 14:30:34 GMT  
		Size: 45.6 MB (45589229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ab581ead9fa3c47fa83014394d89503e845d302567c5fe34b3282d2c15f90`  
		Last Modified: Tue, 05 Apr 2022 14:30:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.0-alpine`

```console
$ docker pull kong@sha256:92e69c043806c7a77f07b3afa23335bd462fcfe4bcc6646b42527ae2e3682177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.8.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:80ab9ea850626def46452d984e32d8a6cba057842e3002e03b83eabbf3b3e983
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49114128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abd56e893359a729325103065a1f6c2e004dec25e2ffc382016551372b6707`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 07:18:12 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:13 GMT
USER kong
# Tue, 05 Apr 2022 07:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c1f4c755850a2adc30b8cc2b020bfbee49e1a10fe126b299cfd80ffed685be`  
		Last Modified: Tue, 05 Apr 2022 07:19:30 GMT  
		Size: 46.3 MB (46298555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f270dea85947274c1da7de384551b7ab5514066ec071ab3d0ac1ca12004290`  
		Last Modified: Tue, 05 Apr 2022 07:19:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.8.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a1b94982b50727d67b57988efb863e3738e28f8f62851f5c0a8f4c8374476ed2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48306718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890c0a81ce116131f054213f59d76846afd1b9efd9893da6c58d37501d4a10c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:21:22 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:23 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:24 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 14:21:25 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 14:21:43 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:21:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:21:44 GMT
USER kong
# Tue, 05 Apr 2022 14:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:21:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:21:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:21:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:21:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab132370421ab09a7865a3492f2060ba102f456f0572e0b574d527ad0dd8f67`  
		Last Modified: Tue, 05 Apr 2022 14:30:34 GMT  
		Size: 45.6 MB (45589229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ab581ead9fa3c47fa83014394d89503e845d302567c5fe34b3282d2c15f90`  
		Last Modified: Tue, 05 Apr 2022 14:30:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.8.0-ubuntu`

```console
$ docker pull kong@sha256:be63c6719492eb26dca9176bb5dfb454ab5dee8af0432e9d800e8755cbbb8173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.8.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9300059a00436270edc60a8c123dbabfcc7707602436e80338edd62c502aef7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121206351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634e26875625abf55467c26fecc529e64d9d43d1ea4df09a5e6b0d318b4c06d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:18:15 GMT
ARG KONG_VERSION=2.8.0
# Wed, 06 Apr 2022 04:18:15 GMT
ENV KONG_VERSION=2.8.0
# Wed, 06 Apr 2022 04:18:15 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Wed, 06 Apr 2022 04:18:34 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:18:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:18:35 GMT
USER kong
# Wed, 06 Apr 2022 04:18:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:18:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:18:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:18:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:18:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c13a008561cf43e3826bc89a81951c725f75dbe6764471c74883592d6614b2`  
		Last Modified: Wed, 06 Apr 2022 04:20:36 GMT  
		Size: 67.6 MB (67557224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e08969d7f94992433e78e6c83b2d3a95c0f12295337b6a6b99bb61af19e0731`  
		Last Modified: Wed, 06 Apr 2022 04:20:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:92e69c043806c7a77f07b3afa23335bd462fcfe4bcc6646b42527ae2e3682177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:80ab9ea850626def46452d984e32d8a6cba057842e3002e03b83eabbf3b3e983
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49114128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abd56e893359a729325103065a1f6c2e004dec25e2ffc382016551372b6707`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 07:18:12 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:13 GMT
USER kong
# Tue, 05 Apr 2022 07:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c1f4c755850a2adc30b8cc2b020bfbee49e1a10fe126b299cfd80ffed685be`  
		Last Modified: Tue, 05 Apr 2022 07:19:30 GMT  
		Size: 46.3 MB (46298555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f270dea85947274c1da7de384551b7ab5514066ec071ab3d0ac1ca12004290`  
		Last Modified: Tue, 05 Apr 2022 07:19:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a1b94982b50727d67b57988efb863e3738e28f8f62851f5c0a8f4c8374476ed2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48306718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890c0a81ce116131f054213f59d76846afd1b9efd9893da6c58d37501d4a10c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:21:22 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:23 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:24 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 14:21:25 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 14:21:43 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:21:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:21:44 GMT
USER kong
# Tue, 05 Apr 2022 14:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:21:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:21:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:21:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:21:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab132370421ab09a7865a3492f2060ba102f456f0572e0b574d527ad0dd8f67`  
		Last Modified: Tue, 05 Apr 2022 14:30:34 GMT  
		Size: 45.6 MB (45589229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ab581ead9fa3c47fa83014394d89503e845d302567c5fe34b3282d2c15f90`  
		Last Modified: Tue, 05 Apr 2022 14:30:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:92e69c043806c7a77f07b3afa23335bd462fcfe4bcc6646b42527ae2e3682177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:80ab9ea850626def46452d984e32d8a6cba057842e3002e03b83eabbf3b3e983
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49114128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abd56e893359a729325103065a1f6c2e004dec25e2ffc382016551372b6707`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:18:04 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 07:18:04 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 07:18:04 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 07:18:05 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 07:18:05 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 07:18:12 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 07:18:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 07:18:13 GMT
USER kong
# Tue, 05 Apr 2022 07:18:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 07:18:13 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 07:18:13 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 07:18:13 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 07:18:13 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170be706142252f720b9b2bcf269531d4b48ae2a10978af5b683db9b2d77921e`  
		Last Modified: Tue, 05 Apr 2022 07:19:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c1f4c755850a2adc30b8cc2b020bfbee49e1a10fe126b299cfd80ffed685be`  
		Last Modified: Tue, 05 Apr 2022 07:19:30 GMT  
		Size: 46.3 MB (46298555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f270dea85947274c1da7de384551b7ab5514066ec071ab3d0ac1ca12004290`  
		Last Modified: Tue, 05 Apr 2022 07:19:22 GMT  
		Size: 882.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a1b94982b50727d67b57988efb863e3738e28f8f62851f5c0a8f4c8374476ed2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48306718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3890c0a81ce116131f054213f59d76846afd1b9efd9893da6c58d37501d4a10c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 14:21:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Tue, 05 Apr 2022 14:21:18 GMT
ARG ASSET=ce
# Tue, 05 Apr 2022 14:21:19 GMT
ENV ASSET=ce
# Tue, 05 Apr 2022 14:21:20 GMT
ARG EE_PORTS
# Tue, 05 Apr 2022 14:21:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 05 Apr 2022 14:21:22 GMT
ARG KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:23 GMT
ENV KONG_VERSION=2.8.0
# Tue, 05 Apr 2022 14:21:24 GMT
ARG KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583
# Tue, 05 Apr 2022 14:21:25 GMT
ARG KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
# Tue, 05 Apr 2022 14:21:43 GMT
# ARGS: KONG_AMD64_SHA=60ef680e0fc4d2cf52934758e6a0dc0f173d2a3b32aca49c7eb31ab478c24583 KONG_ARM64_SHA=5c23f448eeae1b363ece51d066405c13798ee08ca413097a23d9b5ccb49cbf35
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     else       apk upgrade;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Tue, 05 Apr 2022 14:21:44 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Apr 2022 14:21:44 GMT
USER kong
# Tue, 05 Apr 2022 14:21:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 14:21:46 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Apr 2022 14:21:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Apr 2022 14:21:48 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Apr 2022 14:21:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959e28d0468f3d9ca1c7c6337f5b36149c289eae440dda05357f49bede98494`  
		Last Modified: Tue, 05 Apr 2022 14:30:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab132370421ab09a7865a3492f2060ba102f456f0572e0b574d527ad0dd8f67`  
		Last Modified: Tue, 05 Apr 2022 14:30:34 GMT  
		Size: 45.6 MB (45589229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ab581ead9fa3c47fa83014394d89503e845d302567c5fe34b3282d2c15f90`  
		Last Modified: Tue, 05 Apr 2022 14:30:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:1d90bcb91e57fc0a150d4723a1efd473bb2c7349a76660cbdf5e2930a82e98bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:9300059a00436270edc60a8c123dbabfcc7707602436e80338edd62c502aef7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121206351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634e26875625abf55467c26fecc529e64d9d43d1ea4df09a5e6b0d318b4c06d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:18:14 GMT
ARG ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ENV ASSET=ce
# Wed, 06 Apr 2022 04:18:14 GMT
ARG EE_PORTS
# Wed, 06 Apr 2022 04:18:15 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 06 Apr 2022 04:18:15 GMT
ARG KONG_VERSION=2.8.0
# Wed, 06 Apr 2022 04:18:15 GMT
ENV KONG_VERSION=2.8.0
# Wed, 06 Apr 2022 04:18:15 GMT
ARG KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
# Wed, 06 Apr 2022 04:18:34 GMT
# ARGS: KONG_SHA256=f49c6733bf71d5a9079fa7238f8b8cbdab11077a6afd81077a025268c6611744
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && UBUNTU_CODENAME=$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-${UBUNTU_CODENAME}/pool/all/k/kong/kong_${KONG_VERSION}_amd64.deb -o /tmp/kong.deb       && apt-get purge -y curl       && echo "$KONG_SHA256  /tmp/kong.deb" | sha256sum -c -;     else       apt-get upgrade -y ;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 06 Apr 2022 04:18:35 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 06 Apr 2022 04:18:35 GMT
USER kong
# Wed, 06 Apr 2022 04:18:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 06 Apr 2022 04:18:35 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 06 Apr 2022 04:18:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Apr 2022 04:18:35 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 06 Apr 2022 04:18:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb0280ec3b778bc3377472e743ce24bcdd73c3876a924e826b99d1343546cdd`  
		Last Modified: Wed, 06 Apr 2022 04:20:26 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c13a008561cf43e3826bc89a81951c725f75dbe6764471c74883592d6614b2`  
		Last Modified: Wed, 06 Apr 2022 04:20:36 GMT  
		Size: 67.6 MB (67557224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e08969d7f94992433e78e6c83b2d3a95c0f12295337b6a6b99bb61af19e0731`  
		Last Modified: Wed, 06 Apr 2022 04:20:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:7fb163125ba0769471c7adccc2609abcd37c3e58afcfb159ab99aa30f5ba58f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125879708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8100ea3c312d55c4a34fcf3706f2584737cc61f1662715a6dd709d77d3f79138`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 31 Aug 2021 01:41:19 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Tue, 31 Aug 2021 01:41:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:41:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:41:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:41:21 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:13:00 GMT
ARG ASSET=ce
# Tue, 31 Aug 2021 03:13:00 GMT
ENV ASSET=ce
# Tue, 31 Aug 2021 03:13:00 GMT
ARG EE_PORTS
# Tue, 31 Aug 2021 03:13:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 31 Aug 2021 03:13:01 GMT
ARG KONG_VERSION=2.5.0
# Tue, 31 Aug 2021 03:13:01 GMT
ENV KONG_VERSION=2.5.0
# Tue, 31 Aug 2021 03:13:24 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 31 Aug 2021 03:13:25 GMT
COPY file:ae813ec19d3fef1de3793f6717c2aed3a9daa94e583e9e55448084541de3c5ff in /docker-entrypoint.sh 
# Tue, 31 Aug 2021 03:13:25 GMT
USER kong
# Tue, 31 Aug 2021 03:13:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Aug 2021 03:13:25 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 31 Aug 2021 03:13:26 GMT
STOPSIGNAL SIGQUIT
# Tue, 31 Aug 2021 03:13:26 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 31 Aug 2021 03:13:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85569e0c17003d9cf46a8b94076418863e0abfc5474bb830403acf246947fea7`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32ca509d28808ab7c61361835292ee8eddecd0c0949d658bde0ab1a77ecbf6e`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 469.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8168af71f81f1ffa234c301e9cc2ee87b560ad8b74ef4100f8ab4a6abf3a8ad3`  
		Last Modified: Tue, 31 Aug 2021 01:43:39 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee59a359925630cd377c9610b18f7d7797349cdbabeda7b8c8685852a5ff83`  
		Last Modified: Tue, 31 Aug 2021 03:14:48 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbe71eb414d43ff3fbf75c0de9133ebafceaf672848c6e2c17e4ab47780e97b`  
		Last Modified: Tue, 31 Aug 2021 03:15:00 GMT  
		Size: 59.6 MB (59556314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a45ed64e5c35d56c7aafb050d22218142de8f6d3142eba9294d41638844747`  
		Last Modified: Tue, 31 Aug 2021 03:14:46 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
