<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2`](#kong2)
-	[`kong:2.0`](#kong20)
-	[`kong:2.0-centos`](#kong20-centos)
-	[`kong:2.0-ubuntu`](#kong20-ubuntu)
-	[`kong:2.0.5`](#kong205)
-	[`kong:2.0.5-alpine`](#kong205-alpine)
-	[`kong:2.0.5-centos`](#kong205-centos)
-	[`kong:2.0.5-ubuntu`](#kong205-ubuntu)
-	[`kong:2.1`](#kong21)
-	[`kong:2.1-alpine`](#kong21-alpine)
-	[`kong:2.1-centos`](#kong21-centos)
-	[`kong:2.1-ubuntu`](#kong21-ubuntu)
-	[`kong:2.1.4`](#kong214)
-	[`kong:2.1.4-alpine`](#kong214-alpine)
-	[`kong:2.1.4-centos`](#kong214-centos)
-	[`kong:2.1.4-ubuntu`](#kong214-ubuntu)
-	[`kong:2.2`](#kong22)
-	[`kong:2.2-alpine`](#kong22-alpine)
-	[`kong:2.2-centos`](#kong22-centos)
-	[`kong:2.2-ubuntu`](#kong22-ubuntu)
-	[`kong:2.2.2`](#kong222)
-	[`kong:2.2.2-alpine`](#kong222-alpine)
-	[`kong:2.2.2-centos`](#kong222-centos)
-	[`kong:2.2.2-ubuntu`](#kong222-ubuntu)
-	[`kong:2.3`](#kong23)
-	[`kong:2.3-alpine`](#kong23-alpine)
-	[`kong:2.3-centos`](#kong23-centos)
-	[`kong:2.3-ubuntu`](#kong23-ubuntu)
-	[`kong:2.3.3`](#kong233)
-	[`kong:2.3.3-alpine`](#kong233-alpine)
-	[`kong:2.3.3-centos`](#kong233-centos)
-	[`kong:2.3.3-ubuntu`](#kong233-ubuntu)
-	[`kong:2.4`](#kong24)
-	[`kong:2.4-alpine`](#kong24-alpine)
-	[`kong:2.4-centos`](#kong24-centos)
-	[`kong:2.4-ubuntu`](#kong24-ubuntu)
-	[`kong:2.4.1`](#kong241)
-	[`kong:2.4.1-alpine`](#kong241-alpine)
-	[`kong:2.4.1-centos`](#kong241-centos)
-	[`kong:2.4.1-ubuntu`](#kong241-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:centos`](#kongcentos)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2`

```console
$ docker pull kong@sha256:c9872460e6c9cb05d5ac1f125fff571c00541d4da7438f5eb821e07a56efe752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:31e0abee64747a4a31159b4d41538a03d9cbf7bfbe9708e00d5703aa9ce5f2b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51160610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b022e820b9b2bb6de4b8d0a3f8d50702612ef93ab70a2a108c020bac31b4f02a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:48 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 11 May 2021 22:29:49 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:29:49 GMT
USER kong
# Tue, 11 May 2021 22:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:29:49 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:29:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:29:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04308f3534771e4911ece45118ea51db7d9a992c72336fb9c1165a8fe3ca894e`  
		Last Modified: Tue, 11 May 2021 22:33:23 GMT  
		Size: 48.3 MB (48343499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af5626bb095a631ee85ddaae2c1bc71dd4085dfd56e149ba5f34fbe3a71cd05`  
		Last Modified: Tue, 11 May 2021 22:33:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a350bd912a622a02b61e9c5b6b20c5e3365f5544407ee1b8b4c63e9a8f0bdec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50694302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e44d048d3428713b1443578b223a2833de190e4e9adcd22a618d1fba72fd1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:03:52 GMT
ARG KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:04:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:01 GMT
USER kong
# Wed, 16 Jun 2021 01:04:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4661998cf20ee5e8dc00d8c36cc7bac6fb43f2c86ea1c68d7ed96e3698b15`  
		Last Modified: Wed, 16 Jun 2021 01:06:27 GMT  
		Size: 48.0 MB (47966509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afbf6dc6d0b33bda49d4eeb05932798f55369bdb1969730abc0ac73fd9f0e4`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0`

```console
$ docker pull kong@sha256:6166bc1cca2267736253127a0c7eb7f19c3f01bfa9a29b72ad4f7199c00ce51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0` - linux; amd64

```console
$ docker pull kong@sha256:e02a22193c3a09f4a424e80e193c2362b1d29f07be0c3c9d8308ef01eb5bef45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52771040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b7eb60cdeec3a692dfdefb1386dd9bf2d37b78757096bf1bfba22e66c45de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:27:35 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:27:35 GMT
ARG KONG_VERSION=2.0.5
# Wed, 14 Apr 2021 19:27:36 GMT
ENV KONG_VERSION=2.0.5
# Wed, 14 Apr 2021 19:27:36 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 14 Apr 2021 19:27:36 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 14 Apr 2021 19:27:49 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Wed, 14 Apr 2021 19:27:50 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:27:50 GMT
USER kong
# Wed, 14 Apr 2021 19:27:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:27:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:27:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:27:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eab765c4bc06602de99bfddcb851093d98720541c460033346c11ff6d67240e`  
		Last Modified: Wed, 14 Apr 2021 19:32:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a706fa32622b36b894c4c36a9ae7df67cbf5fc469e20896fc04aecdbd8c0d`  
		Last Modified: Wed, 14 Apr 2021 19:32:20 GMT  
		Size: 50.0 MB (49953930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e5f555dac438b8e3f8740c0095114272c3bea1831249451b8f677abeda018a`  
		Last Modified: Wed, 14 Apr 2021 19:32:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0-centos`

```console
$ docker pull kong@sha256:7a6ec5d8213e47be38adc4ccb0a0b6d03d0bd907f5744a64c77ec3ebab74dc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0-centos` - linux; amd64

```console
$ docker pull kong@sha256:8c2de33ebbc32e8740f0a3502233a1e3f1fb047ea12feff6ed2dafe4d94d84d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127537940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e00a921b7d5673370fa7991a4ab42a344a3ea649274a23ca9a5a971ec38465`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:48 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:36:48 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:49 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:49 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 06 Mar 2021 07:36:49 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 06 Mar 2021 07:37:16 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 06 Mar 2021 07:37:16 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:37:16 GMT
USER kong
# Sat, 06 Mar 2021 07:37:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:37:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:37:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:37:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f56126da854435826e67895a0c0904e2d9192aec7b83e187b93fc9e34f9db19`  
		Last Modified: Sat, 06 Mar 2021 07:42:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372cea5912641852de535666cf1cb0204d6ab7c67e54a5bf67440f91f0017f6c`  
		Last Modified: Sat, 06 Mar 2021 07:43:01 GMT  
		Size: 51.4 MB (51439924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4813e3fe68a31d3fbca2ea4ab673b0ae50dca5f95280bc9ce89670e2346b0b80`  
		Last Modified: Sat, 06 Mar 2021 07:42:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0-ubuntu`

```console
$ docker pull kong@sha256:9316bfc042dba24b719939734edf4a8466c719a7504517a8551bb43a33de2032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1c6b110dac9417dd91eea3f6f004c4bd784f85d6455737d1450f40c9eea35f1c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101555862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e906828b997a80eaed96e5db93649b594d7a0b6f7dd7ec73b94bdb4eca16b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:13:07 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Wed, 19 May 2021 21:13:07 GMT
ARG KONG_VERSION=2.0.5
# Wed, 19 May 2021 21:13:07 GMT
ENV KONG_VERSION=2.0.5
# Wed, 19 May 2021 21:13:27 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Wed, 19 May 2021 21:13:28 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:13:28 GMT
USER kong
# Wed, 19 May 2021 21:13:29 GMT
RUN kong version
# Wed, 19 May 2021 21:13:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:13:30 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:13:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:13:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e926417334cac9ea7a3e092369fd1fe7c64522978697082257bcd863206a83`  
		Last Modified: Wed, 19 May 2021 21:16:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6588fdc0513669307d470451335b7736cea827c9a5190ca92bb8835b45af76`  
		Last Modified: Wed, 19 May 2021 21:16:19 GMT  
		Size: 55.1 MB (55091630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78653f64c16e0f0ab1d9d713bf3c1d67e2989d09eb92e41b649eb1ae0e6d96a9`  
		Last Modified: Wed, 19 May 2021 21:16:09 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df37c4ab3867121ca6f9e5a7bfce4c35e54de078d35659e570da61cc509ec33b`  
		Last Modified: Wed, 19 May 2021 21:16:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:150312eec3542413e102f6d4db4d7b6eedd369a3e7dd9ee8d07a803fcf3a7a52
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93397647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e95e866299ba8d43926dbba69f93bdfa64d897e7c139c944452f901814bc88`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:43:15 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 27 May 2021 20:43:15 GMT
ARG KONG_VERSION=2.0.5
# Thu, 27 May 2021 20:43:15 GMT
ENV KONG_VERSION=2.0.5
# Thu, 27 May 2021 20:43:35 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 27 May 2021 20:43:35 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:43:35 GMT
USER kong
# Thu, 27 May 2021 20:43:36 GMT
RUN kong version
# Thu, 27 May 2021 20:43:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:43:36 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:43:37 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:43:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db22f7981d2858e484455e7c7e211d39a5b7f221155ea8e9e233383512032b52`  
		Last Modified: Thu, 27 May 2021 20:48:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d994454210ed5cc1da455370e047a132caab7611ce7a42c830f45d984fa3ce`  
		Last Modified: Thu, 27 May 2021 20:48:47 GMT  
		Size: 52.2 MB (52182744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabec8c13f1f2fa6975badb560b10ac4e73b72a539d16dd61942b18b983e4cb3`  
		Last Modified: Thu, 27 May 2021 20:48:36 GMT  
		Size: 687.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968f5174045c911115313a2247c01d459c55a5c5fb55b06272f2914fdeecd0bd`  
		Last Modified: Thu, 27 May 2021 20:48:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5`

```console
$ docker pull kong@sha256:6166bc1cca2267736253127a0c7eb7f19c3f01bfa9a29b72ad4f7199c00ce51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5` - linux; amd64

```console
$ docker pull kong@sha256:e02a22193c3a09f4a424e80e193c2362b1d29f07be0c3c9d8308ef01eb5bef45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52771040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b7eb60cdeec3a692dfdefb1386dd9bf2d37b78757096bf1bfba22e66c45de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:27:35 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:27:35 GMT
ARG KONG_VERSION=2.0.5
# Wed, 14 Apr 2021 19:27:36 GMT
ENV KONG_VERSION=2.0.5
# Wed, 14 Apr 2021 19:27:36 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 14 Apr 2021 19:27:36 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 14 Apr 2021 19:27:49 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Wed, 14 Apr 2021 19:27:50 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:27:50 GMT
USER kong
# Wed, 14 Apr 2021 19:27:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:27:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:27:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:27:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eab765c4bc06602de99bfddcb851093d98720541c460033346c11ff6d67240e`  
		Last Modified: Wed, 14 Apr 2021 19:32:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a706fa32622b36b894c4c36a9ae7df67cbf5fc469e20896fc04aecdbd8c0d`  
		Last Modified: Wed, 14 Apr 2021 19:32:20 GMT  
		Size: 50.0 MB (49953930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e5f555dac438b8e3f8740c0095114272c3bea1831249451b8f677abeda018a`  
		Last Modified: Wed, 14 Apr 2021 19:32:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-alpine`

```console
$ docker pull kong@sha256:6166bc1cca2267736253127a0c7eb7f19c3f01bfa9a29b72ad4f7199c00ce51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-alpine` - linux; amd64

```console
$ docker pull kong@sha256:e02a22193c3a09f4a424e80e193c2362b1d29f07be0c3c9d8308ef01eb5bef45
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52771040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5b7eb60cdeec3a692dfdefb1386dd9bf2d37b78757096bf1bfba22e66c45de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:27:35 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:27:35 GMT
ARG KONG_VERSION=2.0.5
# Wed, 14 Apr 2021 19:27:36 GMT
ENV KONG_VERSION=2.0.5
# Wed, 14 Apr 2021 19:27:36 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 14 Apr 2021 19:27:36 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 14 Apr 2021 19:27:49 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Wed, 14 Apr 2021 19:27:50 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:27:50 GMT
USER kong
# Wed, 14 Apr 2021 19:27:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:27:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:27:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:27:51 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eab765c4bc06602de99bfddcb851093d98720541c460033346c11ff6d67240e`  
		Last Modified: Wed, 14 Apr 2021 19:32:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013a706fa32622b36b894c4c36a9ae7df67cbf5fc469e20896fc04aecdbd8c0d`  
		Last Modified: Wed, 14 Apr 2021 19:32:20 GMT  
		Size: 50.0 MB (49953930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e5f555dac438b8e3f8740c0095114272c3bea1831249451b8f677abeda018a`  
		Last Modified: Wed, 14 Apr 2021 19:32:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-centos`

```console
$ docker pull kong@sha256:7a6ec5d8213e47be38adc4ccb0a0b6d03d0bd907f5744a64c77ec3ebab74dc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-centos` - linux; amd64

```console
$ docker pull kong@sha256:8c2de33ebbc32e8740f0a3502233a1e3f1fb047ea12feff6ed2dafe4d94d84d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127537940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e00a921b7d5673370fa7991a4ab42a344a3ea649274a23ca9a5a971ec38465`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:48 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:36:48 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:49 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:49 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 06 Mar 2021 07:36:49 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 06 Mar 2021 07:37:16 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 06 Mar 2021 07:37:16 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:37:16 GMT
USER kong
# Sat, 06 Mar 2021 07:37:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:37:17 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:37:17 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:37:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f56126da854435826e67895a0c0904e2d9192aec7b83e187b93fc9e34f9db19`  
		Last Modified: Sat, 06 Mar 2021 07:42:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372cea5912641852de535666cf1cb0204d6ab7c67e54a5bf67440f91f0017f6c`  
		Last Modified: Sat, 06 Mar 2021 07:43:01 GMT  
		Size: 51.4 MB (51439924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4813e3fe68a31d3fbca2ea4ab673b0ae50dca5f95280bc9ce89670e2346b0b80`  
		Last Modified: Sat, 06 Mar 2021 07:42:50 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-ubuntu`

```console
$ docker pull kong@sha256:9316bfc042dba24b719939734edf4a8466c719a7504517a8551bb43a33de2032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1c6b110dac9417dd91eea3f6f004c4bd784f85d6455737d1450f40c9eea35f1c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101555862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e906828b997a80eaed96e5db93649b594d7a0b6f7dd7ec73b94bdb4eca16b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:13:07 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Wed, 19 May 2021 21:13:07 GMT
ARG KONG_VERSION=2.0.5
# Wed, 19 May 2021 21:13:07 GMT
ENV KONG_VERSION=2.0.5
# Wed, 19 May 2021 21:13:27 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Wed, 19 May 2021 21:13:28 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:13:28 GMT
USER kong
# Wed, 19 May 2021 21:13:29 GMT
RUN kong version
# Wed, 19 May 2021 21:13:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:13:30 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:13:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:13:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e926417334cac9ea7a3e092369fd1fe7c64522978697082257bcd863206a83`  
		Last Modified: Wed, 19 May 2021 21:16:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6588fdc0513669307d470451335b7736cea827c9a5190ca92bb8835b45af76`  
		Last Modified: Wed, 19 May 2021 21:16:19 GMT  
		Size: 55.1 MB (55091630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78653f64c16e0f0ab1d9d713bf3c1d67e2989d09eb92e41b649eb1ae0e6d96a9`  
		Last Modified: Wed, 19 May 2021 21:16:09 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df37c4ab3867121ca6f9e5a7bfce4c35e54de078d35659e570da61cc509ec33b`  
		Last Modified: Wed, 19 May 2021 21:16:09 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:150312eec3542413e102f6d4db4d7b6eedd369a3e7dd9ee8d07a803fcf3a7a52
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93397647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e95e866299ba8d43926dbba69f93bdfa64d897e7c139c944452f901814bc88`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:43:15 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 27 May 2021 20:43:15 GMT
ARG KONG_VERSION=2.0.5
# Thu, 27 May 2021 20:43:15 GMT
ENV KONG_VERSION=2.0.5
# Thu, 27 May 2021 20:43:35 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 27 May 2021 20:43:35 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:43:35 GMT
USER kong
# Thu, 27 May 2021 20:43:36 GMT
RUN kong version
# Thu, 27 May 2021 20:43:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:43:36 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:43:37 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:43:37 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db22f7981d2858e484455e7c7e211d39a5b7f221155ea8e9e233383512032b52`  
		Last Modified: Thu, 27 May 2021 20:48:36 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d994454210ed5cc1da455370e047a132caab7611ce7a42c830f45d984fa3ce`  
		Last Modified: Thu, 27 May 2021 20:48:47 GMT  
		Size: 52.2 MB (52182744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabec8c13f1f2fa6975badb560b10ac4e73b72a539d16dd61942b18b983e4cb3`  
		Last Modified: Thu, 27 May 2021 20:48:36 GMT  
		Size: 687.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968f5174045c911115313a2247c01d459c55a5c5fb55b06272f2914fdeecd0bd`  
		Last Modified: Thu, 27 May 2021 20:48:36 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1`

```console
$ docker pull kong@sha256:0ea0ea0e794b215a76cd6f83f1f022d4c10c068fa10575670984b97b24aec01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1` - linux; amd64

```console
$ docker pull kong@sha256:a70b0d822a70ee3d7c25db678002b264d119d40f16473e2c72751dfc44e99614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53156777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c21f899167b0ca1205f6cff3de93acdf86fd7cd681a5af8d81b98b87d0efc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:27:07 GMT
ARG KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 19:27:08 GMT
ENV KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 19:27:19 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 19:27:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:27:21 GMT
USER kong
# Wed, 14 Apr 2021 19:27:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:27:21 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:27:22 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:27:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4e22f2266533339e1b987b153f17ff451eae9391bb49ccb409aea7feadda04`  
		Last Modified: Wed, 14 Apr 2021 19:31:49 GMT  
		Size: 50.3 MB (50339666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51af22022ed927dd1f66070c548e1dfdc18e4b2e077d26ebf6074568d657d055`  
		Last Modified: Wed, 14 Apr 2021 19:31:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:52f5969f41868d62b2c793918eed6591c8ade19bf9588c5fd00ea20be19c5f44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52669692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c23878f11dde433f9ba10328ebdf1a7a98f95b932211c9b34f0c81b790ce7da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:53 GMT
ARG KONG_VERSION=2.1.4
# Wed, 16 Jun 2021 01:04:53 GMT
ENV KONG_VERSION=2.1.4
# Wed, 16 Jun 2021 01:05:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 16 Jun 2021 01:05:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:05:01 GMT
USER kong
# Wed, 16 Jun 2021 01:05:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:05:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:05:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:05:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fb0a30d14a0fe836818c7883bbcb7c6671c3358567187d99105ad02e254de3`  
		Last Modified: Wed, 16 Jun 2021 01:08:07 GMT  
		Size: 49.9 MB (49941899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cfe6df0863024358cf11a143ecc336e9159469a897e17a082c1fdf1c8539ad`  
		Last Modified: Wed, 16 Jun 2021 01:07:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-alpine`

```console
$ docker pull kong@sha256:0ea0ea0e794b215a76cd6f83f1f022d4c10c068fa10575670984b97b24aec01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:a70b0d822a70ee3d7c25db678002b264d119d40f16473e2c72751dfc44e99614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53156777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c21f899167b0ca1205f6cff3de93acdf86fd7cd681a5af8d81b98b87d0efc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:27:07 GMT
ARG KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 19:27:08 GMT
ENV KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 19:27:19 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 19:27:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:27:21 GMT
USER kong
# Wed, 14 Apr 2021 19:27:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:27:21 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:27:22 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:27:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4e22f2266533339e1b987b153f17ff451eae9391bb49ccb409aea7feadda04`  
		Last Modified: Wed, 14 Apr 2021 19:31:49 GMT  
		Size: 50.3 MB (50339666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51af22022ed927dd1f66070c548e1dfdc18e4b2e077d26ebf6074568d657d055`  
		Last Modified: Wed, 14 Apr 2021 19:31:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:52f5969f41868d62b2c793918eed6591c8ade19bf9588c5fd00ea20be19c5f44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52669692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c23878f11dde433f9ba10328ebdf1a7a98f95b932211c9b34f0c81b790ce7da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:53 GMT
ARG KONG_VERSION=2.1.4
# Wed, 16 Jun 2021 01:04:53 GMT
ENV KONG_VERSION=2.1.4
# Wed, 16 Jun 2021 01:05:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 16 Jun 2021 01:05:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:05:01 GMT
USER kong
# Wed, 16 Jun 2021 01:05:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:05:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:05:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:05:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fb0a30d14a0fe836818c7883bbcb7c6671c3358567187d99105ad02e254de3`  
		Last Modified: Wed, 16 Jun 2021 01:08:07 GMT  
		Size: 49.9 MB (49941899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cfe6df0863024358cf11a143ecc336e9159469a897e17a082c1fdf1c8539ad`  
		Last Modified: Wed, 16 Jun 2021 01:07:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-centos`

```console
$ docker pull kong@sha256:77840b0da10999cf8e5f5fc40b74b9a529a4e2741bad37a4ec526ae15d3c54ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:6a9ffdeba8e9265dc75b4886b3c8f6331e6ceb4d9ca780e31b0cd540d98dc1a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127311261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcf1fde3c306e947cfc2a69e01e11d948b4be4b9890331393f37eaffc12bec1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:35:30 GMT
ARG KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:35:30 GMT
ENV KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:35:31 GMT
ARG KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
# Sat, 06 Mar 2021 07:36:02 GMT
# ARGS: KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum --nogpgcheck localinstall -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:36:02 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:03 GMT
USER kong
# Sat, 06 Mar 2021 07:36:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:03 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d58470d12b124664799e1a7498f5ab3c5c3c3e580293ff45e5d3b60b1705d4`  
		Last Modified: Sat, 06 Mar 2021 07:41:51 GMT  
		Size: 51.2 MB (51213243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8addfed624e6ff2dbb27909f1ac74b2b79dd7fec98a7bb7954075023ccfa583`  
		Last Modified: Sat, 06 Mar 2021 07:41:41 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-ubuntu`

```console
$ docker pull kong@sha256:d66d5882ba8a86bda6f0f75e1111987a618a4d8aadfd005260a5a67f7b5bd03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e879ba69a99b5262972b42eb6b2e65629e6c1f264bb16559354feb7122dc647a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139304164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e4b9cac6a96f2e0ac6d1ea1f3d0bc3acd3a30a42d2623cfc7686f8e0fefc32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:12:26 GMT
ARG KONG_VERSION=2.1.4
# Wed, 19 May 2021 21:12:26 GMT
ENV KONG_VERSION=2.1.4
# Wed, 19 May 2021 21:12:52 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:12:52 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:12:53 GMT
USER kong
# Wed, 19 May 2021 21:12:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:12:53 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:12:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:12:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0e85eb949432796454dbe7f6682b01884822426851f33c8d58a0989427c8ed`  
		Last Modified: Wed, 19 May 2021 21:15:55 GMT  
		Size: 67.8 MB (67758183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8c527523baf8db34088bc3993e331d1cf35eb4d98c53f34a85c764e031116`  
		Last Modified: Wed, 19 May 2021 21:15:43 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b9e8b2e04fd3365a6f73e5e181441de157ba61495470fc9bba407307ff9c5ff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a6deee929227b9380460c13185d3a7ee3c6811628a57912f8e5035fd3f28fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:42:38 GMT
ARG KONG_VERSION=2.1.4
# Thu, 27 May 2021 20:42:38 GMT
ENV KONG_VERSION=2.1.4
# Thu, 27 May 2021 20:43:04 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:43:05 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:43:05 GMT
USER kong
# Thu, 27 May 2021 20:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:43:06 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:43:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:43:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5122405f646f90faa360c96e5c52fd6987ca9b7ea4c1a26d692cb272437b64a6`  
		Last Modified: Thu, 27 May 2021 20:48:22 GMT  
		Size: 63.3 MB (63344474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b50ab73645187a463ac3259893277e0710531f964cf2f29b234071c1df75ef`  
		Last Modified: Thu, 27 May 2021 20:48:10 GMT  
		Size: 686.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4`

```console
$ docker pull kong@sha256:0ea0ea0e794b215a76cd6f83f1f022d4c10c068fa10575670984b97b24aec01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4` - linux; amd64

```console
$ docker pull kong@sha256:a70b0d822a70ee3d7c25db678002b264d119d40f16473e2c72751dfc44e99614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53156777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c21f899167b0ca1205f6cff3de93acdf86fd7cd681a5af8d81b98b87d0efc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:27:07 GMT
ARG KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 19:27:08 GMT
ENV KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 19:27:19 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 19:27:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:27:21 GMT
USER kong
# Wed, 14 Apr 2021 19:27:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:27:21 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:27:22 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:27:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4e22f2266533339e1b987b153f17ff451eae9391bb49ccb409aea7feadda04`  
		Last Modified: Wed, 14 Apr 2021 19:31:49 GMT  
		Size: 50.3 MB (50339666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51af22022ed927dd1f66070c548e1dfdc18e4b2e077d26ebf6074568d657d055`  
		Last Modified: Wed, 14 Apr 2021 19:31:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:52f5969f41868d62b2c793918eed6591c8ade19bf9588c5fd00ea20be19c5f44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52669692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c23878f11dde433f9ba10328ebdf1a7a98f95b932211c9b34f0c81b790ce7da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:53 GMT
ARG KONG_VERSION=2.1.4
# Wed, 16 Jun 2021 01:04:53 GMT
ENV KONG_VERSION=2.1.4
# Wed, 16 Jun 2021 01:05:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 16 Jun 2021 01:05:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:05:01 GMT
USER kong
# Wed, 16 Jun 2021 01:05:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:05:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:05:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:05:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fb0a30d14a0fe836818c7883bbcb7c6671c3358567187d99105ad02e254de3`  
		Last Modified: Wed, 16 Jun 2021 01:08:07 GMT  
		Size: 49.9 MB (49941899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cfe6df0863024358cf11a143ecc336e9159469a897e17a082c1fdf1c8539ad`  
		Last Modified: Wed, 16 Jun 2021 01:07:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-alpine`

```console
$ docker pull kong@sha256:0ea0ea0e794b215a76cd6f83f1f022d4c10c068fa10575670984b97b24aec01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:a70b0d822a70ee3d7c25db678002b264d119d40f16473e2c72751dfc44e99614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53156777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c21f899167b0ca1205f6cff3de93acdf86fd7cd681a5af8d81b98b87d0efc3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:27:07 GMT
ARG KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 19:27:08 GMT
ENV KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 19:27:19 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 19:27:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:27:21 GMT
USER kong
# Wed, 14 Apr 2021 19:27:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:27:21 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:27:22 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:27:22 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4e22f2266533339e1b987b153f17ff451eae9391bb49ccb409aea7feadda04`  
		Last Modified: Wed, 14 Apr 2021 19:31:49 GMT  
		Size: 50.3 MB (50339666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51af22022ed927dd1f66070c548e1dfdc18e4b2e077d26ebf6074568d657d055`  
		Last Modified: Wed, 14 Apr 2021 19:31:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:52f5969f41868d62b2c793918eed6591c8ade19bf9588c5fd00ea20be19c5f44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52669692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c23878f11dde433f9ba10328ebdf1a7a98f95b932211c9b34f0c81b790ce7da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:53 GMT
ARG KONG_VERSION=2.1.4
# Wed, 16 Jun 2021 01:04:53 GMT
ENV KONG_VERSION=2.1.4
# Wed, 16 Jun 2021 01:05:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 16 Jun 2021 01:05:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:05:01 GMT
USER kong
# Wed, 16 Jun 2021 01:05:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:05:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:05:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:05:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fb0a30d14a0fe836818c7883bbcb7c6671c3358567187d99105ad02e254de3`  
		Last Modified: Wed, 16 Jun 2021 01:08:07 GMT  
		Size: 49.9 MB (49941899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03cfe6df0863024358cf11a143ecc336e9159469a897e17a082c1fdf1c8539ad`  
		Last Modified: Wed, 16 Jun 2021 01:07:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-centos`

```console
$ docker pull kong@sha256:77840b0da10999cf8e5f5fc40b74b9a529a4e2741bad37a4ec526ae15d3c54ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1.4-centos` - linux; amd64

```console
$ docker pull kong@sha256:6a9ffdeba8e9265dc75b4886b3c8f6331e6ceb4d9ca780e31b0cd540d98dc1a5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127311261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcf1fde3c306e947cfc2a69e01e11d948b4be4b9890331393f37eaffc12bec1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:35:30 GMT
ARG KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:35:30 GMT
ENV KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:35:31 GMT
ARG KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
# Sat, 06 Mar 2021 07:36:02 GMT
# ARGS: KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum --nogpgcheck localinstall -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:36:02 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:03 GMT
USER kong
# Sat, 06 Mar 2021 07:36:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:03 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:03 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d58470d12b124664799e1a7498f5ab3c5c3c3e580293ff45e5d3b60b1705d4`  
		Last Modified: Sat, 06 Mar 2021 07:41:51 GMT  
		Size: 51.2 MB (51213243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8addfed624e6ff2dbb27909f1ac74b2b79dd7fec98a7bb7954075023ccfa583`  
		Last Modified: Sat, 06 Mar 2021 07:41:41 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-ubuntu`

```console
$ docker pull kong@sha256:d66d5882ba8a86bda6f0f75e1111987a618a4d8aadfd005260a5a67f7b5bd03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:e879ba69a99b5262972b42eb6b2e65629e6c1f264bb16559354feb7122dc647a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139304164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e4b9cac6a96f2e0ac6d1ea1f3d0bc3acd3a30a42d2623cfc7686f8e0fefc32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:12:26 GMT
ARG KONG_VERSION=2.1.4
# Wed, 19 May 2021 21:12:26 GMT
ENV KONG_VERSION=2.1.4
# Wed, 19 May 2021 21:12:52 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:12:52 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:12:53 GMT
USER kong
# Wed, 19 May 2021 21:12:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:12:53 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:12:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:12:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0e85eb949432796454dbe7f6682b01884822426851f33c8d58a0989427c8ed`  
		Last Modified: Wed, 19 May 2021 21:15:55 GMT  
		Size: 67.8 MB (67758183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc8c527523baf8db34088bc3993e331d1cf35eb4d98c53f34a85c764e031116`  
		Last Modified: Wed, 19 May 2021 21:15:43 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:b9e8b2e04fd3365a6f73e5e181441de157ba61495470fc9bba407307ff9c5ff5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129641108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a6deee929227b9380460c13185d3a7ee3c6811628a57912f8e5035fd3f28fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:42:38 GMT
ARG KONG_VERSION=2.1.4
# Thu, 27 May 2021 20:42:38 GMT
ENV KONG_VERSION=2.1.4
# Thu, 27 May 2021 20:43:04 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:43:05 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:43:05 GMT
USER kong
# Thu, 27 May 2021 20:43:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:43:06 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:43:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:43:06 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5122405f646f90faa360c96e5c52fd6987ca9b7ea4c1a26d692cb272437b64a6`  
		Last Modified: Thu, 27 May 2021 20:48:22 GMT  
		Size: 63.3 MB (63344474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b50ab73645187a463ac3259893277e0710531f964cf2f29b234071c1df75ef`  
		Last Modified: Thu, 27 May 2021 20:48:10 GMT  
		Size: 686.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2`

```console
$ docker pull kong@sha256:7016621ca8b246a6f0349c1bf4dfef70067b93fab2e9c012edb2ad61296be088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2` - linux; amd64

```console
$ docker pull kong@sha256:c189c2b5b83fe85f15be10bcfde65d5e4ce137d9a1ad01a012a33ba7021412b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50919689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fbb2a6cfa82fa886249da144a7bc4d95a5025901b040aa8fbf0793bb9960f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:26:37 GMT
ARG KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 19:26:37 GMT
ENV KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 19:26:37 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 19:26:38 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 19:26:38 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 19:26:38 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 19:26:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:26:52 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:53 GMT
USER kong
# Wed, 14 Apr 2021 19:26:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:54 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2679286ab43687b201a264d6a24de44bec9832f1a167ede93d4d3f3813064`  
		Last Modified: Wed, 14 Apr 2021 19:31:14 GMT  
		Size: 48.1 MB (48102578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e4629871154d10d6357b168c2a2eb341741c7ed30094a54bc8ca154f3d4aa4`  
		Last Modified: Wed, 14 Apr 2021 19:31:02 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f750bce66511300f2d662159e6cc8e10dca59fa66727d23efc5fbff555bd1543
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50439885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b1c2478ac0e790e27a78be2fa205a43ea63608a0771984849e03c4e139391c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_VERSION=2.2.2
# Wed, 16 Jun 2021 01:04:34 GMT
ENV KONG_VERSION=2.2.2
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 16 Jun 2021 01:04:34 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 16 Jun 2021 01:04:35 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 16 Jun 2021 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:42 GMT
USER kong
# Wed, 16 Jun 2021 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:42 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5150746bb6ca0aa1e3700f60f8f7c6ba8a23f78160761853b5fa96ff07e7505d`  
		Last Modified: Wed, 16 Jun 2021 01:07:37 GMT  
		Size: 47.7 MB (47712092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cb42e361325a982085eac626354555929164c6a415f1f8805451ba4a203666`  
		Last Modified: Wed, 16 Jun 2021 01:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-alpine`

```console
$ docker pull kong@sha256:7016621ca8b246a6f0349c1bf4dfef70067b93fab2e9c012edb2ad61296be088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:c189c2b5b83fe85f15be10bcfde65d5e4ce137d9a1ad01a012a33ba7021412b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50919689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fbb2a6cfa82fa886249da144a7bc4d95a5025901b040aa8fbf0793bb9960f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:26:37 GMT
ARG KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 19:26:37 GMT
ENV KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 19:26:37 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 19:26:38 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 19:26:38 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 19:26:38 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 19:26:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:26:52 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:53 GMT
USER kong
# Wed, 14 Apr 2021 19:26:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:54 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2679286ab43687b201a264d6a24de44bec9832f1a167ede93d4d3f3813064`  
		Last Modified: Wed, 14 Apr 2021 19:31:14 GMT  
		Size: 48.1 MB (48102578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e4629871154d10d6357b168c2a2eb341741c7ed30094a54bc8ca154f3d4aa4`  
		Last Modified: Wed, 14 Apr 2021 19:31:02 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f750bce66511300f2d662159e6cc8e10dca59fa66727d23efc5fbff555bd1543
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50439885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b1c2478ac0e790e27a78be2fa205a43ea63608a0771984849e03c4e139391c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_VERSION=2.2.2
# Wed, 16 Jun 2021 01:04:34 GMT
ENV KONG_VERSION=2.2.2
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 16 Jun 2021 01:04:34 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 16 Jun 2021 01:04:35 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 16 Jun 2021 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:42 GMT
USER kong
# Wed, 16 Jun 2021 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:42 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5150746bb6ca0aa1e3700f60f8f7c6ba8a23f78160761853b5fa96ff07e7505d`  
		Last Modified: Wed, 16 Jun 2021 01:07:37 GMT  
		Size: 47.7 MB (47712092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cb42e361325a982085eac626354555929164c6a415f1f8805451ba4a203666`  
		Last Modified: Wed, 16 Jun 2021 01:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-centos`

```console
$ docker pull kong@sha256:b870aaccdc0455456d5eca3f954663d8132f719c18fa2d47ee4c38673bda0a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.2-centos` - linux; amd64

```console
$ docker pull kong@sha256:b99fd6ff86818d05cee82ce71a63bdfb661693c622b27193b96750dffd562829
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127429787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f71964a13e0b5e7c5d00426038b3ddc6fd2054f7036cee00dd53c7503fe848`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:33:57 GMT
ARG KONG_VERSION=2.2.2
# Sat, 06 Mar 2021 07:33:57 GMT
ENV KONG_VERSION=2.2.2
# Sat, 06 Mar 2021 07:33:57 GMT
ARG KONG_SHA256=862e34dcfff535c795870a6a75e33586e11903e930c6119f25a207558a9b7faa
# Sat, 06 Mar 2021 07:34:44 GMT
# ARGS: KONG_SHA256=862e34dcfff535c795870a6a75e33586e11903e930c6119f25a207558a9b7faa
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:34:44 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:34:44 GMT
USER kong
# Sat, 06 Mar 2021 07:34:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:34:45 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:34:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:34:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ec7fea4bc2c9f42b92666a7ede8cf5320bad3f3056c09c33312e1b0d3b948d`  
		Last Modified: Sat, 06 Mar 2021 07:40:40 GMT  
		Size: 51.3 MB (51331768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097cf65a24bc9245c0d8fb506e5c58d9b0060bcefc75df330ae0581f5e0f76b1`  
		Last Modified: Sat, 06 Mar 2021 07:40:29 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-ubuntu`

```console
$ docker pull kong@sha256:f61bd2e1b0b41dd07382afdabb353d22bd6d30c1a47f47764e70488d6b21cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:bcb1357b29ec9bde311f2d466ed1130a262766426975b82f04318355d7317990
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139391824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743be604932febee26882b27da39f9382e22620f63befd55ea61a1d5a2a93157`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:11:45 GMT
ARG KONG_VERSION=2.2.2
# Wed, 19 May 2021 21:11:45 GMT
ENV KONG_VERSION=2.2.2
# Wed, 19 May 2021 21:12:12 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:12:13 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:12:13 GMT
USER kong
# Wed, 19 May 2021 21:12:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:12:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:12:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:12:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2906b3c85d51763b9c0946341b1794a9fd37b90a57f15023bb49acbdd7326867`  
		Last Modified: Wed, 19 May 2021 21:15:29 GMT  
		Size: 67.8 MB (67845843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ced9e460072cade3879b4bbb5caa9babd77fbda914cc693477c454aba908166`  
		Last Modified: Wed, 19 May 2021 21:15:18 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2ae49a2694fcae820e7ba5669ccd25a774259254814b4b25f69cc06a7c960dee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129778036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35487c745f892bde3d6741e7ae1c7698c412a4d9d7a930246c8c37e6cc859d69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:41:51 GMT
ARG KONG_VERSION=2.2.2
# Thu, 27 May 2021 20:41:51 GMT
ENV KONG_VERSION=2.2.2
# Thu, 27 May 2021 20:42:16 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:42:17 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:42:17 GMT
USER kong
# Thu, 27 May 2021 20:42:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:42:17 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:42:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:42:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c5adba275876eb2c0bf176de0113afd662eb7d44ced32d748a5bce28a4f426`  
		Last Modified: Thu, 27 May 2021 20:47:26 GMT  
		Size: 63.5 MB (63481400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d204a0b1ebb148f97f87c69750c9b348ebd6836d5dd2edea9463c4c16b5db2ae`  
		Last Modified: Thu, 27 May 2021 20:47:15 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2`

```console
$ docker pull kong@sha256:7016621ca8b246a6f0349c1bf4dfef70067b93fab2e9c012edb2ad61296be088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2` - linux; amd64

```console
$ docker pull kong@sha256:c189c2b5b83fe85f15be10bcfde65d5e4ce137d9a1ad01a012a33ba7021412b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50919689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fbb2a6cfa82fa886249da144a7bc4d95a5025901b040aa8fbf0793bb9960f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:26:37 GMT
ARG KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 19:26:37 GMT
ENV KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 19:26:37 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 19:26:38 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 19:26:38 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 19:26:38 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 19:26:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:26:52 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:53 GMT
USER kong
# Wed, 14 Apr 2021 19:26:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:54 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2679286ab43687b201a264d6a24de44bec9832f1a167ede93d4d3f3813064`  
		Last Modified: Wed, 14 Apr 2021 19:31:14 GMT  
		Size: 48.1 MB (48102578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e4629871154d10d6357b168c2a2eb341741c7ed30094a54bc8ca154f3d4aa4`  
		Last Modified: Wed, 14 Apr 2021 19:31:02 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f750bce66511300f2d662159e6cc8e10dca59fa66727d23efc5fbff555bd1543
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50439885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b1c2478ac0e790e27a78be2fa205a43ea63608a0771984849e03c4e139391c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_VERSION=2.2.2
# Wed, 16 Jun 2021 01:04:34 GMT
ENV KONG_VERSION=2.2.2
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 16 Jun 2021 01:04:34 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 16 Jun 2021 01:04:35 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 16 Jun 2021 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:42 GMT
USER kong
# Wed, 16 Jun 2021 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:42 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5150746bb6ca0aa1e3700f60f8f7c6ba8a23f78160761853b5fa96ff07e7505d`  
		Last Modified: Wed, 16 Jun 2021 01:07:37 GMT  
		Size: 47.7 MB (47712092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cb42e361325a982085eac626354555929164c6a415f1f8805451ba4a203666`  
		Last Modified: Wed, 16 Jun 2021 01:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2-alpine`

```console
$ docker pull kong@sha256:7016621ca8b246a6f0349c1bf4dfef70067b93fab2e9c012edb2ad61296be088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:c189c2b5b83fe85f15be10bcfde65d5e4ce137d9a1ad01a012a33ba7021412b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50919689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fbb2a6cfa82fa886249da144a7bc4d95a5025901b040aa8fbf0793bb9960f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:26:37 GMT
ARG KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 19:26:37 GMT
ENV KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 19:26:37 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 19:26:38 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 19:26:38 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 19:26:38 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 19:26:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:26:52 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:53 GMT
USER kong
# Wed, 14 Apr 2021 19:26:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:54 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de2679286ab43687b201a264d6a24de44bec9832f1a167ede93d4d3f3813064`  
		Last Modified: Wed, 14 Apr 2021 19:31:14 GMT  
		Size: 48.1 MB (48102578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e4629871154d10d6357b168c2a2eb341741c7ed30094a54bc8ca154f3d4aa4`  
		Last Modified: Wed, 14 Apr 2021 19:31:02 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:f750bce66511300f2d662159e6cc8e10dca59fa66727d23efc5fbff555bd1543
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50439885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b1c2478ac0e790e27a78be2fa205a43ea63608a0771984849e03c4e139391c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_VERSION=2.2.2
# Wed, 16 Jun 2021 01:04:34 GMT
ENV KONG_VERSION=2.2.2
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 16 Jun 2021 01:04:34 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 16 Jun 2021 01:04:34 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 16 Jun 2021 01:04:35 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 16 Jun 2021 01:04:41 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:42 GMT
USER kong
# Wed, 16 Jun 2021 01:04:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:42 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:42 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5150746bb6ca0aa1e3700f60f8f7c6ba8a23f78160761853b5fa96ff07e7505d`  
		Last Modified: Wed, 16 Jun 2021 01:07:37 GMT  
		Size: 47.7 MB (47712092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cb42e361325a982085eac626354555929164c6a415f1f8805451ba4a203666`  
		Last Modified: Wed, 16 Jun 2021 01:07:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2-centos`

```console
$ docker pull kong@sha256:b870aaccdc0455456d5eca3f954663d8132f719c18fa2d47ee4c38673bda0a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.2.2-centos` - linux; amd64

```console
$ docker pull kong@sha256:b99fd6ff86818d05cee82ce71a63bdfb661693c622b27193b96750dffd562829
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127429787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f71964a13e0b5e7c5d00426038b3ddc6fd2054f7036cee00dd53c7503fe848`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:33:57 GMT
ARG KONG_VERSION=2.2.2
# Sat, 06 Mar 2021 07:33:57 GMT
ENV KONG_VERSION=2.2.2
# Sat, 06 Mar 2021 07:33:57 GMT
ARG KONG_SHA256=862e34dcfff535c795870a6a75e33586e11903e930c6119f25a207558a9b7faa
# Sat, 06 Mar 2021 07:34:44 GMT
# ARGS: KONG_SHA256=862e34dcfff535c795870a6a75e33586e11903e930c6119f25a207558a9b7faa
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:34:44 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:34:44 GMT
USER kong
# Sat, 06 Mar 2021 07:34:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:34:45 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:34:45 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:34:45 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ec7fea4bc2c9f42b92666a7ede8cf5320bad3f3056c09c33312e1b0d3b948d`  
		Last Modified: Sat, 06 Mar 2021 07:40:40 GMT  
		Size: 51.3 MB (51331768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097cf65a24bc9245c0d8fb506e5c58d9b0060bcefc75df330ae0581f5e0f76b1`  
		Last Modified: Sat, 06 Mar 2021 07:40:29 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2-ubuntu`

```console
$ docker pull kong@sha256:f61bd2e1b0b41dd07382afdabb353d22bd6d30c1a47f47764e70488d6b21cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:bcb1357b29ec9bde311f2d466ed1130a262766426975b82f04318355d7317990
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139391824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743be604932febee26882b27da39f9382e22620f63befd55ea61a1d5a2a93157`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:11:45 GMT
ARG KONG_VERSION=2.2.2
# Wed, 19 May 2021 21:11:45 GMT
ENV KONG_VERSION=2.2.2
# Wed, 19 May 2021 21:12:12 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:12:13 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:12:13 GMT
USER kong
# Wed, 19 May 2021 21:12:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:12:14 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:12:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:12:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2906b3c85d51763b9c0946341b1794a9fd37b90a57f15023bb49acbdd7326867`  
		Last Modified: Wed, 19 May 2021 21:15:29 GMT  
		Size: 67.8 MB (67845843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ced9e460072cade3879b4bbb5caa9babd77fbda914cc693477c454aba908166`  
		Last Modified: Wed, 19 May 2021 21:15:18 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2ae49a2694fcae820e7ba5669ccd25a774259254814b4b25f69cc06a7c960dee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129778036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35487c745f892bde3d6741e7ae1c7698c412a4d9d7a930246c8c37e6cc859d69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:41:51 GMT
ARG KONG_VERSION=2.2.2
# Thu, 27 May 2021 20:41:51 GMT
ENV KONG_VERSION=2.2.2
# Thu, 27 May 2021 20:42:16 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:42:17 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:42:17 GMT
USER kong
# Thu, 27 May 2021 20:42:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:42:17 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:42:18 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:42:18 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c5adba275876eb2c0bf176de0113afd662eb7d44ced32d748a5bce28a4f426`  
		Last Modified: Thu, 27 May 2021 20:47:26 GMT  
		Size: 63.5 MB (63481400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d204a0b1ebb148f97f87c69750c9b348ebd6836d5dd2edea9463c4c16b5db2ae`  
		Last Modified: Thu, 27 May 2021 20:47:15 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3`

```console
$ docker pull kong@sha256:0c530f22b7ac433f3934af9b1fa62abd5c3210db6f84dcdd7616abc6872a92a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3` - linux; amd64

```console
$ docker pull kong@sha256:4c043482be9c513a9e73cbd8eea1e1d51d4499ac36b8c631b6bb7e23f1af6587
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50953790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeca87540c8a382cd9efbc86333e415407f3c706d2cb7cff51fe4e1b32021d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:26:10 GMT
ARG KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 19:26:10 GMT
ENV KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 19:26:10 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 19:26:10 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 19:26:11 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 19:26:11 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 19:26:20 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:26:22 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:22 GMT
USER kong
# Wed, 14 Apr 2021 19:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e5dcbae8d4557c1fb8b55e0c1b32088b6c198e5bb54d74de89e82379f731b6`  
		Last Modified: Wed, 14 Apr 2021 19:30:44 GMT  
		Size: 48.1 MB (48136680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d279652dbfcec71815816fb89de598155341301c9bcd22d0c277b96b7cce605`  
		Last Modified: Wed, 14 Apr 2021 19:30:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e9001fc7486c8740e907e27ade32ef5f6383405f4b1e176bdc0e0f77ed318a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50475811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63cc857196b0a223e8ee076d58726741bb2cf81dd1a93b1e8906e795c321100`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:15 GMT
ARG KONG_VERSION=2.3.3
# Wed, 16 Jun 2021 01:04:15 GMT
ENV KONG_VERSION=2.3.3
# Wed, 16 Jun 2021 01:04:15 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 16 Jun 2021 01:04:15 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 16 Jun 2021 01:04:16 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 16 Jun 2021 01:04:16 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 16 Jun 2021 01:04:22 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:22 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:23 GMT
USER kong
# Wed, 16 Jun 2021 01:04:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab1e863454fba348e18ea9b6c8af6fed3bc94e0afd8212ea4786b93c8668410`  
		Last Modified: Wed, 16 Jun 2021 01:07:08 GMT  
		Size: 47.7 MB (47748018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3abefba715c55480a9b0e0e1d49aacfff97f4dbe77f6b1ba9b952e1ab4add3`  
		Last Modified: Wed, 16 Jun 2021 01:06:58 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-alpine`

```console
$ docker pull kong@sha256:0c530f22b7ac433f3934af9b1fa62abd5c3210db6f84dcdd7616abc6872a92a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:4c043482be9c513a9e73cbd8eea1e1d51d4499ac36b8c631b6bb7e23f1af6587
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50953790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeca87540c8a382cd9efbc86333e415407f3c706d2cb7cff51fe4e1b32021d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:26:10 GMT
ARG KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 19:26:10 GMT
ENV KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 19:26:10 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 19:26:10 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 19:26:11 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 19:26:11 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 19:26:20 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:26:22 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:22 GMT
USER kong
# Wed, 14 Apr 2021 19:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e5dcbae8d4557c1fb8b55e0c1b32088b6c198e5bb54d74de89e82379f731b6`  
		Last Modified: Wed, 14 Apr 2021 19:30:44 GMT  
		Size: 48.1 MB (48136680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d279652dbfcec71815816fb89de598155341301c9bcd22d0c277b96b7cce605`  
		Last Modified: Wed, 14 Apr 2021 19:30:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e9001fc7486c8740e907e27ade32ef5f6383405f4b1e176bdc0e0f77ed318a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50475811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63cc857196b0a223e8ee076d58726741bb2cf81dd1a93b1e8906e795c321100`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:15 GMT
ARG KONG_VERSION=2.3.3
# Wed, 16 Jun 2021 01:04:15 GMT
ENV KONG_VERSION=2.3.3
# Wed, 16 Jun 2021 01:04:15 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 16 Jun 2021 01:04:15 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 16 Jun 2021 01:04:16 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 16 Jun 2021 01:04:16 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 16 Jun 2021 01:04:22 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:22 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:23 GMT
USER kong
# Wed, 16 Jun 2021 01:04:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab1e863454fba348e18ea9b6c8af6fed3bc94e0afd8212ea4786b93c8668410`  
		Last Modified: Wed, 16 Jun 2021 01:07:08 GMT  
		Size: 47.7 MB (47748018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3abefba715c55480a9b0e0e1d49aacfff97f4dbe77f6b1ba9b952e1ab4add3`  
		Last Modified: Wed, 16 Jun 2021 01:06:58 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-centos`

```console
$ docker pull kong@sha256:63c7a5459162f96670d69397815c3cf7966f5c4cc65feaafe07051a72e6d2da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.3-centos` - linux; amd64

```console
$ docker pull kong@sha256:7d88eecef23471ad76522ea6be93c56e9ae83de5521ddb7ecd35b9cde89bfb89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127461132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f887f3447b92aa427c43a6c8d6c128cdded951a2d6c5c5d19d441e8b863ea8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
# Sat, 06 Mar 2021 07:32:57 GMT
# ARGS: KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:32:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:32:58 GMT
USER kong
# Sat, 06 Mar 2021 07:32:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:32:59 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:32:59 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:32:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bab90e7db9fd0876a6c6ee71dff10e19542928163fd63e82acecb4f9d497a1c`  
		Last Modified: Sat, 06 Mar 2021 07:39:27 GMT  
		Size: 51.4 MB (51363113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdaad95bf8bd054cd1f7cda0a7b056bde84001412bfde25b58c0811768988ff`  
		Last Modified: Sat, 06 Mar 2021 07:39:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-ubuntu`

```console
$ docker pull kong@sha256:f94cfa0209897635b9afbbbb3bc40c2f86b5cbcf3f44305bb6dd532535b5948d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5a6fc58ce9e861da18b70267f22075c65446188846540881bcc497c22f3ec51b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139433921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fec89674ac41fbca67420963020d1519d71e458256c9fb024612fd511aa55e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:11:04 GMT
ARG KONG_VERSION=2.3.3
# Wed, 19 May 2021 21:11:04 GMT
ENV KONG_VERSION=2.3.3
# Wed, 19 May 2021 21:11:30 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:11:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:11:31 GMT
USER kong
# Wed, 19 May 2021 21:11:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:11:31 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:11:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:11:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eceb572f551ea9e8f9f181384cf6b32ee43afcafa97748ac4e7dc9d124f90835`  
		Last Modified: Wed, 19 May 2021 21:15:05 GMT  
		Size: 67.9 MB (67887940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1436965fd2748dc90f0b2dd04ac24ff13b0eb9a637595f0e15f0a69e793f636`  
		Last Modified: Wed, 19 May 2021 21:14:52 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6a6ba8cf8043b214ca5aa4f6fe7aa853ec8e8bdfc0b01a1d53681cedeb6b5bdd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129816250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b16dfeb64a7650d5524796dd28eaba9297e9af5ce5e70148d7cac8241b06d2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:40:59 GMT
ARG KONG_VERSION=2.3.3
# Thu, 27 May 2021 20:40:59 GMT
ENV KONG_VERSION=2.3.3
# Thu, 27 May 2021 20:41:25 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:41:26 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:41:26 GMT
USER kong
# Thu, 27 May 2021 20:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:41:27 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:41:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7639f63556f9c0c80723cae9efceab85b265e8875821cb79229d6bce8e5a697d`  
		Last Modified: Thu, 27 May 2021 20:46:34 GMT  
		Size: 63.5 MB (63519614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c875329d92ca0ced813bcea0eb5a50262d069b05f0f8a6464f3bc1be3d40ab`  
		Last Modified: Thu, 27 May 2021 20:46:22 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3`

```console
$ docker pull kong@sha256:0c530f22b7ac433f3934af9b1fa62abd5c3210db6f84dcdd7616abc6872a92a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3` - linux; amd64

```console
$ docker pull kong@sha256:4c043482be9c513a9e73cbd8eea1e1d51d4499ac36b8c631b6bb7e23f1af6587
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50953790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeca87540c8a382cd9efbc86333e415407f3c706d2cb7cff51fe4e1b32021d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:26:10 GMT
ARG KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 19:26:10 GMT
ENV KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 19:26:10 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 19:26:10 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 19:26:11 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 19:26:11 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 19:26:20 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:26:22 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:22 GMT
USER kong
# Wed, 14 Apr 2021 19:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e5dcbae8d4557c1fb8b55e0c1b32088b6c198e5bb54d74de89e82379f731b6`  
		Last Modified: Wed, 14 Apr 2021 19:30:44 GMT  
		Size: 48.1 MB (48136680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d279652dbfcec71815816fb89de598155341301c9bcd22d0c277b96b7cce605`  
		Last Modified: Wed, 14 Apr 2021 19:30:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e9001fc7486c8740e907e27ade32ef5f6383405f4b1e176bdc0e0f77ed318a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50475811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63cc857196b0a223e8ee076d58726741bb2cf81dd1a93b1e8906e795c321100`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:15 GMT
ARG KONG_VERSION=2.3.3
# Wed, 16 Jun 2021 01:04:15 GMT
ENV KONG_VERSION=2.3.3
# Wed, 16 Jun 2021 01:04:15 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 16 Jun 2021 01:04:15 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 16 Jun 2021 01:04:16 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 16 Jun 2021 01:04:16 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 16 Jun 2021 01:04:22 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:22 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:23 GMT
USER kong
# Wed, 16 Jun 2021 01:04:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab1e863454fba348e18ea9b6c8af6fed3bc94e0afd8212ea4786b93c8668410`  
		Last Modified: Wed, 16 Jun 2021 01:07:08 GMT  
		Size: 47.7 MB (47748018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3abefba715c55480a9b0e0e1d49aacfff97f4dbe77f6b1ba9b952e1ab4add3`  
		Last Modified: Wed, 16 Jun 2021 01:06:58 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3-alpine`

```console
$ docker pull kong@sha256:0c530f22b7ac433f3934af9b1fa62abd5c3210db6f84dcdd7616abc6872a92a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:4c043482be9c513a9e73cbd8eea1e1d51d4499ac36b8c631b6bb7e23f1af6587
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50953790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faeca87540c8a382cd9efbc86333e415407f3c706d2cb7cff51fe4e1b32021d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 19:26:10 GMT
ARG KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 19:26:10 GMT
ENV KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 19:26:10 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 19:26:10 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 19:26:11 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 19:26:11 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 19:26:20 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:26:22 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:22 GMT
USER kong
# Wed, 14 Apr 2021 19:26:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e5dcbae8d4557c1fb8b55e0c1b32088b6c198e5bb54d74de89e82379f731b6`  
		Last Modified: Wed, 14 Apr 2021 19:30:44 GMT  
		Size: 48.1 MB (48136680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d279652dbfcec71815816fb89de598155341301c9bcd22d0c277b96b7cce605`  
		Last Modified: Wed, 14 Apr 2021 19:30:35 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:73e9001fc7486c8740e907e27ade32ef5f6383405f4b1e176bdc0e0f77ed318a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50475811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b63cc857196b0a223e8ee076d58726741bb2cf81dd1a93b1e8906e795c321100`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:04:15 GMT
ARG KONG_VERSION=2.3.3
# Wed, 16 Jun 2021 01:04:15 GMT
ENV KONG_VERSION=2.3.3
# Wed, 16 Jun 2021 01:04:15 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 16 Jun 2021 01:04:15 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 16 Jun 2021 01:04:16 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 16 Jun 2021 01:04:16 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 16 Jun 2021 01:04:22 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:22 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:23 GMT
USER kong
# Wed, 16 Jun 2021 01:04:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:23 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab1e863454fba348e18ea9b6c8af6fed3bc94e0afd8212ea4786b93c8668410`  
		Last Modified: Wed, 16 Jun 2021 01:07:08 GMT  
		Size: 47.7 MB (47748018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3abefba715c55480a9b0e0e1d49aacfff97f4dbe77f6b1ba9b952e1ab4add3`  
		Last Modified: Wed, 16 Jun 2021 01:06:58 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3-centos`

```console
$ docker pull kong@sha256:63c7a5459162f96670d69397815c3cf7966f5c4cc65feaafe07051a72e6d2da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.3.3-centos` - linux; amd64

```console
$ docker pull kong@sha256:7d88eecef23471ad76522ea6be93c56e9ae83de5521ddb7ecd35b9cde89bfb89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127461132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f887f3447b92aa427c43a6c8d6c128cdded951a2d6c5c5d19d441e8b863ea8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:32:09 GMT
ARG KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
# Sat, 06 Mar 2021 07:32:57 GMT
# ARGS: KONG_SHA256=d81c550921c8e980f7f4e078504a55a774f016c0a572db8153e03027df29f111
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:32:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:32:58 GMT
USER kong
# Sat, 06 Mar 2021 07:32:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:32:59 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:32:59 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:32:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bab90e7db9fd0876a6c6ee71dff10e19542928163fd63e82acecb4f9d497a1c`  
		Last Modified: Sat, 06 Mar 2021 07:39:27 GMT  
		Size: 51.4 MB (51363113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdaad95bf8bd054cd1f7cda0a7b056bde84001412bfde25b58c0811768988ff`  
		Last Modified: Sat, 06 Mar 2021 07:39:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3-ubuntu`

```console
$ docker pull kong@sha256:f94cfa0209897635b9afbbbb3bc40c2f86b5cbcf3f44305bb6dd532535b5948d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5a6fc58ce9e861da18b70267f22075c65446188846540881bcc497c22f3ec51b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139433921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fec89674ac41fbca67420963020d1519d71e458256c9fb024612fd511aa55e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:11:04 GMT
ARG KONG_VERSION=2.3.3
# Wed, 19 May 2021 21:11:04 GMT
ENV KONG_VERSION=2.3.3
# Wed, 19 May 2021 21:11:30 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:11:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:11:31 GMT
USER kong
# Wed, 19 May 2021 21:11:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:11:31 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:11:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:11:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eceb572f551ea9e8f9f181384cf6b32ee43afcafa97748ac4e7dc9d124f90835`  
		Last Modified: Wed, 19 May 2021 21:15:05 GMT  
		Size: 67.9 MB (67887940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1436965fd2748dc90f0b2dd04ac24ff13b0eb9a637595f0e15f0a69e793f636`  
		Last Modified: Wed, 19 May 2021 21:14:52 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6a6ba8cf8043b214ca5aa4f6fe7aa853ec8e8bdfc0b01a1d53681cedeb6b5bdd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129816250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b16dfeb64a7650d5524796dd28eaba9297e9af5ce5e70148d7cac8241b06d2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:40:59 GMT
ARG KONG_VERSION=2.3.3
# Thu, 27 May 2021 20:40:59 GMT
ENV KONG_VERSION=2.3.3
# Thu, 27 May 2021 20:41:25 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:41:26 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:41:26 GMT
USER kong
# Thu, 27 May 2021 20:41:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:41:27 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:41:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7639f63556f9c0c80723cae9efceab85b265e8875821cb79229d6bce8e5a697d`  
		Last Modified: Thu, 27 May 2021 20:46:34 GMT  
		Size: 63.5 MB (63519614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c875329d92ca0ced813bcea0eb5a50262d069b05f0f8a6464f3bc1be3d40ab`  
		Last Modified: Thu, 27 May 2021 20:46:22 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4`

```console
$ docker pull kong@sha256:c9872460e6c9cb05d5ac1f125fff571c00541d4da7438f5eb821e07a56efe752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4` - linux; amd64

```console
$ docker pull kong@sha256:31e0abee64747a4a31159b4d41538a03d9cbf7bfbe9708e00d5703aa9ce5f2b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51160610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b022e820b9b2bb6de4b8d0a3f8d50702612ef93ab70a2a108c020bac31b4f02a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:48 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 11 May 2021 22:29:49 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:29:49 GMT
USER kong
# Tue, 11 May 2021 22:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:29:49 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:29:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:29:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04308f3534771e4911ece45118ea51db7d9a992c72336fb9c1165a8fe3ca894e`  
		Last Modified: Tue, 11 May 2021 22:33:23 GMT  
		Size: 48.3 MB (48343499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af5626bb095a631ee85ddaae2c1bc71dd4085dfd56e149ba5f34fbe3a71cd05`  
		Last Modified: Tue, 11 May 2021 22:33:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a350bd912a622a02b61e9c5b6b20c5e3365f5544407ee1b8b4c63e9a8f0bdec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50694302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e44d048d3428713b1443578b223a2833de190e4e9adcd22a618d1fba72fd1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:03:52 GMT
ARG KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:04:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:01 GMT
USER kong
# Wed, 16 Jun 2021 01:04:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4661998cf20ee5e8dc00d8c36cc7bac6fb43f2c86ea1c68d7ed96e3698b15`  
		Last Modified: Wed, 16 Jun 2021 01:06:27 GMT  
		Size: 48.0 MB (47966509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afbf6dc6d0b33bda49d4eeb05932798f55369bdb1969730abc0ac73fd9f0e4`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-alpine`

```console
$ docker pull kong@sha256:c9872460e6c9cb05d5ac1f125fff571c00541d4da7438f5eb821e07a56efe752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:31e0abee64747a4a31159b4d41538a03d9cbf7bfbe9708e00d5703aa9ce5f2b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51160610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b022e820b9b2bb6de4b8d0a3f8d50702612ef93ab70a2a108c020bac31b4f02a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:48 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 11 May 2021 22:29:49 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:29:49 GMT
USER kong
# Tue, 11 May 2021 22:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:29:49 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:29:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:29:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04308f3534771e4911ece45118ea51db7d9a992c72336fb9c1165a8fe3ca894e`  
		Last Modified: Tue, 11 May 2021 22:33:23 GMT  
		Size: 48.3 MB (48343499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af5626bb095a631ee85ddaae2c1bc71dd4085dfd56e149ba5f34fbe3a71cd05`  
		Last Modified: Tue, 11 May 2021 22:33:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a350bd912a622a02b61e9c5b6b20c5e3365f5544407ee1b8b4c63e9a8f0bdec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50694302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e44d048d3428713b1443578b223a2833de190e4e9adcd22a618d1fba72fd1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:03:52 GMT
ARG KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:04:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:01 GMT
USER kong
# Wed, 16 Jun 2021 01:04:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4661998cf20ee5e8dc00d8c36cc7bac6fb43f2c86ea1c68d7ed96e3698b15`  
		Last Modified: Wed, 16 Jun 2021 01:06:27 GMT  
		Size: 48.0 MB (47966509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afbf6dc6d0b33bda49d4eeb05932798f55369bdb1969730abc0ac73fd9f0e4`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-centos`

```console
$ docker pull kong@sha256:af3b555aafa9057bf0cb66f7257fa5748e328a92cc8324ad5b9de004745bbfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.4-centos` - linux; amd64

```console
$ docker pull kong@sha256:f67758723288bacee4b1a20c4afdad985bd6b338e5d5325a3adf77808c85a593
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127648547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24b1346db87f019dfe4a9929b3e4cde9a8d943f5b7976063dd21e6b3124787a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Tue, 11 May 2021 22:31:19 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:31:19 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:31:19 GMT
ARG KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
# Tue, 11 May 2021 22:31:51 GMT
# ARGS: KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then   curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Tue, 11 May 2021 22:31:52 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:31:52 GMT
USER kong
# Tue, 11 May 2021 22:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:31:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:31:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:31:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab966ea217fbab8c5192165645951c189bf30a8e7646590426a6d246564c324`  
		Last Modified: Tue, 11 May 2021 22:34:20 GMT  
		Size: 51.6 MB (51550529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4193596ed9cb1305f2d4c3fee914eee8727f30d3a96e36fe7f182bd5166de03b`  
		Last Modified: Tue, 11 May 2021 22:34:11 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-ubuntu`

```console
$ docker pull kong@sha256:14542b141a705483dddcc6f0eb9449bdbe1cc2714e2bb1d66dd8e6fdd77e9965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:21ca915f309f364e5ff5e1f9d2edaeff9eb19c5768b3ffbab2cc3311300bbe4c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139618284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3850c98bbfb5eb79f99f0c303aa16b44f4ebb4452a574c7b5c74ad010ca81b90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:10:23 GMT
ARG KONG_VERSION=2.4.1
# Wed, 19 May 2021 21:10:23 GMT
ENV KONG_VERSION=2.4.1
# Wed, 19 May 2021 21:10:52 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:10:53 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:10:53 GMT
USER kong
# Wed, 19 May 2021 21:10:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:10:54 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:10:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:10:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f9067a64751b93c660c5e8b46a054d9810743dbf9c38e7c62c0dbc5c2ee8e4`  
		Last Modified: Wed, 19 May 2021 21:14:36 GMT  
		Size: 68.1 MB (68072303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cae426332dcd3ec9ca6bd61a512c2157cb51dbe4fbb5eeb8ae451c05b0d6e0`  
		Last Modified: Wed, 19 May 2021 21:14:24 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e44056c06a3f50632c15adf1078bb005ecd3f3c20b8245d0fa239b90c2e178f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129962210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b237004f52ceb2de7c6167ed40055d47925da2d73ec5f618ed97e7cd9872b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:40:07 GMT
ARG KONG_VERSION=2.4.1
# Thu, 27 May 2021 20:40:07 GMT
ENV KONG_VERSION=2.4.1
# Thu, 27 May 2021 20:40:33 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:40:34 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:40:34 GMT
USER kong
# Thu, 27 May 2021 20:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:40:34 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:40:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e06679b2ae9cf23f51b8ceea4d7b2beb045963a724289ca2c70b548840c6972`  
		Last Modified: Thu, 27 May 2021 20:45:38 GMT  
		Size: 63.7 MB (63665573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeeb9eb72768ba059fc31ec6033f2ade98ed22597d4e28bb70230d835041e20`  
		Last Modified: Thu, 27 May 2021 20:45:26 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.1`

```console
$ docker pull kong@sha256:c9872460e6c9cb05d5ac1f125fff571c00541d4da7438f5eb821e07a56efe752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.1` - linux; amd64

```console
$ docker pull kong@sha256:31e0abee64747a4a31159b4d41538a03d9cbf7bfbe9708e00d5703aa9ce5f2b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51160610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b022e820b9b2bb6de4b8d0a3f8d50702612ef93ab70a2a108c020bac31b4f02a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:48 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 11 May 2021 22:29:49 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:29:49 GMT
USER kong
# Tue, 11 May 2021 22:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:29:49 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:29:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:29:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04308f3534771e4911ece45118ea51db7d9a992c72336fb9c1165a8fe3ca894e`  
		Last Modified: Tue, 11 May 2021 22:33:23 GMT  
		Size: 48.3 MB (48343499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af5626bb095a631ee85ddaae2c1bc71dd4085dfd56e149ba5f34fbe3a71cd05`  
		Last Modified: Tue, 11 May 2021 22:33:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a350bd912a622a02b61e9c5b6b20c5e3365f5544407ee1b8b4c63e9a8f0bdec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50694302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e44d048d3428713b1443578b223a2833de190e4e9adcd22a618d1fba72fd1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:03:52 GMT
ARG KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:04:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:01 GMT
USER kong
# Wed, 16 Jun 2021 01:04:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4661998cf20ee5e8dc00d8c36cc7bac6fb43f2c86ea1c68d7ed96e3698b15`  
		Last Modified: Wed, 16 Jun 2021 01:06:27 GMT  
		Size: 48.0 MB (47966509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afbf6dc6d0b33bda49d4eeb05932798f55369bdb1969730abc0ac73fd9f0e4`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.1-alpine`

```console
$ docker pull kong@sha256:c9872460e6c9cb05d5ac1f125fff571c00541d4da7438f5eb821e07a56efe752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:31e0abee64747a4a31159b4d41538a03d9cbf7bfbe9708e00d5703aa9ce5f2b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51160610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b022e820b9b2bb6de4b8d0a3f8d50702612ef93ab70a2a108c020bac31b4f02a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:48 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 11 May 2021 22:29:49 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:29:49 GMT
USER kong
# Tue, 11 May 2021 22:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:29:49 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:29:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:29:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04308f3534771e4911ece45118ea51db7d9a992c72336fb9c1165a8fe3ca894e`  
		Last Modified: Tue, 11 May 2021 22:33:23 GMT  
		Size: 48.3 MB (48343499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af5626bb095a631ee85ddaae2c1bc71dd4085dfd56e149ba5f34fbe3a71cd05`  
		Last Modified: Tue, 11 May 2021 22:33:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a350bd912a622a02b61e9c5b6b20c5e3365f5544407ee1b8b4c63e9a8f0bdec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50694302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e44d048d3428713b1443578b223a2833de190e4e9adcd22a618d1fba72fd1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:03:52 GMT
ARG KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:04:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:01 GMT
USER kong
# Wed, 16 Jun 2021 01:04:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4661998cf20ee5e8dc00d8c36cc7bac6fb43f2c86ea1c68d7ed96e3698b15`  
		Last Modified: Wed, 16 Jun 2021 01:06:27 GMT  
		Size: 48.0 MB (47966509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afbf6dc6d0b33bda49d4eeb05932798f55369bdb1969730abc0ac73fd9f0e4`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.1-centos`

```console
$ docker pull kong@sha256:af3b555aafa9057bf0cb66f7257fa5748e328a92cc8324ad5b9de004745bbfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.4.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:f67758723288bacee4b1a20c4afdad985bd6b338e5d5325a3adf77808c85a593
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127648547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24b1346db87f019dfe4a9929b3e4cde9a8d943f5b7976063dd21e6b3124787a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Tue, 11 May 2021 22:31:19 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:31:19 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:31:19 GMT
ARG KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
# Tue, 11 May 2021 22:31:51 GMT
# ARGS: KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then   curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Tue, 11 May 2021 22:31:52 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:31:52 GMT
USER kong
# Tue, 11 May 2021 22:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:31:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:31:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:31:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab966ea217fbab8c5192165645951c189bf30a8e7646590426a6d246564c324`  
		Last Modified: Tue, 11 May 2021 22:34:20 GMT  
		Size: 51.6 MB (51550529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4193596ed9cb1305f2d4c3fee914eee8727f30d3a96e36fe7f182bd5166de03b`  
		Last Modified: Tue, 11 May 2021 22:34:11 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.1-ubuntu`

```console
$ docker pull kong@sha256:14542b141a705483dddcc6f0eb9449bdbe1cc2714e2bb1d66dd8e6fdd77e9965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:21ca915f309f364e5ff5e1f9d2edaeff9eb19c5768b3ffbab2cc3311300bbe4c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139618284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3850c98bbfb5eb79f99f0c303aa16b44f4ebb4452a574c7b5c74ad010ca81b90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:10:23 GMT
ARG KONG_VERSION=2.4.1
# Wed, 19 May 2021 21:10:23 GMT
ENV KONG_VERSION=2.4.1
# Wed, 19 May 2021 21:10:52 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:10:53 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:10:53 GMT
USER kong
# Wed, 19 May 2021 21:10:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:10:54 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:10:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:10:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f9067a64751b93c660c5e8b46a054d9810743dbf9c38e7c62c0dbc5c2ee8e4`  
		Last Modified: Wed, 19 May 2021 21:14:36 GMT  
		Size: 68.1 MB (68072303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cae426332dcd3ec9ca6bd61a512c2157cb51dbe4fbb5eeb8ae451c05b0d6e0`  
		Last Modified: Wed, 19 May 2021 21:14:24 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e44056c06a3f50632c15adf1078bb005ecd3f3c20b8245d0fa239b90c2e178f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129962210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b237004f52ceb2de7c6167ed40055d47925da2d73ec5f618ed97e7cd9872b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:40:07 GMT
ARG KONG_VERSION=2.4.1
# Thu, 27 May 2021 20:40:07 GMT
ENV KONG_VERSION=2.4.1
# Thu, 27 May 2021 20:40:33 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:40:34 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:40:34 GMT
USER kong
# Thu, 27 May 2021 20:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:40:34 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:40:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e06679b2ae9cf23f51b8ceea4d7b2beb045963a724289ca2c70b548840c6972`  
		Last Modified: Thu, 27 May 2021 20:45:38 GMT  
		Size: 63.7 MB (63665573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeeb9eb72768ba059fc31ec6033f2ade98ed22597d4e28bb70230d835041e20`  
		Last Modified: Thu, 27 May 2021 20:45:26 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:c9872460e6c9cb05d5ac1f125fff571c00541d4da7438f5eb821e07a56efe752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:31e0abee64747a4a31159b4d41538a03d9cbf7bfbe9708e00d5703aa9ce5f2b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51160610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b022e820b9b2bb6de4b8d0a3f8d50702612ef93ab70a2a108c020bac31b4f02a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:48 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 11 May 2021 22:29:49 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:29:49 GMT
USER kong
# Tue, 11 May 2021 22:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:29:49 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:29:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:29:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04308f3534771e4911ece45118ea51db7d9a992c72336fb9c1165a8fe3ca894e`  
		Last Modified: Tue, 11 May 2021 22:33:23 GMT  
		Size: 48.3 MB (48343499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af5626bb095a631ee85ddaae2c1bc71dd4085dfd56e149ba5f34fbe3a71cd05`  
		Last Modified: Tue, 11 May 2021 22:33:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a350bd912a622a02b61e9c5b6b20c5e3365f5544407ee1b8b4c63e9a8f0bdec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50694302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e44d048d3428713b1443578b223a2833de190e4e9adcd22a618d1fba72fd1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:03:52 GMT
ARG KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:04:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:01 GMT
USER kong
# Wed, 16 Jun 2021 01:04:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4661998cf20ee5e8dc00d8c36cc7bac6fb43f2c86ea1c68d7ed96e3698b15`  
		Last Modified: Wed, 16 Jun 2021 01:06:27 GMT  
		Size: 48.0 MB (47966509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afbf6dc6d0b33bda49d4eeb05932798f55369bdb1969730abc0ac73fd9f0e4`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:centos`

```console
$ docker pull kong@sha256:af3b555aafa9057bf0cb66f7257fa5748e328a92cc8324ad5b9de004745bbfbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:f67758723288bacee4b1a20c4afdad985bd6b338e5d5325a3adf77808c85a593
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127648547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24b1346db87f019dfe4a9929b3e4cde9a8d943f5b7976063dd21e6b3124787a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:32:08 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:32:08 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:32:08 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:32:08 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Tue, 11 May 2021 22:31:19 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:31:19 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:31:19 GMT
ARG KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
# Tue, 11 May 2021 22:31:51 GMT
# ARGS: KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then   curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Tue, 11 May 2021 22:31:52 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:31:52 GMT
USER kong
# Tue, 11 May 2021 22:31:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:31:52 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:31:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:31:53 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c237ce1272ffe51f7f4a890afaca88db75cb107611ffb1833c9dbd5161df8157`  
		Last Modified: Sat, 06 Mar 2021 07:39:18 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab966ea217fbab8c5192165645951c189bf30a8e7646590426a6d246564c324`  
		Last Modified: Tue, 11 May 2021 22:34:20 GMT  
		Size: 51.6 MB (51550529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4193596ed9cb1305f2d4c3fee914eee8727f30d3a96e36fe7f182bd5166de03b`  
		Last Modified: Tue, 11 May 2021 22:34:11 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:c9872460e6c9cb05d5ac1f125fff571c00541d4da7438f5eb821e07a56efe752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:31e0abee64747a4a31159b4d41538a03d9cbf7bfbe9708e00d5703aa9ce5f2b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51160610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b022e820b9b2bb6de4b8d0a3f8d50702612ef93ab70a2a108c020bac31b4f02a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:23:21 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 19:23:21 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 19:23:21 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 19:23:22 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 19:23:22 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_VERSION=2.4.1
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Tue, 11 May 2021 22:29:40 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:40 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Tue, 11 May 2021 22:29:48 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 11 May 2021 22:29:49 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 11 May 2021 22:29:49 GMT
USER kong
# Tue, 11 May 2021 22:29:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 May 2021 22:29:49 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 11 May 2021 22:29:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 May 2021 22:29:50 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472b23dfb901e3b9a325bd2956bf0a230c603b44b559b671f46090712feaa25`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04308f3534771e4911ece45118ea51db7d9a992c72336fb9c1165a8fe3ca894e`  
		Last Modified: Tue, 11 May 2021 22:33:23 GMT  
		Size: 48.3 MB (48343499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af5626bb095a631ee85ddaae2c1bc71dd4085dfd56e149ba5f34fbe3a71cd05`  
		Last Modified: Tue, 11 May 2021 22:33:15 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a350bd912a622a02b61e9c5b6b20c5e3365f5544407ee1b8b4c63e9a8f0bdec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50694302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e44d048d3428713b1443578b223a2833de190e4e9adcd22a618d1fba72fd1e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 01:03:52 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 16 Jun 2021 01:03:52 GMT
ARG ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ENV ASSET=ce
# Wed, 16 Jun 2021 01:03:52 GMT
ARG EE_PORTS
# Wed, 16 Jun 2021 01:03:52 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 16 Jun 2021 01:03:52 GMT
ARG KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_VERSION=2.4.1
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Wed, 16 Jun 2021 01:03:53 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:03:53 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Wed, 16 Jun 2021 01:04:00 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 16 Jun 2021 01:04:01 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 16 Jun 2021 01:04:01 GMT
USER kong
# Wed, 16 Jun 2021 01:04:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Jun 2021 01:04:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 16 Jun 2021 01:04:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Jun 2021 01:04:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68089cee6c0f6ef8dd053c9f3b7d70c11dda2c426bf38daac971441a912c9bf0`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc4661998cf20ee5e8dc00d8c36cc7bac6fb43f2c86ea1c68d7ed96e3698b15`  
		Last Modified: Wed, 16 Jun 2021 01:06:27 GMT  
		Size: 48.0 MB (47966509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afbf6dc6d0b33bda49d4eeb05932798f55369bdb1969730abc0ac73fd9f0e4`  
		Last Modified: Wed, 16 Jun 2021 01:06:17 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:14542b141a705483dddcc6f0eb9449bdbe1cc2714e2bb1d66dd8e6fdd77e9965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:21ca915f309f364e5ff5e1f9d2edaeff9eb19c5768b3ffbab2cc3311300bbe4c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139618284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3850c98bbfb5eb79f99f0c303aa16b44f4ebb4452a574c7b5c74ad010ca81b90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 19 May 2021 19:45:15 GMT
ADD file:5dd161b04353d3cbc2b258d66ef3c79a8307faa944953a1c7920a3d97468520c in / 
# Wed, 19 May 2021 19:45:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:45:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 19:45:18 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:45:19 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 21:10:22 GMT
ARG ASSET=ce
# Wed, 19 May 2021 21:10:22 GMT
ENV ASSET=ce
# Wed, 19 May 2021 21:10:23 GMT
ARG EE_PORTS
# Wed, 19 May 2021 21:10:23 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 19 May 2021 21:10:23 GMT
ARG KONG_VERSION=2.4.1
# Wed, 19 May 2021 21:10:23 GMT
ENV KONG_VERSION=2.4.1
# Wed, 19 May 2021 21:10:52 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 19 May 2021 21:10:53 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 19 May 2021 21:10:53 GMT
USER kong
# Wed, 19 May 2021 21:10:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 19 May 2021 21:10:54 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 19 May 2021 21:10:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 19 May 2021 21:10:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:80bce60046fa9e5ccbe54c9bd4bfa3f379ce7bc43bed493ae92389050de04024`  
		Last Modified: Thu, 29 Apr 2021 15:24:23 GMT  
		Size: 46.5 MB (46461779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a738a1554069bc9050c0a60b57fc93e98069e59822677a483cc74cafaf2bf7`  
		Last Modified: Wed, 19 May 2021 19:46:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19cf0706c6229033d11dbf952b3eb96ad70e1f32527960aeb3c83ad86f16551`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4cdd6c27d1f17cf5ff350e76b7efe80aceff4dc99fd518065bf048abd6494a`  
		Last Modified: Wed, 19 May 2021 19:46:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d3c8daaad6d13ef4bf576ce9208152535e4bb46b3a9e3f074d4fd696a164e4`  
		Last Modified: Wed, 19 May 2021 21:14:26 GMT  
		Size: 25.1 MB (25081966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f9067a64751b93c660c5e8b46a054d9810743dbf9c38e7c62c0dbc5c2ee8e4`  
		Last Modified: Wed, 19 May 2021 21:14:36 GMT  
		Size: 68.1 MB (68072303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cae426332dcd3ec9ca6bd61a512c2157cb51dbe4fbb5eeb8ae451c05b0d6e0`  
		Last Modified: Wed, 19 May 2021 21:14:24 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1e44056c06a3f50632c15adf1078bb005ecd3f3c20b8245d0fa239b90c2e178f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129962210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77b237004f52ceb2de7c6167ed40055d47925da2d73ec5f618ed97e7cd9872b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 27 May 2021 12:30:43 GMT
ADD file:9417aaf175748bf02265b3fcffc4955c5521d4d51793d599f33e48b7960e453e in / 
# Thu, 27 May 2021 12:30:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:45 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 12:30:46 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:46 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 20:40:06 GMT
ARG ASSET=ce
# Thu, 27 May 2021 20:40:06 GMT
ENV ASSET=ce
# Thu, 27 May 2021 20:40:07 GMT
ARG EE_PORTS
# Thu, 27 May 2021 20:40:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 27 May 2021 20:40:07 GMT
ARG KONG_VERSION=2.4.1
# Thu, 27 May 2021 20:40:07 GMT
ENV KONG_VERSION=2.4.1
# Thu, 27 May 2021 20:40:33 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 27 May 2021 20:40:34 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 27 May 2021 20:40:34 GMT
USER kong
# Thu, 27 May 2021 20:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 27 May 2021 20:40:34 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 27 May 2021 20:40:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 May 2021 20:40:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58be9ce6be6955598846443a55535df82ab8b8489d8a09eb959abd45a368503b`  
		Last Modified: Thu, 29 Apr 2021 08:25:11 GMT  
		Size: 41.2 MB (41212503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2536079c067c30e81c2fd80224355786c22f125638814e45caa9357de3b332b`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1407aa15569186ac220ed788ef58c2821961717f50af3355e9302617acddbfb`  
		Last Modified: Thu, 27 May 2021 12:33:42 GMT  
		Size: 471.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566efc3b50d0a162192bf9a472fe8ff4e3d7be9791f42b800f9475188301ecac`  
		Last Modified: Thu, 27 May 2021 12:33:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daaa1e99fdca50cd282dfb8cc289f5d81eb903a74599492defe4181c10b311a`  
		Last Modified: Thu, 27 May 2021 20:45:28 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e06679b2ae9cf23f51b8ceea4d7b2beb045963a724289ca2c70b548840c6972`  
		Last Modified: Thu, 27 May 2021 20:45:38 GMT  
		Size: 63.7 MB (63665573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeeb9eb72768ba059fc31ec6033f2ade98ed22597d4e28bb70230d835041e20`  
		Last Modified: Thu, 27 May 2021 20:45:26 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
