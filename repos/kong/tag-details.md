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
-	[`kong:alpine`](#kongalpine)
-	[`kong:centos`](#kongcentos)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2`

```console
$ docker pull kong@sha256:c41708bc235dfb1bda2193a88c67d7f75f12bc0ca069f77444fc5b471c2e1d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:deeeaa21a4b3a279fe081ba1d29f6c2d61ffd29509bb17c819a5a8ac02e11f7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cad33482c5789135c18490d8bc58a5ca33594e4bccff7ae6425a59dca3b0c9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:30:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:30:26 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:30:26 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:30:26 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:30:27 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 07:30:27 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:30:27 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 07:30:27 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 07:30:27 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 07:30:28 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 07:30:28 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 07:30:36 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 06 Mar 2021 07:30:37 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:30:37 GMT
USER kong
# Sat, 06 Mar 2021 07:30:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:30:37 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:30:37 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:30:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caafd1a253b0f537460746cdcf3618b9f1b7018ee9fd49fc3afe37a66e4148c5`  
		Last Modified: Sat, 06 Mar 2021 07:38:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4a2464daa995ef790c6a61cea31a358dcbb7493dddbcb8b88ebe870123aeeb`  
		Last Modified: Sat, 06 Mar 2021 07:38:25 GMT  
		Size: 48.1 MB (48134689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82817593c0d29810791181961affa528c92368e76123198121fa27605e6ae6e`  
		Last Modified: Sat, 06 Mar 2021 07:38:16 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:06d53a9dcefe213fd6ebd9a25fc1ab7a86b5174de27a7c36c410b8093754ea38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50471868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8e3ebeb8b18ec45885f8e5b7f6c43f0395a8b2eb596e5555f8c8df67c9b3ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 01:42:55 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:57 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:58 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:42:59 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:43:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 06 Mar 2021 01:43:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:43:13 GMT
USER kong
# Sat, 06 Mar 2021 01:43:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:43:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:43:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:43:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1b9581057bb8e89fbda6e9096550d10fd65a1b20ae8e809d23af344f256870`  
		Last Modified: Sat, 06 Mar 2021 01:45:28 GMT  
		Size: 47.7 MB (47745188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774a49a57fafa127daa510c9429107ccffb5b50b021f7e5bb7aa325d75ae392`  
		Last Modified: Sat, 06 Mar 2021 01:45:14 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0`

```console
$ docker pull kong@sha256:3747b66a12d7184dbdffa8f98c74340afd1787c9b301b2ac8a9ed8a668c3f86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0` - linux; amd64

```console
$ docker pull kong@sha256:0024877dff8be1510c4855bcd176da7fecd11b9ed187854cf56f5d87a83c9aa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52768674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05c524842da1936ef115fe6f9f7e39c9878811fbce5fbedb27e1350982f1d0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:30:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:30:26 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:30:26 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:06 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 07:36:07 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:07 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:07 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Sat, 06 Mar 2021 07:36:07 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Sat, 06 Mar 2021 07:36:13 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Sat, 06 Mar 2021 07:36:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:14 GMT
USER kong
# Sat, 06 Mar 2021 07:36:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1e69fd16601ced6ecdaa4df44ff2ca6f3206a042c14b0c1bc8ea7b114312c1`  
		Last Modified: Sat, 06 Mar 2021 07:42:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933198aa9c2cade757bf5113bd79091805253992a1056ffb9e463b2312b137cd`  
		Last Modified: Sat, 06 Mar 2021 07:42:14 GMT  
		Size: 50.0 MB (49952498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d544fe16cf0f404353f729264844bc9f66f5b1394fa1b7aef56322d74fa3d065`  
		Last Modified: Sat, 06 Mar 2021 07:42:06 GMT  
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
$ docker pull kong@sha256:3fa9a297ef0e66ee36125ed198cbfc309fa9a14280a915b2ce41b655cf304993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:972fb003d4c4894191cd4f32c6148fa830d3398ef10363ceed4cce30312e83ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101036455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3625771b6e687f6d7ff4bfc069f25e3085a8f700414d79f5aee2e89fc17ace`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:30:42 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:30:42 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:18 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Sat, 06 Mar 2021 07:36:18 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:18 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:38 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 06 Mar 2021 07:36:39 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:39 GMT
USER kong
# Sat, 06 Mar 2021 07:36:41 GMT
RUN kong version
# Sat, 06 Mar 2021 07:36:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:41 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:41 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ca137416ac8c1d18dc6634771ff578a89f2731ba0414ff8e5c56f6a1cf3b5a`  
		Last Modified: Sat, 06 Mar 2021 07:42:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e3f2f13cc7cc9a443eeba1aa34f5299ccbec53ed3f4ea8ed2dc7abcf39030`  
		Last Modified: Sat, 06 Mar 2021 07:42:39 GMT  
		Size: 55.1 MB (55071644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c81747f3c72bfb8b53d8a7068788ef87de2c0f033b608b210c6e15e6548d436`  
		Last Modified: Sat, 06 Mar 2021 07:42:28 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639e00eebee70193da0f8c81f68dd6556f37e10c28db8d045cafaab2b3a8ba3d`  
		Last Modified: Sat, 06 Mar 2021 07:42:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2705e7dd0518af4a9c38edfd1092c04dbfbca05e3266383095e2e207ddfc1709
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93072709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47010f98eaabc4154f806c853cc83f2e95bb370fdfbe068b7e5e7cc58cfd7459`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:35:48 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 21 Jan 2021 05:35:49 GMT
ARG KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 05:35:50 GMT
ENV KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 05:36:31 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 21 Jan 2021 05:36:33 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:36:34 GMT
USER kong
# Thu, 21 Jan 2021 05:36:36 GMT
RUN kong version
# Thu, 21 Jan 2021 05:36:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:36:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:36:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:36:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e364343239094535f14c35ef5e131471b966188de44b93aeede0e05b1846721e`  
		Last Modified: Thu, 21 Jan 2021 05:38:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0eac08498e298b622e08a7f87cd69a82817a5ace2acebed22998cd9e1b4fce`  
		Last Modified: Thu, 21 Jan 2021 05:39:00 GMT  
		Size: 52.2 MB (52185091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff3d4450827002eb8ce5cfc3c6b803a2b4c617fb6dd4c9394aefd07a3c80ed0`  
		Last Modified: Thu, 21 Jan 2021 05:38:47 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858413272bc97018762df0a5c950702d25874f24c3830eb17215363a0e826b7`  
		Last Modified: Thu, 21 Jan 2021 05:38:48 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5`

```console
$ docker pull kong@sha256:3747b66a12d7184dbdffa8f98c74340afd1787c9b301b2ac8a9ed8a668c3f86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5` - linux; amd64

```console
$ docker pull kong@sha256:0024877dff8be1510c4855bcd176da7fecd11b9ed187854cf56f5d87a83c9aa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52768674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05c524842da1936ef115fe6f9f7e39c9878811fbce5fbedb27e1350982f1d0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:30:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:30:26 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:30:26 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:06 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 07:36:07 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:07 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:07 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Sat, 06 Mar 2021 07:36:07 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Sat, 06 Mar 2021 07:36:13 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Sat, 06 Mar 2021 07:36:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:14 GMT
USER kong
# Sat, 06 Mar 2021 07:36:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1e69fd16601ced6ecdaa4df44ff2ca6f3206a042c14b0c1bc8ea7b114312c1`  
		Last Modified: Sat, 06 Mar 2021 07:42:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933198aa9c2cade757bf5113bd79091805253992a1056ffb9e463b2312b137cd`  
		Last Modified: Sat, 06 Mar 2021 07:42:14 GMT  
		Size: 50.0 MB (49952498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d544fe16cf0f404353f729264844bc9f66f5b1394fa1b7aef56322d74fa3d065`  
		Last Modified: Sat, 06 Mar 2021 07:42:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-alpine`

```console
$ docker pull kong@sha256:3747b66a12d7184dbdffa8f98c74340afd1787c9b301b2ac8a9ed8a668c3f86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-alpine` - linux; amd64

```console
$ docker pull kong@sha256:0024877dff8be1510c4855bcd176da7fecd11b9ed187854cf56f5d87a83c9aa6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52768674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05c524842da1936ef115fe6f9f7e39c9878811fbce5fbedb27e1350982f1d0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:30:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:30:26 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:30:26 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:06 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 07:36:07 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:07 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:07 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Sat, 06 Mar 2021 07:36:07 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Sat, 06 Mar 2021 07:36:13 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Sat, 06 Mar 2021 07:36:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:14 GMT
USER kong
# Sat, 06 Mar 2021 07:36:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:14 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1e69fd16601ced6ecdaa4df44ff2ca6f3206a042c14b0c1bc8ea7b114312c1`  
		Last Modified: Sat, 06 Mar 2021 07:42:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933198aa9c2cade757bf5113bd79091805253992a1056ffb9e463b2312b137cd`  
		Last Modified: Sat, 06 Mar 2021 07:42:14 GMT  
		Size: 50.0 MB (49952498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d544fe16cf0f404353f729264844bc9f66f5b1394fa1b7aef56322d74fa3d065`  
		Last Modified: Sat, 06 Mar 2021 07:42:06 GMT  
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
$ docker pull kong@sha256:3fa9a297ef0e66ee36125ed198cbfc309fa9a14280a915b2ce41b655cf304993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:972fb003d4c4894191cd4f32c6148fa830d3398ef10363ceed4cce30312e83ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.0 MB (101036455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3625771b6e687f6d7ff4bfc069f25e3085a8f700414d79f5aee2e89fc17ace`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:39:31 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 21 Jan 2021 03:39:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:39:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:39:35 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:39:36 GMT
CMD ["/bin/bash"]
# Sat, 06 Mar 2021 07:30:42 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:30:42 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:36:18 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Sat, 06 Mar 2021 07:36:18 GMT
ARG KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:18 GMT
ENV KONG_VERSION=2.0.5
# Sat, 06 Mar 2021 07:36:38 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 06 Mar 2021 07:36:39 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:36:39 GMT
USER kong
# Sat, 06 Mar 2021 07:36:41 GMT
RUN kong version
# Sat, 06 Mar 2021 07:36:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:36:41 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:36:41 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:36:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfa26c6b9c9d1ccbcb1eaa65befa376805d9324174ac580ca76fdedc3575f54`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7bf18aa406cb7dc372ac732de222b04d1c824ff1705d8900831c3d1361ff5`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ec688ebe374ea7d89ce967576d221a177ebd2c02ca9f053197f954102e30b`  
		Last Modified: Thu, 21 Jan 2021 03:41:24 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ca137416ac8c1d18dc6634771ff578a89f2731ba0414ff8e5c56f6a1cf3b5a`  
		Last Modified: Sat, 06 Mar 2021 07:42:28 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e3f2f13cc7cc9a443eeba1aa34f5299ccbec53ed3f4ea8ed2dc7abcf39030`  
		Last Modified: Sat, 06 Mar 2021 07:42:39 GMT  
		Size: 55.1 MB (55071644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c81747f3c72bfb8b53d8a7068788ef87de2c0f033b608b210c6e15e6548d436`  
		Last Modified: Sat, 06 Mar 2021 07:42:28 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639e00eebee70193da0f8c81f68dd6556f37e10c28db8d045cafaab2b3a8ba3d`  
		Last Modified: Sat, 06 Mar 2021 07:42:28 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.0.5-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:2705e7dd0518af4a9c38edfd1092c04dbfbca05e3266383095e2e207ddfc1709
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93072709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47010f98eaabc4154f806c853cc83f2e95bb370fdfbe068b7e5e7cc58cfd7459`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:35:48 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 21 Jan 2021 05:35:49 GMT
ARG KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 05:35:50 GMT
ENV KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 05:36:31 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 21 Jan 2021 05:36:33 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:36:34 GMT
USER kong
# Thu, 21 Jan 2021 05:36:36 GMT
RUN kong version
# Thu, 21 Jan 2021 05:36:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:36:37 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:36:38 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:36:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e364343239094535f14c35ef5e131471b966188de44b93aeede0e05b1846721e`  
		Last Modified: Thu, 21 Jan 2021 05:38:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0eac08498e298b622e08a7f87cd69a82817a5ace2acebed22998cd9e1b4fce`  
		Last Modified: Thu, 21 Jan 2021 05:39:00 GMT  
		Size: 52.2 MB (52185091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff3d4450827002eb8ce5cfc3c6b803a2b4c617fb6dd4c9394aefd07a3c80ed0`  
		Last Modified: Thu, 21 Jan 2021 05:38:47 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b858413272bc97018762df0a5c950702d25874f24c3830eb17215363a0e826b7`  
		Last Modified: Thu, 21 Jan 2021 05:38:48 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1`

```console
$ docker pull kong@sha256:e96e5d22dfe40ad5400fe3709697debc91cbca23cfca8c7f4a829d9bd39b4c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1` - linux; amd64

```console
$ docker pull kong@sha256:3a2dd5541ea54b820ae18e3a52953249af81a412863c3260b452079aaa238e8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53154863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c8ec3d8433d33a9152c8a12d74feb4bb327f3d490539d07f4e1deb8d6b9ad8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Sat, 06 Mar 2021 07:30:26 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 06 Mar 2021 07:30:26 GMT
ARG ASSET=ce
# Sat, 06 Mar 2021 07:30:26 GMT
ENV ASSET=ce
# Sat, 06 Mar 2021 07:30:26 GMT
ARG EE_PORTS
# Sat, 06 Mar 2021 07:30:27 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 07:34:48 GMT
ARG KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:34:49 GMT
ENV KONG_VERSION=2.1.4
# Sat, 06 Mar 2021 07:34:54 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 06 Mar 2021 07:34:55 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 07:34:55 GMT
USER kong
# Sat, 06 Mar 2021 07:34:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 07:34:56 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 07:34:56 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 07:34:56 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caafd1a253b0f537460746cdcf3618b9f1b7018ee9fd49fc3afe37a66e4148c5`  
		Last Modified: Sat, 06 Mar 2021 07:38:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe94a89771990b9bd9518673a0985ec8a3eb82bad3b20a86c6c79a07bd399f1`  
		Last Modified: Sat, 06 Mar 2021 07:41:00 GMT  
		Size: 50.3 MB (50338685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9108ed2eb389d0d860338cadae0fdef9d5ce7108d1ed7ddfb25fc0c51a1c3de`  
		Last Modified: Sat, 06 Mar 2021 07:40:51 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a940ff2f448a784ceb25388d1bafe3c4ea3e4b0404acd46b4f184ea2b595c895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52667459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0856d3faf7443df0af02626c8a0d0670511fb1d7f5cca8d56d46fc0efacb6d5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:35:36 GMT
ARG KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:35:37 GMT
ENV KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:35:56 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 24 Feb 2021 23:35:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:36:00 GMT
USER kong
# Wed, 24 Feb 2021 23:36:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:36:02 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:36:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:36:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4849364d30998f9fd8405748f2decd10c7941f71159fb050584735d5de1f5b64`  
		Last Modified: Wed, 24 Feb 2021 23:38:11 GMT  
		Size: 49.9 MB (49940779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5081e391f6090fde1d389758e314d13ca936444f377e624c9d767f2618f45b57`  
		Last Modified: Wed, 24 Feb 2021 23:37:55 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-alpine`

```console
$ docker pull kong@sha256:f154aa8473f597414e7f894047b10290b112a97ae6ac37b963995e66c3441d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:0291873762bc2cb62109099ddc7426a45d6d15fe474efedbf9cafbd4ae7a1c0a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53155863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c42c67e8a0a98d879c81a6da7729f0443f826e13e156a1a8a7e047e6f47e07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:50:23 GMT
ARG KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:23 GMT
ENV KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:29 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Fri, 26 Mar 2021 07:50:29 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:29 GMT
USER kong
# Fri, 26 Mar 2021 07:50:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:30 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009c6cd9d98bb440f21a4bfe413fc0fd62b6f1cdea19592be57792d094d293`  
		Last Modified: Fri, 26 Mar 2021 07:54:13 GMT  
		Size: 50.3 MB (50339667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220a43c03d423d33880c2144f3d4731b03933152d45215c4f7fb022980d2ce7`  
		Last Modified: Fri, 26 Mar 2021 07:54:05 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a940ff2f448a784ceb25388d1bafe3c4ea3e4b0404acd46b4f184ea2b595c895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52667459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0856d3faf7443df0af02626c8a0d0670511fb1d7f5cca8d56d46fc0efacb6d5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:35:36 GMT
ARG KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:35:37 GMT
ENV KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:35:56 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 24 Feb 2021 23:35:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:36:00 GMT
USER kong
# Wed, 24 Feb 2021 23:36:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:36:02 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:36:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:36:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4849364d30998f9fd8405748f2decd10c7941f71159fb050584735d5de1f5b64`  
		Last Modified: Wed, 24 Feb 2021 23:38:11 GMT  
		Size: 49.9 MB (49940779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5081e391f6090fde1d389758e314d13ca936444f377e624c9d767f2618f45b57`  
		Last Modified: Wed, 24 Feb 2021 23:37:55 GMT  
		Size: 733.0 B  
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
$ docker pull kong@sha256:2996a43ccd31eef4663ab675a796f0232e3af5171a910a33c2fe864b3094fc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5980a8a059ae11cb6db58faef722ad8f03556259598f9632012f3796cc32df53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133894593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea0d7858cc558c8dc74aca701c77f2810f3cb8cedf4e93f82a553b969f57e2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:50:34 GMT
ARG KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:34 GMT
ENV KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:53 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:50:54 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:54 GMT
USER kong
# Fri, 26 Mar 2021 07:50:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:55 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3eb698e6d02079dc8282f61c17f743abcbdc0200517a88d1ee48be67432d58`  
		Last Modified: Fri, 26 Mar 2021 07:54:39 GMT  
		Size: 62.8 MB (62848061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c792b7a3ce2c394da24736e516c7d3f00ae35fe543bc80b60d4f71168ab806c`  
		Last Modified: Fri, 26 Mar 2021 07:54:28 GMT  
		Size: 686.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:49baf2f4e15be6f983e1c64447cac8320374e4febeecdb236d31baf651756995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125199807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1fde0c7a655bd82a5ce2e18ae7ffa4d9ed68905b1182906263de7418295374`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 21 Jan 2021 05:34:29 GMT
ARG KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 05:34:30 GMT
ENV KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 05:35:34 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 21 Jan 2021 05:35:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:35:38 GMT
USER kong
# Thu, 21 Jan 2021 05:35:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:35:39 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:35:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:35:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac4802aab8eabcd73e4641d6fe9c881be6b1d4564d4e3908ac28ae82444846f`  
		Last Modified: Thu, 21 Jan 2021 05:38:36 GMT  
		Size: 59.2 MB (59230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6220a51772734a4fe75e8179450595e1682af3caec53ce05dd7891e8accb5811`  
		Last Modified: Thu, 21 Jan 2021 05:38:20 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4`

```console
$ docker pull kong@sha256:f154aa8473f597414e7f894047b10290b112a97ae6ac37b963995e66c3441d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4` - linux; amd64

```console
$ docker pull kong@sha256:0291873762bc2cb62109099ddc7426a45d6d15fe474efedbf9cafbd4ae7a1c0a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53155863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c42c67e8a0a98d879c81a6da7729f0443f826e13e156a1a8a7e047e6f47e07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:50:23 GMT
ARG KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:23 GMT
ENV KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:29 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Fri, 26 Mar 2021 07:50:29 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:29 GMT
USER kong
# Fri, 26 Mar 2021 07:50:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:30 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009c6cd9d98bb440f21a4bfe413fc0fd62b6f1cdea19592be57792d094d293`  
		Last Modified: Fri, 26 Mar 2021 07:54:13 GMT  
		Size: 50.3 MB (50339667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220a43c03d423d33880c2144f3d4731b03933152d45215c4f7fb022980d2ce7`  
		Last Modified: Fri, 26 Mar 2021 07:54:05 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a940ff2f448a784ceb25388d1bafe3c4ea3e4b0404acd46b4f184ea2b595c895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52667459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0856d3faf7443df0af02626c8a0d0670511fb1d7f5cca8d56d46fc0efacb6d5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:35:36 GMT
ARG KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:35:37 GMT
ENV KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:35:56 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 24 Feb 2021 23:35:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:36:00 GMT
USER kong
# Wed, 24 Feb 2021 23:36:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:36:02 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:36:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:36:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4849364d30998f9fd8405748f2decd10c7941f71159fb050584735d5de1f5b64`  
		Last Modified: Wed, 24 Feb 2021 23:38:11 GMT  
		Size: 49.9 MB (49940779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5081e391f6090fde1d389758e314d13ca936444f377e624c9d767f2618f45b57`  
		Last Modified: Wed, 24 Feb 2021 23:37:55 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-alpine`

```console
$ docker pull kong@sha256:f154aa8473f597414e7f894047b10290b112a97ae6ac37b963995e66c3441d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:0291873762bc2cb62109099ddc7426a45d6d15fe474efedbf9cafbd4ae7a1c0a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53155863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c42c67e8a0a98d879c81a6da7729f0443f826e13e156a1a8a7e047e6f47e07`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:50:23 GMT
ARG KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:23 GMT
ENV KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:29 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Fri, 26 Mar 2021 07:50:29 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:29 GMT
USER kong
# Fri, 26 Mar 2021 07:50:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:30 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52009c6cd9d98bb440f21a4bfe413fc0fd62b6f1cdea19592be57792d094d293`  
		Last Modified: Fri, 26 Mar 2021 07:54:13 GMT  
		Size: 50.3 MB (50339667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220a43c03d423d33880c2144f3d4731b03933152d45215c4f7fb022980d2ce7`  
		Last Modified: Fri, 26 Mar 2021 07:54:05 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a940ff2f448a784ceb25388d1bafe3c4ea3e4b0404acd46b4f184ea2b595c895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52667459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0856d3faf7443df0af02626c8a0d0670511fb1d7f5cca8d56d46fc0efacb6d5e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:35:36 GMT
ARG KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:35:37 GMT
ENV KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:35:56 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 24 Feb 2021 23:35:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:36:00 GMT
USER kong
# Wed, 24 Feb 2021 23:36:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:36:02 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:36:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:36:04 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4849364d30998f9fd8405748f2decd10c7941f71159fb050584735d5de1f5b64`  
		Last Modified: Wed, 24 Feb 2021 23:38:11 GMT  
		Size: 49.9 MB (49940779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5081e391f6090fde1d389758e314d13ca936444f377e624c9d767f2618f45b57`  
		Last Modified: Wed, 24 Feb 2021 23:37:55 GMT  
		Size: 733.0 B  
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
$ docker pull kong@sha256:2996a43ccd31eef4663ab675a796f0232e3af5171a910a33c2fe864b3094fc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5980a8a059ae11cb6db58faef722ad8f03556259598f9632012f3796cc32df53
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133894593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea0d7858cc558c8dc74aca701c77f2810f3cb8cedf4e93f82a553b969f57e2b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:50:34 GMT
ARG KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:34 GMT
ENV KONG_VERSION=2.1.4
# Fri, 26 Mar 2021 07:50:53 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:50:54 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:54 GMT
USER kong
# Fri, 26 Mar 2021 07:50:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:55 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:55 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3eb698e6d02079dc8282f61c17f743abcbdc0200517a88d1ee48be67432d58`  
		Last Modified: Fri, 26 Mar 2021 07:54:39 GMT  
		Size: 62.8 MB (62848061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c792b7a3ce2c394da24736e516c7d3f00ae35fe543bc80b60d4f71168ab806c`  
		Last Modified: Fri, 26 Mar 2021 07:54:28 GMT  
		Size: 686.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.1.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:49baf2f4e15be6f983e1c64447cac8320374e4febeecdb236d31baf651756995
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125199807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1fde0c7a655bd82a5ce2e18ae7ffa4d9ed68905b1182906263de7418295374`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 21 Jan 2021 05:34:29 GMT
ARG KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 05:34:30 GMT
ENV KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 05:35:34 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 21 Jan 2021 05:35:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:35:38 GMT
USER kong
# Thu, 21 Jan 2021 05:35:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:35:39 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:35:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:35:40 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac4802aab8eabcd73e4641d6fe9c881be6b1d4564d4e3908ac28ae82444846f`  
		Last Modified: Thu, 21 Jan 2021 05:38:36 GMT  
		Size: 59.2 MB (59230458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6220a51772734a4fe75e8179450595e1682af3caec53ce05dd7891e8accb5811`  
		Last Modified: Thu, 21 Jan 2021 05:38:20 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2`

```console
$ docker pull kong@sha256:10fe9af4273b590d7737a8f0edeafc96dd9b1bb3f1d567158dabe478341e2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2` - linux; amd64

```console
$ docker pull kong@sha256:bd41aba100216eaa2f9acfc710f8f55889391b7fa91b14a20d6b85faf65347f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50918588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bd3d53273b3d3280d938d8362587a3993f3d6b50d203809c09a159a760ddd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:49:44 GMT
ARG KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:44 GMT
ENV KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:44 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Fri, 26 Mar 2021 07:49:44 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Fri, 26 Mar 2021 07:49:45 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Fri, 26 Mar 2021 07:49:45 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Fri, 26 Mar 2021 07:49:50 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:49:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:51 GMT
USER kong
# Fri, 26 Mar 2021 07:49:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:51 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c56f35d152e3281178cfe372ce08d8265b685a2527154c577b44685f1f574`  
		Last Modified: Fri, 26 Mar 2021 07:53:27 GMT  
		Size: 48.1 MB (48102392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7a2040c8a4c617f50183ebe03f7f68919cf8c6680bf0cd59ac5891d3c2a8f9`  
		Last Modified: Fri, 26 Mar 2021 07:53:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a7fc1bbebdd006f69af8d7977c1effd443b75bee5400198f43f1d334a0c59d9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3386f059d95dc9a653b704f92bc3c8d2a3cc75ca18d8eae37f311f6dd753f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 02 Mar 2021 01:05:26 GMT
ARG KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:05:27 GMT
ENV KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:05:28 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Tue, 02 Mar 2021 01:05:28 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Tue, 02 Mar 2021 01:05:29 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Tue, 02 Mar 2021 01:05:30 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Tue, 02 Mar 2021 01:05:43 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 02 Mar 2021 01:05:46 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 02 Mar 2021 01:05:47 GMT
USER kong
# Tue, 02 Mar 2021 01:05:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Mar 2021 01:05:48 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Mar 2021 01:05:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Mar 2021 01:05:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9bb7ecb4911fed3246f81f8a222247dad88542f91481a6b880b169a72386b6`  
		Last Modified: Tue, 02 Mar 2021 01:08:48 GMT  
		Size: 47.7 MB (47710596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ef6f918a74ae67775ac223f6726a2ee9e33b40009317459844fce20afa97f`  
		Last Modified: Tue, 02 Mar 2021 01:08:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-alpine`

```console
$ docker pull kong@sha256:10fe9af4273b590d7737a8f0edeafc96dd9b1bb3f1d567158dabe478341e2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:bd41aba100216eaa2f9acfc710f8f55889391b7fa91b14a20d6b85faf65347f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50918588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bd3d53273b3d3280d938d8362587a3993f3d6b50d203809c09a159a760ddd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:49:44 GMT
ARG KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:44 GMT
ENV KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:44 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Fri, 26 Mar 2021 07:49:44 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Fri, 26 Mar 2021 07:49:45 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Fri, 26 Mar 2021 07:49:45 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Fri, 26 Mar 2021 07:49:50 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:49:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:51 GMT
USER kong
# Fri, 26 Mar 2021 07:49:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:51 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c56f35d152e3281178cfe372ce08d8265b685a2527154c577b44685f1f574`  
		Last Modified: Fri, 26 Mar 2021 07:53:27 GMT  
		Size: 48.1 MB (48102392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7a2040c8a4c617f50183ebe03f7f68919cf8c6680bf0cd59ac5891d3c2a8f9`  
		Last Modified: Fri, 26 Mar 2021 07:53:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a7fc1bbebdd006f69af8d7977c1effd443b75bee5400198f43f1d334a0c59d9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3386f059d95dc9a653b704f92bc3c8d2a3cc75ca18d8eae37f311f6dd753f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 02 Mar 2021 01:05:26 GMT
ARG KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:05:27 GMT
ENV KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:05:28 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Tue, 02 Mar 2021 01:05:28 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Tue, 02 Mar 2021 01:05:29 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Tue, 02 Mar 2021 01:05:30 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Tue, 02 Mar 2021 01:05:43 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 02 Mar 2021 01:05:46 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 02 Mar 2021 01:05:47 GMT
USER kong
# Tue, 02 Mar 2021 01:05:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Mar 2021 01:05:48 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Mar 2021 01:05:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Mar 2021 01:05:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9bb7ecb4911fed3246f81f8a222247dad88542f91481a6b880b169a72386b6`  
		Last Modified: Tue, 02 Mar 2021 01:08:48 GMT  
		Size: 47.7 MB (47710596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ef6f918a74ae67775ac223f6726a2ee9e33b40009317459844fce20afa97f`  
		Last Modified: Tue, 02 Mar 2021 01:08:34 GMT  
		Size: 733.0 B  
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
$ docker pull kong@sha256:d2b356e70f1422567ea71ba2c3c8b0c3c9e666625589875d7a744edeaa4456f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:633f9725bbb07c54a82dedf2b085e6918ae968e3f8244c8f1f900df7e971fb8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133978267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f5fea5d432a10856a87964116d1dce39dc21c2e2720616aec3f6444e8bfb2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:49:55 GMT
ARG KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:55 GMT
ENV KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:50:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:50:16 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:16 GMT
USER kong
# Fri, 26 Mar 2021 07:50:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:16 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acffd89d236b04f1fc078cc30b74c04a573e16e9430fe4badd7ee208106dad7`  
		Last Modified: Fri, 26 Mar 2021 07:53:53 GMT  
		Size: 62.9 MB (62931733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa38b78d1f6ce40f8dca1891c9a5e4122228c4764d64e7d450dca06a7d9a16a5`  
		Last Modified: Fri, 26 Mar 2021 07:53:42 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6c23c408a685f6ea1a5d4147c37672d50bfd0cad13db46cf3eb668f329cf9f67
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125313399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f7aae149cd0de107495cf4ec47a1de269c1f3cf1feb61c4cf816dfc52304ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Mar 2021 01:06:13 GMT
ARG KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:06:14 GMT
ENV KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:07:33 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Tue, 02 Mar 2021 01:07:35 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Tue, 02 Mar 2021 01:07:36 GMT
USER kong
# Tue, 02 Mar 2021 01:07:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Mar 2021 01:07:37 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Mar 2021 01:07:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Mar 2021 01:07:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbe89e14a980b1beac708e2a9316b0a92318359dc549fea9705c13c9975d101`  
		Last Modified: Tue, 02 Mar 2021 01:09:21 GMT  
		Size: 59.3 MB (59344049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb25e8d274e645369666fb60d5a19c9ad4fcf8970d03f7a468339c980c10c47`  
		Last Modified: Tue, 02 Mar 2021 01:09:02 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2`

```console
$ docker pull kong@sha256:10fe9af4273b590d7737a8f0edeafc96dd9b1bb3f1d567158dabe478341e2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2` - linux; amd64

```console
$ docker pull kong@sha256:bd41aba100216eaa2f9acfc710f8f55889391b7fa91b14a20d6b85faf65347f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50918588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bd3d53273b3d3280d938d8362587a3993f3d6b50d203809c09a159a760ddd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:49:44 GMT
ARG KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:44 GMT
ENV KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:44 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Fri, 26 Mar 2021 07:49:44 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Fri, 26 Mar 2021 07:49:45 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Fri, 26 Mar 2021 07:49:45 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Fri, 26 Mar 2021 07:49:50 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:49:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:51 GMT
USER kong
# Fri, 26 Mar 2021 07:49:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:51 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c56f35d152e3281178cfe372ce08d8265b685a2527154c577b44685f1f574`  
		Last Modified: Fri, 26 Mar 2021 07:53:27 GMT  
		Size: 48.1 MB (48102392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7a2040c8a4c617f50183ebe03f7f68919cf8c6680bf0cd59ac5891d3c2a8f9`  
		Last Modified: Fri, 26 Mar 2021 07:53:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a7fc1bbebdd006f69af8d7977c1effd443b75bee5400198f43f1d334a0c59d9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3386f059d95dc9a653b704f92bc3c8d2a3cc75ca18d8eae37f311f6dd753f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 02 Mar 2021 01:05:26 GMT
ARG KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:05:27 GMT
ENV KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:05:28 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Tue, 02 Mar 2021 01:05:28 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Tue, 02 Mar 2021 01:05:29 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Tue, 02 Mar 2021 01:05:30 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Tue, 02 Mar 2021 01:05:43 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 02 Mar 2021 01:05:46 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 02 Mar 2021 01:05:47 GMT
USER kong
# Tue, 02 Mar 2021 01:05:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Mar 2021 01:05:48 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Mar 2021 01:05:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Mar 2021 01:05:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9bb7ecb4911fed3246f81f8a222247dad88542f91481a6b880b169a72386b6`  
		Last Modified: Tue, 02 Mar 2021 01:08:48 GMT  
		Size: 47.7 MB (47710596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ef6f918a74ae67775ac223f6726a2ee9e33b40009317459844fce20afa97f`  
		Last Modified: Tue, 02 Mar 2021 01:08:34 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2-alpine`

```console
$ docker pull kong@sha256:10fe9af4273b590d7737a8f0edeafc96dd9b1bb3f1d567158dabe478341e2e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:bd41aba100216eaa2f9acfc710f8f55889391b7fa91b14a20d6b85faf65347f5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50918588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bd3d53273b3d3280d938d8362587a3993f3d6b50d203809c09a159a760ddd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:49:44 GMT
ARG KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:44 GMT
ENV KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:44 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Fri, 26 Mar 2021 07:49:44 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Fri, 26 Mar 2021 07:49:45 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Fri, 26 Mar 2021 07:49:45 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Fri, 26 Mar 2021 07:49:50 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:49:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:51 GMT
USER kong
# Fri, 26 Mar 2021 07:49:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:51 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916c56f35d152e3281178cfe372ce08d8265b685a2527154c577b44685f1f574`  
		Last Modified: Fri, 26 Mar 2021 07:53:27 GMT  
		Size: 48.1 MB (48102392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7a2040c8a4c617f50183ebe03f7f68919cf8c6680bf0cd59ac5891d3c2a8f9`  
		Last Modified: Fri, 26 Mar 2021 07:53:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:a7fc1bbebdd006f69af8d7977c1effd443b75bee5400198f43f1d334a0c59d9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3386f059d95dc9a653b704f92bc3c8d2a3cc75ca18d8eae37f311f6dd753f68`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Tue, 02 Mar 2021 01:05:26 GMT
ARG KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:05:27 GMT
ENV KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:05:28 GMT
ARG KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Tue, 02 Mar 2021 01:05:28 GMT
ENV KONG_AMD64_SHA=f5e635e4241c3ad6943ff08724a363af430f7372a6d6e2892223dc2e3f9e01a7
# Tue, 02 Mar 2021 01:05:29 GMT
ARG KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Tue, 02 Mar 2021 01:05:30 GMT
ENV KONG_ARM64_SHA=435d8cd377978fbdde06e602e39584b17db832a154b5d80aa83a69c59aca9f70
# Tue, 02 Mar 2021 01:05:43 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Tue, 02 Mar 2021 01:05:46 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Tue, 02 Mar 2021 01:05:47 GMT
USER kong
# Tue, 02 Mar 2021 01:05:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Mar 2021 01:05:48 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Mar 2021 01:05:49 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Mar 2021 01:05:49 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9bb7ecb4911fed3246f81f8a222247dad88542f91481a6b880b169a72386b6`  
		Last Modified: Tue, 02 Mar 2021 01:08:48 GMT  
		Size: 47.7 MB (47710596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ef6f918a74ae67775ac223f6726a2ee9e33b40009317459844fce20afa97f`  
		Last Modified: Tue, 02 Mar 2021 01:08:34 GMT  
		Size: 733.0 B  
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
$ docker pull kong@sha256:d2b356e70f1422567ea71ba2c3c8b0c3c9e666625589875d7a744edeaa4456f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:633f9725bbb07c54a82dedf2b085e6918ae968e3f8244c8f1f900df7e971fb8a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133978267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f5fea5d432a10856a87964116d1dce39dc21c2e2720616aec3f6444e8bfb2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:49:55 GMT
ARG KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:49:55 GMT
ENV KONG_VERSION=2.2.2
# Fri, 26 Mar 2021 07:50:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:50:16 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:50:16 GMT
USER kong
# Fri, 26 Mar 2021 07:50:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:50:16 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:50:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:50:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2acffd89d236b04f1fc078cc30b74c04a573e16e9430fe4badd7ee208106dad7`  
		Last Modified: Fri, 26 Mar 2021 07:53:53 GMT  
		Size: 62.9 MB (62931733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa38b78d1f6ce40f8dca1891c9a5e4122228c4764d64e7d450dca06a7d9a16a5`  
		Last Modified: Fri, 26 Mar 2021 07:53:42 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:6c23c408a685f6ea1a5d4147c37672d50bfd0cad13db46cf3eb668f329cf9f67
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125313399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f7aae149cd0de107495cf4ec47a1de269c1f3cf1feb61c4cf816dfc52304ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 02 Mar 2021 01:06:13 GMT
ARG KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:06:14 GMT
ENV KONG_VERSION=2.2.2
# Tue, 02 Mar 2021 01:07:33 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Tue, 02 Mar 2021 01:07:35 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Tue, 02 Mar 2021 01:07:36 GMT
USER kong
# Tue, 02 Mar 2021 01:07:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 02 Mar 2021 01:07:37 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 02 Mar 2021 01:07:38 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Mar 2021 01:07:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbe89e14a980b1beac708e2a9316b0a92318359dc549fea9705c13c9975d101`  
		Last Modified: Tue, 02 Mar 2021 01:09:21 GMT  
		Size: 59.3 MB (59344049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb25e8d274e645369666fb60d5a19c9ad4fcf8970d03f7a468339c980c10c47`  
		Last Modified: Tue, 02 Mar 2021 01:09:02 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3`

```console
$ docker pull kong@sha256:798f1fc874cc7157b6092c436cb942a3745e4d6407c3872119fcdb0515ea9702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3` - linux; amd64

```console
$ docker pull kong@sha256:ebf7a6bd5286c8a35a43e0319234223f1dab538eaf7ddc4460cb761f77255e94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a725b7188db8b6e051470f65257a09c6adb6eeda641ac94e163f43a1ed9db97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:24 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:48:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:48:25 GMT
USER kong
# Fri, 26 Mar 2021 07:48:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:48:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:48:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:48:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540296b44621f22ceab619f6568a09362c6af52dd52adcb6dbe99b65216ddcd0`  
		Last Modified: Fri, 26 Mar 2021 07:52:26 GMT  
		Size: 48.1 MB (48136467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a7f2c520645fdd219038f92d6842bbe8f8f19a9735fbe6c23d963d8517de7b`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:06d53a9dcefe213fd6ebd9a25fc1ab7a86b5174de27a7c36c410b8093754ea38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50471868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8e3ebeb8b18ec45885f8e5b7f6c43f0395a8b2eb596e5555f8c8df67c9b3ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 01:42:55 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:57 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:58 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:42:59 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:43:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 06 Mar 2021 01:43:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:43:13 GMT
USER kong
# Sat, 06 Mar 2021 01:43:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:43:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:43:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:43:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1b9581057bb8e89fbda6e9096550d10fd65a1b20ae8e809d23af344f256870`  
		Last Modified: Sat, 06 Mar 2021 01:45:28 GMT  
		Size: 47.7 MB (47745188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774a49a57fafa127daa510c9429107ccffb5b50b021f7e5bb7aa325d75ae392`  
		Last Modified: Sat, 06 Mar 2021 01:45:14 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-alpine`

```console
$ docker pull kong@sha256:798f1fc874cc7157b6092c436cb942a3745e4d6407c3872119fcdb0515ea9702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:ebf7a6bd5286c8a35a43e0319234223f1dab538eaf7ddc4460cb761f77255e94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a725b7188db8b6e051470f65257a09c6adb6eeda641ac94e163f43a1ed9db97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:24 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:48:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:48:25 GMT
USER kong
# Fri, 26 Mar 2021 07:48:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:48:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:48:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:48:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540296b44621f22ceab619f6568a09362c6af52dd52adcb6dbe99b65216ddcd0`  
		Last Modified: Fri, 26 Mar 2021 07:52:26 GMT  
		Size: 48.1 MB (48136467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a7f2c520645fdd219038f92d6842bbe8f8f19a9735fbe6c23d963d8517de7b`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:06d53a9dcefe213fd6ebd9a25fc1ab7a86b5174de27a7c36c410b8093754ea38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50471868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8e3ebeb8b18ec45885f8e5b7f6c43f0395a8b2eb596e5555f8c8df67c9b3ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 01:42:55 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:57 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:58 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:42:59 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:43:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 06 Mar 2021 01:43:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:43:13 GMT
USER kong
# Sat, 06 Mar 2021 01:43:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:43:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:43:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:43:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1b9581057bb8e89fbda6e9096550d10fd65a1b20ae8e809d23af344f256870`  
		Last Modified: Sat, 06 Mar 2021 01:45:28 GMT  
		Size: 47.7 MB (47745188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774a49a57fafa127daa510c9429107ccffb5b50b021f7e5bb7aa325d75ae392`  
		Last Modified: Sat, 06 Mar 2021 01:45:14 GMT  
		Size: 733.0 B  
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
$ docker pull kong@sha256:a7722ab924713f2dde2dd2f12c26b5e99e9fc040c2753ef7d3a747575903cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:04e830cc5adbbfb8e410ec41a12454718130286c852ba404b2db483cc6c1cbd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3547c5f087a61cfde7927c87c52a4c5d071419dea63f34506bc8f0dffa095dce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:48:31 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:31 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:49:36 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:49:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:37 GMT
USER kong
# Fri, 26 Mar 2021 07:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:38 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164fd2e347006e7ea5368a6c544a851ff1023b68f35f01273e4ba5ff69377b3`  
		Last Modified: Fri, 26 Mar 2021 07:53:04 GMT  
		Size: 63.0 MB (62965553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69b3edcd0e49b2e0fbd0d8fe23549b38d01dcb805d5bd9506133aaecacf86ed`  
		Last Modified: Fri, 26 Mar 2021 07:52:53 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:74f104a8dea77d1504c12ed59a6dbcade78b9810477072df77c566c73258a944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125351993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fadd75ad516e36f3733cb8aa8b1234aa7fe4428fbfec68f629a559549d1eee3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 06 Mar 2021 01:43:23 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:43:24 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:44:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Sat, 06 Mar 2021 01:44:18 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:44:19 GMT
USER kong
# Sat, 06 Mar 2021 01:44:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:44:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:44:20 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:44:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6a000ab4c5dba26b3a2a9b2ff40ad15c5bd087547d4ead387e544dd4994fb`  
		Last Modified: Sat, 06 Mar 2021 01:45:56 GMT  
		Size: 59.4 MB (59382644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de241f277a6749a12c8e5e7be3a45d232043c0249227796c146b22f18249833`  
		Last Modified: Sat, 06 Mar 2021 01:45:40 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3`

```console
$ docker pull kong@sha256:798f1fc874cc7157b6092c436cb942a3745e4d6407c3872119fcdb0515ea9702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3` - linux; amd64

```console
$ docker pull kong@sha256:ebf7a6bd5286c8a35a43e0319234223f1dab538eaf7ddc4460cb761f77255e94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a725b7188db8b6e051470f65257a09c6adb6eeda641ac94e163f43a1ed9db97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:24 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:48:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:48:25 GMT
USER kong
# Fri, 26 Mar 2021 07:48:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:48:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:48:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:48:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540296b44621f22ceab619f6568a09362c6af52dd52adcb6dbe99b65216ddcd0`  
		Last Modified: Fri, 26 Mar 2021 07:52:26 GMT  
		Size: 48.1 MB (48136467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a7f2c520645fdd219038f92d6842bbe8f8f19a9735fbe6c23d963d8517de7b`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:06d53a9dcefe213fd6ebd9a25fc1ab7a86b5174de27a7c36c410b8093754ea38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50471868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8e3ebeb8b18ec45885f8e5b7f6c43f0395a8b2eb596e5555f8c8df67c9b3ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 01:42:55 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:57 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:58 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:42:59 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:43:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 06 Mar 2021 01:43:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:43:13 GMT
USER kong
# Sat, 06 Mar 2021 01:43:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:43:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:43:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:43:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1b9581057bb8e89fbda6e9096550d10fd65a1b20ae8e809d23af344f256870`  
		Last Modified: Sat, 06 Mar 2021 01:45:28 GMT  
		Size: 47.7 MB (47745188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774a49a57fafa127daa510c9429107ccffb5b50b021f7e5bb7aa325d75ae392`  
		Last Modified: Sat, 06 Mar 2021 01:45:14 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.3-alpine`

```console
$ docker pull kong@sha256:798f1fc874cc7157b6092c436cb942a3745e4d6407c3872119fcdb0515ea9702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:ebf7a6bd5286c8a35a43e0319234223f1dab538eaf7ddc4460cb761f77255e94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a725b7188db8b6e051470f65257a09c6adb6eeda641ac94e163f43a1ed9db97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:24 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:48:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:48:25 GMT
USER kong
# Fri, 26 Mar 2021 07:48:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:48:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:48:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:48:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540296b44621f22ceab619f6568a09362c6af52dd52adcb6dbe99b65216ddcd0`  
		Last Modified: Fri, 26 Mar 2021 07:52:26 GMT  
		Size: 48.1 MB (48136467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a7f2c520645fdd219038f92d6842bbe8f8f19a9735fbe6c23d963d8517de7b`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:06d53a9dcefe213fd6ebd9a25fc1ab7a86b5174de27a7c36c410b8093754ea38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50471868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8e3ebeb8b18ec45885f8e5b7f6c43f0395a8b2eb596e5555f8c8df67c9b3ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 01:42:55 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:57 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:58 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:42:59 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:43:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 06 Mar 2021 01:43:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:43:13 GMT
USER kong
# Sat, 06 Mar 2021 01:43:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:43:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:43:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:43:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1b9581057bb8e89fbda6e9096550d10fd65a1b20ae8e809d23af344f256870`  
		Last Modified: Sat, 06 Mar 2021 01:45:28 GMT  
		Size: 47.7 MB (47745188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774a49a57fafa127daa510c9429107ccffb5b50b021f7e5bb7aa325d75ae392`  
		Last Modified: Sat, 06 Mar 2021 01:45:14 GMT  
		Size: 733.0 B  
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
$ docker pull kong@sha256:a7722ab924713f2dde2dd2f12c26b5e99e9fc040c2753ef7d3a747575903cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:04e830cc5adbbfb8e410ec41a12454718130286c852ba404b2db483cc6c1cbd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3547c5f087a61cfde7927c87c52a4c5d071419dea63f34506bc8f0dffa095dce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:48:31 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:31 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:49:36 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:49:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:37 GMT
USER kong
# Fri, 26 Mar 2021 07:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:38 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164fd2e347006e7ea5368a6c544a851ff1023b68f35f01273e4ba5ff69377b3`  
		Last Modified: Fri, 26 Mar 2021 07:53:04 GMT  
		Size: 63.0 MB (62965553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69b3edcd0e49b2e0fbd0d8fe23549b38d01dcb805d5bd9506133aaecacf86ed`  
		Last Modified: Fri, 26 Mar 2021 07:52:53 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:74f104a8dea77d1504c12ed59a6dbcade78b9810477072df77c566c73258a944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125351993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fadd75ad516e36f3733cb8aa8b1234aa7fe4428fbfec68f629a559549d1eee3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 06 Mar 2021 01:43:23 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:43:24 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:44:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Sat, 06 Mar 2021 01:44:18 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:44:19 GMT
USER kong
# Sat, 06 Mar 2021 01:44:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:44:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:44:20 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:44:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6a000ab4c5dba26b3a2a9b2ff40ad15c5bd087547d4ead387e544dd4994fb`  
		Last Modified: Sat, 06 Mar 2021 01:45:56 GMT  
		Size: 59.4 MB (59382644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de241f277a6749a12c8e5e7be3a45d232043c0249227796c146b22f18249833`  
		Last Modified: Sat, 06 Mar 2021 01:45:40 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:798f1fc874cc7157b6092c436cb942a3745e4d6407c3872119fcdb0515ea9702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:ebf7a6bd5286c8a35a43e0319234223f1dab538eaf7ddc4460cb761f77255e94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a725b7188db8b6e051470f65257a09c6adb6eeda641ac94e163f43a1ed9db97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:24 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:48:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:48:25 GMT
USER kong
# Fri, 26 Mar 2021 07:48:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:48:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:48:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:48:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540296b44621f22ceab619f6568a09362c6af52dd52adcb6dbe99b65216ddcd0`  
		Last Modified: Fri, 26 Mar 2021 07:52:26 GMT  
		Size: 48.1 MB (48136467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a7f2c520645fdd219038f92d6842bbe8f8f19a9735fbe6c23d963d8517de7b`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:06d53a9dcefe213fd6ebd9a25fc1ab7a86b5174de27a7c36c410b8093754ea38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50471868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8e3ebeb8b18ec45885f8e5b7f6c43f0395a8b2eb596e5555f8c8df67c9b3ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 01:42:55 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:57 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:58 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:42:59 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:43:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 06 Mar 2021 01:43:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:43:13 GMT
USER kong
# Sat, 06 Mar 2021 01:43:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:43:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:43:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:43:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1b9581057bb8e89fbda6e9096550d10fd65a1b20ae8e809d23af344f256870`  
		Last Modified: Sat, 06 Mar 2021 01:45:28 GMT  
		Size: 47.7 MB (47745188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774a49a57fafa127daa510c9429107ccffb5b50b021f7e5bb7aa325d75ae392`  
		Last Modified: Sat, 06 Mar 2021 01:45:14 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:centos`

```console
$ docker pull kong@sha256:63c7a5459162f96670d69397815c3cf7966f5c4cc65feaafe07051a72e6d2da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

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

## `kong:latest`

```console
$ docker pull kong@sha256:798f1fc874cc7157b6092c436cb942a3745e4d6407c3872119fcdb0515ea9702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:ebf7a6bd5286c8a35a43e0319234223f1dab538eaf7ddc4460cb761f77255e94
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50952661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a725b7188db8b6e051470f65257a09c6adb6eeda641ac94e163f43a1ed9db97`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:43 GMT
ADD file:05adf37fc1a41a31d8e0e0b9371a01161abc0d348adacbc81689a1a34e8fe12d in / 
# Thu, 25 Mar 2021 22:19:43 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 07:48:17 GMT
LABEL maintainer=Kong <support@konghq.com>
# Fri, 26 Mar 2021 07:48:17 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:17 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:17 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Fri, 26 Mar 2021 07:48:18 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:18 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Fri, 26 Mar 2021 07:48:24 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Fri, 26 Mar 2021 07:48:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:48:25 GMT
USER kong
# Fri, 26 Mar 2021 07:48:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:48:25 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:48:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:48:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:839b45e0263abc8ab2dc0bfabc91a19947e932ffbd551a93970ea3ee971eadf6`  
		Last Modified: Thu, 25 Mar 2021 22:20:47 GMT  
		Size: 2.8 MB (2815332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6bb24fb29121870216a8970c53c48eb7a6dc19d419ae6e77ca455ce36bbc93`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540296b44621f22ceab619f6568a09362c6af52dd52adcb6dbe99b65216ddcd0`  
		Last Modified: Fri, 26 Mar 2021 07:52:26 GMT  
		Size: 48.1 MB (48136467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a7f2c520645fdd219038f92d6842bbe8f8f19a9735fbe6c23d963d8517de7b`  
		Last Modified: Fri, 26 Mar 2021 07:52:18 GMT  
		Size: 731.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:06d53a9dcefe213fd6ebd9a25fc1ab7a86b5174de27a7c36c410b8093754ea38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50471868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8e3ebeb8b18ec45885f8e5b7f6c43f0395a8b2eb596e5555f8c8df67c9b3ff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:51 GMT
ADD file:f8a47118a2fe92c166c426620bb4ea0090dbf17aed269177989f6dca70438750 in / 
# Wed, 24 Feb 2021 20:39:52 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:33:46 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:33:46 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:33:47 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:33:48 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:33:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 06 Mar 2021 01:42:55 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:42:56 GMT
ARG KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:57 GMT
ENV KONG_AMD64_SHA=82a4eac75d45a1f2ce65ae185467e20533428b3d368e5e091fe4ddf427296e0b
# Sat, 06 Mar 2021 01:42:58 GMT
ARG KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:42:59 GMT
ENV KONG_ARM64_SHA=b2b8a0fe0cdb81d244e08c23a3143e4ae08b7c771a2cc35e24ffabfc54f4ba60
# Sat, 06 Mar 2021 01:43:11 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 06 Mar 2021 01:43:13 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:43:13 GMT
USER kong
# Sat, 06 Mar 2021 01:43:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:43:15 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:43:15 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:43:16 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:0328c39aea610966704bee2d2a1c7108816950703f98b4585083cd18f8354380`  
		Last Modified: Wed, 24 Feb 2021 20:40:35 GMT  
		Size: 2.7 MB (2725816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd85be744ec3f041627a0878f28833617c9680fc2b1809bb11ef8ddaa9b64a0a`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1b9581057bb8e89fbda6e9096550d10fd65a1b20ae8e809d23af344f256870`  
		Last Modified: Sat, 06 Mar 2021 01:45:28 GMT  
		Size: 47.7 MB (47745188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2774a49a57fafa127daa510c9429107ccffb5b50b021f7e5bb7aa325d75ae392`  
		Last Modified: Sat, 06 Mar 2021 01:45:14 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:a7722ab924713f2dde2dd2f12c26b5e99e9fc040c2753ef7d3a747575903cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:04e830cc5adbbfb8e410ec41a12454718130286c852ba404b2db483cc6c1cbd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134012087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3547c5f087a61cfde7927c87c52a4c5d071419dea63f34506bc8f0dffa095dce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:52 GMT
ADD file:925571658dd8453e5c80d862f5791d6b26b3c2a8688937b11741f2f2c5cdbfd7 in / 
# Thu, 25 Mar 2021 22:33:53 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:54 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 25 Mar 2021 22:33:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 07:48:30 GMT
ARG ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ENV ASSET=ce
# Fri, 26 Mar 2021 07:48:30 GMT
ARG EE_PORTS
# Fri, 26 Mar 2021 07:48:30 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Fri, 26 Mar 2021 07:48:31 GMT
ARG KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:48:31 GMT
ENV KONG_VERSION=2.3.3
# Fri, 26 Mar 2021 07:49:36 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Fri, 26 Mar 2021 07:49:37 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Fri, 26 Mar 2021 07:49:37 GMT
USER kong
# Fri, 26 Mar 2021 07:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 26 Mar 2021 07:49:38 GMT
EXPOSE 8000 8001 8443 8444
# Fri, 26 Mar 2021 07:49:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 07:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:4007a89234b4f56c03e6831dc220550d2e5fba935d9f5f5bcea64857ac4f4888`  
		Last Modified: Mon, 18 Jan 2021 19:38:08 GMT  
		Size: 46.0 MB (45962352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1de0f9cdfc1f9f595acd2ea8724ea92a509d64a6936f0e645c65b504e7e4bc6`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee6ca703b866ac2b74b6129d2db331936292f899e8e3a794474fdf81343605`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 526.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e2761d3d4971e78914857af4c6bd9989873b53426cf2fef3e76983b166fa2`  
		Last Modified: Thu, 25 Mar 2021 22:36:02 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe3258ce31af7e50969b231009f390c1b44a06e5a89da2cc4b60484d2143a9`  
		Last Modified: Fri, 26 Mar 2021 07:52:55 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1164fd2e347006e7ea5368a6c544a851ff1023b68f35f01273e4ba5ff69377b3`  
		Last Modified: Fri, 26 Mar 2021 07:53:04 GMT  
		Size: 63.0 MB (62965553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69b3edcd0e49b2e0fbd0d8fe23549b38d01dcb805d5bd9506133aaecacf86ed`  
		Last Modified: Fri, 26 Mar 2021 07:52:53 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:74f104a8dea77d1504c12ed59a6dbcade78b9810477072df77c566c73258a944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125351993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fadd75ad516e36f3733cb8aa8b1234aa7fe4428fbfec68f629a559549d1eee3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 05:32:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 05:32:06 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 05:32:07 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 06 Mar 2021 01:43:23 GMT
ARG KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:43:24 GMT
ENV KONG_VERSION=2.3.3
# Sat, 06 Mar 2021 01:44:15 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Sat, 06 Mar 2021 01:44:18 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 06 Mar 2021 01:44:19 GMT
USER kong
# Sat, 06 Mar 2021 01:44:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 06 Mar 2021 01:44:20 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 06 Mar 2021 01:44:20 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Mar 2021 01:44:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e81e83cdfa4fc6fce4a28de27bb31753456d14bad0dcc25aabceaa0a03a3345`  
		Last Modified: Thu, 21 Jan 2021 05:37:21 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6a000ab4c5dba26b3a2a9b2ff40ad15c5bd087547d4ead387e544dd4994fb`  
		Last Modified: Sat, 06 Mar 2021 01:45:56 GMT  
		Size: 59.4 MB (59382644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de241f277a6749a12c8e5e7be3a45d232043c0249227796c146b22f18249833`  
		Last Modified: Sat, 06 Mar 2021 01:45:40 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
