## `traefik:maroilles-alpine`

```console
$ docker pull traefik@sha256:36645215a2367d25d1aa9d82a00a3d55b78da3a77f5a742a354c3eee6ca9696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles-alpine` - linux; amd64

```console
$ docker pull traefik@sha256:26057fa675bf46c770691d54fa06179744a268643d6d9265a100b33f7616a7fe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25663227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0385562c2ca638c3e56fc5e368e0d760861501c3acb1be07b1ec2ff5f4ec8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:23:08 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:32:17 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:32:17 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:32:17 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:32:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:32:18 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:32:18 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1084cd799816f7a030d5c7985d2b38853f5ad434ee8ee15f2993cd000e5bbd`  
		Last Modified: Sat, 13 Nov 2021 07:24:22 GMT  
		Size: 677.8 KB (677824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8fccde93889bb45e3ec014080674609715442d77a83c4e22aed842c54aa320`  
		Last Modified: Fri, 10 Dec 2021 21:33:40 GMT  
		Size: 22.2 MB (22162054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5edab535d879083fbb7bc0569dd3b1588e3ad6549c4ba201eecf74820ad66aa`  
		Last Modified: Fri, 10 Dec 2021 21:33:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm variant v6

```console
$ docker pull traefik@sha256:d6148854489f78aa02ad57c0ffdf49690f1df5e8419adb2677d1bac979a6b58c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23942165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e476d9b470f0d848b51a66f192af4d51464443367916280dfffa10d7c00efec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:51:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 21:50:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 21:50:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 21:50:20 GMT
EXPOSE 80
# Fri, 10 Dec 2021 21:50:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 21:50:21 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 21:50:21 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b00cdbc51db9651a9c09390b641face7e18e642e3ff49397c6d477c89c3d7e`  
		Last Modified: Sat, 13 Nov 2021 06:54:26 GMT  
		Size: 683.0 KB (682972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3379812682fc7d134d4c61b4dc36cfa6924cd554bfed9e11a2ce6927d111484`  
		Last Modified: Fri, 10 Dec 2021 21:53:07 GMT  
		Size: 20.6 MB (20623432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae87b8d30f43743051ca67a1de1aae50831617389e950c804f7267fa8d100ef`  
		Last Modified: Fri, 10 Dec 2021 21:52:53 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles-alpine` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:32a677053c58d48c9176bad0f34a4c615d3f56aa02d5227d6a6bf4405197095d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23529454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d2aabeb48500d4f5cd1417d792e3589d251ffdffa051738ed4465ca5dedec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:16:32 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 10 Dec 2021 22:10:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='arm' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /usr/local/bin/traefik "https://github.com/traefik/traefik/releases/download/v1.7.34/traefik_linux-$arch"; 	chmod +x /usr/local/bin/traefik
# Fri, 10 Dec 2021 22:10:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 10 Dec 2021 22:10:41 GMT
EXPOSE 80
# Fri, 10 Dec 2021 22:10:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 10 Dec 2021 22:10:43 GMT
CMD ["traefik"]
# Fri, 10 Dec 2021 22:10:44 GMT
LABEL org.opencontainers.image.vendor=traefik org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cc5a4b7f102f236064e4712164f29c52d256612820409cc28c41a7f5def4a5`  
		Last Modified: Fri, 12 Nov 2021 18:17:40 GMT  
		Size: 680.0 KB (680008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2cdc6d798fd61d5f7a4c0530d3cec221698500c821c7c43d03b7ba1956b8ad`  
		Last Modified: Fri, 10 Dec 2021 22:12:07 GMT  
		Size: 20.1 MB (20131378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c1839484effd5cd9538632a7a114e155d1dfa9c0acc3db51242271af684434`  
		Last Modified: Fri, 10 Dec 2021 22:12:03 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
