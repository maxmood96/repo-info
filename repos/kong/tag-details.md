<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kong`

-	[`kong:2`](#kong2)
-	[`kong:2.0`](#kong20)
-	[`kong:2.0.5`](#kong205)
-	[`kong:2.0.5-alpine`](#kong205-alpine)
-	[`kong:2.0.5-centos`](#kong205-centos)
-	[`kong:2.0.5-ubuntu`](#kong205-ubuntu)
-	[`kong:2.0-centos`](#kong20-centos)
-	[`kong:2.0-ubuntu`](#kong20-ubuntu)
-	[`kong:2.1`](#kong21)
-	[`kong:2.1.4`](#kong214)
-	[`kong:2.1.4-alpine`](#kong214-alpine)
-	[`kong:2.1.4-centos`](#kong214-centos)
-	[`kong:2.1.4-ubuntu`](#kong214-ubuntu)
-	[`kong:2.1-alpine`](#kong21-alpine)
-	[`kong:2.1-centos`](#kong21-centos)
-	[`kong:2.1-ubuntu`](#kong21-ubuntu)
-	[`kong:2.2`](#kong22)
-	[`kong:2.2.2`](#kong222)
-	[`kong:2.2.2-alpine`](#kong222-alpine)
-	[`kong:2.2.2-centos`](#kong222-centos)
-	[`kong:2.2.2-ubuntu`](#kong222-ubuntu)
-	[`kong:2.2-alpine`](#kong22-alpine)
-	[`kong:2.2-centos`](#kong22-centos)
-	[`kong:2.2-ubuntu`](#kong22-ubuntu)
-	[`kong:2.3`](#kong23)
-	[`kong:2.3.2`](#kong232)
-	[`kong:2.3.2-alpine`](#kong232-alpine)
-	[`kong:2.3.2-centos`](#kong232-centos)
-	[`kong:2.3.2-ubuntu`](#kong232-ubuntu)
-	[`kong:2.3-alpine`](#kong23-alpine)
-	[`kong:2.3-centos`](#kong23-centos)
-	[`kong:2.3-ubuntu`](#kong23-ubuntu)
-	[`kong:alpine`](#kongalpine)
-	[`kong:centos`](#kongcentos)
-	[`kong:latest`](#konglatest)
-	[`kong:ubuntu`](#kongubuntu)

## `kong:2`

```console
$ docker pull kong@sha256:b6df904a47c82dd0701dc13f65b6266908cbeb3bbeec8e0579cfbcc6fd4e791e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2` - linux; amd64

```console
$ docker pull kong@sha256:264012de525385f2db42318611e387b306380354d273e81e6e56e120b6517338
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50938390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb50817914445878879a768e55a80d4ecca29754f7b653bf1c070b5598bc1ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:54:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:54:52 GMT
USER kong
# Wed, 24 Feb 2021 23:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:54:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:54:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:54:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24fc8c85ed2920bce371544b9e89e3aab573f62b95d1d49df9a02c2a51936e5`  
		Last Modified: Wed, 24 Feb 2021 23:57:52 GMT  
		Size: 48.1 MB (48122212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96136c04ffeebb0b7fc6524bf5277a483472101f625f359f94a50e827ce264fc`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bb9932af2cac4eda8f7394651f8657be5396d5a01dba0976d08070b8fd0117e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50465123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282e4dce09f74eaa7ba83dae27a5462dad636d02ed6b9c9553c4e66fcc2dc51`
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
# Wed, 24 Feb 2021 23:33:50 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:50 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:51 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:52 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:53 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:33:54 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:34:15 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:34:18 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:34:20 GMT
USER kong
# Wed, 24 Feb 2021 23:34:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:34:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:34:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:34:26 GMT
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
	-	`sha256:d761e799b29bca6ab070a506112eb88010e4f015a27e9b673e5f63c492c33f2c`  
		Last Modified: Wed, 24 Feb 2021 23:37:15 GMT  
		Size: 47.7 MB (47738443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e81a656d179645231aa7afd3e70d4ab1ca97115a29e3e20f20ee8afaa0b93`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0`

```console
$ docker pull kong@sha256:2497e9fbf9174f0f4a9cf556d96550c0f53e807bf8bdb81790285b0194950134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0` - linux; amd64

```console
$ docker pull kong@sha256:cb66d60c8df4f13daa669ab53e35e562812b4f5e82963b4439fcb43ec0ac4e97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52767219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3969808a3391d7ab575139085385df60ef8052886b99266ebed7b1cebce764`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:56:20 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:56:20 GMT
ARG KONG_VERSION=2.0.5
# Wed, 24 Feb 2021 23:56:20 GMT
ENV KONG_VERSION=2.0.5
# Wed, 24 Feb 2021 23:56:21 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 24 Feb 2021 23:56:21 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 24 Feb 2021 23:56:33 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Wed, 24 Feb 2021 23:56:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:56:34 GMT
USER kong
# Wed, 24 Feb 2021 23:56:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:56:34 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:56:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:56:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd8d038b0f020e5db920d9154cd4f0e97be7906db4bb15ccf7c6d467a035ffb`  
		Last Modified: Wed, 24 Feb 2021 23:58:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbde60845e9c7acd1135c24c4d5bfa2986bce3c9e1a5b2e3c688b8df835e763`  
		Last Modified: Wed, 24 Feb 2021 23:59:12 GMT  
		Size: 50.0 MB (49951044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19627347c5a15a3ba1f712747deb0e8d456a2880855516a833fcee6c18b2d8`  
		Last Modified: Wed, 24 Feb 2021 23:58:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5`

```console
$ docker pull kong@sha256:2497e9fbf9174f0f4a9cf556d96550c0f53e807bf8bdb81790285b0194950134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5` - linux; amd64

```console
$ docker pull kong@sha256:cb66d60c8df4f13daa669ab53e35e562812b4f5e82963b4439fcb43ec0ac4e97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52767219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3969808a3391d7ab575139085385df60ef8052886b99266ebed7b1cebce764`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:56:20 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:56:20 GMT
ARG KONG_VERSION=2.0.5
# Wed, 24 Feb 2021 23:56:20 GMT
ENV KONG_VERSION=2.0.5
# Wed, 24 Feb 2021 23:56:21 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 24 Feb 2021 23:56:21 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 24 Feb 2021 23:56:33 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Wed, 24 Feb 2021 23:56:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:56:34 GMT
USER kong
# Wed, 24 Feb 2021 23:56:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:56:34 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:56:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:56:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd8d038b0f020e5db920d9154cd4f0e97be7906db4bb15ccf7c6d467a035ffb`  
		Last Modified: Wed, 24 Feb 2021 23:58:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbde60845e9c7acd1135c24c4d5bfa2986bce3c9e1a5b2e3c688b8df835e763`  
		Last Modified: Wed, 24 Feb 2021 23:59:12 GMT  
		Size: 50.0 MB (49951044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19627347c5a15a3ba1f712747deb0e8d456a2880855516a833fcee6c18b2d8`  
		Last Modified: Wed, 24 Feb 2021 23:58:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-alpine`

```console
$ docker pull kong@sha256:2497e9fbf9174f0f4a9cf556d96550c0f53e807bf8bdb81790285b0194950134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-alpine` - linux; amd64

```console
$ docker pull kong@sha256:cb66d60c8df4f13daa669ab53e35e562812b4f5e82963b4439fcb43ec0ac4e97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52767219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3969808a3391d7ab575139085385df60ef8052886b99266ebed7b1cebce764`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:56:20 GMT
COPY file:987d0472e007e4e357d96fa432bce568836a2259b787227f9a9e1c369d9efc37 in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:56:20 GMT
ARG KONG_VERSION=2.0.5
# Wed, 24 Feb 2021 23:56:20 GMT
ENV KONG_VERSION=2.0.5
# Wed, 24 Feb 2021 23:56:21 GMT
ARG KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 24 Feb 2021 23:56:21 GMT
ENV KONG_SHA256=2e78dee0e695c238cde7e607e85c2e62e44422b57c626ea12822d15ed898769b
# Wed, 24 Feb 2021 23:56:33 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.amd64.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libgcc openssl pcre perl tzdata libcap zip bash zlib git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz && 	kong version
# Wed, 24 Feb 2021 23:56:33 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:56:34 GMT
USER kong
# Wed, 24 Feb 2021 23:56:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:56:34 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:56:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:56:35 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd8d038b0f020e5db920d9154cd4f0e97be7906db4bb15ccf7c6d467a035ffb`  
		Last Modified: Wed, 24 Feb 2021 23:58:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbde60845e9c7acd1135c24c4d5bfa2986bce3c9e1a5b2e3c688b8df835e763`  
		Last Modified: Wed, 24 Feb 2021 23:59:12 GMT  
		Size: 50.0 MB (49951044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e19627347c5a15a3ba1f712747deb0e8d456a2880855516a833fcee6c18b2d8`  
		Last Modified: Wed, 24 Feb 2021 23:58:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-centos`

```console
$ docker pull kong@sha256:079abab579c65a5b8d16be6cee38003ba4a57fd7e94b7de9168bb5c5d4d15ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0.5-centos` - linux; amd64

```console
$ docker pull kong@sha256:554d9579ae5ccc7da6cfd7a742010c445cca0294e446abd55c10903c395e902b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127491262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9f5083661211369645dcdeb6b3f5338fd57bf7316dcde5c1258cad2f951eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:02:56 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Sat, 14 Nov 2020 01:02:57 GMT
ARG KONG_VERSION=2.0.5
# Sat, 14 Nov 2020 01:02:57 GMT
ENV KONG_VERSION=2.0.5
# Sat, 14 Nov 2020 01:02:57 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 14 Nov 2020 01:02:57 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 14 Nov 2020 01:03:20 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 14 Nov 2020 01:03:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 14 Nov 2020 01:03:21 GMT
USER kong
# Sat, 14 Nov 2020 01:03:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Nov 2020 01:03:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 14 Nov 2020 01:03:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Nov 2020 01:03:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692b26149754880bb26d043fb2a9bba7fe1fb5406a67028d073895681609b4df`  
		Last Modified: Sat, 14 Nov 2020 01:04:21 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f3c5952d48cacf33b16df4f8fac200bbecacd4350fd0629a4815eec28ff1cb`  
		Last Modified: Sat, 14 Nov 2020 01:04:31 GMT  
		Size: 51.4 MB (51393250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86ddac787b13b6ae84c90e260caa89eeb915b690116162d279d9fa5197477dc`  
		Last Modified: Sat, 14 Nov 2020 01:04:20 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0.5-ubuntu`

```console
$ docker pull kong@sha256:a253f04133d6d0148add4df08c7e1af76a1d4f725d7105bf4085a1938ede66d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0.5-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d4a0adc64047bf3d0068bba75919963496dac9e4e3ecee7154bf6fba0fd53ca6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101061262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c632b0b299f9193785f70b918f73b2b4292b8b9836aa5cce54a2fe9418fa7186`
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
# Thu, 21 Jan 2021 10:27:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 10:29:10 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 21 Jan 2021 10:29:10 GMT
ARG KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 10:29:10 GMT
ENV KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 10:29:31 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 21 Jan 2021 10:29:32 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 10:29:32 GMT
USER kong
# Thu, 21 Jan 2021 10:29:33 GMT
RUN kong version
# Thu, 21 Jan 2021 10:29:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 10:29:33 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 10:29:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 10:29:34 GMT
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
	-	`sha256:e59df306867f48f345aeecb87f998c383dab57de7368896bab3a4fc9aabf2928`  
		Last Modified: Thu, 21 Jan 2021 10:31:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaf794695116fea4fb60d592e4743d8cf5fd58375981c44b4d55c3673503be2`  
		Last Modified: Thu, 21 Jan 2021 10:32:00 GMT  
		Size: 55.1 MB (55096456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6609ef38227fc6f093b2cb90924604b7d65ef7190c21aa12f77633cce60923d`  
		Last Modified: Thu, 21 Jan 2021 10:31:48 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb7e5879b9302ce552acc5e0491da8154bd2db0c24cffe78e1866ccb191ceac`  
		Last Modified: Thu, 21 Jan 2021 10:31:48 GMT  
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

## `kong:2.0-centos`

```console
$ docker pull kong@sha256:079abab579c65a5b8d16be6cee38003ba4a57fd7e94b7de9168bb5c5d4d15ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.0-centos` - linux; amd64

```console
$ docker pull kong@sha256:554d9579ae5ccc7da6cfd7a742010c445cca0294e446abd55c10903c395e902b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127491262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b9f5083661211369645dcdeb6b3f5338fd57bf7316dcde5c1258cad2f951eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:02:56 GMT
COPY file:73044b225363e2703a176f55b132687ead4bab30398788756be18d2965fac2cd in /tmp/kong.rpm 
# Sat, 14 Nov 2020 01:02:57 GMT
ARG KONG_VERSION=2.0.5
# Sat, 14 Nov 2020 01:02:57 GMT
ENV KONG_VERSION=2.0.5
# Sat, 14 Nov 2020 01:02:57 GMT
ARG KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 14 Nov 2020 01:02:57 GMT
ENV KONG_SHA256=e05340680de3541c4c940f54e64f00c90fb5137f6a8c71e413b815a411d74fc6
# Sat, 14 Nov 2020 01:03:20 GMT
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git zlib 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum install -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Sat, 14 Nov 2020 01:03:20 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 14 Nov 2020 01:03:21 GMT
USER kong
# Sat, 14 Nov 2020 01:03:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Nov 2020 01:03:21 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 14 Nov 2020 01:03:21 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Nov 2020 01:03:21 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692b26149754880bb26d043fb2a9bba7fe1fb5406a67028d073895681609b4df`  
		Last Modified: Sat, 14 Nov 2020 01:04:21 GMT  
		Size: 123.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f3c5952d48cacf33b16df4f8fac200bbecacd4350fd0629a4815eec28ff1cb`  
		Last Modified: Sat, 14 Nov 2020 01:04:31 GMT  
		Size: 51.4 MB (51393250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86ddac787b13b6ae84c90e260caa89eeb915b690116162d279d9fa5197477dc`  
		Last Modified: Sat, 14 Nov 2020 01:04:20 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.0-ubuntu`

```console
$ docker pull kong@sha256:a253f04133d6d0148add4df08c7e1af76a1d4f725d7105bf4085a1938ede66d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.0-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:d4a0adc64047bf3d0068bba75919963496dac9e4e3ecee7154bf6fba0fd53ca6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101061262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c632b0b299f9193785f70b918f73b2b4292b8b9836aa5cce54a2fe9418fa7186`
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
# Thu, 21 Jan 2021 10:27:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 10:29:10 GMT
COPY file:5307743dbc5e81034b8adaf56f281bcb13b0da2d468cb6450d72fa5b77543ccf in /tmp/kong.deb 
# Thu, 21 Jan 2021 10:29:10 GMT
ARG KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 10:29:10 GMT
ENV KONG_VERSION=2.0.5
# Thu, 21 Jan 2021 10:29:31 GMT
RUN set -ex;     if [ "$ASSET" = "ce" ] ; then         apt-get update &&         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get update     && apt-get install -y --no-install-recommends perl unzip git zlib1g     && rm -rf /var/lib/apt/lists/* 	&& dpkg -i /tmp/kong.deb 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong 	&& kong version
# Thu, 21 Jan 2021 10:29:32 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 10:29:32 GMT
USER kong
# Thu, 21 Jan 2021 10:29:33 GMT
RUN kong version
# Thu, 21 Jan 2021 10:29:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 10:29:33 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 10:29:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 10:29:34 GMT
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
	-	`sha256:e59df306867f48f345aeecb87f998c383dab57de7368896bab3a4fc9aabf2928`  
		Last Modified: Thu, 21 Jan 2021 10:31:48 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbaf794695116fea4fb60d592e4743d8cf5fd58375981c44b4d55c3673503be2`  
		Last Modified: Thu, 21 Jan 2021 10:32:00 GMT  
		Size: 55.1 MB (55096456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6609ef38227fc6f093b2cb90924604b7d65ef7190c21aa12f77633cce60923d`  
		Last Modified: Thu, 21 Jan 2021 10:31:48 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb7e5879b9302ce552acc5e0491da8154bd2db0c24cffe78e1866ccb191ceac`  
		Last Modified: Thu, 21 Jan 2021 10:31:48 GMT  
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

## `kong:2.1`

```console
$ docker pull kong@sha256:dae2c8899386874a757cc5b4fcbfcb9fd8400e8859c92896503aac9e957f6b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1` - linux; amd64

```console
$ docker pull kong@sha256:ddbb3aae4307a5aba6e94d98080ef2769dbb62c4c3be9392900d083a8f687ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53154490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49b4951d5599a1fe5f695efab666402c41a8706135f8d810ca89f919d06d14f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:55:45 GMT
ARG KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:55:46 GMT
ENV KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:55:58 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 24 Feb 2021 23:55:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:55:59 GMT
USER kong
# Wed, 24 Feb 2021 23:56:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:56:00 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:56:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:56:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a565c9799293e6a874681e8b1f960ca078baabfff62d7e15f2804dbbdc8d979`  
		Last Modified: Wed, 24 Feb 2021 23:58:48 GMT  
		Size: 50.3 MB (50338312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12c4762266655c2c7a65b86b2dd286b69a6a3065f435bff48154ffdeeea8935`  
		Last Modified: Wed, 24 Feb 2021 23:58:33 GMT  
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

## `kong:2.1.4`

```console
$ docker pull kong@sha256:dae2c8899386874a757cc5b4fcbfcb9fd8400e8859c92896503aac9e957f6b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4` - linux; amd64

```console
$ docker pull kong@sha256:ddbb3aae4307a5aba6e94d98080ef2769dbb62c4c3be9392900d083a8f687ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53154490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49b4951d5599a1fe5f695efab666402c41a8706135f8d810ca89f919d06d14f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:55:45 GMT
ARG KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:55:46 GMT
ENV KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:55:58 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 24 Feb 2021 23:55:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:55:59 GMT
USER kong
# Wed, 24 Feb 2021 23:56:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:56:00 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:56:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:56:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a565c9799293e6a874681e8b1f960ca078baabfff62d7e15f2804dbbdc8d979`  
		Last Modified: Wed, 24 Feb 2021 23:58:48 GMT  
		Size: 50.3 MB (50338312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12c4762266655c2c7a65b86b2dd286b69a6a3065f435bff48154ffdeeea8935`  
		Last Modified: Wed, 24 Feb 2021 23:58:33 GMT  
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
$ docker pull kong@sha256:dae2c8899386874a757cc5b4fcbfcb9fd8400e8859c92896503aac9e957f6b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-alpine` - linux; amd64

```console
$ docker pull kong@sha256:ddbb3aae4307a5aba6e94d98080ef2769dbb62c4c3be9392900d083a8f687ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53154490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49b4951d5599a1fe5f695efab666402c41a8706135f8d810ca89f919d06d14f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:55:45 GMT
ARG KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:55:46 GMT
ENV KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:55:58 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 24 Feb 2021 23:55:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:55:59 GMT
USER kong
# Wed, 24 Feb 2021 23:56:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:56:00 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:56:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:56:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a565c9799293e6a874681e8b1f960ca078baabfff62d7e15f2804dbbdc8d979`  
		Last Modified: Wed, 24 Feb 2021 23:58:48 GMT  
		Size: 50.3 MB (50338312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12c4762266655c2c7a65b86b2dd286b69a6a3065f435bff48154ffdeeea8935`  
		Last Modified: Wed, 24 Feb 2021 23:58:33 GMT  
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
$ docker pull kong@sha256:2074a8dbc332a2d158a41f480915d2cca721cd24449a36a956d673b992551da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1.4-centos` - linux; amd64

```console
$ docker pull kong@sha256:9abae830a109a6c87cf973fab99656a87fe37c1a53c195d79fa8b2448d85a75d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127260020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a08e453725f88199609cc19d52cc849a8b829755d8ea61b90d497a84e9c4b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 14 Nov 2020 01:02:16 GMT
ARG KONG_VERSION=2.1.4
# Sat, 14 Nov 2020 01:02:16 GMT
ENV KONG_VERSION=2.1.4
# Sat, 14 Nov 2020 01:02:16 GMT
ARG KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
# Sat, 14 Nov 2020 01:02:42 GMT
# ARGS: KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum --nogpgcheck localinstall -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 14 Nov 2020 01:02:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 14 Nov 2020 01:02:43 GMT
USER kong
# Sat, 14 Nov 2020 01:02:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Nov 2020 01:02:43 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 14 Nov 2020 01:02:43 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Nov 2020 01:02:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a690a7e5955b5f53b5859ac1391b51d1584818a0bbc504061e654b26d4d71f`  
		Last Modified: Sat, 14 Nov 2020 01:04:13 GMT  
		Size: 51.2 MB (51162000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4dd8889546b4ae415188145fb1dde0b9c303884420d3874d1673772dd91321`  
		Last Modified: Sat, 14 Nov 2020 01:04:01 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1.4-ubuntu`

```console
$ docker pull kong@sha256:fbb43a92e427a8c475ca9aeab6da893dcbe664c2f5fe8662a4d9097ac8dc5a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1.4-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c217a71f4c1b03322b0cb0cdaf0ef0f43cad8c383bbe7965df2c321769baafb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133892825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b939a024df189cd0c5d8d1b18bab5c712caae887c9b0f1952f0dd501cb55ee`
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
# Thu, 21 Jan 2021 10:27:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 10:27:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 21 Jan 2021 10:28:29 GMT
ARG KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 10:28:29 GMT
ENV KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 10:28:53 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 21 Jan 2021 10:28:54 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 10:28:54 GMT
USER kong
# Thu, 21 Jan 2021 10:28:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 10:28:54 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 10:28:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 10:28:55 GMT
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
	-	`sha256:7491b48e51562c145461304393cbc54944e319e09a7714bf0e4264da38b8a8f0`  
		Last Modified: Thu, 21 Jan 2021 10:30:38 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478fb2c434a20e74e5b8e75ac9bee465de878d648ea39cd63d103f13094e148c`  
		Last Modified: Thu, 21 Jan 2021 10:31:36 GMT  
		Size: 62.8 MB (62846282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b38df337740461e6803aeffe82a6b1667ea01b7ad839bebd14044c0b47ec4c`  
		Last Modified: Thu, 21 Jan 2021 10:31:24 GMT  
		Size: 689.0 B  
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

## `kong:2.1-alpine`

```console
$ docker pull kong@sha256:dae2c8899386874a757cc5b4fcbfcb9fd8400e8859c92896503aac9e957f6b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-alpine` - linux; amd64

```console
$ docker pull kong@sha256:ddbb3aae4307a5aba6e94d98080ef2769dbb62c4c3be9392900d083a8f687ab0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53154490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49b4951d5599a1fe5f695efab666402c41a8706135f8d810ca89f919d06d14f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:55:45 GMT
ARG KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:55:46 GMT
ENV KONG_VERSION=2.1.4
# Wed, 24 Feb 2021 23:55:58 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='760cea1f7a058be6000e14dfecfeb73cc79245f696f18e0fcf0825935b944ab3' ;; 		aarch64) arch='arm64'; KONG_SHA256='08038f49f162ab5edc357d7712e90241f6571027cb8741b15ba0c951653764c2' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong; 	tar -C /kong -xzf /tmp/kong.tar.gz && 	mv /kong/usr/local/* /usr/local && 	mv /kong/etc/* /etc && 	rm -rf /kong && 	apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash zlib zlib-dev git ca-certificates && 	adduser -S kong && 	mkdir -p "/usr/local/kong" && 	chown -R kong:0 /usr/local/kong && 	chown kong:0 /usr/local/bin/kong && 	chmod -R g=u /usr/local/kong && 	rm -rf /tmp/kong.tar.gz &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 24 Feb 2021 23:55:59 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:55:59 GMT
USER kong
# Wed, 24 Feb 2021 23:56:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:56:00 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:56:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:56:01 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a565c9799293e6a874681e8b1f960ca078baabfff62d7e15f2804dbbdc8d979`  
		Last Modified: Wed, 24 Feb 2021 23:58:48 GMT  
		Size: 50.3 MB (50338312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12c4762266655c2c7a65b86b2dd286b69a6a3065f435bff48154ffdeeea8935`  
		Last Modified: Wed, 24 Feb 2021 23:58:33 GMT  
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
$ docker pull kong@sha256:2074a8dbc332a2d158a41f480915d2cca721cd24449a36a956d673b992551da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.1-centos` - linux; amd64

```console
$ docker pull kong@sha256:9abae830a109a6c87cf973fab99656a87fe37c1a53c195d79fa8b2448d85a75d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127260020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a08e453725f88199609cc19d52cc849a8b829755d8ea61b90d497a84e9c4b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Sat, 14 Nov 2020 01:02:16 GMT
ARG KONG_VERSION=2.1.4
# Sat, 14 Nov 2020 01:02:16 GMT
ENV KONG_VERSION=2.1.4
# Sat, 14 Nov 2020 01:02:16 GMT
ARG KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
# Sat, 14 Nov 2020 01:02:42 GMT
# ARGS: KONG_SHA256=5f44985dcf79e0ad59463b3e3eb9d6623dc9234793bd9c108c0eac8d65b62ab0
RUN set -ex; 	if [ "$ASSET" = "ce" ] ; then 		curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm 		&& echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -; 	fi; 	yum install -y -q unzip shadow-utils git 	&& yum clean all -q 	&& rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki 	&& useradd kong 	&& mkdir -p "/usr/local/kong" 	&& yum --nogpgcheck localinstall -y /tmp/kong.rpm 	&& yum clean all 	&& rm /tmp/kong.rpm 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Sat, 14 Nov 2020 01:02:42 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Sat, 14 Nov 2020 01:02:43 GMT
USER kong
# Sat, 14 Nov 2020 01:02:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 14 Nov 2020 01:02:43 GMT
EXPOSE 8000 8001 8443 8444
# Sat, 14 Nov 2020 01:02:43 GMT
STOPSIGNAL SIGQUIT
# Sat, 14 Nov 2020 01:02:43 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a690a7e5955b5f53b5859ac1391b51d1584818a0bbc504061e654b26d4d71f`  
		Last Modified: Sat, 14 Nov 2020 01:04:13 GMT  
		Size: 51.2 MB (51162000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4dd8889546b4ae415188145fb1dde0b9c303884420d3874d1673772dd91321`  
		Last Modified: Sat, 14 Nov 2020 01:04:01 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.1-ubuntu`

```console
$ docker pull kong@sha256:fbb43a92e427a8c475ca9aeab6da893dcbe664c2f5fe8662a4d9097ac8dc5a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.1-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:c217a71f4c1b03322b0cb0cdaf0ef0f43cad8c383bbe7965df2c321769baafb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.9 MB (133892825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b939a024df189cd0c5d8d1b18bab5c712caae887c9b0f1952f0dd501cb55ee`
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
# Thu, 21 Jan 2021 10:27:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 10:27:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 21 Jan 2021 10:28:29 GMT
ARG KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 10:28:29 GMT
ENV KONG_VERSION=2.1.4
# Thu, 21 Jan 2021 10:28:53 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update 	&& apt install --yes /tmp/kong.deb 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /tmp/kong.deb 	&& useradd -ms /bin/bash kong     && mkdir -p "/usr/local/kong" 	&& chown -R kong:0 /usr/local/kong 	&& chown kong:0 /usr/local/bin/kong 	&& chmod -R g=u /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 21 Jan 2021 10:28:54 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 10:28:54 GMT
USER kong
# Thu, 21 Jan 2021 10:28:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 10:28:54 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 10:28:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 10:28:55 GMT
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
	-	`sha256:7491b48e51562c145461304393cbc54944e319e09a7714bf0e4264da38b8a8f0`  
		Last Modified: Thu, 21 Jan 2021 10:30:38 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478fb2c434a20e74e5b8e75ac9bee465de878d648ea39cd63d103f13094e148c`  
		Last Modified: Thu, 21 Jan 2021 10:31:36 GMT  
		Size: 62.8 MB (62846282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b38df337740461e6803aeffe82a6b1667ea01b7ad839bebd14044c0b47ec4c`  
		Last Modified: Thu, 21 Jan 2021 10:31:24 GMT  
		Size: 689.0 B  
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

## `kong:2.2`

```console
$ docker pull kong@sha256:208d69edfd8ed138f6e63ae1593e15ce36fa31664c2d13c8c886ea031c8c1b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2` - linux; amd64

```console
$ docker pull kong@sha256:81528a450c475a819688b2f9894387cfb1b6b46c61a5dedae8d24ed53d859f80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53281097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d037544a9572ee401030f9f2bab5e2e60536ea3d4e22e8aa6acb09eab516cfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:55:09 GMT
ARG KONG_VERSION=2.2.1
# Wed, 24 Feb 2021 23:55:11 GMT
ENV KONG_VERSION=2.2.1
# Wed, 24 Feb 2021 23:55:26 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:55:27 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:55:27 GMT
USER kong
# Wed, 24 Feb 2021 23:55:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:55:28 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:55:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:55:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17154cf4731d2d5c2aa6bb28f251c94024865662aa4dea77023b25cc835d0c7`  
		Last Modified: Wed, 24 Feb 2021 23:58:23 GMT  
		Size: 50.5 MB (50464918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2c4c596620ff4926027481535366073a8bd81ac5856d2aaf12fabe1bdf9ecc`  
		Last Modified: Wed, 24 Feb 2021 23:58:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1846da93104802031dadcb88fde2ee0a33e8e468ae7b3141a754c98fa5e05afa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52804344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354dbe8be81e8a6c2af186c111fbb6dcd903d3c2cb94ad0d840a2a889e97f940`
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
# Wed, 24 Feb 2021 23:34:46 GMT
ARG KONG_VERSION=2.2.1
# Wed, 24 Feb 2021 23:34:47 GMT
ENV KONG_VERSION=2.2.1
# Wed, 24 Feb 2021 23:35:07 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:35:10 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:35:11 GMT
USER kong
# Wed, 24 Feb 2021 23:35:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:35:13 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:35:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:35:16 GMT
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
	-	`sha256:9b92d5b5d9892febad85751c3f1d669e2904bba57f44d7eec28eef85aa38c315`  
		Last Modified: Wed, 24 Feb 2021 23:37:44 GMT  
		Size: 50.1 MB (50077664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acb289077bed0b4531c3781d479c2c08fe523fe7ec9b82fa7967576b6e21c94`  
		Last Modified: Wed, 24 Feb 2021 23:37:29 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2.2`

**does not exist** (yet?)

## `kong:2.2.2-alpine`

**does not exist** (yet?)

## `kong:2.2.2-centos`

**does not exist** (yet?)

## `kong:2.2.2-ubuntu`

**does not exist** (yet?)

## `kong:2.2-alpine`

```console
$ docker pull kong@sha256:208d69edfd8ed138f6e63ae1593e15ce36fa31664c2d13c8c886ea031c8c1b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:81528a450c475a819688b2f9894387cfb1b6b46c61a5dedae8d24ed53d859f80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53281097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d037544a9572ee401030f9f2bab5e2e60536ea3d4e22e8aa6acb09eab516cfc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:55:09 GMT
ARG KONG_VERSION=2.2.1
# Wed, 24 Feb 2021 23:55:11 GMT
ENV KONG_VERSION=2.2.1
# Wed, 24 Feb 2021 23:55:26 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:55:27 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:55:27 GMT
USER kong
# Wed, 24 Feb 2021 23:55:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:55:28 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:55:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:55:28 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17154cf4731d2d5c2aa6bb28f251c94024865662aa4dea77023b25cc835d0c7`  
		Last Modified: Wed, 24 Feb 2021 23:58:23 GMT  
		Size: 50.5 MB (50464918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2c4c596620ff4926027481535366073a8bd81ac5856d2aaf12fabe1bdf9ecc`  
		Last Modified: Wed, 24 Feb 2021 23:58:08 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1846da93104802031dadcb88fde2ee0a33e8e468ae7b3141a754c98fa5e05afa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52804344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354dbe8be81e8a6c2af186c111fbb6dcd903d3c2cb94ad0d840a2a889e97f940`
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
# Wed, 24 Feb 2021 23:34:46 GMT
ARG KONG_VERSION=2.2.1
# Wed, 24 Feb 2021 23:34:47 GMT
ENV KONG_VERSION=2.2.1
# Wed, 24 Feb 2021 23:35:07 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256='e05c7075ae263bb7ef84b0370bf4e31f5246a41d910e5d4336216ae95b654af1' ;; 		aarch64) arch='arm64'; KONG_SHA256='c7b2c0e1f47e3009e55b492344bd1ff689a41eca91c21f2c3f57f9172932c96d' ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:35:10 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:35:11 GMT
USER kong
# Wed, 24 Feb 2021 23:35:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:35:13 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:35:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:35:16 GMT
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
	-	`sha256:9b92d5b5d9892febad85751c3f1d669e2904bba57f44d7eec28eef85aa38c315`  
		Last Modified: Wed, 24 Feb 2021 23:37:44 GMT  
		Size: 50.1 MB (50077664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3acb289077bed0b4531c3781d479c2c08fe523fe7ec9b82fa7967576b6e21c94`  
		Last Modified: Wed, 24 Feb 2021 23:37:29 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-centos`

```console
$ docker pull kong@sha256:ad8632341f4a81d75058c45dff279fa8938f20b2a18d7eae41b843fb2d94f4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.2-centos` - linux; amd64

```console
$ docker pull kong@sha256:6a710cd063951cfe5e89bca7b1f64e68ad1b5ea33f7268fb9ba13c530dcb9307
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127352007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a665d19b27df8e7b9b66445eeae0c72957bde11c041ee73094b778406c6d86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 02 Dec 2020 01:05:53 GMT
ARG KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:53 GMT
ENV KONG_VERSION=2.2.1
# Wed, 02 Dec 2020 01:05:53 GMT
ARG KONG_SHA256=aed53fd4779559d9ff618c634e4c3c3281cca550d9b1bcdae8e7359602bd6771
# Wed, 02 Dec 2020 01:06:25 GMT
# ARGS: KONG_SHA256=aed53fd4779559d9ff618c634e4c3c3281cca550d9b1bcdae8e7359602bd6771
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 02 Dec 2020 01:06:25 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 02 Dec 2020 01:06:25 GMT
USER kong
# Wed, 02 Dec 2020 01:06:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Dec 2020 01:06:26 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 02 Dec 2020 01:06:26 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Dec 2020 01:06:26 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef344440583f6238cd4ca52ab5606f1580aa083301cde2fc96a8a774b86132`  
		Last Modified: Wed, 02 Dec 2020 01:07:59 GMT  
		Size: 51.3 MB (51253987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4f52bbd47f126044058af2b82176e13c002b85536baa59a34e64c9b3f78e70`  
		Last Modified: Wed, 02 Dec 2020 01:07:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.2-ubuntu`

```console
$ docker pull kong@sha256:06ac94140ba2decd2ef435f85b639f7a2ed7e9727e02637a2a594917897a0aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:b9e0f47fc5cd1de5b7b4a66de656beb70a80f14682d05ed1a544b0aedf56bcf9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133971365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6571bd1a9beea71ef9e8413ff7ac5035cf9f508766cdaa9142dcba12432a3b0c`
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
# Thu, 21 Jan 2021 10:27:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 10:27:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Thu, 21 Jan 2021 10:27:46 GMT
ARG KONG_VERSION=2.2.1
# Thu, 21 Jan 2021 10:27:47 GMT
ENV KONG_VERSION=2.2.1
# Thu, 21 Jan 2021 10:28:11 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 21 Jan 2021 10:28:12 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 10:28:12 GMT
USER kong
# Thu, 21 Jan 2021 10:28:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 10:28:12 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 10:28:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 10:28:13 GMT
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
	-	`sha256:7491b48e51562c145461304393cbc54944e319e09a7714bf0e4264da38b8a8f0`  
		Last Modified: Thu, 21 Jan 2021 10:30:38 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c723eda59c9aaf83a7cfabf052c52524f972d8b7e7143311cba0c901f9d3fba`  
		Last Modified: Thu, 21 Jan 2021 10:31:12 GMT  
		Size: 62.9 MB (62924822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a06631380cf61805879ae1c3ba484ca939c7e1ead8649519907b9326657599`  
		Last Modified: Thu, 21 Jan 2021 10:31:00 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:1f260bffdb3ba66996ff0dfefb4752c826a10fe2f86671d7680de040b117dc98
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125310381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06364eb859878bd561e717336897154eb340edd64b397a641760a25bce9b5f6`
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
# Thu, 21 Jan 2021 05:33:17 GMT
ARG KONG_VERSION=2.2.1
# Thu, 21 Jan 2021 05:33:18 GMT
ENV KONG_VERSION=2.2.1
# Thu, 21 Jan 2021 05:34:09 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Thu, 21 Jan 2021 05:34:11 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Thu, 21 Jan 2021 05:34:11 GMT
USER kong
# Thu, 21 Jan 2021 05:34:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Jan 2021 05:34:13 GMT
EXPOSE 8000 8001 8443 8444
# Thu, 21 Jan 2021 05:34:13 GMT
STOPSIGNAL SIGQUIT
# Thu, 21 Jan 2021 05:34:14 GMT
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
	-	`sha256:5c07b5f37536d981d099266e8c8e6378a5db1ef1f1fc4eb7237506959e2e467b`  
		Last Modified: Thu, 21 Jan 2021 05:38:06 GMT  
		Size: 59.3 MB (59341032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325527c598003a1519b9e3b5ae36346af0aacfcf97c4b60f77653fa6c7d821ba`  
		Last Modified: Thu, 21 Jan 2021 05:37:52 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3`

```console
$ docker pull kong@sha256:b6df904a47c82dd0701dc13f65b6266908cbeb3bbeec8e0579cfbcc6fd4e791e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3` - linux; amd64

```console
$ docker pull kong@sha256:264012de525385f2db42318611e387b306380354d273e81e6e56e120b6517338
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50938390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb50817914445878879a768e55a80d4ecca29754f7b653bf1c070b5598bc1ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:54:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:54:52 GMT
USER kong
# Wed, 24 Feb 2021 23:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:54:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:54:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:54:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24fc8c85ed2920bce371544b9e89e3aab573f62b95d1d49df9a02c2a51936e5`  
		Last Modified: Wed, 24 Feb 2021 23:57:52 GMT  
		Size: 48.1 MB (48122212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96136c04ffeebb0b7fc6524bf5277a483472101f625f359f94a50e827ce264fc`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bb9932af2cac4eda8f7394651f8657be5396d5a01dba0976d08070b8fd0117e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50465123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282e4dce09f74eaa7ba83dae27a5462dad636d02ed6b9c9553c4e66fcc2dc51`
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
# Wed, 24 Feb 2021 23:33:50 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:50 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:51 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:52 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:53 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:33:54 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:34:15 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:34:18 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:34:20 GMT
USER kong
# Wed, 24 Feb 2021 23:34:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:34:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:34:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:34:26 GMT
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
	-	`sha256:d761e799b29bca6ab070a506112eb88010e4f015a27e9b673e5f63c492c33f2c`  
		Last Modified: Wed, 24 Feb 2021 23:37:15 GMT  
		Size: 47.7 MB (47738443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e81a656d179645231aa7afd3e70d4ab1ca97115a29e3e20f20ee8afaa0b93`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.2`

```console
$ docker pull kong@sha256:b6df904a47c82dd0701dc13f65b6266908cbeb3bbeec8e0579cfbcc6fd4e791e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.2` - linux; amd64

```console
$ docker pull kong@sha256:264012de525385f2db42318611e387b306380354d273e81e6e56e120b6517338
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50938390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb50817914445878879a768e55a80d4ecca29754f7b653bf1c070b5598bc1ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:54:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:54:52 GMT
USER kong
# Wed, 24 Feb 2021 23:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:54:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:54:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:54:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24fc8c85ed2920bce371544b9e89e3aab573f62b95d1d49df9a02c2a51936e5`  
		Last Modified: Wed, 24 Feb 2021 23:57:52 GMT  
		Size: 48.1 MB (48122212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96136c04ffeebb0b7fc6524bf5277a483472101f625f359f94a50e827ce264fc`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.2` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bb9932af2cac4eda8f7394651f8657be5396d5a01dba0976d08070b8fd0117e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50465123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282e4dce09f74eaa7ba83dae27a5462dad636d02ed6b9c9553c4e66fcc2dc51`
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
# Wed, 24 Feb 2021 23:33:50 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:50 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:51 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:52 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:53 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:33:54 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:34:15 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:34:18 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:34:20 GMT
USER kong
# Wed, 24 Feb 2021 23:34:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:34:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:34:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:34:26 GMT
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
	-	`sha256:d761e799b29bca6ab070a506112eb88010e4f015a27e9b673e5f63c492c33f2c`  
		Last Modified: Wed, 24 Feb 2021 23:37:15 GMT  
		Size: 47.7 MB (47738443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e81a656d179645231aa7afd3e70d4ab1ca97115a29e3e20f20ee8afaa0b93`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.2-alpine`

```console
$ docker pull kong@sha256:b6df904a47c82dd0701dc13f65b6266908cbeb3bbeec8e0579cfbcc6fd4e791e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.2-alpine` - linux; amd64

```console
$ docker pull kong@sha256:264012de525385f2db42318611e387b306380354d273e81e6e56e120b6517338
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50938390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb50817914445878879a768e55a80d4ecca29754f7b653bf1c070b5598bc1ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:54:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:54:52 GMT
USER kong
# Wed, 24 Feb 2021 23:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:54:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:54:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:54:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24fc8c85ed2920bce371544b9e89e3aab573f62b95d1d49df9a02c2a51936e5`  
		Last Modified: Wed, 24 Feb 2021 23:57:52 GMT  
		Size: 48.1 MB (48122212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96136c04ffeebb0b7fc6524bf5277a483472101f625f359f94a50e827ce264fc`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.2-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bb9932af2cac4eda8f7394651f8657be5396d5a01dba0976d08070b8fd0117e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50465123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282e4dce09f74eaa7ba83dae27a5462dad636d02ed6b9c9553c4e66fcc2dc51`
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
# Wed, 24 Feb 2021 23:33:50 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:50 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:51 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:52 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:53 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:33:54 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:34:15 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:34:18 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:34:20 GMT
USER kong
# Wed, 24 Feb 2021 23:34:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:34:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:34:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:34:26 GMT
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
	-	`sha256:d761e799b29bca6ab070a506112eb88010e4f015a27e9b673e5f63c492c33f2c`  
		Last Modified: Wed, 24 Feb 2021 23:37:15 GMT  
		Size: 47.7 MB (47738443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e81a656d179645231aa7afd3e70d4ab1ca97115a29e3e20f20ee8afaa0b93`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.2-centos`

```console
$ docker pull kong@sha256:0cc576dd4ef99a2b49bae75fd85e6d493a777eacf8833dc5daa0c5de9564c261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.3.2-centos` - linux; amd64

```console
$ docker pull kong@sha256:7bd92331a362473eb429c998283d4dd7c4d3ab81c7488f07b0e4c83fbcf7d253
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127452514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793035e30a2dff29e7b79510065aef13499f016f8318e9a75377b095fc7d59e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 10 Feb 2021 19:21:10 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:10 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:10 GMT
ARG KONG_SHA256=aad05b5b7425a0c1dc3095363c785a4147d3cd91064f0221a2a818c7bdcc97dc
# Wed, 10 Feb 2021 19:21:43 GMT
# ARGS: KONG_SHA256=aad05b5b7425a0c1dc3095363c785a4147d3cd91064f0221a2a818c7bdcc97dc
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 10 Feb 2021 19:21:43 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:21:43 GMT
USER kong
# Wed, 10 Feb 2021 19:21:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:21:43 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:21:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:21:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2f33f2efc166cb5c8fe700bba55f203a47ac68805d7584af1566032ae9fdb8`  
		Last Modified: Wed, 10 Feb 2021 19:23:37 GMT  
		Size: 51.4 MB (51354495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c8c693e04f11baabbca865e259871d10ac47ad2086140fb01a92d250a28c6`  
		Last Modified: Wed, 10 Feb 2021 19:23:27 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3.2-ubuntu`

```console
$ docker pull kong@sha256:66668da50260386c63cc5b0ca236930af6824c6aef04f4e032a164c2c899b3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3.2-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:01d99df2c738fd91787846bb092443f5a571b9cb616cad124bf24de44d2484bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcf5a3c8737b98c5576918ff224bad267e7fd85be030a022ed377528777b59a`
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
# Thu, 21 Jan 2021 10:27:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 10:27:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 10 Feb 2021 19:20:15 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:20:15 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:01 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 10 Feb 2021 19:21:01 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:21:01 GMT
USER kong
# Wed, 10 Feb 2021 19:21:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:21:02 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:21:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:21:02 GMT
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
	-	`sha256:7491b48e51562c145461304393cbc54944e319e09a7714bf0e4264da38b8a8f0`  
		Last Modified: Thu, 21 Jan 2021 10:30:38 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ddd885e4337d0d4280e48c08d2773cbeccea9252012a28ad3821276198768`  
		Last Modified: Wed, 10 Feb 2021 19:23:21 GMT  
		Size: 63.0 MB (62954901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405885a488da2ca714ecb770191dbc053142aff91c8caff9add9693d8e0b7ec4`  
		Last Modified: Wed, 10 Feb 2021 19:23:09 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3.2-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8b32f5c81ad988f7f1ffaedb8db2c020e1423185479c6ea84ef6f20396e7ec2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f3c28b9d419ba648d327a792d2dfe3f1cd06667f4471a7ec81f237521544ee`
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
# Wed, 10 Feb 2021 19:41:15 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:41:16 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:42:06 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 10 Feb 2021 19:42:08 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:42:09 GMT
USER kong
# Wed, 10 Feb 2021 19:42:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:42:10 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:42:11 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:42:11 GMT
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
	-	`sha256:036fc6b35d8ab60f3b9e2d326a78b3b2eb5240b04a4c1a529ba999d0c3851c53`  
		Last Modified: Wed, 10 Feb 2021 19:43:51 GMT  
		Size: 59.4 MB (59375600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befa029f7c70e574e1c86bd6f238b2180766bf437e3bf72d446a94a3fa97e99b`  
		Last Modified: Wed, 10 Feb 2021 19:43:34 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-alpine`

```console
$ docker pull kong@sha256:b6df904a47c82dd0701dc13f65b6266908cbeb3bbeec8e0579cfbcc6fd4e791e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-alpine` - linux; amd64

```console
$ docker pull kong@sha256:264012de525385f2db42318611e387b306380354d273e81e6e56e120b6517338
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50938390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb50817914445878879a768e55a80d4ecca29754f7b653bf1c070b5598bc1ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:54:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:54:52 GMT
USER kong
# Wed, 24 Feb 2021 23:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:54:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:54:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:54:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24fc8c85ed2920bce371544b9e89e3aab573f62b95d1d49df9a02c2a51936e5`  
		Last Modified: Wed, 24 Feb 2021 23:57:52 GMT  
		Size: 48.1 MB (48122212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96136c04ffeebb0b7fc6524bf5277a483472101f625f359f94a50e827ce264fc`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bb9932af2cac4eda8f7394651f8657be5396d5a01dba0976d08070b8fd0117e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50465123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282e4dce09f74eaa7ba83dae27a5462dad636d02ed6b9c9553c4e66fcc2dc51`
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
# Wed, 24 Feb 2021 23:33:50 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:50 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:51 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:52 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:53 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:33:54 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:34:15 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:34:18 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:34:20 GMT
USER kong
# Wed, 24 Feb 2021 23:34:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:34:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:34:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:34:26 GMT
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
	-	`sha256:d761e799b29bca6ab070a506112eb88010e4f015a27e9b673e5f63c492c33f2c`  
		Last Modified: Wed, 24 Feb 2021 23:37:15 GMT  
		Size: 47.7 MB (47738443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e81a656d179645231aa7afd3e70d4ab1ca97115a29e3e20f20ee8afaa0b93`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-centos`

```console
$ docker pull kong@sha256:0cc576dd4ef99a2b49bae75fd85e6d493a777eacf8833dc5daa0c5de9564c261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:2.3-centos` - linux; amd64

```console
$ docker pull kong@sha256:7bd92331a362473eb429c998283d4dd7c4d3ab81c7488f07b0e4c83fbcf7d253
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127452514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793035e30a2dff29e7b79510065aef13499f016f8318e9a75377b095fc7d59e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 10 Feb 2021 19:21:10 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:10 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:10 GMT
ARG KONG_SHA256=aad05b5b7425a0c1dc3095363c785a4147d3cd91064f0221a2a818c7bdcc97dc
# Wed, 10 Feb 2021 19:21:43 GMT
# ARGS: KONG_SHA256=aad05b5b7425a0c1dc3095363c785a4147d3cd91064f0221a2a818c7bdcc97dc
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 10 Feb 2021 19:21:43 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:21:43 GMT
USER kong
# Wed, 10 Feb 2021 19:21:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:21:43 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:21:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:21:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2f33f2efc166cb5c8fe700bba55f203a47ac68805d7584af1566032ae9fdb8`  
		Last Modified: Wed, 10 Feb 2021 19:23:37 GMT  
		Size: 51.4 MB (51354495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c8c693e04f11baabbca865e259871d10ac47ad2086140fb01a92d250a28c6`  
		Last Modified: Wed, 10 Feb 2021 19:23:27 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:2.3-ubuntu`

```console
$ docker pull kong@sha256:66668da50260386c63cc5b0ca236930af6824c6aef04f4e032a164c2c899b3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:2.3-ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:01d99df2c738fd91787846bb092443f5a571b9cb616cad124bf24de44d2484bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcf5a3c8737b98c5576918ff224bad267e7fd85be030a022ed377528777b59a`
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
# Thu, 21 Jan 2021 10:27:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 10:27:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 10 Feb 2021 19:20:15 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:20:15 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:01 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 10 Feb 2021 19:21:01 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:21:01 GMT
USER kong
# Wed, 10 Feb 2021 19:21:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:21:02 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:21:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:21:02 GMT
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
	-	`sha256:7491b48e51562c145461304393cbc54944e319e09a7714bf0e4264da38b8a8f0`  
		Last Modified: Thu, 21 Jan 2021 10:30:38 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ddd885e4337d0d4280e48c08d2773cbeccea9252012a28ad3821276198768`  
		Last Modified: Wed, 10 Feb 2021 19:23:21 GMT  
		Size: 63.0 MB (62954901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405885a488da2ca714ecb770191dbc053142aff91c8caff9add9693d8e0b7ec4`  
		Last Modified: Wed, 10 Feb 2021 19:23:09 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:2.3-ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8b32f5c81ad988f7f1ffaedb8db2c020e1423185479c6ea84ef6f20396e7ec2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f3c28b9d419ba648d327a792d2dfe3f1cd06667f4471a7ec81f237521544ee`
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
# Wed, 10 Feb 2021 19:41:15 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:41:16 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:42:06 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 10 Feb 2021 19:42:08 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:42:09 GMT
USER kong
# Wed, 10 Feb 2021 19:42:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:42:10 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:42:11 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:42:11 GMT
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
	-	`sha256:036fc6b35d8ab60f3b9e2d326a78b3b2eb5240b04a4c1a529ba999d0c3851c53`  
		Last Modified: Wed, 10 Feb 2021 19:43:51 GMT  
		Size: 59.4 MB (59375600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befa029f7c70e574e1c86bd6f238b2180766bf437e3bf72d446a94a3fa97e99b`  
		Last Modified: Wed, 10 Feb 2021 19:43:34 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:alpine`

```console
$ docker pull kong@sha256:b6df904a47c82dd0701dc13f65b6266908cbeb3bbeec8e0579cfbcc6fd4e791e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:alpine` - linux; amd64

```console
$ docker pull kong@sha256:264012de525385f2db42318611e387b306380354d273e81e6e56e120b6517338
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50938390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb50817914445878879a768e55a80d4ecca29754f7b653bf1c070b5598bc1ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:54:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:54:52 GMT
USER kong
# Wed, 24 Feb 2021 23:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:54:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:54:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:54:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24fc8c85ed2920bce371544b9e89e3aab573f62b95d1d49df9a02c2a51936e5`  
		Last Modified: Wed, 24 Feb 2021 23:57:52 GMT  
		Size: 48.1 MB (48122212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96136c04ffeebb0b7fc6524bf5277a483472101f625f359f94a50e827ce264fc`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:alpine` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bb9932af2cac4eda8f7394651f8657be5396d5a01dba0976d08070b8fd0117e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50465123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282e4dce09f74eaa7ba83dae27a5462dad636d02ed6b9c9553c4e66fcc2dc51`
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
# Wed, 24 Feb 2021 23:33:50 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:50 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:51 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:52 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:53 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:33:54 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:34:15 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:34:18 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:34:20 GMT
USER kong
# Wed, 24 Feb 2021 23:34:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:34:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:34:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:34:26 GMT
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
	-	`sha256:d761e799b29bca6ab070a506112eb88010e4f015a27e9b673e5f63c492c33f2c`  
		Last Modified: Wed, 24 Feb 2021 23:37:15 GMT  
		Size: 47.7 MB (47738443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e81a656d179645231aa7afd3e70d4ab1ca97115a29e3e20f20ee8afaa0b93`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:centos`

```console
$ docker pull kong@sha256:0cc576dd4ef99a2b49bae75fd85e6d493a777eacf8833dc5daa0c5de9564c261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kong:centos` - linux; amd64

```console
$ docker pull kong@sha256:7bd92331a362473eb429c998283d4dd7c4d3ab81c7488f07b0e4c83fbcf7d253
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127452514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793035e30a2dff29e7b79510065aef13499f016f8318e9a75377b095fc7d59e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 01:01:33 GMT
LABEL maintainer=Kong <support@konghq.com>
# Sat, 14 Nov 2020 01:01:33 GMT
ARG ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ENV ASSET=ce
# Sat, 14 Nov 2020 01:01:34 GMT
ARG EE_PORTS
# Sat, 14 Nov 2020 01:01:34 GMT
COPY file:ff02c070e4c89f043b176279a7e41464b5fab8cb98cfcd6332fad2d2741fc41d in /tmp/kong.rpm 
# Wed, 10 Feb 2021 19:21:10 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:10 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:10 GMT
ARG KONG_SHA256=aad05b5b7425a0c1dc3095363c785a4147d3cd91064f0221a2a818c7bdcc97dc
# Wed, 10 Feb 2021 19:21:43 GMT
# ARGS: KONG_SHA256=aad05b5b7425a0c1dc3095363c785a4147d3cd91064f0221a2a818c7bdcc97dc
RUN set -ex;   if [ "$ASSET" = "ce" ] ; then     curl -fL "https://bintray.com/kong/kong-rpm/download_file?file_path=centos/7/kong-$KONG_VERSION.el7.amd64.rpm" -o /tmp/kong.rpm     && echo "$KONG_SHA256  /tmp/kong.rpm" | sha256sum -c -;   fi;   yum install -y -q unzip shadow-utils git   && yum clean all -q   && rm -fr /var/cache/yum/* /tmp/yum_save*.yumtx /root/.pki   && yum install -y /tmp/kong.rpm   && yum clean all   && rm /tmp/kong.rpm   && chown kong:0 /usr/local/bin/kong   && chown -R kong:0 /usr/local/kong &&   if [ "$ASSET" = "ce" ] ; then     kong version ;   fi;
# Wed, 10 Feb 2021 19:21:43 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:21:43 GMT
USER kong
# Wed, 10 Feb 2021 19:21:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:21:43 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:21:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:21:44 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4dc7c6a187fe570e563de224bd35775b78d3ff78f05cf73c4e08319b2dc232`  
		Last Modified: Sat, 14 Nov 2020 01:03:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2f33f2efc166cb5c8fe700bba55f203a47ac68805d7584af1566032ae9fdb8`  
		Last Modified: Wed, 10 Feb 2021 19:23:37 GMT  
		Size: 51.4 MB (51354495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c8c693e04f11baabbca865e259871d10ac47ad2086140fb01a92d250a28c6`  
		Last Modified: Wed, 10 Feb 2021 19:23:27 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:latest`

```console
$ docker pull kong@sha256:b6df904a47c82dd0701dc13f65b6266908cbeb3bbeec8e0579cfbcc6fd4e791e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:latest` - linux; amd64

```console
$ docker pull kong@sha256:264012de525385f2db42318611e387b306380354d273e81e6e56e120b6517338
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50938390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb50817914445878879a768e55a80d4ecca29754f7b653bf1c070b5598bc1ae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["kong","docker-start"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:11 GMT
ADD file:7eeea546ecde7a036bf634c08719879d32c7ec6ae599708cd91dc1b830735223 in / 
# Wed, 24 Feb 2021 20:20:12 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:54:42 GMT
LABEL maintainer=Kong <support@konghq.com>
# Wed, 24 Feb 2021 23:54:42 GMT
ARG ASSET=ce
# Wed, 24 Feb 2021 23:54:42 GMT
ENV ASSET=ce
# Wed, 24 Feb 2021 23:54:43 GMT
ARG EE_PORTS
# Wed, 24 Feb 2021 23:54:43 GMT
COPY file:9073480627c34fa516ae48557d24314a31d17b88798bd04c46162029e368d39c in /tmp/kong.tar.gz 
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:54:43 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:54:44 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:44 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:54:51 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:54:51 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:54:52 GMT
USER kong
# Wed, 24 Feb 2021 23:54:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:54:52 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:54:52 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:54:52 GMT
CMD ["kong" "docker-start"]
```

-	Layers:
	-	`sha256:e95f33c60a645d6d31f52fdc334aecec0d79a1b410789eae37fbf69efcd587ab`  
		Last Modified: Wed, 24 Feb 2021 20:20:43 GMT  
		Size: 2.8 MB (2815313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab3768d001dd6ad72a6b6e9c47c8de3967efb8031eb5471e0a48d98f2619558`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24fc8c85ed2920bce371544b9e89e3aab573f62b95d1d49df9a02c2a51936e5`  
		Last Modified: Wed, 24 Feb 2021 23:57:52 GMT  
		Size: 48.1 MB (48122212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96136c04ffeebb0b7fc6524bf5277a483472101f625f359f94a50e827ce264fc`  
		Last Modified: Wed, 24 Feb 2021 23:57:37 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:latest` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:bb9932af2cac4eda8f7394651f8657be5396d5a01dba0976d08070b8fd0117e8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50465123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d282e4dce09f74eaa7ba83dae27a5462dad636d02ed6b9c9553c4e66fcc2dc51`
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
# Wed, 24 Feb 2021 23:33:50 GMT
ARG KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:50 GMT
ENV KONG_VERSION=2.3.2
# Wed, 24 Feb 2021 23:33:51 GMT
ARG KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:52 GMT
ENV KONG_AMD64_SHA=4c2e26b3719349d02fe0585a74fcb187e638095b42eea3d08f96d8a30e56e07e
# Wed, 24 Feb 2021 23:33:53 GMT
ARG KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:33:54 GMT
ENV KONG_ARM64_SHA=0f5770d67dda761437f365686f87ce821e5848ca0583e502bf5edfb0ba2bfbc3
# Wed, 24 Feb 2021 23:34:15 GMT
RUN set -eux; 	arch="$(apk --print-arch)"; 	case "${arch}" in 		x86_64) arch='amd64'; KONG_SHA256=$KONG_AMD64_SHA ;; 		aarch64) arch='arm64'; KONG_SHA256=$KONG_ARM64_SHA ;; 	esac;     if [ "$ASSET" = "ce" ] ; then         apk add --no-cache --virtual .build-deps curl wget tar ca-certificates &&         curl -fL "https://bintray.com/kong/kong-alpine-tar/download_file?file_path=kong-$KONG_VERSION.$arch.apk.tar.gz" -o /tmp/kong.tar.gz &&         echo "$KONG_SHA256  /tmp/kong.tar.gz" | sha256sum -c -;         apk del .build-deps;     fi;     mkdir /kong;     tar -C /kong -xzf /tmp/kong.tar.gz &&     mv /kong/usr/local/* /usr/local &&     mv /kong/etc/* /etc &&     rm -rf /kong &&     apk add --no-cache libstdc++ libgcc openssl pcre perl tzdata libcap zip bash   zlib zlib-dev git ca-certificates &&     adduser -S kong &&     mkdir -p "/usr/local/kong" &&     chown -R kong:0 /usr/local/kong &&     chown kong:0 /usr/local/bin/kong &&     chmod -R g=u /usr/local/kong &&     rm -rf /tmp/kong.tar.gz &&     if [ "$ASSET" = "ce" ] ; then       kong version ;     fi;
# Wed, 24 Feb 2021 23:34:18 GMT
COPY file:c60e90d02b3d93627e1f0d577e2298e266f50cc620574d3ef11b8b30cd8a906c in /docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:34:20 GMT
USER kong
# Wed, 24 Feb 2021 23:34:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:34:23 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 24 Feb 2021 23:34:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Feb 2021 23:34:26 GMT
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
	-	`sha256:d761e799b29bca6ab070a506112eb88010e4f015a27e9b673e5f63c492c33f2c`  
		Last Modified: Wed, 24 Feb 2021 23:37:15 GMT  
		Size: 47.7 MB (47738443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e81a656d179645231aa7afd3e70d4ab1ca97115a29e3e20f20ee8afaa0b93`  
		Last Modified: Wed, 24 Feb 2021 23:37:00 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kong:ubuntu`

```console
$ docker pull kong@sha256:66668da50260386c63cc5b0ca236930af6824c6aef04f4e032a164c2c899b3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `kong:ubuntu` - linux; amd64

```console
$ docker pull kong@sha256:01d99df2c738fd91787846bb092443f5a571b9cb616cad124bf24de44d2484bd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134001444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcf5a3c8737b98c5576918ff224bad267e7fd85be030a022ed377528777b59a`
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
# Thu, 21 Jan 2021 10:27:05 GMT
ARG ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ENV ASSET=ce
# Thu, 21 Jan 2021 10:27:05 GMT
ARG EE_PORTS
# Thu, 21 Jan 2021 10:27:06 GMT
COPY file:5da22ad111df95d5c0f9c17c60cd4123a51ad46a41d3f442fca7b2bcc8d7d11b in /tmp/kong.deb 
# Wed, 10 Feb 2021 19:20:15 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:20:15 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:21:01 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 10 Feb 2021 19:21:01 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:21:01 GMT
USER kong
# Wed, 10 Feb 2021 19:21:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:21:02 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:21:02 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:21:02 GMT
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
	-	`sha256:7491b48e51562c145461304393cbc54944e319e09a7714bf0e4264da38b8a8f0`  
		Last Modified: Thu, 21 Jan 2021 10:30:38 GMT  
		Size: 25.1 MB (25081954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5ddd885e4337d0d4280e48c08d2773cbeccea9252012a28ad3821276198768`  
		Last Modified: Wed, 10 Feb 2021 19:23:21 GMT  
		Size: 63.0 MB (62954901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405885a488da2ca714ecb770191dbc053142aff91c8caff9add9693d8e0b7ec4`  
		Last Modified: Wed, 10 Feb 2021 19:23:09 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kong:ubuntu` - linux; arm64 variant v8

```console
$ docker pull kong@sha256:8b32f5c81ad988f7f1ffaedb8db2c020e1423185479c6ea84ef6f20396e7ec2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125344949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f3c28b9d419ba648d327a792d2dfe3f1cd06667f4471a7ec81f237521544ee`
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
# Wed, 10 Feb 2021 19:41:15 GMT
ARG KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:41:16 GMT
ENV KONG_VERSION=2.3.2
# Wed, 10 Feb 2021 19:42:06 GMT
RUN set -ex;     apt-get update &&     if [ "$ASSET" = "ce" ] ; then         apt-get install -y curl &&         curl -fL "https://bintray.com/kong/kong-deb/download_file?file_path=kong-$KONG_VERSION.xenial.$(dpkg --print-architecture).deb" -o /tmp/kong.deb         && apt-get purge -y curl;     fi;     apt-get install -y --no-install-recommends unzip git 	&& apt update     && apt install --yes /tmp/kong.deb     && rm -rf /var/lib/apt/lists/*     && rm -rf /tmp/kong.deb     && chown kong:0 /usr/local/bin/kong     && chown -R kong:0 /usr/local/kong     && if [ "$ASSET" = "ce" ] ; then         kong version ;     fi;
# Wed, 10 Feb 2021 19:42:08 GMT
COPY file:3f0ac4e41f7591702adf841081157578863b364bb31cfb02189411168744a26e in /docker-entrypoint.sh 
# Wed, 10 Feb 2021 19:42:09 GMT
USER kong
# Wed, 10 Feb 2021 19:42:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Feb 2021 19:42:10 GMT
EXPOSE 8000 8001 8443 8444
# Wed, 10 Feb 2021 19:42:11 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Feb 2021 19:42:11 GMT
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
	-	`sha256:036fc6b35d8ab60f3b9e2d326a78b3b2eb5240b04a4c1a529ba999d0c3851c53`  
		Last Modified: Wed, 10 Feb 2021 19:43:51 GMT  
		Size: 59.4 MB (59375600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befa029f7c70e574e1c86bd6f238b2180766bf437e3bf72d446a94a3fa97e99b`  
		Last Modified: Wed, 10 Feb 2021 19:43:34 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
