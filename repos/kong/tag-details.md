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
-	[`kong:2.4.0`](#kong240)
-	[`kong:2.4.0-alpine`](#kong240-alpine)
-	[`kong:2.4.0-centos`](#kong240-centos)
-	[`kong:2.4.0-ubuntu`](#kong240-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:centos`](#kongcentos)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2`

```console
$ docker pull kong@sha256:91e8a6689f3c5c522dabbae93d5cc5006da9931ab3e325de2c944ba87622e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:0372a0a05c5a4066cbfa1836766d6726edd55a4e3e1ee3a962c85c517a137339
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51157442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e950e221f43ed7989260b2a61accb568d9d3cdd7df13c9a42f4edd83329851`
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
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:38 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:23:39 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:39 GMT
USER kong
# Wed, 14 Apr 2021 19:23:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:23:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:23:41 GMT
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
	-	`sha256:cc91e546b96c68aa68775d1e466977f5340f41446ca8722944a19c714306e48b`  
		Last Modified: Wed, 14 Apr 2021 19:29:15 GMT  
		Size: 48.3 MB (48340332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b835101a2100b139d649deb78fbeeec2a8efd295f076021c79fc15e733fbeaaa`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2fb2782ecc0a030b096d909c23b05b82ece464b5db82d214ada47cd5f6927448
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50688463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b697428de94c2f258b89f87fbae0df5a5a01c8e3853c5446dede9bbfb89ff06b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:26:29 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:30 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:31 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:31 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:32 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:33 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:45 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:26:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:26:49 GMT
USER kong
# Wed, 14 Apr 2021 23:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:26:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:26:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f621485fe99632d7e0c3b4a5f9d900b0f7084270bc696b8697bf72c0203f3b`  
		Last Modified: Wed, 14 Apr 2021 23:32:27 GMT  
		Size: 48.0 MB (47960669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150e2e25f3f7a98718567a47d1429faf8d204b3229779965970dc1f86a69ea3`  
		Last Modified: Wed, 14 Apr 2021 23:32:04 GMT  
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
$ docker pull kong@sha256:7f02c62e1884da1d052fb6395936e3b79cc5266777366d75ea779a8aa41d8e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b55166f4cc463278122c2839ea74b6e3426d3ef7dfb3c9c3ec31f642bec3ee0e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101348400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8fe9773c51e6b9a588528206e1d50cd05ef64233cf1fab8e56a16ed9cdc37b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:44:13 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:44:13 GMT
ARG KONG_VERSION=2.0.5
# Fri, 23 Apr 2021 23:44:13 GMT
ENV KONG_VERSION=2.0.5
# Fri, 23 Apr 2021 23:44:30 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Fri, 23 Apr 2021 23:44:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:44:31 GMT
USER kong
# Fri, 23 Apr 2021 23:44:32 GMT
RUN kong version
# Fri, 23 Apr 2021 23:44:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:44:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:44:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242df1854d2c84ffee2f845a0ce498d08732eab0246beea68b89f5b9f2c8582b`  
		Last Modified: Fri, 23 Apr 2021 23:47:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6f365ec05d65c81f104b73cdc115829ba593c90e8fcff6f37a4bf87abf82d`  
		Last Modified: Fri, 23 Apr 2021 23:47:52 GMT  
		Size: 55.1 MB (55091492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77536820457082de917364a9f4d2d52f7c50bb4ef51a4b4c3f00801c2d517c28`  
		Last Modified: Fri, 23 Apr 2021 23:47:37 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aebdc7875ba3a8834064e3e8fca9c624234814aeba71e65401997ac50803dfd`  
		Last Modified: Fri, 23 Apr 2021 23:47:37 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1dc5372d03c840ff335b5703c079a4b4b39098a0b89d7084409eb17d5a8e5d63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93211319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c911a540c2ecd8be80bdbaae2e3a696acd59f3a676b578a3d2d562159a3ec2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:28:10 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:28:11 GMT
ARG KONG_VERSION=2.0.5
# Fri, 23 Apr 2021 23:28:12 GMT
ENV KONG_VERSION=2.0.5
# Fri, 23 Apr 2021 23:28:53 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Fri, 23 Apr 2021 23:28:56 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:28:57 GMT
USER kong
# Fri, 23 Apr 2021 23:28:59 GMT
RUN kong version
# Fri, 23 Apr 2021 23:29:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:29:01 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:29:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:29:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b27fac971ef733384650e6c9ada90cb408ccd8eb656a7935fc5d1c7c7eeb7d`  
		Last Modified: Fri, 23 Apr 2021 23:31:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044162ca9d8f9fab91ae25a14cd772432e503ea1fdbc23f20cd409ead3cb9523`  
		Last Modified: Fri, 23 Apr 2021 23:32:03 GMT  
		Size: 52.2 MB (52182166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5f2df82b25d1a8c9a90ce1c4aabf541775b149b95bd3cdf201f01eb93a7bb9`  
		Last Modified: Fri, 23 Apr 2021 23:31:47 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2829f71ad2e81aa38caecfa924aeaed770273ef966f9f09930566029537c280c`  
		Last Modified: Fri, 23 Apr 2021 23:31:47 GMT  
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
$ docker pull kong@sha256:7f02c62e1884da1d052fb6395936e3b79cc5266777366d75ea779a8aa41d8e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b55166f4cc463278122c2839ea74b6e3426d3ef7dfb3c9c3ec31f642bec3ee0e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101348400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8fe9773c51e6b9a588528206e1d50cd05ef64233cf1fab8e56a16ed9cdc37b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:44:13 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:44:13 GMT
ARG KONG_VERSION=2.0.5
# Fri, 23 Apr 2021 23:44:13 GMT
ENV KONG_VERSION=2.0.5
# Fri, 23 Apr 2021 23:44:30 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Fri, 23 Apr 2021 23:44:31 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:44:31 GMT
USER kong
# Fri, 23 Apr 2021 23:44:32 GMT
RUN kong version
# Fri, 23 Apr 2021 23:44:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:44:33 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:44:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:44:33 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242df1854d2c84ffee2f845a0ce498d08732eab0246beea68b89f5b9f2c8582b`  
		Last Modified: Fri, 23 Apr 2021 23:47:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6f365ec05d65c81f104b73cdc115829ba593c90e8fcff6f37a4bf87abf82d`  
		Last Modified: Fri, 23 Apr 2021 23:47:52 GMT  
		Size: 55.1 MB (55091492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77536820457082de917364a9f4d2d52f7c50bb4ef51a4b4c3f00801c2d517c28`  
		Last Modified: Fri, 23 Apr 2021 23:47:37 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aebdc7875ba3a8834064e3e8fca9c624234814aeba71e65401997ac50803dfd`  
		Last Modified: Fri, 23 Apr 2021 23:47:37 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1dc5372d03c840ff335b5703c079a4b4b39098a0b89d7084409eb17d5a8e5d63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93211319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c911a540c2ecd8be80bdbaae2e3a696acd59f3a676b578a3d2d562159a3ec2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:28:10 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:28:11 GMT
ARG KONG_VERSION=2.0.5
# Fri, 23 Apr 2021 23:28:12 GMT
ENV KONG_VERSION=2.0.5
# Fri, 23 Apr 2021 23:28:53 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Fri, 23 Apr 2021 23:28:56 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:28:57 GMT
USER kong
# Fri, 23 Apr 2021 23:28:59 GMT
RUN kong version
# Fri, 23 Apr 2021 23:29:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:29:01 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:29:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:29:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b27fac971ef733384650e6c9ada90cb408ccd8eb656a7935fc5d1c7c7eeb7d`  
		Last Modified: Fri, 23 Apr 2021 23:31:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044162ca9d8f9fab91ae25a14cd772432e503ea1fdbc23f20cd409ead3cb9523`  
		Last Modified: Fri, 23 Apr 2021 23:32:03 GMT  
		Size: 52.2 MB (52182166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5f2df82b25d1a8c9a90ce1c4aabf541775b149b95bd3cdf201f01eb93a7bb9`  
		Last Modified: Fri, 23 Apr 2021 23:31:47 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2829f71ad2e81aa38caecfa924aeaed770273ef966f9f09930566029537c280c`  
		Last Modified: Fri, 23 Apr 2021 23:31:47 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1`

```console
$ docker pull kong@sha256:080552837b5b67917db581a2c7b0e11a5da95d15292183d214a0ed3de6c2df79
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
$ docker pull kong@sha256:7f06a0f0840e73e8a91419c740ea8f016a9afbfe0eda8dd6577ce9d8cc042491
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52669949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451e98aedd9fc04d503c3590778d9b1e6bbefba7d244f5aafd910e59cb500d0e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:30:22 GMT
ARG KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 23:30:24 GMT
ENV KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 23:30:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 23:30:50 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:30:51 GMT
USER kong
# Wed, 14 Apr 2021 23:30:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:30:55 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:30:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:30:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ad5becac5b7d120a6512a7f48009dd90d1955e5331e2fcf3c355fcf9c117f`  
		Last Modified: Wed, 14 Apr 2021 23:34:18 GMT  
		Size: 49.9 MB (49942155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37908e43c4abd0ec7698ce114617f10b37480d9768926f09810a0664a7e4ca15`  
		Last Modified: Wed, 14 Apr 2021 23:34:02 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-alpine`

```console
$ docker pull kong@sha256:080552837b5b67917db581a2c7b0e11a5da95d15292183d214a0ed3de6c2df79
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
$ docker pull kong@sha256:7f06a0f0840e73e8a91419c740ea8f016a9afbfe0eda8dd6577ce9d8cc042491
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52669949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451e98aedd9fc04d503c3590778d9b1e6bbefba7d244f5aafd910e59cb500d0e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:30:22 GMT
ARG KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 23:30:24 GMT
ENV KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 23:30:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 23:30:50 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:30:51 GMT
USER kong
# Wed, 14 Apr 2021 23:30:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:30:55 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:30:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:30:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ad5becac5b7d120a6512a7f48009dd90d1955e5331e2fcf3c355fcf9c117f`  
		Last Modified: Wed, 14 Apr 2021 23:34:18 GMT  
		Size: 49.9 MB (49942155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37908e43c4abd0ec7698ce114617f10b37480d9768926f09810a0664a7e4ca15`  
		Last Modified: Wed, 14 Apr 2021 23:34:02 GMT  
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
$ docker pull kong@sha256:e1b331430664ec7e8423067ff0e5157f48709804f88e50c375b35e7084f8136b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:190d638ce7ce2ef9065acf5eb52055c6926e36fe1cc0e33f34d6a084e5dfb4c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134190003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f16a5cb3c111ed04b5b1326c3e0bdfbc129d96e94ef741621cdec0ce875108`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:43:26 GMT
ARG KONG_VERSION=2.1.4
# Fri, 23 Apr 2021 23:43:26 GMT
ENV KONG_VERSION=2.1.4
# Fri, 23 Apr 2021 23:44:01 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:44:01 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:44:02 GMT
USER kong
# Fri, 23 Apr 2021 23:44:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:44:02 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:44:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:44:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3385c46a641bbdecf7ef95c1b741275fdc4c9ec8f59fe698054051d12a87de`  
		Last Modified: Fri, 23 Apr 2021 23:47:24 GMT  
		Size: 62.9 MB (62851353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd69242a30e6741f420fb33ed988ab680185bde798c09bdaf6ea381c6242b9a`  
		Last Modified: Fri, 23 Apr 2021 23:47:09 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4df5ff045584ae7e140ed80ef5db414c57ec4cc555b090b66d823b9d20bfe35e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125334029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2509542a10411d5c23bb409eb268b0742019cd5d275f7e57676d64f71893f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:26:50 GMT
ARG KONG_VERSION=2.1.4
# Fri, 23 Apr 2021 23:26:51 GMT
ENV KONG_VERSION=2.1.4
# Fri, 23 Apr 2021 23:27:45 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:27:48 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:27:52 GMT
USER kong
# Fri, 23 Apr 2021 23:27:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:27:57 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:27:58 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:27:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c703a63dfa901e5446a941055d5c96ebd51c5d670284def0a5c73cbc5c15fc`  
		Last Modified: Fri, 23 Apr 2021 23:31:40 GMT  
		Size: 59.2 MB (59223122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bb5a007f3e1d34a449e7f69937baedcc6a80401a8ff9e57f632d53b7066255`  
		Last Modified: Fri, 23 Apr 2021 23:31:22 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4`

```console
$ docker pull kong@sha256:080552837b5b67917db581a2c7b0e11a5da95d15292183d214a0ed3de6c2df79
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
$ docker pull kong@sha256:7f06a0f0840e73e8a91419c740ea8f016a9afbfe0eda8dd6577ce9d8cc042491
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52669949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451e98aedd9fc04d503c3590778d9b1e6bbefba7d244f5aafd910e59cb500d0e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:30:22 GMT
ARG KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 23:30:24 GMT
ENV KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 23:30:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 23:30:50 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:30:51 GMT
USER kong
# Wed, 14 Apr 2021 23:30:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:30:55 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:30:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:30:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ad5becac5b7d120a6512a7f48009dd90d1955e5331e2fcf3c355fcf9c117f`  
		Last Modified: Wed, 14 Apr 2021 23:34:18 GMT  
		Size: 49.9 MB (49942155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37908e43c4abd0ec7698ce114617f10b37480d9768926f09810a0664a7e4ca15`  
		Last Modified: Wed, 14 Apr 2021 23:34:02 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-alpine`

```console
$ docker pull kong@sha256:080552837b5b67917db581a2c7b0e11a5da95d15292183d214a0ed3de6c2df79
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
$ docker pull kong@sha256:7f06a0f0840e73e8a91419c740ea8f016a9afbfe0eda8dd6577ce9d8cc042491
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52669949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:451e98aedd9fc04d503c3590778d9b1e6bbefba7d244f5aafd910e59cb500d0e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:30:22 GMT
ARG KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 23:30:24 GMT
ENV KONG_VERSION=2.1.4
# Wed, 14 Apr 2021 23:30:46 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 23:30:50 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:30:51 GMT
USER kong
# Wed, 14 Apr 2021 23:30:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:30:55 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:30:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:30:57 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ad5becac5b7d120a6512a7f48009dd90d1955e5331e2fcf3c355fcf9c117f`  
		Last Modified: Wed, 14 Apr 2021 23:34:18 GMT  
		Size: 49.9 MB (49942155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37908e43c4abd0ec7698ce114617f10b37480d9768926f09810a0664a7e4ca15`  
		Last Modified: Wed, 14 Apr 2021 23:34:02 GMT  
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
$ docker pull kong@sha256:e1b331430664ec7e8423067ff0e5157f48709804f88e50c375b35e7084f8136b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:190d638ce7ce2ef9065acf5eb52055c6926e36fe1cc0e33f34d6a084e5dfb4c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 MB (134190003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f16a5cb3c111ed04b5b1326c3e0bdfbc129d96e94ef741621cdec0ce875108`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:43:26 GMT
ARG KONG_VERSION=2.1.4
# Fri, 23 Apr 2021 23:43:26 GMT
ENV KONG_VERSION=2.1.4
# Fri, 23 Apr 2021 23:44:01 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:44:01 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:44:02 GMT
USER kong
# Fri, 23 Apr 2021 23:44:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:44:02 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:44:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:44:02 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3385c46a641bbdecf7ef95c1b741275fdc4c9ec8f59fe698054051d12a87de`  
		Last Modified: Fri, 23 Apr 2021 23:47:24 GMT  
		Size: 62.9 MB (62851353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd69242a30e6741f420fb33ed988ab680185bde798c09bdaf6ea381c6242b9a`  
		Last Modified: Fri, 23 Apr 2021 23:47:09 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:4df5ff045584ae7e140ed80ef5db414c57ec4cc555b090b66d823b9d20bfe35e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125334029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2509542a10411d5c23bb409eb268b0742019cd5d275f7e57676d64f71893f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:26:50 GMT
ARG KONG_VERSION=2.1.4
# Fri, 23 Apr 2021 23:26:51 GMT
ENV KONG_VERSION=2.1.4
# Fri, 23 Apr 2021 23:27:45 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:27:48 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:27:52 GMT
USER kong
# Fri, 23 Apr 2021 23:27:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:27:57 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:27:58 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:27:59 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c703a63dfa901e5446a941055d5c96ebd51c5d670284def0a5c73cbc5c15fc`  
		Last Modified: Fri, 23 Apr 2021 23:31:40 GMT  
		Size: 59.2 MB (59223122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bb5a007f3e1d34a449e7f69937baedcc6a80401a8ff9e57f632d53b7066255`  
		Last Modified: Fri, 23 Apr 2021 23:31:22 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2`

```console
$ docker pull kong@sha256:c7809f2de514584025a99f7a814259077e7f6e6a6b4dc591187dc5c3a7e73a3d
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
$ docker pull kong@sha256:2a51b8c9a12b2a5878300bc43b5d8a9d124abeb416d4efd6a1f470f9601d1ef7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50439993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee87cb8bde77feac59a72b2fdcd24268ce77960090307cfff4994d827830f90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:29:23 GMT
ARG KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 23:29:24 GMT
ENV KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 23:29:25 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 23:29:27 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 23:29:28 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 23:29:30 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 23:29:52 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:29:57 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:29:58 GMT
USER kong
# Wed, 14 Apr 2021 23:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:30:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:30:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:30:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c82e91254a911dd844a9aeab52730c2ea7c4073ae47bf57e395e0d359c6bfb`  
		Last Modified: Wed, 14 Apr 2021 23:33:51 GMT  
		Size: 47.7 MB (47712199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f95c7f8ef522a8dd04cb2db1a9ed53507253d251f7a0de10d5457d8b0dfe8b`  
		Last Modified: Wed, 14 Apr 2021 23:33:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-alpine`

```console
$ docker pull kong@sha256:c7809f2de514584025a99f7a814259077e7f6e6a6b4dc591187dc5c3a7e73a3d
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
$ docker pull kong@sha256:2a51b8c9a12b2a5878300bc43b5d8a9d124abeb416d4efd6a1f470f9601d1ef7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50439993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee87cb8bde77feac59a72b2fdcd24268ce77960090307cfff4994d827830f90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:29:23 GMT
ARG KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 23:29:24 GMT
ENV KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 23:29:25 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 23:29:27 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 23:29:28 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 23:29:30 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 23:29:52 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:29:57 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:29:58 GMT
USER kong
# Wed, 14 Apr 2021 23:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:30:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:30:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:30:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c82e91254a911dd844a9aeab52730c2ea7c4073ae47bf57e395e0d359c6bfb`  
		Last Modified: Wed, 14 Apr 2021 23:33:51 GMT  
		Size: 47.7 MB (47712199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f95c7f8ef522a8dd04cb2db1a9ed53507253d251f7a0de10d5457d8b0dfe8b`  
		Last Modified: Wed, 14 Apr 2021 23:33:38 GMT  
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
$ docker pull kong@sha256:284982d2e83aff6075e88d4264c48e6b50224d2745e16a6b0637f256578c1a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:80ad790d549a4bebfafe597f22d161a46949eca06a5c9da17b5e5d9799e2fd41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134282708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8671c12f6abbed92b828b99462d83810cf807960ad9c52fbfa29161e6204555`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:42:27 GMT
ARG KONG_VERSION=2.2.2
# Fri, 23 Apr 2021 23:42:27 GMT
ENV KONG_VERSION=2.2.2
# Fri, 23 Apr 2021 23:43:09 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:43:10 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:43:11 GMT
USER kong
# Fri, 23 Apr 2021 23:43:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:43:11 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:43:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:43:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a9a1ec3d259268ec3053cf30fa322f67c49954cd0bb8beae5eb7bd9f8a217f`  
		Last Modified: Fri, 23 Apr 2021 23:46:52 GMT  
		Size: 62.9 MB (62944058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c3afa1055e85dd6653241e5377f3cb47403cc35822cbfb9eb02b43502dffc5`  
		Last Modified: Fri, 23 Apr 2021 23:46:36 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d347dd63799aa05643714a42c4e2bc7d6abf04fc946c9d7b8dbaeb15b4ef0e19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125467085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ef759df72ee9d9835035555c3133a6aa51592c2d892288eb160e9a86761b53`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:25:26 GMT
ARG KONG_VERSION=2.2.2
# Fri, 23 Apr 2021 23:25:27 GMT
ENV KONG_VERSION=2.2.2
# Fri, 23 Apr 2021 23:26:22 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:26:24 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:26:27 GMT
USER kong
# Fri, 23 Apr 2021 23:26:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:26:30 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:26:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:26:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eb18fb74b45ee82aceaa9fed7c541f4663018b0b82bbf5737822400666974f`  
		Last Modified: Fri, 23 Apr 2021 23:31:12 GMT  
		Size: 59.4 MB (59356178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2295b38e0147c0c4ba9107bac396c0d1e0921e87d8a493f14c5a9c32ec23fab7`  
		Last Modified: Fri, 23 Apr 2021 23:30:52 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2`

```console
$ docker pull kong@sha256:c7809f2de514584025a99f7a814259077e7f6e6a6b4dc591187dc5c3a7e73a3d
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
$ docker pull kong@sha256:2a51b8c9a12b2a5878300bc43b5d8a9d124abeb416d4efd6a1f470f9601d1ef7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50439993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee87cb8bde77feac59a72b2fdcd24268ce77960090307cfff4994d827830f90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:29:23 GMT
ARG KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 23:29:24 GMT
ENV KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 23:29:25 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 23:29:27 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 23:29:28 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 23:29:30 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 23:29:52 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:29:57 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:29:58 GMT
USER kong
# Wed, 14 Apr 2021 23:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:30:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:30:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:30:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c82e91254a911dd844a9aeab52730c2ea7c4073ae47bf57e395e0d359c6bfb`  
		Last Modified: Wed, 14 Apr 2021 23:33:51 GMT  
		Size: 47.7 MB (47712199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f95c7f8ef522a8dd04cb2db1a9ed53507253d251f7a0de10d5457d8b0dfe8b`  
		Last Modified: Wed, 14 Apr 2021 23:33:38 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2-alpine`

```console
$ docker pull kong@sha256:c7809f2de514584025a99f7a814259077e7f6e6a6b4dc591187dc5c3a7e73a3d
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
$ docker pull kong@sha256:2a51b8c9a12b2a5878300bc43b5d8a9d124abeb416d4efd6a1f470f9601d1ef7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50439993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee87cb8bde77feac59a72b2fdcd24268ce77960090307cfff4994d827830f90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:29:23 GMT
ARG KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 23:29:24 GMT
ENV KONG_VERSION=2.2.2
# Wed, 14 Apr 2021 23:29:25 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 23:29:27 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Wed, 14 Apr 2021 23:29:28 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 23:29:30 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Wed, 14 Apr 2021 23:29:52 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:29:57 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:29:58 GMT
USER kong
# Wed, 14 Apr 2021 23:29:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:30:01 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:30:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:30:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c82e91254a911dd844a9aeab52730c2ea7c4073ae47bf57e395e0d359c6bfb`  
		Last Modified: Wed, 14 Apr 2021 23:33:51 GMT  
		Size: 47.7 MB (47712199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f95c7f8ef522a8dd04cb2db1a9ed53507253d251f7a0de10d5457d8b0dfe8b`  
		Last Modified: Wed, 14 Apr 2021 23:33:38 GMT  
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
$ docker pull kong@sha256:284982d2e83aff6075e88d4264c48e6b50224d2745e16a6b0637f256578c1a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:80ad790d549a4bebfafe597f22d161a46949eca06a5c9da17b5e5d9799e2fd41
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134282708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8671c12f6abbed92b828b99462d83810cf807960ad9c52fbfa29161e6204555`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:42:27 GMT
ARG KONG_VERSION=2.2.2
# Fri, 23 Apr 2021 23:42:27 GMT
ENV KONG_VERSION=2.2.2
# Fri, 23 Apr 2021 23:43:09 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:43:10 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:43:11 GMT
USER kong
# Fri, 23 Apr 2021 23:43:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:43:11 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:43:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:43:12 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a9a1ec3d259268ec3053cf30fa322f67c49954cd0bb8beae5eb7bd9f8a217f`  
		Last Modified: Fri, 23 Apr 2021 23:46:52 GMT  
		Size: 62.9 MB (62944058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c3afa1055e85dd6653241e5377f3cb47403cc35822cbfb9eb02b43502dffc5`  
		Last Modified: Fri, 23 Apr 2021 23:46:36 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:d347dd63799aa05643714a42c4e2bc7d6abf04fc946c9d7b8dbaeb15b4ef0e19
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125467085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ef759df72ee9d9835035555c3133a6aa51592c2d892288eb160e9a86761b53`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:25:26 GMT
ARG KONG_VERSION=2.2.2
# Fri, 23 Apr 2021 23:25:27 GMT
ENV KONG_VERSION=2.2.2
# Fri, 23 Apr 2021 23:26:22 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:26:24 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:26:27 GMT
USER kong
# Fri, 23 Apr 2021 23:26:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:26:30 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:26:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:26:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17eb18fb74b45ee82aceaa9fed7c541f4663018b0b82bbf5737822400666974f`  
		Last Modified: Fri, 23 Apr 2021 23:31:12 GMT  
		Size: 59.4 MB (59356178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2295b38e0147c0c4ba9107bac396c0d1e0921e87d8a493f14c5a9c32ec23fab7`  
		Last Modified: Fri, 23 Apr 2021 23:30:52 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3`

```console
$ docker pull kong@sha256:d4c036d82d35e0c56a5a7dc1d018a92e97b7a9540cb202dd39753e70bac72de9
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
$ docker pull kong@sha256:1a1b00431b1acfe47c84e1ec738b28c13152e39aeb830cc1cb3968ef3c1bcbb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50476207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab9aa177e846506b11e7469bdc11c9ff791b64e09e31edcab3809933ec80e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:28:38 GMT
ARG KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 23:28:39 GMT
ENV KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 23:28:40 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 23:28:42 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 23:28:43 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 23:28:44 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 23:28:55 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:28:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:29:00 GMT
USER kong
# Wed, 14 Apr 2021 23:29:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:29:03 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:29:05 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:29:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c324f2e0f9958126e884450451ead5be7cd89e92443c4d85e16da072245f0d`  
		Last Modified: Wed, 14 Apr 2021 23:33:27 GMT  
		Size: 47.7 MB (47748413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38193a001f0ac7f8928f664e2837dbbb82e93513989f45be5f7bbe0895742e57`  
		Last Modified: Wed, 14 Apr 2021 23:33:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-alpine`

```console
$ docker pull kong@sha256:d4c036d82d35e0c56a5a7dc1d018a92e97b7a9540cb202dd39753e70bac72de9
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
$ docker pull kong@sha256:1a1b00431b1acfe47c84e1ec738b28c13152e39aeb830cc1cb3968ef3c1bcbb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50476207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab9aa177e846506b11e7469bdc11c9ff791b64e09e31edcab3809933ec80e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:28:38 GMT
ARG KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 23:28:39 GMT
ENV KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 23:28:40 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 23:28:42 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 23:28:43 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 23:28:44 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 23:28:55 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:28:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:29:00 GMT
USER kong
# Wed, 14 Apr 2021 23:29:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:29:03 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:29:05 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:29:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c324f2e0f9958126e884450451ead5be7cd89e92443c4d85e16da072245f0d`  
		Last Modified: Wed, 14 Apr 2021 23:33:27 GMT  
		Size: 47.7 MB (47748413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38193a001f0ac7f8928f664e2837dbbb82e93513989f45be5f7bbe0895742e57`  
		Last Modified: Wed, 14 Apr 2021 23:33:13 GMT  
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
$ docker pull kong@sha256:7310d615ae5ea351a900fb62ae9d903de8895799cff1f8b09fefd83509e2e5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:231b102678ec86130dfa5a7bb6d6e0ff23178826285a3d626f76db40e7bbc20c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134315285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d22fe408acabeaec961beeef7f5ce57102d82d3d5175a2f0035983c5c632424`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:41:36 GMT
ARG KONG_VERSION=2.3.3
# Fri, 23 Apr 2021 23:41:36 GMT
ENV KONG_VERSION=2.3.3
# Fri, 23 Apr 2021 23:42:06 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:42:07 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:42:07 GMT
USER kong
# Fri, 23 Apr 2021 23:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:42:08 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:42:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:42:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b564409657e729dbc2e760fdc4d6a9c205bfc4d709cb291518b63bc02cab4266`  
		Last Modified: Fri, 23 Apr 2021 23:46:19 GMT  
		Size: 63.0 MB (62976635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f809e535b8e8e68cdf969348897bfa59977881e2c507a069e2b20ffc7ba1255`  
		Last Modified: Fri, 23 Apr 2021 23:46:04 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5513227f1519340223f6843a1046e6a0af0bbdc0fc645ba4d89d5a49d7f7d65e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125495136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ce706d55e5f2e98ff822b0b1a809a625a277b0a17fc11aafaf9c26539d88a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:24:03 GMT
ARG KONG_VERSION=2.3.3
# Fri, 23 Apr 2021 23:24:04 GMT
ENV KONG_VERSION=2.3.3
# Fri, 23 Apr 2021 23:24:54 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:24:58 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:24:59 GMT
USER kong
# Fri, 23 Apr 2021 23:25:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:25:01 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:25:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:25:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb718698e75e37b12cda6c96e06a911e80dd636f113b6a99a7b5b7d044677d7`  
		Last Modified: Fri, 23 Apr 2021 23:30:43 GMT  
		Size: 59.4 MB (59384229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e35f3a9fa2afe4385beead0187c2c4e587c356f1da1bb7f075d4fcbfa171ce2`  
		Last Modified: Fri, 23 Apr 2021 23:30:24 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3`

```console
$ docker pull kong@sha256:d4c036d82d35e0c56a5a7dc1d018a92e97b7a9540cb202dd39753e70bac72de9
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
$ docker pull kong@sha256:1a1b00431b1acfe47c84e1ec738b28c13152e39aeb830cc1cb3968ef3c1bcbb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50476207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab9aa177e846506b11e7469bdc11c9ff791b64e09e31edcab3809933ec80e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:28:38 GMT
ARG KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 23:28:39 GMT
ENV KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 23:28:40 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 23:28:42 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 23:28:43 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 23:28:44 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 23:28:55 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:28:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:29:00 GMT
USER kong
# Wed, 14 Apr 2021 23:29:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:29:03 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:29:05 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:29:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c324f2e0f9958126e884450451ead5be7cd89e92443c4d85e16da072245f0d`  
		Last Modified: Wed, 14 Apr 2021 23:33:27 GMT  
		Size: 47.7 MB (47748413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38193a001f0ac7f8928f664e2837dbbb82e93513989f45be5f7bbe0895742e57`  
		Last Modified: Wed, 14 Apr 2021 23:33:13 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3-alpine`

```console
$ docker pull kong@sha256:d4c036d82d35e0c56a5a7dc1d018a92e97b7a9540cb202dd39753e70bac72de9
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
$ docker pull kong@sha256:1a1b00431b1acfe47c84e1ec738b28c13152e39aeb830cc1cb3968ef3c1bcbb2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50476207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab9aa177e846506b11e7469bdc11c9ff791b64e09e31edcab3809933ec80e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:28:38 GMT
ARG KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 23:28:39 GMT
ENV KONG_VERSION=2.3.3
# Wed, 14 Apr 2021 23:28:40 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 23:28:42 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Wed, 14 Apr 2021 23:28:43 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 23:28:44 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Wed, 14 Apr 2021 23:28:55 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:28:58 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:29:00 GMT
USER kong
# Wed, 14 Apr 2021 23:29:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:29:03 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:29:05 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:29:07 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83c324f2e0f9958126e884450451ead5be7cd89e92443c4d85e16da072245f0d`  
		Last Modified: Wed, 14 Apr 2021 23:33:27 GMT  
		Size: 47.7 MB (47748413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38193a001f0ac7f8928f664e2837dbbb82e93513989f45be5f7bbe0895742e57`  
		Last Modified: Wed, 14 Apr 2021 23:33:13 GMT  
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
$ docker pull kong@sha256:7310d615ae5ea351a900fb62ae9d903de8895799cff1f8b09fefd83509e2e5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:231b102678ec86130dfa5a7bb6d6e0ff23178826285a3d626f76db40e7bbc20c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134315285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d22fe408acabeaec961beeef7f5ce57102d82d3d5175a2f0035983c5c632424`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:41:36 GMT
ARG KONG_VERSION=2.3.3
# Fri, 23 Apr 2021 23:41:36 GMT
ENV KONG_VERSION=2.3.3
# Fri, 23 Apr 2021 23:42:06 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:42:07 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:42:07 GMT
USER kong
# Fri, 23 Apr 2021 23:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:42:08 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:42:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:42:08 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b564409657e729dbc2e760fdc4d6a9c205bfc4d709cb291518b63bc02cab4266`  
		Last Modified: Fri, 23 Apr 2021 23:46:19 GMT  
		Size: 63.0 MB (62976635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f809e535b8e8e68cdf969348897bfa59977881e2c507a069e2b20ffc7ba1255`  
		Last Modified: Fri, 23 Apr 2021 23:46:04 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5513227f1519340223f6843a1046e6a0af0bbdc0fc645ba4d89d5a49d7f7d65e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.5 MB (125495136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ce706d55e5f2e98ff822b0b1a809a625a277b0a17fc11aafaf9c26539d88a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:24:03 GMT
ARG KONG_VERSION=2.3.3
# Fri, 23 Apr 2021 23:24:04 GMT
ENV KONG_VERSION=2.3.3
# Fri, 23 Apr 2021 23:24:54 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:24:58 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:24:59 GMT
USER kong
# Fri, 23 Apr 2021 23:25:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:25:01 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:25:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:25:03 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb718698e75e37b12cda6c96e06a911e80dd636f113b6a99a7b5b7d044677d7`  
		Last Modified: Fri, 23 Apr 2021 23:30:43 GMT  
		Size: 59.4 MB (59384229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e35f3a9fa2afe4385beead0187c2c4e587c356f1da1bb7f075d4fcbfa171ce2`  
		Last Modified: Fri, 23 Apr 2021 23:30:24 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4`

```console
$ docker pull kong@sha256:91e8a6689f3c5c522dabbae93d5cc5006da9931ab3e325de2c944ba87622e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4` - linux; amd64

```console
$ docker pull kong@sha256:0372a0a05c5a4066cbfa1836766d6726edd55a4e3e1ee3a962c85c517a137339
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51157442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e950e221f43ed7989260b2a61accb568d9d3cdd7df13c9a42f4edd83329851`
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
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:38 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:23:39 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:39 GMT
USER kong
# Wed, 14 Apr 2021 19:23:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:23:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:23:41 GMT
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
	-	`sha256:cc91e546b96c68aa68775d1e466977f5340f41446ca8722944a19c714306e48b`  
		Last Modified: Wed, 14 Apr 2021 19:29:15 GMT  
		Size: 48.3 MB (48340332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b835101a2100b139d649deb78fbeeec2a8efd295f076021c79fc15e733fbeaaa`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2fb2782ecc0a030b096d909c23b05b82ece464b5db82d214ada47cd5f6927448
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50688463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b697428de94c2f258b89f87fbae0df5a5a01c8e3853c5446dede9bbfb89ff06b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:26:29 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:30 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:31 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:31 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:32 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:33 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:45 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:26:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:26:49 GMT
USER kong
# Wed, 14 Apr 2021 23:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:26:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:26:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f621485fe99632d7e0c3b4a5f9d900b0f7084270bc696b8697bf72c0203f3b`  
		Last Modified: Wed, 14 Apr 2021 23:32:27 GMT  
		Size: 48.0 MB (47960669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150e2e25f3f7a98718567a47d1429faf8d204b3229779965970dc1f86a69ea3`  
		Last Modified: Wed, 14 Apr 2021 23:32:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-alpine`

```console
$ docker pull kong@sha256:91e8a6689f3c5c522dabbae93d5cc5006da9931ab3e325de2c944ba87622e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:0372a0a05c5a4066cbfa1836766d6726edd55a4e3e1ee3a962c85c517a137339
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51157442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e950e221f43ed7989260b2a61accb568d9d3cdd7df13c9a42f4edd83329851`
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
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:38 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:23:39 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:39 GMT
USER kong
# Wed, 14 Apr 2021 19:23:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:23:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:23:41 GMT
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
	-	`sha256:cc91e546b96c68aa68775d1e466977f5340f41446ca8722944a19c714306e48b`  
		Last Modified: Wed, 14 Apr 2021 19:29:15 GMT  
		Size: 48.3 MB (48340332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b835101a2100b139d649deb78fbeeec2a8efd295f076021c79fc15e733fbeaaa`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2fb2782ecc0a030b096d909c23b05b82ece464b5db82d214ada47cd5f6927448
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50688463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b697428de94c2f258b89f87fbae0df5a5a01c8e3853c5446dede9bbfb89ff06b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:26:29 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:30 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:31 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:31 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:32 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:33 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:45 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:26:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:26:49 GMT
USER kong
# Wed, 14 Apr 2021 23:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:26:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:26:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f621485fe99632d7e0c3b4a5f9d900b0f7084270bc696b8697bf72c0203f3b`  
		Last Modified: Wed, 14 Apr 2021 23:32:27 GMT  
		Size: 48.0 MB (47960669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150e2e25f3f7a98718567a47d1429faf8d204b3229779965970dc1f86a69ea3`  
		Last Modified: Wed, 14 Apr 2021 23:32:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-centos`

```console
$ docker pull kong@sha256:967ff8cf02ed4fb65d336f052d39c2a2ea8974c216ed862603a6762ab2c87791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.4-centos` - linux; amd64

```console
$ docker pull kong@sha256:56f36f6395ef0352f1aea7382eaa1b2b6dfd0f0d197615c93e95427a16331c60
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127637118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0518d3fe9239f7ce1c32d81ea5daf92e51a19821ffd784f2c97853efa8b39fc`
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
# Wed, 14 Apr 2021 19:25:27 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:25:28 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:25:28 GMT
ARG KONG_SHA256=edbea2fe235bc65087b67fe071449b98476a4a8d12f9919b63100cffcdc0c103
# Wed, 14 Apr 2021 19:26:03 GMT
# ARGS: KONG_SHA256=edbea2fe235bc65087b67fe071449b98476a4a8d12f9919b63100cffcdc0c103
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 19:26:03 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:04 GMT
USER kong
# Wed, 14 Apr 2021 19:26:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:04 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:04 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:04 GMT
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
	-	`sha256:7709b337ddf42300cd09210494630031e63b98507255236b95a5c27227277866`  
		Last Modified: Wed, 14 Apr 2021 19:30:21 GMT  
		Size: 51.5 MB (51539099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9936aa953bd714ddba9df7f6f7293a403283eb77cc8f4b59605a20c6a49b34`  
		Last Modified: Wed, 14 Apr 2021 19:30:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-ubuntu`

```console
$ docker pull kong@sha256:d20da2bff851e8f36660f8aa0cc9ca9d5f41f0cd63a449713d6dd182eeef9b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f671b3192ce757aa89c06cc57b81a256496a837b278bfb16e567465642f3f86d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134505896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a554e2490fbda5e238fb8cf3ce7da615af70888ecd6316b97b8eb4def200cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:41:01 GMT
ARG KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:41:01 GMT
ENV KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:41:23 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:41:24 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:41:24 GMT
USER kong
# Fri, 23 Apr 2021 23:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:41:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:41:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:41:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7793c10ae43bbe577345598469d4f2e815e1033038f04872ccacd3b2a2c066`  
		Last Modified: Fri, 23 Apr 2021 23:45:44 GMT  
		Size: 63.2 MB (63167246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12092440ba79e693ee28ff038ff3076b3d2d62cc183260a16d5f97eb9ff2fdaf`  
		Last Modified: Fri, 23 Apr 2021 23:45:31 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:608708ef122ccc209e7f967e7e6aa4ef512033c19118def2969fece3e7a83931
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125636879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872ba797e7fb85760f623db6bd3e1a2267247117d5e7fc5dff1b6600ff15b24e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:22:44 GMT
ARG KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:22:45 GMT
ENV KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:23:40 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:23:43 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:23:44 GMT
USER kong
# Fri, 23 Apr 2021 23:23:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:23:47 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:23:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:23:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92968f5c96017c8a1d1de4ce128bb953e8b8533b4722709baa548ae6d521b26d`  
		Last Modified: Fri, 23 Apr 2021 23:30:05 GMT  
		Size: 59.5 MB (59525972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7b73297a041eca67ce0ac37bd25f70f859917ab3ad9f8b05815c937da5882f`  
		Last Modified: Fri, 23 Apr 2021 23:29:47 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.0`

```console
$ docker pull kong@sha256:91e8a6689f3c5c522dabbae93d5cc5006da9931ab3e325de2c944ba87622e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.0` - linux; amd64

```console
$ docker pull kong@sha256:0372a0a05c5a4066cbfa1836766d6726edd55a4e3e1ee3a962c85c517a137339
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51157442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e950e221f43ed7989260b2a61accb568d9d3cdd7df13c9a42f4edd83329851`
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
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:38 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:23:39 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:39 GMT
USER kong
# Wed, 14 Apr 2021 19:23:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:23:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:23:41 GMT
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
	-	`sha256:cc91e546b96c68aa68775d1e466977f5340f41446ca8722944a19c714306e48b`  
		Last Modified: Wed, 14 Apr 2021 19:29:15 GMT  
		Size: 48.3 MB (48340332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b835101a2100b139d649deb78fbeeec2a8efd295f076021c79fc15e733fbeaaa`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2fb2782ecc0a030b096d909c23b05b82ece464b5db82d214ada47cd5f6927448
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50688463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b697428de94c2f258b89f87fbae0df5a5a01c8e3853c5446dede9bbfb89ff06b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:26:29 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:30 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:31 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:31 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:32 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:33 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:45 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:26:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:26:49 GMT
USER kong
# Wed, 14 Apr 2021 23:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:26:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:26:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f621485fe99632d7e0c3b4a5f9d900b0f7084270bc696b8697bf72c0203f3b`  
		Last Modified: Wed, 14 Apr 2021 23:32:27 GMT  
		Size: 48.0 MB (47960669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150e2e25f3f7a98718567a47d1429faf8d204b3229779965970dc1f86a69ea3`  
		Last Modified: Wed, 14 Apr 2021 23:32:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.0-alpine`

```console
$ docker pull kong@sha256:91e8a6689f3c5c522dabbae93d5cc5006da9931ab3e325de2c944ba87622e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:0372a0a05c5a4066cbfa1836766d6726edd55a4e3e1ee3a962c85c517a137339
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51157442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e950e221f43ed7989260b2a61accb568d9d3cdd7df13c9a42f4edd83329851`
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
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:38 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:23:39 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:39 GMT
USER kong
# Wed, 14 Apr 2021 19:23:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:23:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:23:41 GMT
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
	-	`sha256:cc91e546b96c68aa68775d1e466977f5340f41446ca8722944a19c714306e48b`  
		Last Modified: Wed, 14 Apr 2021 19:29:15 GMT  
		Size: 48.3 MB (48340332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b835101a2100b139d649deb78fbeeec2a8efd295f076021c79fc15e733fbeaaa`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2fb2782ecc0a030b096d909c23b05b82ece464b5db82d214ada47cd5f6927448
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50688463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b697428de94c2f258b89f87fbae0df5a5a01c8e3853c5446dede9bbfb89ff06b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:26:29 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:30 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:31 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:31 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:32 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:33 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:45 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:26:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:26:49 GMT
USER kong
# Wed, 14 Apr 2021 23:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:26:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:26:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f621485fe99632d7e0c3b4a5f9d900b0f7084270bc696b8697bf72c0203f3b`  
		Last Modified: Wed, 14 Apr 2021 23:32:27 GMT  
		Size: 48.0 MB (47960669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150e2e25f3f7a98718567a47d1429faf8d204b3229779965970dc1f86a69ea3`  
		Last Modified: Wed, 14 Apr 2021 23:32:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.0-centos`

```console
$ docker pull kong@sha256:967ff8cf02ed4fb65d336f052d39c2a2ea8974c216ed862603a6762ab2c87791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.4.0-centos` - linux; amd64

```console
$ docker pull kong@sha256:56f36f6395ef0352f1aea7382eaa1b2b6dfd0f0d197615c93e95427a16331c60
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127637118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0518d3fe9239f7ce1c32d81ea5daf92e51a19821ffd784f2c97853efa8b39fc`
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
# Wed, 14 Apr 2021 19:25:27 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:25:28 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:25:28 GMT
ARG KONG_SHA256=edbea2fe235bc65087b67fe071449b98476a4a8d12f9919b63100cffcdc0c103
# Wed, 14 Apr 2021 19:26:03 GMT
# ARGS: KONG_SHA256=edbea2fe235bc65087b67fe071449b98476a4a8d12f9919b63100cffcdc0c103
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 19:26:03 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:04 GMT
USER kong
# Wed, 14 Apr 2021 19:26:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:04 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:04 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:04 GMT
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
	-	`sha256:7709b337ddf42300cd09210494630031e63b98507255236b95a5c27227277866`  
		Last Modified: Wed, 14 Apr 2021 19:30:21 GMT  
		Size: 51.5 MB (51539099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9936aa953bd714ddba9df7f6f7293a403283eb77cc8f4b59605a20c6a49b34`  
		Last Modified: Wed, 14 Apr 2021 19:30:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.0-ubuntu`

```console
$ docker pull kong@sha256:d20da2bff851e8f36660f8aa0cc9ca9d5f41f0cd63a449713d6dd182eeef9b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f671b3192ce757aa89c06cc57b81a256496a837b278bfb16e567465642f3f86d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134505896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a554e2490fbda5e238fb8cf3ce7da615af70888ecd6316b97b8eb4def200cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:41:01 GMT
ARG KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:41:01 GMT
ENV KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:41:23 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:41:24 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:41:24 GMT
USER kong
# Fri, 23 Apr 2021 23:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:41:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:41:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:41:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7793c10ae43bbe577345598469d4f2e815e1033038f04872ccacd3b2a2c066`  
		Last Modified: Fri, 23 Apr 2021 23:45:44 GMT  
		Size: 63.2 MB (63167246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12092440ba79e693ee28ff038ff3076b3d2d62cc183260a16d5f97eb9ff2fdaf`  
		Last Modified: Fri, 23 Apr 2021 23:45:31 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:608708ef122ccc209e7f967e7e6aa4ef512033c19118def2969fece3e7a83931
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125636879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872ba797e7fb85760f623db6bd3e1a2267247117d5e7fc5dff1b6600ff15b24e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:22:44 GMT
ARG KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:22:45 GMT
ENV KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:23:40 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:23:43 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:23:44 GMT
USER kong
# Fri, 23 Apr 2021 23:23:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:23:47 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:23:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:23:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92968f5c96017c8a1d1de4ce128bb953e8b8533b4722709baa548ae6d521b26d`  
		Last Modified: Fri, 23 Apr 2021 23:30:05 GMT  
		Size: 59.5 MB (59525972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7b73297a041eca67ce0ac37bd25f70f859917ab3ad9f8b05815c937da5882f`  
		Last Modified: Fri, 23 Apr 2021 23:29:47 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:91e8a6689f3c5c522dabbae93d5cc5006da9931ab3e325de2c944ba87622e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:0372a0a05c5a4066cbfa1836766d6726edd55a4e3e1ee3a962c85c517a137339
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51157442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e950e221f43ed7989260b2a61accb568d9d3cdd7df13c9a42f4edd83329851`
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
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:38 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:23:39 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:39 GMT
USER kong
# Wed, 14 Apr 2021 19:23:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:23:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:23:41 GMT
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
	-	`sha256:cc91e546b96c68aa68775d1e466977f5340f41446ca8722944a19c714306e48b`  
		Last Modified: Wed, 14 Apr 2021 19:29:15 GMT  
		Size: 48.3 MB (48340332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b835101a2100b139d649deb78fbeeec2a8efd295f076021c79fc15e733fbeaaa`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2fb2782ecc0a030b096d909c23b05b82ece464b5db82d214ada47cd5f6927448
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50688463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b697428de94c2f258b89f87fbae0df5a5a01c8e3853c5446dede9bbfb89ff06b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:26:29 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:30 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:31 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:31 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:32 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:33 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:45 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:26:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:26:49 GMT
USER kong
# Wed, 14 Apr 2021 23:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:26:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:26:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f621485fe99632d7e0c3b4a5f9d900b0f7084270bc696b8697bf72c0203f3b`  
		Last Modified: Wed, 14 Apr 2021 23:32:27 GMT  
		Size: 48.0 MB (47960669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150e2e25f3f7a98718567a47d1429faf8d204b3229779965970dc1f86a69ea3`  
		Last Modified: Wed, 14 Apr 2021 23:32:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:centos`

```console
$ docker pull kong@sha256:967ff8cf02ed4fb65d336f052d39c2a2ea8974c216ed862603a6762ab2c87791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:56f36f6395ef0352f1aea7382eaa1b2b6dfd0f0d197615c93e95427a16331c60
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127637118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0518d3fe9239f7ce1c32d81ea5daf92e51a19821ffd784f2c97853efa8b39fc`
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
# Wed, 14 Apr 2021 19:25:27 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:25:28 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:25:28 GMT
ARG KONG_SHA256=edbea2fe235bc65087b67fe071449b98476a4a8d12f9919b63100cffcdc0c103
# Wed, 14 Apr 2021 19:26:03 GMT
# ARGS: KONG_SHA256=edbea2fe235bc65087b67fe071449b98476a4a8d12f9919b63100cffcdc0c103
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 14 Apr 2021 19:26:03 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:26:04 GMT
USER kong
# Wed, 14 Apr 2021 19:26:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:26:04 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:26:04 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:26:04 GMT
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
	-	`sha256:7709b337ddf42300cd09210494630031e63b98507255236b95a5c27227277866`  
		Last Modified: Wed, 14 Apr 2021 19:30:21 GMT  
		Size: 51.5 MB (51539099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9936aa953bd714ddba9df7f6f7293a403283eb77cc8f4b59605a20c6a49b34`  
		Last Modified: Wed, 14 Apr 2021 19:30:12 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:91e8a6689f3c5c522dabbae93d5cc5006da9931ab3e325de2c944ba87622e906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:0372a0a05c5a4066cbfa1836766d6726edd55a4e3e1ee3a962c85c517a137339
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51157442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e950e221f43ed7989260b2a61accb568d9d3cdd7df13c9a42f4edd83329851`
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
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 19:23:23 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 19:23:24 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:24 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 19:23:38 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 19:23:39 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 19:23:39 GMT
USER kong
# Wed, 14 Apr 2021 19:23:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 19:23:40 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 19:23:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 19:23:41 GMT
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
	-	`sha256:cc91e546b96c68aa68775d1e466977f5340f41446ca8722944a19c714306e48b`  
		Last Modified: Wed, 14 Apr 2021 19:29:15 GMT  
		Size: 48.3 MB (48340332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b835101a2100b139d649deb78fbeeec2a8efd295f076021c79fc15e733fbeaaa`  
		Last Modified: Wed, 14 Apr 2021 19:29:06 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2fb2782ecc0a030b096d909c23b05b82ece464b5db82d214ada47cd5f6927448
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50688463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b697428de94c2f258b89f87fbae0df5a5a01c8e3853c5446dede9bbfb89ff06b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:05 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Wed, 14 Apr 2021 18:43:06 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:26:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 14 Apr 2021 23:26:26 GMT
ARG ASSET=ce
# Wed, 14 Apr 2021 23:26:27 GMT
ENV ASSET=ce
# Wed, 14 Apr 2021 23:26:28 GMT
ARG EE_PORTS
# Wed, 14 Apr 2021 23:26:28 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 14 Apr 2021 23:26:29 GMT
ARG KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:30 GMT
ENV KONG_VERSION=2.4.0
# Wed, 14 Apr 2021 23:26:31 GMT
ARG KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:31 GMT
ENV KONG_AMD64_SHA=a69246ac847e63fa878a4c91fcd097d3ce11db00fd2ce647f1afdf60b5271fa8
# Wed, 14 Apr 2021 23:26:32 GMT
ARG KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:33 GMT
ENV KONG_ARM64_SHA=59150130fa4571a406ba72e71dc9ac64ccf48bdf3941ee1965e6a3626d0fbc18
# Wed, 14 Apr 2021 23:26:45 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 14 Apr 2021 23:26:48 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:26:49 GMT
USER kong
# Wed, 14 Apr 2021 23:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:26:51 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 14 Apr 2021 23:26:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Apr 2021 23:26:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9932115f0c3c7d09ef931e95a6041d63ed4929d04fab6245a93281008ddd4496`  
		Last Modified: Wed, 14 Apr 2021 23:32:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f621485fe99632d7e0c3b4a5f9d900b0f7084270bc696b8697bf72c0203f3b`  
		Last Modified: Wed, 14 Apr 2021 23:32:27 GMT  
		Size: 48.0 MB (47960669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1150e2e25f3f7a98718567a47d1429faf8d204b3229779965970dc1f86a69ea3`  
		Last Modified: Wed, 14 Apr 2021 23:32:04 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:d20da2bff851e8f36660f8aa0cc9ca9d5f41f0cd63a449713d6dd182eeef9b6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:f671b3192ce757aa89c06cc57b81a256496a837b278bfb16e567465642f3f86d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134505896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a554e2490fbda5e238fb8cf3ce7da615af70888ecd6316b97b8eb4def200cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:41:00 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:41:00 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:41:00 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:41:01 GMT
ARG KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:41:01 GMT
ENV KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:41:23 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:41:24 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:41:24 GMT
USER kong
# Fri, 23 Apr 2021 23:41:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:41:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:41:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:41:25 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f306ae915616100b1c2aaba985765c88c649774d2f34fce447a32a2294606a20`  
		Last Modified: Fri, 23 Apr 2021 23:45:32 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7793c10ae43bbe577345598469d4f2e815e1033038f04872ccacd3b2a2c066`  
		Last Modified: Fri, 23 Apr 2021 23:45:44 GMT  
		Size: 63.2 MB (63167246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12092440ba79e693ee28ff038ff3076b3d2d62cc183260a16d5f97eb9ff2fdaf`  
		Last Modified: Fri, 23 Apr 2021 23:45:31 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:608708ef122ccc209e7f967e7e6aa4ef512033c19118def2969fece3e7a83931
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125636879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:872ba797e7fb85760f623db6bd3e1a2267247117d5e7fc5dff1b6600ff15b24e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 23 Apr 2021 22:49:13 GMT
ADD file:f7933af6e4e3a52794ae852310c5fd423b1afeb32576f8e3c3bc695db17d34e4 in / 
# Fri, 23 Apr 2021 22:49:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:49:20 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:49:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:49:24 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:38 GMT
ARG ASSET=ce
# Fri, 23 Apr 2021 23:22:39 GMT
ENV ASSET=ce
# Fri, 23 Apr 2021 23:22:41 GMT
ARG EE_PORTS
# Fri, 23 Apr 2021 23:22:42 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 23 Apr 2021 23:22:44 GMT
ARG KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:22:45 GMT
ENV KONG_VERSION=2.4.0
# Fri, 23 Apr 2021 23:23:40 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 23 Apr 2021 23:23:43 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 23 Apr 2021 23:23:44 GMT
USER kong
# Fri, 23 Apr 2021 23:23:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 23 Apr 2021 23:23:47 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 23 Apr 2021 23:23:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 23 Apr 2021 23:23:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:ea68ed57e24afe569fc149143e2b3c46c597abcbb61449c3652998e4bb1b5440`  
		Last Modified: Sat, 17 Apr 2021 00:25:08 GMT  
		Size: 41.0 MB (41026756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12a5b59372be005e03800813e52c56f42f21410e07162424afb9662a5620f7c`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a820d46388e3f6c8bd0bdd7d2079370426b00565c4fffac3f138c26af2408de2`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1af45b45bb6a5e3119ffb671a33eb4a934675de944eee38f1aba43f3967c533`  
		Last Modified: Fri, 23 Apr 2021 22:50:56 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a54738339d87f4d33a6bbe531d1c8f82f068991ba47b49a018515a2c2a5d4b`  
		Last Modified: Fri, 23 Apr 2021 23:29:49 GMT  
		Size: 25.1 MB (25081971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92968f5c96017c8a1d1de4ce128bb953e8b8533b4722709baa548ae6d521b26d`  
		Last Modified: Fri, 23 Apr 2021 23:30:05 GMT  
		Size: 59.5 MB (59525972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7b73297a041eca67ce0ac37bd25f70f859917ab3ad9f8b05815c937da5882f`  
		Last Modified: Fri, 23 Apr 2021 23:29:47 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
