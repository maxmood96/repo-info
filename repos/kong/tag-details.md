<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2.4`](#kong24)
-	[`kong:2.4-alpine`](#kong24-alpine)
-	[`kong:2.4-centos`](#kong24-centos)
-	[`kong:2.4-ubuntu`](#kong24-ubuntu)
-	[`kong:2.4.1`](#kong241)
-	[`kong:2.4.1-alpine`](#kong241-alpine)
-	[`kong:2.4.1-centos`](#kong241-centos)
-	[`kong:2.4.1-ubuntu`](#kong241-ubuntu)
-	[`kong:2.5`](#kong25)
-	[`kong:2.5-centos`](#kong25-centos)
-	[`kong:2.5-ubuntu`](#kong25-ubuntu)
-	[`kong:2.5.1`](#kong251)
-	[`kong:2.5.1-alpine`](#kong251-alpine)
-	[`kong:2.5.1-centos`](#kong251-centos)
-	[`kong:2.5.1-ubuntu`](#kong251-ubuntu)
-	[`kong:2.6`](#kong26)
-	[`kong:2.6-centos`](#kong26-centos)
-	[`kong:2.6-ubuntu`](#kong26-ubuntu)
-	[`kong:2.6.0`](#kong260)
-	[`kong:2.6.0-alpine`](#kong260-alpine)
-	[`kong:2.6.0-centos`](#kong260-centos)
-	[`kong:2.6.0-ubuntu`](#kong260-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:centos`](#kongcentos)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2.4`

```console
$ docker pull kong@sha256:aad8b5ca5ad388dec99b2d9c4ab9242352d71f1ddc9250d522fc00f121ee9776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4` - linux; amd64

```console
$ docker pull kong@sha256:fd512d0444c67558130f975441a5b1e20b3a7540fe4344c17f8ea69164d4a15d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51214178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35e43314cb8a796de59cb26575bb79807d17be93b6d96f4e88ae80999293598`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:17 GMT
ADD file:efe2d94a88cdbbd01c3ef095f0a2473cec9e74804b49cd6fb9b837d362631409 in / 
# Fri, 12 Nov 2021 17:20:17 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:48 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:48 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:49 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:49 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:49 GMT
ARG KONG_VERSION=2.4.1
# Sat, 13 Nov 2021 05:49:49 GMT
ENV KONG_VERSION=2.4.1
# Sat, 13 Nov 2021 05:49:50 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 13 Nov 2021 05:49:50 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 13 Nov 2021 05:49:50 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 13 Nov 2021 05:49:50 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 13 Nov 2021 05:49:58 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 13 Nov 2021 05:49:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:59 GMT
USER kong
# Sat, 13 Nov 2021 05:49:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:50:00 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:50:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:50:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79e9f2f55bf5465a02ee6a6170e66005b20c7aa6b115af6fcd04fad706ea651a`  
		Last Modified: Fri, 12 Nov 2021 17:21:24 GMT  
		Size: 2.8 MB (2817409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce26b4325645c1dad3b9d5b8fc5444824e2ea2de3e9d5f4559f426cff04104a`  
		Last Modified: Sat, 13 Nov 2021 05:51:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411b62f8c9e7fab3b27cbef1249f57a659b7471c4e076b5378dcee8a4a790996`  
		Last Modified: Sat, 13 Nov 2021 05:51:47 GMT  
		Size: 48.4 MB (48395903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9a6559336344b66a8656da9e28fdfc9894a9b2fc09e5b64fb72ea36724f82`  
		Last Modified: Sat, 13 Nov 2021 05:51:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c1fb6f9c8730ee375048bc1e84b55d0fca9fc03c399c829b003099e7f7fa1cee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50747067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7564222c2b4c012d7efcefc1991b942d5cbe82b9e40cb5b1ffa07d88cf3e0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:59 GMT
ADD file:da6c0ac7cb9f819998546d88fb489b746004eb2ad6da64a39210696ef0e66e54 in / 
# Wed, 01 Sep 2021 02:50:59 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:40:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:40:57 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:40:58 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:40:59 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:41:01 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:41:01 GMT
ARG KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:02 GMT
ENV KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:03 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 16 Oct 2021 03:41:04 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 16 Oct 2021 03:41:05 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 16 Oct 2021 03:41:06 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 16 Oct 2021 03:41:21 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 16 Oct 2021 03:41:23 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:41:23 GMT
USER kong
# Sat, 16 Oct 2021 03:41:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:41:25 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:41:26 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:07d756952c5cd45726cf9e8a292a3e05ca67eee5da176df7d632be8c5bb0ad04`  
		Last Modified: Wed, 01 Sep 2021 02:52:00 GMT  
		Size: 2.7 MB (2728407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e0f0fd92517b6d59463cbd452c23b55fbd7896bfe7e84b42714d29f55f949e`  
		Last Modified: Sat, 16 Oct 2021 03:44:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b659ade90c85e3ce8143b53a7f50a85d7a5c14915501effa14bc4d7f6a126c4a`  
		Last Modified: Sat, 16 Oct 2021 03:44:12 GMT  
		Size: 48.0 MB (48017796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffc9c89fe95a05f0d1cd219458f6515b923b624046322f009f6d1d77f211f08`  
		Last Modified: Sat, 16 Oct 2021 03:44:03 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-alpine`

```console
$ docker pull kong@sha256:aad8b5ca5ad388dec99b2d9c4ab9242352d71f1ddc9250d522fc00f121ee9776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:fd512d0444c67558130f975441a5b1e20b3a7540fe4344c17f8ea69164d4a15d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51214178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35e43314cb8a796de59cb26575bb79807d17be93b6d96f4e88ae80999293598`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:17 GMT
ADD file:efe2d94a88cdbbd01c3ef095f0a2473cec9e74804b49cd6fb9b837d362631409 in / 
# Fri, 12 Nov 2021 17:20:17 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:48 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:48 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:49 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:49 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:49 GMT
ARG KONG_VERSION=2.4.1
# Sat, 13 Nov 2021 05:49:49 GMT
ENV KONG_VERSION=2.4.1
# Sat, 13 Nov 2021 05:49:50 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 13 Nov 2021 05:49:50 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 13 Nov 2021 05:49:50 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 13 Nov 2021 05:49:50 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 13 Nov 2021 05:49:58 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 13 Nov 2021 05:49:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:59 GMT
USER kong
# Sat, 13 Nov 2021 05:49:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:50:00 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:50:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:50:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79e9f2f55bf5465a02ee6a6170e66005b20c7aa6b115af6fcd04fad706ea651a`  
		Last Modified: Fri, 12 Nov 2021 17:21:24 GMT  
		Size: 2.8 MB (2817409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce26b4325645c1dad3b9d5b8fc5444824e2ea2de3e9d5f4559f426cff04104a`  
		Last Modified: Sat, 13 Nov 2021 05:51:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411b62f8c9e7fab3b27cbef1249f57a659b7471c4e076b5378dcee8a4a790996`  
		Last Modified: Sat, 13 Nov 2021 05:51:47 GMT  
		Size: 48.4 MB (48395903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9a6559336344b66a8656da9e28fdfc9894a9b2fc09e5b64fb72ea36724f82`  
		Last Modified: Sat, 13 Nov 2021 05:51:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c1fb6f9c8730ee375048bc1e84b55d0fca9fc03c399c829b003099e7f7fa1cee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50747067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7564222c2b4c012d7efcefc1991b942d5cbe82b9e40cb5b1ffa07d88cf3e0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:59 GMT
ADD file:da6c0ac7cb9f819998546d88fb489b746004eb2ad6da64a39210696ef0e66e54 in / 
# Wed, 01 Sep 2021 02:50:59 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:40:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:40:57 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:40:58 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:40:59 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:41:01 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:41:01 GMT
ARG KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:02 GMT
ENV KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:03 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 16 Oct 2021 03:41:04 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 16 Oct 2021 03:41:05 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 16 Oct 2021 03:41:06 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 16 Oct 2021 03:41:21 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 16 Oct 2021 03:41:23 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:41:23 GMT
USER kong
# Sat, 16 Oct 2021 03:41:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:41:25 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:41:26 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:07d756952c5cd45726cf9e8a292a3e05ca67eee5da176df7d632be8c5bb0ad04`  
		Last Modified: Wed, 01 Sep 2021 02:52:00 GMT  
		Size: 2.7 MB (2728407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e0f0fd92517b6d59463cbd452c23b55fbd7896bfe7e84b42714d29f55f949e`  
		Last Modified: Sat, 16 Oct 2021 03:44:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b659ade90c85e3ce8143b53a7f50a85d7a5c14915501effa14bc4d7f6a126c4a`  
		Last Modified: Sat, 16 Oct 2021 03:44:12 GMT  
		Size: 48.0 MB (48017796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffc9c89fe95a05f0d1cd219458f6515b923b624046322f009f6d1d77f211f08`  
		Last Modified: Sat, 16 Oct 2021 03:44:03 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-centos`

```console
$ docker pull kong@sha256:49dddad34751502c9aee35caeae45b24fc0ac296357711b9de1f8fceb4fd7895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.4-centos` - linux; amd64

```console
$ docker pull kong@sha256:feb4461a2a085b2042c075e2d1744d3ff6b207e775b291cc3675b80461db8029
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127646569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cc1bb25437f8a5dbed0102a4231f576e55f5d303012939db68a9bc52785fca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:51:18 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 19:51:18 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 19:51:18 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 19:51:19 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 19:51:19 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 15 Sep 2021 19:52:07 GMT
ARG KONG_VERSION=2.4.1
# Wed, 15 Sep 2021 19:52:07 GMT
ENV KONG_VERSION=2.4.1
# Wed, 15 Sep 2021 19:52:07 GMT
ARG KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
# Wed, 15 Sep 2021 19:52:42 GMT
# ARGS: KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then   curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 15 Sep 2021 19:52:43 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 15 Sep 2021 19:52:43 GMT
USER kong
# Wed, 15 Sep 2021 19:52:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 19:52:44 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 15 Sep 2021 19:52:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Sep 2021 19:52:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5a22c33293d0d5fc35b813a8f71d89abcd8398213f41285640177d7580dac`  
		Last Modified: Wed, 15 Sep 2021 19:53:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bbc591d91f6a82fd63289e983b1baa055494e373060828ea98a396e7860bdc`  
		Last Modified: Wed, 15 Sep 2021 19:53:48 GMT  
		Size: 51.5 MB (51548551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcc045327ddc9eda05feb281dcbf8434f27be814258455a2b415a6f13544d03`  
		Last Modified: Wed, 15 Sep 2021 19:53:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4-ubuntu`

```console
$ docker pull kong@sha256:a48040038d4a0bf7989e37c68b16af2035c82e195820b8d2d8ae77bd18421633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1b238a9ef17d623392714e7a5a498a16874b87ae19d56c6f85cb0f937289a079
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134752818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee52b964888ac2d31cac4c35679b93f316cde405b3d62620dfdfd6d466ac6c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:40:30 GMT
ARG ASSET=ce
# Tue, 31 Aug 2021 03:40:31 GMT
ENV ASSET=ce
# Tue, 31 Aug 2021 03:40:31 GMT
ARG EE_PORTS
# Tue, 31 Aug 2021 03:40:31 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 31 Aug 2021 03:41:06 GMT
ARG KONG_VERSION=2.4.1
# Tue, 31 Aug 2021 03:41:06 GMT
ENV KONG_VERSION=2.4.1
# Tue, 31 Aug 2021 03:41:28 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Tue, 31 Aug 2021 03:41:29 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Tue, 31 Aug 2021 03:41:29 GMT
USER kong
# Tue, 31 Aug 2021 03:41:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Aug 2021 03:41:30 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 31 Aug 2021 03:41:30 GMT
STOPSIGNAL SIGQUIT
# Tue, 31 Aug 2021 03:41:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f9bf842551a4304b6e9bb37db25ba1932a186b178e50b94d7ba879d235b8ef`  
		Last Modified: Tue, 31 Aug 2021 03:42:03 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2b40add1d10ca76f9333f9a91f0c033556d4058acbcbb216d98d522fd9d6d1`  
		Last Modified: Tue, 31 Aug 2021 03:42:37 GMT  
		Size: 63.2 MB (63171073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a244e218996bdeaf548d3d178afa2a7f14e419f5a6359218e3983fab9f08b71`  
		Last Modified: Tue, 31 Aug 2021 03:42:26 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e0686699b0b342e98015bae36012487efbf032da49d71fa0712f0c9442098c24
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125855174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e49f8462bf8c748ed6879b14f939a89191987e8d9eb28b0063bf59d23a5b8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 16 Oct 2021 01:48:22 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Sat, 16 Oct 2021 01:48:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 16 Oct 2021 01:48:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:48:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 16 Oct 2021 01:48:25 GMT
CMD ["/bin/bash"]
# Sat, 16 Oct 2021 03:41:33 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:41:34 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:41:35 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:41:37 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Oct 2021 03:41:37 GMT
ARG KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:38 GMT
ENV KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:42:27 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Sat, 16 Oct 2021 03:42:28 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:42:28 GMT
USER kong
# Sat, 16 Oct 2021 03:42:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:42:30 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:42:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:42:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e9b8fdf46981043813ae269c4420735959dd01d4d15c420b66448523e9adc`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5b1b49195905e9415adfe3583301316ef591d794fcfd12b5cd29103fa7ee6b`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a6c6175ba12a0fd708883c2625167711f111f24ce2bb79221fda132487e57`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335856b8d9f9c59f06ad63f804ae54ee2f1913c6706391caa4d086e40a3c930f`  
		Last Modified: Sat, 16 Oct 2021 03:44:31 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d70ebd843f26a8e48d1b27e979ccf1f4bba9a1ff72e5b234bdfa4e3c19656e3`  
		Last Modified: Sat, 16 Oct 2021 03:44:39 GMT  
		Size: 59.5 MB (59531785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3123cd78ddff7a07a3179f9b8f4354dca238b6e042783f2628c0352d6f9b59f`  
		Last Modified: Sat, 16 Oct 2021 03:44:29 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.1`

```console
$ docker pull kong@sha256:aad8b5ca5ad388dec99b2d9c4ab9242352d71f1ddc9250d522fc00f121ee9776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.1` - linux; amd64

```console
$ docker pull kong@sha256:fd512d0444c67558130f975441a5b1e20b3a7540fe4344c17f8ea69164d4a15d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51214178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35e43314cb8a796de59cb26575bb79807d17be93b6d96f4e88ae80999293598`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:17 GMT
ADD file:efe2d94a88cdbbd01c3ef095f0a2473cec9e74804b49cd6fb9b837d362631409 in / 
# Fri, 12 Nov 2021 17:20:17 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:48 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:48 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:49 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:49 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:49 GMT
ARG KONG_VERSION=2.4.1
# Sat, 13 Nov 2021 05:49:49 GMT
ENV KONG_VERSION=2.4.1
# Sat, 13 Nov 2021 05:49:50 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 13 Nov 2021 05:49:50 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 13 Nov 2021 05:49:50 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 13 Nov 2021 05:49:50 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 13 Nov 2021 05:49:58 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 13 Nov 2021 05:49:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:59 GMT
USER kong
# Sat, 13 Nov 2021 05:49:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:50:00 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:50:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:50:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79e9f2f55bf5465a02ee6a6170e66005b20c7aa6b115af6fcd04fad706ea651a`  
		Last Modified: Fri, 12 Nov 2021 17:21:24 GMT  
		Size: 2.8 MB (2817409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce26b4325645c1dad3b9d5b8fc5444824e2ea2de3e9d5f4559f426cff04104a`  
		Last Modified: Sat, 13 Nov 2021 05:51:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411b62f8c9e7fab3b27cbef1249f57a659b7471c4e076b5378dcee8a4a790996`  
		Last Modified: Sat, 13 Nov 2021 05:51:47 GMT  
		Size: 48.4 MB (48395903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9a6559336344b66a8656da9e28fdfc9894a9b2fc09e5b64fb72ea36724f82`  
		Last Modified: Sat, 13 Nov 2021 05:51:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c1fb6f9c8730ee375048bc1e84b55d0fca9fc03c399c829b003099e7f7fa1cee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50747067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7564222c2b4c012d7efcefc1991b942d5cbe82b9e40cb5b1ffa07d88cf3e0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:59 GMT
ADD file:da6c0ac7cb9f819998546d88fb489b746004eb2ad6da64a39210696ef0e66e54 in / 
# Wed, 01 Sep 2021 02:50:59 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:40:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:40:57 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:40:58 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:40:59 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:41:01 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:41:01 GMT
ARG KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:02 GMT
ENV KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:03 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 16 Oct 2021 03:41:04 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 16 Oct 2021 03:41:05 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 16 Oct 2021 03:41:06 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 16 Oct 2021 03:41:21 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 16 Oct 2021 03:41:23 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:41:23 GMT
USER kong
# Sat, 16 Oct 2021 03:41:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:41:25 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:41:26 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:07d756952c5cd45726cf9e8a292a3e05ca67eee5da176df7d632be8c5bb0ad04`  
		Last Modified: Wed, 01 Sep 2021 02:52:00 GMT  
		Size: 2.7 MB (2728407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e0f0fd92517b6d59463cbd452c23b55fbd7896bfe7e84b42714d29f55f949e`  
		Last Modified: Sat, 16 Oct 2021 03:44:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b659ade90c85e3ce8143b53a7f50a85d7a5c14915501effa14bc4d7f6a126c4a`  
		Last Modified: Sat, 16 Oct 2021 03:44:12 GMT  
		Size: 48.0 MB (48017796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffc9c89fe95a05f0d1cd219458f6515b923b624046322f009f6d1d77f211f08`  
		Last Modified: Sat, 16 Oct 2021 03:44:03 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.1-alpine`

```console
$ docker pull kong@sha256:aad8b5ca5ad388dec99b2d9c4ab9242352d71f1ddc9250d522fc00f121ee9776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:fd512d0444c67558130f975441a5b1e20b3a7540fe4344c17f8ea69164d4a15d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51214178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35e43314cb8a796de59cb26575bb79807d17be93b6d96f4e88ae80999293598`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:17 GMT
ADD file:efe2d94a88cdbbd01c3ef095f0a2473cec9e74804b49cd6fb9b837d362631409 in / 
# Fri, 12 Nov 2021 17:20:17 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:48 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:48 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:49 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:49 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:49 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:49 GMT
ARG KONG_VERSION=2.4.1
# Sat, 13 Nov 2021 05:49:49 GMT
ENV KONG_VERSION=2.4.1
# Sat, 13 Nov 2021 05:49:50 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 13 Nov 2021 05:49:50 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 13 Nov 2021 05:49:50 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 13 Nov 2021 05:49:50 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 13 Nov 2021 05:49:58 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 13 Nov 2021 05:49:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:59 GMT
USER kong
# Sat, 13 Nov 2021 05:49:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:50:00 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:50:00 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:50:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:79e9f2f55bf5465a02ee6a6170e66005b20c7aa6b115af6fcd04fad706ea651a`  
		Last Modified: Fri, 12 Nov 2021 17:21:24 GMT  
		Size: 2.8 MB (2817409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dce26b4325645c1dad3b9d5b8fc5444824e2ea2de3e9d5f4559f426cff04104a`  
		Last Modified: Sat, 13 Nov 2021 05:51:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411b62f8c9e7fab3b27cbef1249f57a659b7471c4e076b5378dcee8a4a790996`  
		Last Modified: Sat, 13 Nov 2021 05:51:47 GMT  
		Size: 48.4 MB (48395903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb9a6559336344b66a8656da9e28fdfc9894a9b2fc09e5b64fb72ea36724f82`  
		Last Modified: Sat, 13 Nov 2021 05:51:37 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:c1fb6f9c8730ee375048bc1e84b55d0fca9fc03c399c829b003099e7f7fa1cee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50747067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7564222c2b4c012d7efcefc1991b942d5cbe82b9e40cb5b1ffa07d88cf3e0d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:59 GMT
ADD file:da6c0ac7cb9f819998546d88fb489b746004eb2ad6da64a39210696ef0e66e54 in / 
# Wed, 01 Sep 2021 02:50:59 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:40:56 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:40:57 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:40:58 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:40:59 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:41:01 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:41:01 GMT
ARG KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:02 GMT
ENV KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:03 GMT
ARG KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 16 Oct 2021 03:41:04 GMT
ENV KONG_AMD64_SHA=582cbcf23eb4dcdf9873105ac7d8428a4022ec61bcc68642ad9dd8a5c03e2a57
# Sat, 16 Oct 2021 03:41:05 GMT
ARG KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 16 Oct 2021 03:41:06 GMT
ENV KONG_ARM64_SHA=5ec35d1b19dd4e6592ad2c6586e68bfd1549c6a22840ce7d5654677b94e5028a
# Sat, 16 Oct 2021 03:41:21 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Sat, 16 Oct 2021 03:41:23 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:41:23 GMT
USER kong
# Sat, 16 Oct 2021 03:41:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:41:25 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:41:26 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:41:27 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:07d756952c5cd45726cf9e8a292a3e05ca67eee5da176df7d632be8c5bb0ad04`  
		Last Modified: Wed, 01 Sep 2021 02:52:00 GMT  
		Size: 2.7 MB (2728407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e0f0fd92517b6d59463cbd452c23b55fbd7896bfe7e84b42714d29f55f949e`  
		Last Modified: Sat, 16 Oct 2021 03:44:03 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b659ade90c85e3ce8143b53a7f50a85d7a5c14915501effa14bc4d7f6a126c4a`  
		Last Modified: Sat, 16 Oct 2021 03:44:12 GMT  
		Size: 48.0 MB (48017796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffc9c89fe95a05f0d1cd219458f6515b923b624046322f009f6d1d77f211f08`  
		Last Modified: Sat, 16 Oct 2021 03:44:03 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.1-centos`

```console
$ docker pull kong@sha256:49dddad34751502c9aee35caeae45b24fc0ac296357711b9de1f8fceb4fd7895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.4.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:feb4461a2a085b2042c075e2d1744d3ff6b207e775b291cc3675b80461db8029
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127646569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82cc1bb25437f8a5dbed0102a4231f576e55f5d303012939db68a9bc52785fca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:51:18 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 19:51:18 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 19:51:18 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 19:51:19 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 19:51:19 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 15 Sep 2021 19:52:07 GMT
ARG KONG_VERSION=2.4.1
# Wed, 15 Sep 2021 19:52:07 GMT
ENV KONG_VERSION=2.4.1
# Wed, 15 Sep 2021 19:52:07 GMT
ARG KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
# Wed, 15 Sep 2021 19:52:42 GMT
# ARGS: KONG_SHA256=b8083a6c268f69865e66a8d504fcdacab49ba36a4194ccfc9737d65e6863c30a
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then   curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 15 Sep 2021 19:52:43 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 15 Sep 2021 19:52:43 GMT
USER kong
# Wed, 15 Sep 2021 19:52:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 19:52:44 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 15 Sep 2021 19:52:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Sep 2021 19:52:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf5a22c33293d0d5fc35b813a8f71d89abcd8398213f41285640177d7580dac`  
		Last Modified: Wed, 15 Sep 2021 19:53:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bbc591d91f6a82fd63289e983b1baa055494e373060828ea98a396e7860bdc`  
		Last Modified: Wed, 15 Sep 2021 19:53:48 GMT  
		Size: 51.5 MB (51548551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcc045327ddc9eda05feb281dcbf8434f27be814258455a2b415a6f13544d03`  
		Last Modified: Wed, 15 Sep 2021 19:53:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.4.1-ubuntu`

```console
$ docker pull kong@sha256:a48040038d4a0bf7989e37c68b16af2035c82e195820b8d2d8ae77bd18421633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.4.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:1b238a9ef17d623392714e7a5a498a16874b87ae19d56c6f85cb0f937289a079
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134752818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee52b964888ac2d31cac4c35679b93f316cde405b3d62620dfdfd6d466ac6c8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Tue, 31 Aug 2021 01:21:27 GMT
ADD file:11b425d4c08e81a3e0cb2e0345d27cd5fc844dd83f1096af4cc05f635824ff5d in / 
# Tue, 31 Aug 2021 01:21:28 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 31 Aug 2021 01:21:29 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 01:21:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 31 Aug 2021 01:21:30 GMT
CMD ["/bin/bash"]
# Tue, 31 Aug 2021 03:40:30 GMT
ARG ASSET=ce
# Tue, 31 Aug 2021 03:40:31 GMT
ENV ASSET=ce
# Tue, 31 Aug 2021 03:40:31 GMT
ARG EE_PORTS
# Tue, 31 Aug 2021 03:40:31 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Tue, 31 Aug 2021 03:41:06 GMT
ARG KONG_VERSION=2.4.1
# Tue, 31 Aug 2021 03:41:06 GMT
ENV KONG_VERSION=2.4.1
# Tue, 31 Aug 2021 03:41:28 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Tue, 31 Aug 2021 03:41:29 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Tue, 31 Aug 2021 03:41:29 GMT
USER kong
# Tue, 31 Aug 2021 03:41:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 31 Aug 2021 03:41:30 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 31 Aug 2021 03:41:30 GMT
STOPSIGNAL SIGQUIT
# Tue, 31 Aug 2021 03:41:30 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:58690f9b18fca6469a14da4e212c96849469f9b1be6661d2342a4bf01774aa50`  
		Last Modified: Thu, 05 Aug 2021 00:25:05 GMT  
		Size: 46.5 MB (46497548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51569e7c50720acf6860327847fe342a1afbe148d24c529fb81df105e3eed01`  
		Last Modified: Tue, 31 Aug 2021 01:23:09 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8ef40b9ecabc2679fe2419957220c0272a965c5cf7e0269fa1aeeb8c56f2e1`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb15d46c38dcd1ea0b1990006c3366ecd10c79d374f341687eb2cb23a2c8672e`  
		Last Modified: Tue, 31 Aug 2021 01:23:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f9bf842551a4304b6e9bb37db25ba1932a186b178e50b94d7ba879d235b8ef`  
		Last Modified: Tue, 31 Aug 2021 03:42:03 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2b40add1d10ca76f9333f9a91f0c033556d4058acbcbb216d98d522fd9d6d1`  
		Last Modified: Tue, 31 Aug 2021 03:42:37 GMT  
		Size: 63.2 MB (63171073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a244e218996bdeaf548d3d178afa2a7f14e419f5a6359218e3983fab9f08b71`  
		Last Modified: Tue, 31 Aug 2021 03:42:26 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.4.1-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:e0686699b0b342e98015bae36012487efbf032da49d71fa0712f0c9442098c24
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125855174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e49f8462bf8c748ed6879b14f939a89191987e8d9eb28b0063bf59d23a5b8a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 16 Oct 2021 01:48:22 GMT
ADD file:3c6dc937cb7b4c81b42126f377d23320ec1d0a8ca34d38e7c45871f1d08dac43 in / 
# Sat, 16 Oct 2021 01:48:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 16 Oct 2021 01:48:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 01:48:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 16 Oct 2021 01:48:25 GMT
CMD ["/bin/bash"]
# Sat, 16 Oct 2021 03:41:33 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:41:34 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:41:35 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:41:37 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Oct 2021 03:41:37 GMT
ARG KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:41:38 GMT
ENV KONG_VERSION=2.4.1
# Sat, 16 Oct 2021 03:42:27 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL 		https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-xenial/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Sat, 16 Oct 2021 03:42:28 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:42:28 GMT
USER kong
# Sat, 16 Oct 2021 03:42:29 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:42:30 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:42:31 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:42:32 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:828b35a09f0b2f3d1dead43aa2468ff5eba6c463423b3fff7ee6d150f6fd1b6b`  
		Last Modified: Thu, 05 Aug 2021 00:25:09 GMT  
		Size: 41.2 MB (41239253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238e9b8fdf46981043813ae269c4420735959dd01d4d15c420b66448523e9adc`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5b1b49195905e9415adfe3583301316ef591d794fcfd12b5cd29103fa7ee6b`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269a6c6175ba12a0fd708883c2625167711f111f24ce2bb79221fda132487e57`  
		Last Modified: Sat, 16 Oct 2021 01:50:40 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335856b8d9f9c59f06ad63f804ae54ee2f1913c6706391caa4d086e40a3c930f`  
		Last Modified: Sat, 16 Oct 2021 03:44:31 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d70ebd843f26a8e48d1b27e979ccf1f4bba9a1ff72e5b234bdfa4e3c19656e3`  
		Last Modified: Sat, 16 Oct 2021 03:44:39 GMT  
		Size: 59.5 MB (59531785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3123cd78ddff7a07a3179f9b8f4354dca238b6e042783f2628c0352d6f9b59f`  
		Last Modified: Sat, 16 Oct 2021 03:44:29 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5`

```console
$ docker pull kong@sha256:460e1873eb420104cbdb5a316503dabc21c0350f8a95259e5e7637f117196d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5` - linux; amd64

```console
$ docker pull kong@sha256:6896f87b90dcea49ee7009a9963a709e5644ebf0dff8491d2c010bf7fab6a974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b114251eef2a2e43dbd58ea78009aa1eee554e03aad3399ccd64dac711f6437`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:26 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:26 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:36 GMT
USER kong
# Sat, 13 Nov 2021 05:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:37 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:37 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ab7edbafff55c804c295704914b38324636bc651035e4f405b24f4b86948`  
		Last Modified: Sat, 13 Nov 2021 05:51:23 GMT  
		Size: 47.0 MB (47002560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a49a9faa0e6e6630ec2942c9320fa92d94e2e7f5be3ed6cb179adc2cdf39e`  
		Last Modified: Sat, 13 Nov 2021 05:51:14 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5cd4260b499355edfefc64e2f8ae25c1f29e3d87210df6673c714304eaa444b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49236216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66091a53a5018032cb3c5b0210f3b699ac1cb5ae5da60ad69d5aaa7b7e54597`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:37:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:37:26 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:37:27 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:37:28 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:37:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:39:15 GMT
ARG KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 03:39:16 GMT
ENV KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 03:39:17 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 16 Oct 2021 03:39:18 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 16 Oct 2021 03:39:19 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 16 Oct 2021 03:39:20 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 16 Oct 2021 03:39:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Oct 2021 03:39:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:39:36 GMT
USER kong
# Sat, 16 Oct 2021 03:39:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:39:38 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:39:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:39:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 03:39:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf524f62eb906cf9274183d48b257701a07f0795d229fd3138874d18a3ba14a`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d187d89be5d54f647b5b0973c96f006f7f0ac6bce79e77a33224ed16fe068b3c`  
		Last Modified: Sat, 16 Oct 2021 03:43:50 GMT  
		Size: 46.5 MB (46523378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a96dccbac69770421aef4ea746d5fc652844019d9979cb3e959d5b635aea80`  
		Last Modified: Sat, 16 Oct 2021 03:43:41 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-centos`

```console
$ docker pull kong@sha256:29f839eedc97022967ae46e0ec2ba5dfe75b37525c409b475b7a61a7c0e0ee91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.5-centos` - linux; amd64

```console
$ docker pull kong@sha256:033decce472824142c52050eeb2ad85a24f1f775d00888d421ad065b3113e223
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160921195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5212ef94876a94444a623c7c826d7ea5bd5d0fce1958eb2cd472a8a0f58befd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 23:21:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 23:21:23 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 23:21:23 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 23:21:24 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 23:21:24 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 15 Sep 2021 23:21:24 GMT
ARG KONG_VERSION=2.5.1
# Wed, 15 Sep 2021 23:21:24 GMT
ENV KONG_VERSION=2.5.1
# Wed, 15 Sep 2021 23:21:24 GMT
ARG KONG_SHA256=36c03c53a4e3a3f6f0968f68258fa93a584af5c33ed29fa5e05e089dfb97b730
# Wed, 15 Sep 2021 23:21:58 GMT
# ARGS: KONG_SHA256=36c03c53a4e3a3f6f0968f68258fa93a584af5c33ed29fa5e05e089dfb97b730
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then       curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm       && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils git     && yum clean all -q     && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki     && yum install -y /tmp/kong.rpm     && yum clean all     && rm /tmp/kong.rpm     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 15 Sep 2021 23:21:59 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 15 Sep 2021 23:21:59 GMT
USER kong
# Wed, 15 Sep 2021 23:21:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 23:22:00 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 15 Sep 2021 23:22:00 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Sep 2021 23:22:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 15 Sep 2021 23:22:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb8a137fa2b84d66997b2207a6880267b365a0a2d08a22a00c4965ecbec7f93`  
		Last Modified: Wed, 15 Sep 2021 23:23:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5520f68e079f5dbe56c351330fdc8e5688d18f21e5b3059e73da20ea1f82e79c`  
		Last Modified: Wed, 15 Sep 2021 23:23:37 GMT  
		Size: 77.4 MB (77402098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af293b6ea93ad38f2ce79b696ebdcf75d1917845c0eaf599089bea1eec48e287`  
		Last Modified: Wed, 15 Sep 2021 23:23:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5-ubuntu`

```console
$ docker pull kong@sha256:bfc5bc3fe4ade86cbb676eede121210b4311a0a257ff5cba3207741e77efabe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5992659176defe3a2cb08d82fade385d1bea3b88148e5a940cf3af678250c610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128036481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc48a633e5485b161e995eeefeb395dc3e2a1cc7fc08684d3ac70fb07ee5e5f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:50:17 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 02:50:17 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 02:50:18 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 02:50:18 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Oct 2021 02:50:54 GMT
ARG KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 02:50:54 GMT
ENV KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 02:51:15 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Oct 2021 02:51:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 02:51:16 GMT
USER kong
# Sat, 16 Oct 2021 02:51:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 02:51:16 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 02:51:16 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 02:51:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 02:51:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a161c721a16c61e7d874293e0cdd47f98a8f82b390bdf961d621a52dbdc1ac41`  
		Last Modified: Sat, 16 Oct 2021 02:51:59 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eed63b5a7b3d59da5743acef3a98fafd449e690ba488ac5dbc375b1828fb39`  
		Last Modified: Sat, 16 Oct 2021 02:52:36 GMT  
		Size: 74.4 MB (74386536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5309cf88284208ec6c93ef9bf3450ce5b34e97c60de0f576f3139dd1c99d472`  
		Last Modified: Sat, 16 Oct 2021 02:52:24 GMT  
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
$ docker pull kong@sha256:460e1873eb420104cbdb5a316503dabc21c0350f8a95259e5e7637f117196d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1` - linux; amd64

```console
$ docker pull kong@sha256:6896f87b90dcea49ee7009a9963a709e5644ebf0dff8491d2c010bf7fab6a974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b114251eef2a2e43dbd58ea78009aa1eee554e03aad3399ccd64dac711f6437`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:26 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:26 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:36 GMT
USER kong
# Sat, 13 Nov 2021 05:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:37 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:37 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ab7edbafff55c804c295704914b38324636bc651035e4f405b24f4b86948`  
		Last Modified: Sat, 13 Nov 2021 05:51:23 GMT  
		Size: 47.0 MB (47002560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a49a9faa0e6e6630ec2942c9320fa92d94e2e7f5be3ed6cb179adc2cdf39e`  
		Last Modified: Sat, 13 Nov 2021 05:51:14 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.1` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5cd4260b499355edfefc64e2f8ae25c1f29e3d87210df6673c714304eaa444b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49236216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66091a53a5018032cb3c5b0210f3b699ac1cb5ae5da60ad69d5aaa7b7e54597`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:37:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:37:26 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:37:27 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:37:28 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:37:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:39:15 GMT
ARG KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 03:39:16 GMT
ENV KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 03:39:17 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 16 Oct 2021 03:39:18 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 16 Oct 2021 03:39:19 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 16 Oct 2021 03:39:20 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 16 Oct 2021 03:39:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Oct 2021 03:39:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:39:36 GMT
USER kong
# Sat, 16 Oct 2021 03:39:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:39:38 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:39:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:39:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 03:39:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf524f62eb906cf9274183d48b257701a07f0795d229fd3138874d18a3ba14a`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d187d89be5d54f647b5b0973c96f006f7f0ac6bce79e77a33224ed16fe068b3c`  
		Last Modified: Sat, 16 Oct 2021 03:43:50 GMT  
		Size: 46.5 MB (46523378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a96dccbac69770421aef4ea746d5fc652844019d9979cb3e959d5b635aea80`  
		Last Modified: Sat, 16 Oct 2021 03:43:41 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-alpine`

```console
$ docker pull kong@sha256:460e1873eb420104cbdb5a316503dabc21c0350f8a95259e5e7637f117196d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.5.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:6896f87b90dcea49ee7009a9963a709e5644ebf0dff8491d2c010bf7fab6a974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49826551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b114251eef2a2e43dbd58ea78009aa1eee554e03aad3399ccd64dac711f6437`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_VERSION=2.5.1
# Sat, 13 Nov 2021 05:49:25 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:25 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 13 Nov 2021 05:49:26 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:26 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 13 Nov 2021 05:49:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:36 GMT
USER kong
# Sat, 13 Nov 2021 05:49:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:37 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:37 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:37 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:38 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc7ab7edbafff55c804c295704914b38324636bc651035e4f405b24f4b86948`  
		Last Modified: Sat, 13 Nov 2021 05:51:23 GMT  
		Size: 47.0 MB (47002560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f1a49a9faa0e6e6630ec2942c9320fa92d94e2e7f5be3ed6cb179adc2cdf39e`  
		Last Modified: Sat, 13 Nov 2021 05:51:14 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.5.1-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:5cd4260b499355edfefc64e2f8ae25c1f29e3d87210df6673c714304eaa444b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49236216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66091a53a5018032cb3c5b0210f3b699ac1cb5ae5da60ad69d5aaa7b7e54597`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:37:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:37:26 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:37:27 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:37:28 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:37:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:39:15 GMT
ARG KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 03:39:16 GMT
ENV KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 03:39:17 GMT
ARG KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 16 Oct 2021 03:39:18 GMT
ENV KONG_AMD64_SHA=f3fc429372e473e8616cf6afc56543a151bd08ba2bc235176d671515f691f20b
# Sat, 16 Oct 2021 03:39:19 GMT
ARG KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 16 Oct 2021 03:39:20 GMT
ENV KONG_ARM64_SHA=e6d002b49aab10c1ae74cd533640eddc9e7f0ce30562cd7079d4b76d9eb70340
# Sat, 16 Oct 2021 03:39:35 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Oct 2021 03:39:36 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:39:36 GMT
USER kong
# Sat, 16 Oct 2021 03:39:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:39:38 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:39:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:39:40 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 03:39:41 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf524f62eb906cf9274183d48b257701a07f0795d229fd3138874d18a3ba14a`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d187d89be5d54f647b5b0973c96f006f7f0ac6bce79e77a33224ed16fe068b3c`  
		Last Modified: Sat, 16 Oct 2021 03:43:50 GMT  
		Size: 46.5 MB (46523378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a96dccbac69770421aef4ea746d5fc652844019d9979cb3e959d5b635aea80`  
		Last Modified: Sat, 16 Oct 2021 03:43:41 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-centos`

```console
$ docker pull kong@sha256:29f839eedc97022967ae46e0ec2ba5dfe75b37525c409b475b7a61a7c0e0ee91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.5.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:033decce472824142c52050eeb2ad85a24f1f775d00888d421ad065b3113e223
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160921195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5212ef94876a94444a623c7c826d7ea5bd5d0fce1958eb2cd472a8a0f58befd1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 23:21:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 23:21:23 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 23:21:23 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 23:21:24 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 23:21:24 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 15 Sep 2021 23:21:24 GMT
ARG KONG_VERSION=2.5.1
# Wed, 15 Sep 2021 23:21:24 GMT
ENV KONG_VERSION=2.5.1
# Wed, 15 Sep 2021 23:21:24 GMT
ARG KONG_SHA256=36c03c53a4e3a3f6f0968f68258fa93a584af5c33ed29fa5e05e089dfb97b730
# Wed, 15 Sep 2021 23:21:58 GMT
# ARGS: KONG_SHA256=36c03c53a4e3a3f6f0968f68258fa93a584af5c33ed29fa5e05e089dfb97b730
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then       curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm       && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils git     && yum clean all -q     && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki     && yum install -y /tmp/kong.rpm     && yum clean all     && rm /tmp/kong.rpm     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Wed, 15 Sep 2021 23:21:59 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Wed, 15 Sep 2021 23:21:59 GMT
USER kong
# Wed, 15 Sep 2021 23:21:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Sep 2021 23:22:00 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 15 Sep 2021 23:22:00 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Sep 2021 23:22:00 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Wed, 15 Sep 2021 23:22:00 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb8a137fa2b84d66997b2207a6880267b365a0a2d08a22a00c4965ecbec7f93`  
		Last Modified: Wed, 15 Sep 2021 23:23:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5520f68e079f5dbe56c351330fdc8e5688d18f21e5b3059e73da20ea1f82e79c`  
		Last Modified: Wed, 15 Sep 2021 23:23:37 GMT  
		Size: 77.4 MB (77402098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af293b6ea93ad38f2ce79b696ebdcf75d1917845c0eaf599089bea1eec48e287`  
		Last Modified: Wed, 15 Sep 2021 23:23:25 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.5.1-ubuntu`

```console
$ docker pull kong@sha256:673c148c94846a72e041f9f1ec0b04d113786cec6712799b4209eda2af4ffb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.5.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:5992659176defe3a2cb08d82fade385d1bea3b88148e5a940cf3af678250c610
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.0 MB (128036481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc48a633e5485b161e995eeefeb395dc3e2a1cc7fc08684d3ac70fb07ee5e5f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:50:17 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 02:50:17 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 02:50:18 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 02:50:18 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Oct 2021 02:50:54 GMT
ARG KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 02:50:54 GMT
ENV KONG_VERSION=2.5.1
# Sat, 16 Oct 2021 02:51:15 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Oct 2021 02:51:16 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 02:51:16 GMT
USER kong
# Sat, 16 Oct 2021 02:51:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 02:51:16 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 02:51:16 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 02:51:16 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 02:51:17 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a161c721a16c61e7d874293e0cdd47f98a8f82b390bdf961d621a52dbdc1ac41`  
		Last Modified: Sat, 16 Oct 2021 02:51:59 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eed63b5a7b3d59da5743acef3a98fafd449e690ba488ac5dbc375b1828fb39`  
		Last Modified: Sat, 16 Oct 2021 02:52:36 GMT  
		Size: 74.4 MB (74386536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5309cf88284208ec6c93ef9bf3450ce5b34e97c60de0f576f3139dd1c99d472`  
		Last Modified: Sat, 16 Oct 2021 02:52:24 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6`

```console
$ docker pull kong@sha256:0d3acebb9b7db196689b36e906942640a4a02b731199aef16823b5a0a336ca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6` - linux; amd64

```console
$ docker pull kong@sha256:95515d0f66dd958be1e30af772ada51bd4812d2a27bcb9124074fd1a2df4402e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49865802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b92ff33146bb0aa7d22bd05cf622124574febe4ee673d92dfed8299b140ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:04 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:12 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:13 GMT
USER kong
# Sat, 13 Nov 2021 05:49:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c7e18e0a769d4001d507fbe88c18e222f1ef8b290b08b684cbe031f308a212`  
		Last Modified: Sat, 13 Nov 2021 05:50:51 GMT  
		Size: 47.0 MB (47041810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9e277edccd9c623819e5913361a38ef18b0d49d8563a765c7cbda0260b9d4`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:eb57fd149e5fe95d073e7a36c082c9bd47c7a9853df05aa03238226ff7866903
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49265990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec6b4428e14e75cb168840828b4cc4f32a835e74bd82d2e56e1dda7c2c1fb7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:37:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:37:26 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:37:27 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:37:28 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:37:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:37:30 GMT
ARG KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:31 GMT
ENV KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:33 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:34 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:35 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:48 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Oct 2021 03:37:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:37:49 GMT
USER kong
# Sat, 16 Oct 2021 03:37:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:37:51 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:37:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:37:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 03:37:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf524f62eb906cf9274183d48b257701a07f0795d229fd3138874d18a3ba14a`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01bfca048d1ceeaa05e27bb8ebed0b9eab2e4bb78b53c85c15370508cc58c3`  
		Last Modified: Sat, 16 Oct 2021 03:43:23 GMT  
		Size: 46.6 MB (46553151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d780c4722fe7929b92ba27bb68aaa27f4e53da70f2c057d7d63750bf99258c97`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-centos`

```console
$ docker pull kong@sha256:03453c57b918faa98be9faf2ee7b91239c4a4030a5478b750712408b4104b6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6-centos` - linux; amd64

```console
$ docker pull kong@sha256:27efe9259a4da91b92a42030be7bec0d4d3e09b6483ac9473dd4996037c84d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160965349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d952d7b8eb428c80083082cfea96234e5a263dea8f0a1ef32882fbcec5920`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 23:21:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 23:21:23 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 23:21:23 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 23:21:24 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 23:21:24 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Tue, 05 Oct 2021 17:43:00 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Oct 2021 17:43:00 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Oct 2021 17:43:01 GMT
ARG KONG_SHA256=f83a1030b01aa3deb4535394b550228f4804a6fd35a4ea4b11e12dcbcacdadc0
# Tue, 05 Oct 2021 17:43:40 GMT
# ARGS: KONG_SHA256=f83a1030b01aa3deb4535394b550228f4804a6fd35a4ea4b11e12dcbcacdadc0
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then       curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm       && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils git     && yum clean all -q     && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki     && yum install -y /tmp/kong.rpm     && yum clean all     && rm /tmp/kong.rpm     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Oct 2021 17:43:41 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Oct 2021 17:43:41 GMT
USER kong
# Tue, 05 Oct 2021 17:43:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:43:42 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Oct 2021 17:43:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Oct 2021 17:43:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Oct 2021 17:43:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb8a137fa2b84d66997b2207a6880267b365a0a2d08a22a00c4965ecbec7f93`  
		Last Modified: Wed, 15 Sep 2021 23:23:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3563bfe40d23f8dbed26358d7c01a711109642f9d164dacf921387cfe9d5ca`  
		Last Modified: Tue, 05 Oct 2021 17:45:39 GMT  
		Size: 77.4 MB (77446253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b3206af33126cd570c9aa494380def6d75f1e4cdde13c3ea55ccedd8641c93`  
		Last Modified: Tue, 05 Oct 2021 17:45:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6-ubuntu`

```console
$ docker pull kong@sha256:012f338f574499c2da21a8a77e07014b7b902a12080793ffd7771f0c50f04467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:06f8b70186fa150cc0933f591307263c9de0df8d59cd4dd0715d586184461b41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128079977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf2a2b99637a1eb48882fba6faa579247ff8818f0cdcf3c5a77ff361da4a243`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:50:17 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 02:50:17 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 02:50:18 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 02:50:18 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Oct 2021 02:50:18 GMT
ARG KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 02:50:18 GMT
ENV KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 02:50:42 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Oct 2021 02:50:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 02:50:43 GMT
USER kong
# Sat, 16 Oct 2021 02:50:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 02:50:43 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 02:50:44 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 02:50:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 02:50:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a161c721a16c61e7d874293e0cdd47f98a8f82b390bdf961d621a52dbdc1ac41`  
		Last Modified: Sat, 16 Oct 2021 02:51:59 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745eff81ab1e1489b4fee2bf5aa39eef6d63e8a5dd9f1f0921ca369dfb3582f`  
		Last Modified: Sat, 16 Oct 2021 02:52:10 GMT  
		Size: 74.4 MB (74430032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7526fc9f882ef9a7c3b3e67b003a8d9c1caa238e2f3f40b6174ff750d5e5d9a6`  
		Last Modified: Sat, 16 Oct 2021 02:51:57 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0`

```console
$ docker pull kong@sha256:0d3acebb9b7db196689b36e906942640a4a02b731199aef16823b5a0a336ca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0` - linux; amd64

```console
$ docker pull kong@sha256:95515d0f66dd958be1e30af772ada51bd4812d2a27bcb9124074fd1a2df4402e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49865802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b92ff33146bb0aa7d22bd05cf622124574febe4ee673d92dfed8299b140ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:04 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:12 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:13 GMT
USER kong
# Sat, 13 Nov 2021 05:49:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c7e18e0a769d4001d507fbe88c18e222f1ef8b290b08b684cbe031f308a212`  
		Last Modified: Sat, 13 Nov 2021 05:50:51 GMT  
		Size: 47.0 MB (47041810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9e277edccd9c623819e5913361a38ef18b0d49d8563a765c7cbda0260b9d4`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.0` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:eb57fd149e5fe95d073e7a36c082c9bd47c7a9853df05aa03238226ff7866903
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49265990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec6b4428e14e75cb168840828b4cc4f32a835e74bd82d2e56e1dda7c2c1fb7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:37:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:37:26 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:37:27 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:37:28 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:37:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:37:30 GMT
ARG KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:31 GMT
ENV KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:33 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:34 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:35 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:48 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Oct 2021 03:37:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:37:49 GMT
USER kong
# Sat, 16 Oct 2021 03:37:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:37:51 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:37:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:37:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 03:37:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf524f62eb906cf9274183d48b257701a07f0795d229fd3138874d18a3ba14a`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01bfca048d1ceeaa05e27bb8ebed0b9eab2e4bb78b53c85c15370508cc58c3`  
		Last Modified: Sat, 16 Oct 2021 03:43:23 GMT  
		Size: 46.6 MB (46553151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d780c4722fe7929b92ba27bb68aaa27f4e53da70f2c057d7d63750bf99258c97`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-alpine`

```console
$ docker pull kong@sha256:0d3acebb9b7db196689b36e906942640a4a02b731199aef16823b5a0a336ca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.6.0-alpine` - linux; amd64

```console
$ docker pull kong@sha256:95515d0f66dd958be1e30af772ada51bd4812d2a27bcb9124074fd1a2df4402e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49865802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b92ff33146bb0aa7d22bd05cf622124574febe4ee673d92dfed8299b140ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:04 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:12 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:13 GMT
USER kong
# Sat, 13 Nov 2021 05:49:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c7e18e0a769d4001d507fbe88c18e222f1ef8b290b08b684cbe031f308a212`  
		Last Modified: Sat, 13 Nov 2021 05:50:51 GMT  
		Size: 47.0 MB (47041810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9e277edccd9c623819e5913361a38ef18b0d49d8563a765c7cbda0260b9d4`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.6.0-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:eb57fd149e5fe95d073e7a36c082c9bd47c7a9853df05aa03238226ff7866903
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49265990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec6b4428e14e75cb168840828b4cc4f32a835e74bd82d2e56e1dda7c2c1fb7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:37:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:37:26 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:37:27 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:37:28 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:37:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:37:30 GMT
ARG KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:31 GMT
ENV KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:33 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:34 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:35 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:48 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Oct 2021 03:37:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:37:49 GMT
USER kong
# Sat, 16 Oct 2021 03:37:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:37:51 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:37:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:37:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 03:37:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf524f62eb906cf9274183d48b257701a07f0795d229fd3138874d18a3ba14a`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01bfca048d1ceeaa05e27bb8ebed0b9eab2e4bb78b53c85c15370508cc58c3`  
		Last Modified: Sat, 16 Oct 2021 03:43:23 GMT  
		Size: 46.6 MB (46553151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d780c4722fe7929b92ba27bb68aaa27f4e53da70f2c057d7d63750bf99258c97`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-centos`

```console
$ docker pull kong@sha256:03453c57b918faa98be9faf2ee7b91239c4a4030a5478b750712408b4104b6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6.0-centos` - linux; amd64

```console
$ docker pull kong@sha256:27efe9259a4da91b92a42030be7bec0d4d3e09b6483ac9473dd4996037c84d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160965349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d952d7b8eb428c80083082cfea96234e5a263dea8f0a1ef32882fbcec5920`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 23:21:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 23:21:23 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 23:21:23 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 23:21:24 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 23:21:24 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Tue, 05 Oct 2021 17:43:00 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Oct 2021 17:43:00 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Oct 2021 17:43:01 GMT
ARG KONG_SHA256=f83a1030b01aa3deb4535394b550228f4804a6fd35a4ea4b11e12dcbcacdadc0
# Tue, 05 Oct 2021 17:43:40 GMT
# ARGS: KONG_SHA256=f83a1030b01aa3deb4535394b550228f4804a6fd35a4ea4b11e12dcbcacdadc0
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then       curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm       && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils git     && yum clean all -q     && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki     && yum install -y /tmp/kong.rpm     && yum clean all     && rm /tmp/kong.rpm     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Oct 2021 17:43:41 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Oct 2021 17:43:41 GMT
USER kong
# Tue, 05 Oct 2021 17:43:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:43:42 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Oct 2021 17:43:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Oct 2021 17:43:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Oct 2021 17:43:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb8a137fa2b84d66997b2207a6880267b365a0a2d08a22a00c4965ecbec7f93`  
		Last Modified: Wed, 15 Sep 2021 23:23:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3563bfe40d23f8dbed26358d7c01a711109642f9d164dacf921387cfe9d5ca`  
		Last Modified: Tue, 05 Oct 2021 17:45:39 GMT  
		Size: 77.4 MB (77446253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b3206af33126cd570c9aa494380def6d75f1e4cdde13c3ea55ccedd8641c93`  
		Last Modified: Tue, 05 Oct 2021 17:45:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.6.0-ubuntu`

```console
$ docker pull kong@sha256:012f338f574499c2da21a8a77e07014b7b902a12080793ffd7771f0c50f04467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:2.6.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:06f8b70186fa150cc0933f591307263c9de0df8d59cd4dd0715d586184461b41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128079977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf2a2b99637a1eb48882fba6faa579247ff8818f0cdcf3c5a77ff361da4a243`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:50:17 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 02:50:17 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 02:50:18 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 02:50:18 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Oct 2021 02:50:18 GMT
ARG KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 02:50:18 GMT
ENV KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 02:50:42 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Oct 2021 02:50:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 02:50:43 GMT
USER kong
# Sat, 16 Oct 2021 02:50:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 02:50:43 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 02:50:44 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 02:50:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 02:50:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a161c721a16c61e7d874293e0cdd47f98a8f82b390bdf961d621a52dbdc1ac41`  
		Last Modified: Sat, 16 Oct 2021 02:51:59 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745eff81ab1e1489b4fee2bf5aa39eef6d63e8a5dd9f1f0921ca369dfb3582f`  
		Last Modified: Sat, 16 Oct 2021 02:52:10 GMT  
		Size: 74.4 MB (74430032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7526fc9f882ef9a7c3b3e67b003a8d9c1caa238e2f3f40b6174ff750d5e5d9a6`  
		Last Modified: Sat, 16 Oct 2021 02:51:57 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:0d3acebb9b7db196689b36e906942640a4a02b731199aef16823b5a0a336ca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:95515d0f66dd958be1e30af772ada51bd4812d2a27bcb9124074fd1a2df4402e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49865802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b92ff33146bb0aa7d22bd05cf622124574febe4ee673d92dfed8299b140ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:04 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:12 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:13 GMT
USER kong
# Sat, 13 Nov 2021 05:49:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c7e18e0a769d4001d507fbe88c18e222f1ef8b290b08b684cbe031f308a212`  
		Last Modified: Sat, 13 Nov 2021 05:50:51 GMT  
		Size: 47.0 MB (47041810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9e277edccd9c623819e5913361a38ef18b0d49d8563a765c7cbda0260b9d4`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:eb57fd149e5fe95d073e7a36c082c9bd47c7a9853df05aa03238226ff7866903
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49265990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec6b4428e14e75cb168840828b4cc4f32a835e74bd82d2e56e1dda7c2c1fb7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:37:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:37:26 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:37:27 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:37:28 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:37:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:37:30 GMT
ARG KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:31 GMT
ENV KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:33 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:34 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:35 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:48 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Oct 2021 03:37:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:37:49 GMT
USER kong
# Sat, 16 Oct 2021 03:37:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:37:51 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:37:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:37:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 03:37:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf524f62eb906cf9274183d48b257701a07f0795d229fd3138874d18a3ba14a`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01bfca048d1ceeaa05e27bb8ebed0b9eab2e4bb78b53c85c15370508cc58c3`  
		Last Modified: Sat, 16 Oct 2021 03:43:23 GMT  
		Size: 46.6 MB (46553151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d780c4722fe7929b92ba27bb68aaa27f4e53da70f2c057d7d63750bf99258c97`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:centos`

```console
$ docker pull kong@sha256:03453c57b918faa98be9faf2ee7b91239c4a4030a5478b750712408b4104b6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:27efe9259a4da91b92a42030be7bec0d4d3e09b6483ac9473dd4996037c84d3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160965349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5d952d7b8eb428c80083082cfea96234e5a263dea8f0a1ef32882fbcec5920`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 23:21:23 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 15 Sep 2021 23:21:23 GMT
ARG ASSET=ce
# Wed, 15 Sep 2021 23:21:23 GMT
ENV ASSET=ce
# Wed, 15 Sep 2021 23:21:24 GMT
ARG EE_PORTS
# Wed, 15 Sep 2021 23:21:24 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Tue, 05 Oct 2021 17:43:00 GMT
ARG KONG_VERSION=2.6.0
# Tue, 05 Oct 2021 17:43:00 GMT
ENV KONG_VERSION=2.6.0
# Tue, 05 Oct 2021 17:43:01 GMT
ARG KONG_SHA256=f83a1030b01aa3deb4535394b550228f4804a6fd35a4ea4b11e12dcbcacdadc0
# Tue, 05 Oct 2021 17:43:40 GMT
# ARGS: KONG_SHA256=f83a1030b01aa3deb4535394b550228f4804a6fd35a4ea4b11e12dcbcacdadc0
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then       curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-centos-7/Packages/k/kong-$KONG_VERSION.el7.amd64.rpm -o /tmp/kong.rpm       && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;     fi;     yum install -y -q unzip shadow-utils git     && yum clean all -q     && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki     && yum install -y /tmp/kong.rpm     && yum clean all     && rm /tmp/kong.rpm     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Tue, 05 Oct 2021 17:43:41 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Tue, 05 Oct 2021 17:43:41 GMT
USER kong
# Tue, 05 Oct 2021 17:43:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Oct 2021 17:43:42 GMT
EXPOSE 8000 8001 8443 8444
# Tue, 05 Oct 2021 17:43:42 GMT
STOPSIGNAL SIGQUIT
# Tue, 05 Oct 2021 17:43:42 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Tue, 05 Oct 2021 17:43:42 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb8a137fa2b84d66997b2207a6880267b365a0a2d08a22a00c4965ecbec7f93`  
		Last Modified: Wed, 15 Sep 2021 23:23:25 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3563bfe40d23f8dbed26358d7c01a711109642f9d164dacf921387cfe9d5ca`  
		Last Modified: Tue, 05 Oct 2021 17:45:39 GMT  
		Size: 77.4 MB (77446253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b3206af33126cd570c9aa494380def6d75f1e4cdde13c3ea55ccedd8641c93`  
		Last Modified: Tue, 05 Oct 2021 17:45:26 GMT  
		Size: 880.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:0d3acebb9b7db196689b36e906942640a4a02b731199aef16823b5a0a336ca1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:95515d0f66dd958be1e30af772ada51bd4812d2a27bcb9124074fd1a2df4402e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49865802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51b92ff33146bb0aa7d22bd05cf622124574febe4ee673d92dfed8299b140ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 05:49:01 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 13 Nov 2021 05:49:02 GMT
ARG ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ENV ASSET=ce
# Sat, 13 Nov 2021 05:49:02 GMT
ARG EE_PORTS
# Sat, 13 Nov 2021 05:49:02 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_VERSION=2.6.0
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 13 Nov 2021 05:49:03 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:04 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 13 Nov 2021 05:49:12 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 13 Nov 2021 05:49:13 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 13 Nov 2021 05:49:13 GMT
USER kong
# Sat, 13 Nov 2021 05:49:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 13 Nov 2021 05:49:14 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 13 Nov 2021 05:49:14 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Nov 2021 05:49:14 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 13 Nov 2021 05:49:15 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e8b2c66462e7a485d21bf9baf11a6e252511cd3612b6fa68b0c1da6972f4cd`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8c7e18e0a769d4001d507fbe88c18e222f1ef8b290b08b684cbe031f308a212`  
		Last Modified: Sat, 13 Nov 2021 05:50:51 GMT  
		Size: 47.0 MB (47041810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f9e277edccd9c623819e5913361a38ef18b0d49d8563a765c7cbda0260b9d4`  
		Last Modified: Sat, 13 Nov 2021 05:50:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:eb57fd149e5fe95d073e7a36c082c9bd47c7a9853df05aa03238226ff7866903
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49265990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec6b4428e14e75cb168840828b4cc4f32a835e74bd82d2e56e1dda7c2c1fb7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Sat, 16 Oct 2021 03:37:25 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 16 Oct 2021 03:37:26 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 03:37:27 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 03:37:28 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 03:37:30 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Sat, 16 Oct 2021 03:37:30 GMT
ARG KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:31 GMT
ENV KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 03:37:32 GMT
ARG KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:33 GMT
ENV KONG_AMD64_SHA=43fb5f27185e274e22b4a36b93b1b7e27afe94b9fd2efbe4ec69b8ed8a9e5902
# Sat, 16 Oct 2021 03:37:34 GMT
ARG KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:35 GMT
ENV KONG_ARM64_SHA=a057eaa6d10ecf49443ec0cac6e1b70a62ee357a777e0e169c780e18fd5c5544
# Sat, 16 Oct 2021 03:37:48 GMT
RUN set -eux;     arch="$(apk --print-arch)";     case "${arch}" in       x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;;       aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;;     esac;     if [ "$ASSET" = "ce" ] ; then       apk add --no-cache --virtual .build-deps curl wget tar ca-certificates       && curl -fL "https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-alpine/kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz       && echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -       && apk del .build-deps;     fi;     mkdir /kong     && tar -C /kong -xzf /tmp/kong.tar.gz     && mv /kong/usr/local/* /usr/local     && mv /kong/etc/* /etc     && rm -rf /kong     && apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates     && adduser -S kong     && addgroup -S kong     && mkdir -p "/usr/local/kong"     && chown -R kong:0 /usr/local/kong     && chown kong:0 /usr/local/bin/kong     && chmod -R g=u /usr/local/kong     && rm -rf /tmp/kong.tar.gz     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version;     fi
# Sat, 16 Oct 2021 03:37:49 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 03:37:49 GMT
USER kong
# Sat, 16 Oct 2021 03:37:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 03:37:51 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 03:37:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 03:37:53 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 03:37:54 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf524f62eb906cf9274183d48b257701a07f0795d229fd3138874d18a3ba14a`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a01bfca048d1ceeaa05e27bb8ebed0b9eab2e4bb78b53c85c15370508cc58c3`  
		Last Modified: Sat, 16 Oct 2021 03:43:23 GMT  
		Size: 46.6 MB (46553151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d780c4722fe7929b92ba27bb68aaa27f4e53da70f2c057d7d63750bf99258c97`  
		Last Modified: Sat, 16 Oct 2021 03:43:14 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:6a6f1d61aaf60e3bd32bfad1f19ffa060f0f7e8336d237e178eb82268fdce447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:06f8b70186fa150cc0933f591307263c9de0df8d59cd4dd0715d586184461b41
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128079977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf2a2b99637a1eb48882fba6faa579247ff8818f0cdcf3c5a77ff361da4a243`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:50:17 GMT
ARG ASSET=ce
# Sat, 16 Oct 2021 02:50:17 GMT
ENV ASSET=ce
# Sat, 16 Oct 2021 02:50:18 GMT
ARG EE_PORTS
# Sat, 16 Oct 2021 02:50:18 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Sat, 16 Oct 2021 02:50:18 GMT
ARG KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 02:50:18 GMT
ENV KONG_VERSION=2.6.0
# Sat, 16 Oct 2021 02:50:42 GMT
RUN set -ex     && apt-get update     && if [ "$ASSET" = "ce" ] ; then       apt-get install -y curl       && curl -fL https://download.konghq.com/gateway-${KONG_VERSION%%.*}.x-ubuntu-$(cat /etc/os-release | grep UBUNTU_CODENAME | cut -d = -f 2)/pool/all/k/kong/kong_${KONG_VERSION}_$(dpkg --print-architecture).deb -o /tmp/kong.deb       && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && ln -s /usr/local/openresty/bin/resty /usr/local/bin/resty     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/luajit     && ln -s /usr/local/openresty/luajit/bin/luajit /usr/local/bin/lua     && ln -s /usr/local/openresty/nginx/sbin/nginx /usr/local/bin/nginx     && if [ "$ASSET" = "ce" ] ; then       kong version ;     fi
# Sat, 16 Oct 2021 02:50:43 GMT
COPY file:df7f26941e26fd034e43646906785ecba3877cf078fa891fd1d304925f70408e in /docker-entrypoint.sh 
# Sat, 16 Oct 2021 02:50:43 GMT
USER kong
# Sat, 16 Oct 2021 02:50:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 16 Oct 2021 02:50:43 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 16 Oct 2021 02:50:44 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Oct 2021 02:50:44 GMT
HEALTHCHECK &{["CMD-SHELL" "kong health"] "10s" "10s" "0s" '\n'}
# Sat, 16 Oct 2021 02:50:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a161c721a16c61e7d874293e0cdd47f98a8f82b390bdf961d621a52dbdc1ac41`  
		Last Modified: Sat, 16 Oct 2021 02:51:59 GMT  
		Size: 25.1 MB (25081963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1745eff81ab1e1489b4fee2bf5aa39eef6d63e8a5dd9f1f0921ca369dfb3582f`  
		Last Modified: Sat, 16 Oct 2021 02:52:10 GMT  
		Size: 74.4 MB (74430032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7526fc9f882ef9a7c3b3e67b003a8d9c1caa238e2f3f40b6174ff750d5e5d9a6`  
		Last Modified: Sat, 16 Oct 2021 02:51:57 GMT  
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
