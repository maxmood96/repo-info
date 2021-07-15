## `traefik:brie`

```console
$ docker pull traefik@sha256:df90799aaca1ad6fb9e06d311140035d2a0c2295a4f8f508f6b55ee056bb677e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:brie` - linux; amd64

```console
$ docker pull traefik@sha256:5488ec92e9f82de52de604a7bfa4a3c30e5315f9875ad43e05160c81b87c3acb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.0 MB (28966764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dd41b9aaa93f698361b1da1c410ce99e3f681d4697eca8cb1719bd29d2d6ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:56 GMT
ADD file:282b9d56236cae29600bf8b698cb0a865ab17db7beea0be6870f9de63e7d4f80 in / 
# Wed, 14 Apr 2021 19:19:56 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:04:42 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 29 Jun 2021 03:09:39 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc2/traefik_v2.5.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 29 Jun 2021 03:09:39 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 29 Jun 2021 03:09:39 GMT
EXPOSE 80
# Tue, 29 Jun 2021 03:09:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Jun 2021 03:09:40 GMT
CMD ["traefik"]
# Tue, 29 Jun 2021 03:09:40 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:ddad3d7c1e96adf9153f8921a7c9790f880a390163df453be1566e9ef0d546e0`  
		Last Modified: Wed, 14 Apr 2021 19:21:03 GMT  
		Size: 2.8 MB (2816246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6722e60c2f6c55424dadebe886f88ba1b903df075b00048427439abb91b85a`  
		Last Modified: Thu, 15 Apr 2021 03:05:57 GMT  
		Size: 674.2 KB (674210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbfdd1c5c151322f4ab094416205c09673148cdbb26ed1c1ce22bfd3bd5f356`  
		Last Modified: Tue, 29 Jun 2021 03:10:20 GMT  
		Size: 25.5 MB (25475940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f988c50dc1065536fd64492838426bb43fa62a273c449081ff4ca1dc8774a9`  
		Last Modified: Tue, 29 Jun 2021 03:10:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ac452353215b3b8c89074980fce1c52c6a19427cf80c4bd1095c82d318da1021
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27081935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f673f569fb012bb5b7175f8ce9662725828e9cd93d4a80e86e65673ecb60679`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:47 GMT
ADD file:d8df176c5a97047d4ac655ebfc7bf2cde0a513f0120a6a7796c9724fee8acb22 in / 
# Tue, 15 Jun 2021 22:57:47 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 21:20:44 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 29 Jun 2021 02:09:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc2/traefik_v2.5.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 29 Jun 2021 02:09:33 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 29 Jun 2021 02:09:34 GMT
EXPOSE 80
# Tue, 29 Jun 2021 02:09:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Jun 2021 02:09:34 GMT
CMD ["traefik"]
# Tue, 29 Jun 2021 02:09:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1a82e2abdb8183eef16afe6d45e16c1b000a908fe3f8fcd17adef7778ecb37d9`  
		Last Modified: Wed, 14 Apr 2021 18:50:45 GMT  
		Size: 2.6 MB (2621912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799f7ee570a1df0b7eadabb3db5e0cb7e7eef59e623df4f40c3e9d94007b4c9d`  
		Last Modified: Tue, 22 Jun 2021 21:23:04 GMT  
		Size: 677.0 KB (677010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a19fee1068c0396fc3dfa4c98024b21e7419184297b2d0ffe75d4a924941aa`  
		Last Modified: Tue, 29 Jun 2021 02:12:11 GMT  
		Size: 23.8 MB (23782645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e571ebc069572f01900ff6d20321f5cf519ed93558f3d75753db8bbbb324c2fa`  
		Last Modified: Tue, 29 Jun 2021 02:11:54 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:brie` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:964c30609ba0c8bb3134cb4c7adc798944b20dc7bc0c3782055c3e02405bb4a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26490876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a27f9fc1ed432e444b7b3a76b74440e436357d16030eed687716b5483f4c80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:15 GMT
ADD file:62109d08b751b6f41eb8dc5dcb3ea6b553619ef0a58a40685faa749a20c3b051 in / 
# Tue, 15 Jun 2021 21:45:15 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 11:17:24 GMT
RUN apk --no-cache add ca-certificates tzdata
# Tue, 29 Jun 2021 03:43:19 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.5.0-rc2/traefik_v2.5.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Tue, 29 Jun 2021 03:43:19 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Tue, 29 Jun 2021 03:43:19 GMT
EXPOSE 80
# Tue, 29 Jun 2021 03:43:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 29 Jun 2021 03:43:20 GMT
CMD ["traefik"]
# Tue, 29 Jun 2021 03:43:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.5.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:535256e01bcb9590f56b9b2a053648a1d98fbe4dc0fd34c1fc3f32afec8c6e7b`  
		Last Modified: Wed, 14 Apr 2021 18:44:02 GMT  
		Size: 2.7 MB (2726928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb39c774f8e6176a8c3728cde4ec4fc741ab8ff2040415b9f55bbd839dc73b78`  
		Last Modified: Wed, 16 Jun 2021 11:18:33 GMT  
		Size: 675.5 KB (675546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7a0ac9033288295928b519e525561083e658749a6fe17f0fd29b5ca955f32b`  
		Last Modified: Tue, 29 Jun 2021 03:44:35 GMT  
		Size: 23.1 MB (23088033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d235761e10abfceee0da2605cc0256b4c741b4f4a194feb53a69348c3e673027`  
		Last Modified: Tue, 29 Jun 2021 03:44:30 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
