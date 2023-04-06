## `traefik:latest`

```console
$ docker pull traefik@sha256:a920aced1da7890410fe75e5c8bfa21e58f1a0f333b001db5c5498d9d8eb41ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:6dee6938b5ebfc511a82ef4e09c80268835a2f67393e5c06c3e4ef9a14d1817b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39613072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1e26b5f8193d713eb8f39d0ab0e3d513278f86e41644b07e189e1aef536b335`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:37:38 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 06 Apr 2023 18:24:43 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.10/traefik_v2.9.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 06 Apr 2023 18:24:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 06 Apr 2023 18:24:44 GMT
EXPOSE 80
# Thu, 06 Apr 2023 18:24:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 06 Apr 2023 18:24:44 GMT
CMD ["traefik"]
# Thu, 06 Apr 2023 18:24:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d055169f9c6f7e08b88a6ef90eba203750fcc51761ecb994e40aa2aaa640ff72`  
		Last Modified: Thu, 30 Mar 2023 02:38:35 GMT  
		Size: 622.2 KB (622239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afaddc85d79e665b30c4ee7ce9fc12425532f4695c6888b052086589f12aa687`  
		Last Modified: Thu, 06 Apr 2023 18:25:11 GMT  
		Size: 35.6 MB (35615902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff733a62a1272d7fe4817f1b3a8faf56c8a7f0e3808baec593378d274c1d081`  
		Last Modified: Thu, 06 Apr 2023 18:25:06 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:10b691b83d9ed9bac5ac8d7c37c79398bfec79e73c5b7882a6d6da069d3eb277
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37252169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a74fe8cbe09d9e0c7f9f1f5eae5d4c1ce1a39daf65907779900cdce45c36ed4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:09 GMT
ADD file:2dd294d20c0b500c8fed6b410b059429b36f51cd48a45eaf7a06ecbef9e2a3bb in / 
# Wed, 29 Mar 2023 18:01:09 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:39:39 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 30 Mar 2023 00:39:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.9/traefik_v2.9.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 30 Mar 2023 00:39:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 30 Mar 2023 00:39:44 GMT
EXPOSE 80
# Thu, 30 Mar 2023 00:39:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 00:39:44 GMT
CMD ["traefik"]
# Thu, 30 Mar 2023 00:39:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:75257e753735e4ff78fae2d44018022a6ac775290e02103713a70699ece7576e`  
		Last Modified: Wed, 29 Mar 2023 18:01:52 GMT  
		Size: 3.1 MB (3110802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bd7901efecc8425b6d98584a9ee5d091a238a8936fb50b8aa4654afb90d05d`  
		Last Modified: Thu, 30 Mar 2023 00:41:05 GMT  
		Size: 624.4 KB (624425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46d6063123b03962a02bfe27e1157e7a846da318f6438997b771048f14b7cc0b`  
		Last Modified: Thu, 30 Mar 2023 00:41:10 GMT  
		Size: 33.5 MB (33516575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f46160874c0a777742654e0fd3a6789ac1b431552c3e2c875c39273c198f54`  
		Last Modified: Thu, 30 Mar 2023 00:41:04 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e605e6aa8e04c39718acf21f2bd86beca4f4c5c8f82f937721a7bb237b0935f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 MB (36495598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81983806f35cf323c9f74c24470cac17e49b22d180900d0960831ada2bef9526`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 03:26:37 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 30 Mar 2023 03:26:40 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.9/traefik_v2.9.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 30 Mar 2023 03:26:41 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 30 Mar 2023 03:26:41 GMT
EXPOSE 80
# Thu, 30 Mar 2023 03:26:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 30 Mar 2023 03:26:41 GMT
CMD ["traefik"]
# Thu, 30 Mar 2023 03:26:41 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4336eee5b1b811f9668d2251fb67e6099c4089ef7b26ade14aacd2f5f0982e06`  
		Last Modified: Thu, 30 Mar 2023 03:27:34 GMT  
		Size: 624.2 KB (624204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b17f6f1f14685fa57486153a50b0c3d6af2c279ad5b0267fde7b7c45411a547`  
		Last Modified: Thu, 30 Mar 2023 03:27:37 GMT  
		Size: 32.6 MB (32609173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78142774db650d3288d267f8277915b97ff122d7db1fbf483a375fb77e3ea8b9`  
		Last Modified: Thu, 30 Mar 2023 03:27:33 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:a4e2b23ab0e116c6c63eb883e41b410879f8ce7ba0705f343cac8711cfb716fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.3 MB (38327529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0140a070a5b28be241ddcb7b569ab11635cc2f95065d7c38d10085dbd4b8bd9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 29 Mar 2023 17:41:57 GMT
ADD file:675ad8acf4b076e34aeeba26dd482be7640df5912b1ec5e3183b7eb69c01e83e in / 
# Wed, 29 Mar 2023 17:41:57 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:38:21 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 29 Mar 2023 22:38:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.9.9/traefik_v2.9.9_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 29 Mar 2023 22:38:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 29 Mar 2023 22:38:27 GMT
EXPOSE 80
# Wed, 29 Mar 2023 22:38:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Mar 2023 22:38:27 GMT
CMD ["traefik"]
# Wed, 29 Mar 2023 22:38:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.9.9 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:a76f78d8854217635d8049ec8501edb806f961e72989cfff8503982e6ff2579d`  
		Last Modified: Wed, 29 Mar 2023 17:42:31 GMT  
		Size: 3.2 MB (3175187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096a495bd82a55e97c5be084787578b5b5af0321a33c70ccf19bca0dc260a981`  
		Last Modified: Wed, 29 Mar 2023 22:39:11 GMT  
		Size: 622.6 KB (622584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f26afb3e4c2022602d8a38957a1218703bec9d64167ba3d830a0d7216bf8f02`  
		Last Modified: Wed, 29 Mar 2023 22:39:17 GMT  
		Size: 34.5 MB (34529391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f96123c52fa98b6189d9190c14398bee66527d253e31488dc4ce2abd7f62881`  
		Last Modified: Wed, 29 Mar 2023 22:39:11 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
