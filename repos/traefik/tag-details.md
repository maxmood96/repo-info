<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-windowsservercore-1809`](#traefik211-windowsservercore-1809)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.0`](#traefik2110)
-	[`traefik:2.11.0-windowsservercore-1809`](#traefik2110-windowsservercore-1809)
-	[`traefik:2.11.0-windowsservercore-ltsc2022`](#traefik2110-windowsservercore-ltsc2022)
-	[`traefik:3.0`](#traefik30)
-	[`traefik:3.0-windowsservercore-1809`](#traefik30-windowsservercore-1809)
-	[`traefik:3.0-windowsservercore-ltsc2022`](#traefik30-windowsservercore-ltsc2022)
-	[`traefik:3.0.0-rc3`](#traefik300-rc3)
-	[`traefik:3.0.0-rc3-windowsservercore-1809`](#traefik300-rc3-windowsservercore-1809)
-	[`traefik:3.0.0-rc3-windowsservercore-ltsc2022`](#traefik300-rc3-windowsservercore-ltsc2022)
-	[`traefik:beaufort`](#traefikbeaufort)
-	[`traefik:beaufort-windowsservercore-1809`](#traefikbeaufort-windowsservercore-1809)
-	[`traefik:beaufort-windowsservercore-ltsc2022`](#traefikbeaufort-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-windowsservercore-1809`](#traefikmimolette-windowsservercore-1809)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-windowsservercore-1809`](#traefikv211-windowsservercore-1809)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.0`](#traefikv2110)
-	[`traefik:v2.11.0-windowsservercore-1809`](#traefikv2110-windowsservercore-1809)
-	[`traefik:v2.11.0-windowsservercore-ltsc2022`](#traefikv2110-windowsservercore-ltsc2022)
-	[`traefik:v3.0`](#traefikv30)
-	[`traefik:v3.0-windowsservercore-1809`](#traefikv30-windowsservercore-1809)
-	[`traefik:v3.0-windowsservercore-ltsc2022`](#traefikv30-windowsservercore-ltsc2022)
-	[`traefik:v3.0.0-rc3`](#traefikv300-rc3)
-	[`traefik:v3.0.0-rc3-windowsservercore-1809`](#traefikv300-rc3-windowsservercore-1809)
-	[`traefik:v3.0.0-rc3-windowsservercore-ltsc2022`](#traefikv300-rc3-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2.11`

```console
$ docker pull traefik@sha256:0a5157f742d2900389da6ce60ea80cc476801dc951917a993cd848d982f58265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:2.11` - linux; amd64

```console
$ docker pull traefik@sha256:903f89ddacc3059657565d3e5b3b8e8dcba4cc3b8af08183dad6fdc415459111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44764460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef9171e9d171746404b3deec2a4c9902a34ab090be5e0af6292cf46d578b35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:23 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:23 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f89104cf675aa8f174193c769467325e9ad59468b56c24f1e06873996e837`  
		Last Modified: Sat, 16 Mar 2024 09:02:59 GMT  
		Size: 40.7 MB (40735737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2854bd2e93ffa353be4c4af010c11b6015af14d8a01fd44caecd27f005eae`  
		Last Modified: Sat, 16 Mar 2024 09:02:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a98638c22a31753067775956551e83e71b5ff2492436692542809e3b1fdaa601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380a6fb69f6060cd614ddf88be41e93bc4524de186877df85fa546422a8b866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:14 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:14 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437ceea7b75ae735791dbc150afc3c2b26d4b431ac5ced56cf805dc8d154199a`  
		Last Modified: Sat, 16 Mar 2024 06:38:52 GMT  
		Size: 38.3 MB (38330899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87966e6d71b48984faa23eab03ff499a107931cbad2b1706e61e0d40a4023f03`  
		Last Modified: Sat, 16 Mar 2024 06:38:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5582b38228735e42e3fe1dd3fb49a2cc139cb1d19908c01de8ef0e53ca0372f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41660229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159525f47b70184553832cc3b646d48d2332462c674682d816707461d47c6965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:38 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:38 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ec8d4c0d6b39d6ac772df1a381c54b5ebdb0684a410a3b4b7ab1f8c0c822f5`  
		Last Modified: Sat, 16 Mar 2024 02:44:13 GMT  
		Size: 37.7 MB (37689392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9404f9e59a2c0cb69ba89ce113f9619427ba2d0367deef6e4f972c6b1afc86`  
		Last Modified: Sat, 16 Mar 2024 02:44:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:efba7027881dc510d374099389b6fce438104f92fcbe138111d6bbf962a3a37c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b813ffcb52083c55280ab73b23a8959359b21911352dc99841977ffbddb2566`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:10:00 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:10:01 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:10:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6724621d9ac1c4db5f182eebf62e6acdae57a70ba04d78722643af376dcfc8`  
		Last Modified: Sat, 16 Mar 2024 07:10:42 GMT  
		Size: 36.7 MB (36651920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fba92839f2ee812037158b91abd37cfdcc5d3ad9de09c6e89590d6dc517ca0b`  
		Last Modified: Sat, 16 Mar 2024 07:10:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:1d0f4e79aff6ff4b564fb2292af4e11eebe6b9d3b9d4ac77e417a46547654fca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43543560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d62fa36bfbf517be29ac764fe9ecd768c79ed91997ac822d4366c9176913d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:55:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:55:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:55:27 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:55:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:55:27 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:55:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee11a4c1b9e5b32b4cbd7ab4b6b2476c247fead47a16cecae7df62ed85faa9`  
		Last Modified: Sat, 16 Mar 2024 22:56:58 GMT  
		Size: 39.7 MB (39679543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629032b546364a1aa7b1ed4eb597d0e0feb5e38dda13289fc414edebb3bbeeb8`  
		Last Modified: Sat, 16 Mar 2024 22:56:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-1809`

```console
$ docker pull traefik@sha256:68f280958b91c3ad020661f9d8dfcdc2937e23bb906301bc70d74f58412b7d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:2.11-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:6c5955d8c7d640ef1e953033bfe26e8446361c887e850375f77a328d6c5b1a9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206657579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617262a4ea137484e609ac8a8a11f20bbcfa9814a6efaa6e14a4933b07ce9aa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:47:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:47:58 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:47:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:48:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aacf44a3b14b8a83aef647a55a384882381ac41332f8dd2ef1c98c17b2f7acb`  
		Last Modified: Wed, 10 Apr 2024 03:50:00 GMT  
		Size: 42.2 MB (42223956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b263b54faf1ee656a3aebca88c4e3149b74fa9ea9f0da62f0696ab77cdb78c`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e280c61423acf1dd14d8703c15995d019ed30d6861fa81b56d74ac76cd963011`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dcbeb77a8df85630996daf57474e78c714c6149ba840b4419b5d7587d718bf`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d0b4d7c2b58fb45cae594447e61aa75eb6af746c3b3049c4de395f366102dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:3a49fb5b2da8093efb0ce0c81508cbd0da2094ad86ab54211a9d795409d46fd1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041584646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33031be9b8289d6354979333b3469cb1c2caf98f54ff84ddbb9bd0355bce8e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:46:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:46:05 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:46:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:46:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da328a847e4abad0f2877e248def5be636cb88ab9c263d476c4c0324ada9aa57`  
		Last Modified: Wed, 10 Apr 2024 03:49:34 GMT  
		Size: 42.2 MB (42205404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1871eb9258c0b7ed2735a70a2004c355e79c1c23e77067b50f9dc006660ab6c`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1279d1342efb5efb211769e19e67d9f012252ee5ea3c9c3d2a55a5c7defd5fa0`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d9e3e2a3252feeed2131f724369a572d22b136c23636ce651e302fac336e5`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0`

```console
$ docker pull traefik@sha256:0a5157f742d2900389da6ce60ea80cc476801dc951917a993cd848d982f58265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:2.11.0` - linux; amd64

```console
$ docker pull traefik@sha256:903f89ddacc3059657565d3e5b3b8e8dcba4cc3b8af08183dad6fdc415459111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44764460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef9171e9d171746404b3deec2a4c9902a34ab090be5e0af6292cf46d578b35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:23 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:23 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f89104cf675aa8f174193c769467325e9ad59468b56c24f1e06873996e837`  
		Last Modified: Sat, 16 Mar 2024 09:02:59 GMT  
		Size: 40.7 MB (40735737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2854bd2e93ffa353be4c4af010c11b6015af14d8a01fd44caecd27f005eae`  
		Last Modified: Sat, 16 Mar 2024 09:02:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a98638c22a31753067775956551e83e71b5ff2492436692542809e3b1fdaa601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380a6fb69f6060cd614ddf88be41e93bc4524de186877df85fa546422a8b866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:14 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:14 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437ceea7b75ae735791dbc150afc3c2b26d4b431ac5ced56cf805dc8d154199a`  
		Last Modified: Sat, 16 Mar 2024 06:38:52 GMT  
		Size: 38.3 MB (38330899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87966e6d71b48984faa23eab03ff499a107931cbad2b1706e61e0d40a4023f03`  
		Last Modified: Sat, 16 Mar 2024 06:38:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5582b38228735e42e3fe1dd3fb49a2cc139cb1d19908c01de8ef0e53ca0372f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41660229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159525f47b70184553832cc3b646d48d2332462c674682d816707461d47c6965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:38 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:38 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ec8d4c0d6b39d6ac772df1a381c54b5ebdb0684a410a3b4b7ab1f8c0c822f5`  
		Last Modified: Sat, 16 Mar 2024 02:44:13 GMT  
		Size: 37.7 MB (37689392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9404f9e59a2c0cb69ba89ce113f9619427ba2d0367deef6e4f972c6b1afc86`  
		Last Modified: Sat, 16 Mar 2024 02:44:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:efba7027881dc510d374099389b6fce438104f92fcbe138111d6bbf962a3a37c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b813ffcb52083c55280ab73b23a8959359b21911352dc99841977ffbddb2566`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:10:00 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:10:01 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:10:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6724621d9ac1c4db5f182eebf62e6acdae57a70ba04d78722643af376dcfc8`  
		Last Modified: Sat, 16 Mar 2024 07:10:42 GMT  
		Size: 36.7 MB (36651920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fba92839f2ee812037158b91abd37cfdcc5d3ad9de09c6e89590d6dc517ca0b`  
		Last Modified: Sat, 16 Mar 2024 07:10:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.0` - linux; s390x

```console
$ docker pull traefik@sha256:1d0f4e79aff6ff4b564fb2292af4e11eebe6b9d3b9d4ac77e417a46547654fca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43543560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d62fa36bfbf517be29ac764fe9ecd768c79ed91997ac822d4366c9176913d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:55:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:55:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:55:27 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:55:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:55:27 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:55:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee11a4c1b9e5b32b4cbd7ab4b6b2476c247fead47a16cecae7df62ed85faa9`  
		Last Modified: Sat, 16 Mar 2024 22:56:58 GMT  
		Size: 39.7 MB (39679543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629032b546364a1aa7b1ed4eb597d0e0feb5e38dda13289fc414edebb3bbeeb8`  
		Last Modified: Sat, 16 Mar 2024 22:56:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:68f280958b91c3ad020661f9d8dfcdc2937e23bb906301bc70d74f58412b7d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:2.11.0-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:6c5955d8c7d640ef1e953033bfe26e8446361c887e850375f77a328d6c5b1a9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206657579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617262a4ea137484e609ac8a8a11f20bbcfa9814a6efaa6e14a4933b07ce9aa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:47:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:47:58 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:47:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:48:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aacf44a3b14b8a83aef647a55a384882381ac41332f8dd2ef1c98c17b2f7acb`  
		Last Modified: Wed, 10 Apr 2024 03:50:00 GMT  
		Size: 42.2 MB (42223956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b263b54faf1ee656a3aebca88c4e3149b74fa9ea9f0da62f0696ab77cdb78c`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e280c61423acf1dd14d8703c15995d019ed30d6861fa81b56d74ac76cd963011`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dcbeb77a8df85630996daf57474e78c714c6149ba840b4419b5d7587d718bf`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d0b4d7c2b58fb45cae594447e61aa75eb6af746c3b3049c4de395f366102dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:2.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:3a49fb5b2da8093efb0ce0c81508cbd0da2094ad86ab54211a9d795409d46fd1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041584646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33031be9b8289d6354979333b3469cb1c2caf98f54ff84ddbb9bd0355bce8e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:46:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:46:05 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:46:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:46:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da328a847e4abad0f2877e248def5be636cb88ab9c263d476c4c0324ada9aa57`  
		Last Modified: Wed, 10 Apr 2024 03:49:34 GMT  
		Size: 42.2 MB (42205404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1871eb9258c0b7ed2735a70a2004c355e79c1c23e77067b50f9dc006660ab6c`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1279d1342efb5efb211769e19e67d9f012252ee5ea3c9c3d2a55a5c7defd5fa0`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d9e3e2a3252feeed2131f724369a572d22b136c23636ce651e302fac336e5`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0`

```console
$ docker pull traefik@sha256:940b0c3dd5468fb2dbc26eb6180a213e2f05ea5d10eeec4373abee136a159652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:3.0` - linux; amd64

```console
$ docker pull traefik@sha256:8b5a00052b4a25122b79e261d58f2bbf87937a0b11cbe62e9dc73394bbd3ed88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45167757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e595ae387b49f63c46bf7c0df3e3a1ade691546b8807fc90194f4a49e3dcaf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:15 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:15 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c86d42c6ee19def22cfadf30c6270aaac42a1c52c96179fc0ada179978ee0`  
		Last Modified: Sat, 16 Mar 2024 09:02:40 GMT  
		Size: 41.1 MB (41139034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad5694bc6f8a623b0eb1d57dc0a088f293870691c7e47310f5a18c0cde7674a`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:90d8997366af2b199b6f072ef057b01fe586dd0823a95846926fa174291c157c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42390472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6485015395492e18c678e74352403c96e5c0bb05aa7ec53a6f8a517bc9cf67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:07 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:07 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08fc1b14a3d3556165bedf1d94c8630dc1d0c7b33e4cd65a677907b5bba6cc1`  
		Last Modified: Sat, 16 Mar 2024 06:38:32 GMT  
		Size: 38.6 MB (38603704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8eb8e998597054adc242b95b60bdeb2e8e7020acf9f054b54fdc5e0d584ae4`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e68604ff497f79d9522e437ee66a3645de33494a2767872371a803212039993
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42043483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1f8efc9eb622c56f587602b707c3238b25d6f32d32d008b9a33cd7ac516216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:32 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:32 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e9487662ce49d04a55c69f1640870789f94bfd6e0dc32a28c511ddd3489b71`  
		Last Modified: Sat, 16 Mar 2024 02:43:55 GMT  
		Size: 38.1 MB (38072646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c15ff70d10a381654357ae74e33269071ee5380f03f4e11119fb2c8b79fb51d`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:edf5a96c035e0f6e682fff437a86d64199346ac4053e0286c1a823e7bc848a70
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dcb125de975065559e7f4373f2446f91076c02cdd79b57001543bed8db41a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:09:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:09:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:09:45 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:09:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07e78c4c5c1b86e845ed8a0fb75da1329adbc4fe731a0ee8b03ae71446ba1fd`  
		Last Modified: Sat, 16 Mar 2024 07:10:20 GMT  
		Size: 36.9 MB (36929870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d024b32c9d738039d6f452d8dbad3ae0d3faeb42c48460138da619c23164b4`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; s390x

```console
$ docker pull traefik@sha256:0bf8cfc60d3bc736604925e6047e58069ffbeeb39badbf495482a0ebbe91fb6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43797288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc3a16e2b34522b6f52599f397c5dc56a3a3b85400b6b88d908c98b35ac29d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:54:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:54:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:54:04 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:54:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:54:04 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:54:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc322c0721e5037c2543b6dd0f8d2414a757ad55ed5e16a9ace5f22c8428b9`  
		Last Modified: Sat, 16 Mar 2024 22:56:39 GMT  
		Size: 39.9 MB (39933271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e7a3d560876dfda34b978cf1250873cc7d723c8f46a77feedf1849e388f42`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a0357d92202a7e0fcaae4dd3cc728417289f51f1d8d21ec1c92ab6fbcab5133a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:75b5ef91faf5391e02263555071c35a5fc363874e2059ff151a933d04ceb64f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207243489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3dc00cb417c957e75a19010044938884a685c80da9d420089e1b77f83af88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:45:08 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:45:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:45:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688fe15c79b7db926c9e01771f49e6967e652ff34f7d3cc9421e16274bdabdf8`  
		Last Modified: Wed, 10 Apr 2024 03:49:11 GMT  
		Size: 42.8 MB (42809933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ca6e2850a6cfdf104e40c31579893a55030554c6b9507cad3756bdeaed1f5`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039938c2016338255e75112d1d20fe2f2a0421c222e9429a2e08335e0d882b1c`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fef8b7c7c9bed557697ce2c9abd90a94a06c108a3afb420fd7435856f43026`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:3a1fdc89de455b9c22251ffab5f844a259045b3de5a809d11d393886f9f2d263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:fca33031dd6909250cf0beaf5b81ebe87b40bb8e04697a184ce2f72fe6ffea6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042199913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89955d6980fa4a5298483012509b0098e371ecd53371e2969d3e939117d5b1d0`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:43:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:43:17 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:43:18 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16dca97b74396719506a92c84457e45ebb658e173a0581aad8debfc58de6690`  
		Last Modified: Wed, 10 Apr 2024 03:48:47 GMT  
		Size: 42.8 MB (42821001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31eee5a20b340589cc77b66bd8bdf6ceab83dd4dc68e337a42ef920eb20905d0`  
		Last Modified: Wed, 10 Apr 2024 03:48:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a5f2e153db15d696864529c6bb50afcb6527159a6e03879328350dd5b7b88`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca516aa541cd69f8936f5e586b58f6d9fc0135990cc558de86ab5ababf963b29`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3`

```console
$ docker pull traefik@sha256:940b0c3dd5468fb2dbc26eb6180a213e2f05ea5d10eeec4373abee136a159652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:3.0.0-rc3` - linux; amd64

```console
$ docker pull traefik@sha256:8b5a00052b4a25122b79e261d58f2bbf87937a0b11cbe62e9dc73394bbd3ed88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45167757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e595ae387b49f63c46bf7c0df3e3a1ade691546b8807fc90194f4a49e3dcaf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:15 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:15 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c86d42c6ee19def22cfadf30c6270aaac42a1c52c96179fc0ada179978ee0`  
		Last Modified: Sat, 16 Mar 2024 09:02:40 GMT  
		Size: 41.1 MB (41139034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad5694bc6f8a623b0eb1d57dc0a088f293870691c7e47310f5a18c0cde7674a`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:90d8997366af2b199b6f072ef057b01fe586dd0823a95846926fa174291c157c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42390472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6485015395492e18c678e74352403c96e5c0bb05aa7ec53a6f8a517bc9cf67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:07 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:07 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08fc1b14a3d3556165bedf1d94c8630dc1d0c7b33e4cd65a677907b5bba6cc1`  
		Last Modified: Sat, 16 Mar 2024 06:38:32 GMT  
		Size: 38.6 MB (38603704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8eb8e998597054adc242b95b60bdeb2e8e7020acf9f054b54fdc5e0d584ae4`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e68604ff497f79d9522e437ee66a3645de33494a2767872371a803212039993
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42043483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1f8efc9eb622c56f587602b707c3238b25d6f32d32d008b9a33cd7ac516216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:32 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:32 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e9487662ce49d04a55c69f1640870789f94bfd6e0dc32a28c511ddd3489b71`  
		Last Modified: Sat, 16 Mar 2024 02:43:55 GMT  
		Size: 38.1 MB (38072646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c15ff70d10a381654357ae74e33269071ee5380f03f4e11119fb2c8b79fb51d`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc3` - linux; ppc64le

```console
$ docker pull traefik@sha256:edf5a96c035e0f6e682fff437a86d64199346ac4053e0286c1a823e7bc848a70
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dcb125de975065559e7f4373f2446f91076c02cdd79b57001543bed8db41a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:09:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:09:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:09:45 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:09:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07e78c4c5c1b86e845ed8a0fb75da1329adbc4fe731a0ee8b03ae71446ba1fd`  
		Last Modified: Sat, 16 Mar 2024 07:10:20 GMT  
		Size: 36.9 MB (36929870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d024b32c9d738039d6f452d8dbad3ae0d3faeb42c48460138da619c23164b4`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc3` - linux; s390x

```console
$ docker pull traefik@sha256:0bf8cfc60d3bc736604925e6047e58069ffbeeb39badbf495482a0ebbe91fb6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43797288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc3a16e2b34522b6f52599f397c5dc56a3a3b85400b6b88d908c98b35ac29d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:54:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:54:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:54:04 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:54:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:54:04 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:54:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc322c0721e5037c2543b6dd0f8d2414a757ad55ed5e16a9ace5f22c8428b9`  
		Last Modified: Sat, 16 Mar 2024 22:56:39 GMT  
		Size: 39.9 MB (39933271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e7a3d560876dfda34b978cf1250873cc7d723c8f46a77feedf1849e388f42`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a0357d92202a7e0fcaae4dd3cc728417289f51f1d8d21ec1c92ab6fbcab5133a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:3.0.0-rc3-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:75b5ef91faf5391e02263555071c35a5fc363874e2059ff151a933d04ceb64f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207243489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3dc00cb417c957e75a19010044938884a685c80da9d420089e1b77f83af88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:45:08 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:45:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:45:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688fe15c79b7db926c9e01771f49e6967e652ff34f7d3cc9421e16274bdabdf8`  
		Last Modified: Wed, 10 Apr 2024 03:49:11 GMT  
		Size: 42.8 MB (42809933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ca6e2850a6cfdf104e40c31579893a55030554c6b9507cad3756bdeaed1f5`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039938c2016338255e75112d1d20fe2f2a0421c222e9429a2e08335e0d882b1c`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fef8b7c7c9bed557697ce2c9abd90a94a06c108a3afb420fd7435856f43026`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:3a1fdc89de455b9c22251ffab5f844a259045b3de5a809d11d393886f9f2d263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:3.0.0-rc3-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:fca33031dd6909250cf0beaf5b81ebe87b40bb8e04697a184ce2f72fe6ffea6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042199913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89955d6980fa4a5298483012509b0098e371ecd53371e2969d3e939117d5b1d0`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:43:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:43:17 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:43:18 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16dca97b74396719506a92c84457e45ebb658e173a0581aad8debfc58de6690`  
		Last Modified: Wed, 10 Apr 2024 03:48:47 GMT  
		Size: 42.8 MB (42821001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31eee5a20b340589cc77b66bd8bdf6ceab83dd4dc68e337a42ef920eb20905d0`  
		Last Modified: Wed, 10 Apr 2024 03:48:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a5f2e153db15d696864529c6bb50afcb6527159a6e03879328350dd5b7b88`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca516aa541cd69f8936f5e586b58f6d9fc0135990cc558de86ab5ababf963b29`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:940b0c3dd5468fb2dbc26eb6180a213e2f05ea5d10eeec4373abee136a159652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:beaufort` - linux; amd64

```console
$ docker pull traefik@sha256:8b5a00052b4a25122b79e261d58f2bbf87937a0b11cbe62e9dc73394bbd3ed88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45167757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e595ae387b49f63c46bf7c0df3e3a1ade691546b8807fc90194f4a49e3dcaf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:15 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:15 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c86d42c6ee19def22cfadf30c6270aaac42a1c52c96179fc0ada179978ee0`  
		Last Modified: Sat, 16 Mar 2024 09:02:40 GMT  
		Size: 41.1 MB (41139034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad5694bc6f8a623b0eb1d57dc0a088f293870691c7e47310f5a18c0cde7674a`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:90d8997366af2b199b6f072ef057b01fe586dd0823a95846926fa174291c157c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42390472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6485015395492e18c678e74352403c96e5c0bb05aa7ec53a6f8a517bc9cf67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:07 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:07 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08fc1b14a3d3556165bedf1d94c8630dc1d0c7b33e4cd65a677907b5bba6cc1`  
		Last Modified: Sat, 16 Mar 2024 06:38:32 GMT  
		Size: 38.6 MB (38603704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8eb8e998597054adc242b95b60bdeb2e8e7020acf9f054b54fdc5e0d584ae4`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e68604ff497f79d9522e437ee66a3645de33494a2767872371a803212039993
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42043483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1f8efc9eb622c56f587602b707c3238b25d6f32d32d008b9a33cd7ac516216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:32 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:32 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e9487662ce49d04a55c69f1640870789f94bfd6e0dc32a28c511ddd3489b71`  
		Last Modified: Sat, 16 Mar 2024 02:43:55 GMT  
		Size: 38.1 MB (38072646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c15ff70d10a381654357ae74e33269071ee5380f03f4e11119fb2c8b79fb51d`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; ppc64le

```console
$ docker pull traefik@sha256:edf5a96c035e0f6e682fff437a86d64199346ac4053e0286c1a823e7bc848a70
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dcb125de975065559e7f4373f2446f91076c02cdd79b57001543bed8db41a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:09:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:09:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:09:45 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:09:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07e78c4c5c1b86e845ed8a0fb75da1329adbc4fe731a0ee8b03ae71446ba1fd`  
		Last Modified: Sat, 16 Mar 2024 07:10:20 GMT  
		Size: 36.9 MB (36929870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d024b32c9d738039d6f452d8dbad3ae0d3faeb42c48460138da619c23164b4`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:0bf8cfc60d3bc736604925e6047e58069ffbeeb39badbf495482a0ebbe91fb6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43797288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc3a16e2b34522b6f52599f397c5dc56a3a3b85400b6b88d908c98b35ac29d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:54:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:54:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:54:04 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:54:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:54:04 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:54:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc322c0721e5037c2543b6dd0f8d2414a757ad55ed5e16a9ace5f22c8428b9`  
		Last Modified: Sat, 16 Mar 2024 22:56:39 GMT  
		Size: 39.9 MB (39933271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e7a3d560876dfda34b978cf1250873cc7d723c8f46a77feedf1849e388f42`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a0357d92202a7e0fcaae4dd3cc728417289f51f1d8d21ec1c92ab6fbcab5133a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:75b5ef91faf5391e02263555071c35a5fc363874e2059ff151a933d04ceb64f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207243489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3dc00cb417c957e75a19010044938884a685c80da9d420089e1b77f83af88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:45:08 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:45:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:45:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688fe15c79b7db926c9e01771f49e6967e652ff34f7d3cc9421e16274bdabdf8`  
		Last Modified: Wed, 10 Apr 2024 03:49:11 GMT  
		Size: 42.8 MB (42809933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ca6e2850a6cfdf104e40c31579893a55030554c6b9507cad3756bdeaed1f5`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039938c2016338255e75112d1d20fe2f2a0421c222e9429a2e08335e0d882b1c`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fef8b7c7c9bed557697ce2c9abd90a94a06c108a3afb420fd7435856f43026`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:3a1fdc89de455b9c22251ffab5f844a259045b3de5a809d11d393886f9f2d263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:fca33031dd6909250cf0beaf5b81ebe87b40bb8e04697a184ce2f72fe6ffea6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042199913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89955d6980fa4a5298483012509b0098e371ecd53371e2969d3e939117d5b1d0`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:43:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:43:17 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:43:18 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16dca97b74396719506a92c84457e45ebb658e173a0581aad8debfc58de6690`  
		Last Modified: Wed, 10 Apr 2024 03:48:47 GMT  
		Size: 42.8 MB (42821001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31eee5a20b340589cc77b66bd8bdf6ceab83dd4dc68e337a42ef920eb20905d0`  
		Last Modified: Wed, 10 Apr 2024 03:48:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a5f2e153db15d696864529c6bb50afcb6527159a6e03879328350dd5b7b88`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca516aa541cd69f8936f5e586b58f6d9fc0135990cc558de86ab5ababf963b29`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:0a5157f742d2900389da6ce60ea80cc476801dc951917a993cd848d982f58265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:903f89ddacc3059657565d3e5b3b8e8dcba4cc3b8af08183dad6fdc415459111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44764460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef9171e9d171746404b3deec2a4c9902a34ab090be5e0af6292cf46d578b35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:23 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:23 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f89104cf675aa8f174193c769467325e9ad59468b56c24f1e06873996e837`  
		Last Modified: Sat, 16 Mar 2024 09:02:59 GMT  
		Size: 40.7 MB (40735737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2854bd2e93ffa353be4c4af010c11b6015af14d8a01fd44caecd27f005eae`  
		Last Modified: Sat, 16 Mar 2024 09:02:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a98638c22a31753067775956551e83e71b5ff2492436692542809e3b1fdaa601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380a6fb69f6060cd614ddf88be41e93bc4524de186877df85fa546422a8b866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:14 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:14 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437ceea7b75ae735791dbc150afc3c2b26d4b431ac5ced56cf805dc8d154199a`  
		Last Modified: Sat, 16 Mar 2024 06:38:52 GMT  
		Size: 38.3 MB (38330899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87966e6d71b48984faa23eab03ff499a107931cbad2b1706e61e0d40a4023f03`  
		Last Modified: Sat, 16 Mar 2024 06:38:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5582b38228735e42e3fe1dd3fb49a2cc139cb1d19908c01de8ef0e53ca0372f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41660229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159525f47b70184553832cc3b646d48d2332462c674682d816707461d47c6965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:38 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:38 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ec8d4c0d6b39d6ac772df1a381c54b5ebdb0684a410a3b4b7ab1f8c0c822f5`  
		Last Modified: Sat, 16 Mar 2024 02:44:13 GMT  
		Size: 37.7 MB (37689392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9404f9e59a2c0cb69ba89ce113f9619427ba2d0367deef6e4f972c6b1afc86`  
		Last Modified: Sat, 16 Mar 2024 02:44:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:efba7027881dc510d374099389b6fce438104f92fcbe138111d6bbf962a3a37c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b813ffcb52083c55280ab73b23a8959359b21911352dc99841977ffbddb2566`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:10:00 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:10:01 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:10:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6724621d9ac1c4db5f182eebf62e6acdae57a70ba04d78722643af376dcfc8`  
		Last Modified: Sat, 16 Mar 2024 07:10:42 GMT  
		Size: 36.7 MB (36651920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fba92839f2ee812037158b91abd37cfdcc5d3ad9de09c6e89590d6dc517ca0b`  
		Last Modified: Sat, 16 Mar 2024 07:10:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:1d0f4e79aff6ff4b564fb2292af4e11eebe6b9d3b9d4ac77e417a46547654fca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43543560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d62fa36bfbf517be29ac764fe9ecd768c79ed91997ac822d4366c9176913d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:55:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:55:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:55:27 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:55:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:55:27 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:55:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee11a4c1b9e5b32b4cbd7ab4b6b2476c247fead47a16cecae7df62ed85faa9`  
		Last Modified: Sat, 16 Mar 2024 22:56:58 GMT  
		Size: 39.7 MB (39679543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629032b546364a1aa7b1ed4eb597d0e0feb5e38dda13289fc414edebb3bbeeb8`  
		Last Modified: Sat, 16 Mar 2024 22:56:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:0a5157f742d2900389da6ce60ea80cc476801dc951917a993cd848d982f58265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:903f89ddacc3059657565d3e5b3b8e8dcba4cc3b8af08183dad6fdc415459111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44764460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef9171e9d171746404b3deec2a4c9902a34ab090be5e0af6292cf46d578b35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:23 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:23 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f89104cf675aa8f174193c769467325e9ad59468b56c24f1e06873996e837`  
		Last Modified: Sat, 16 Mar 2024 09:02:59 GMT  
		Size: 40.7 MB (40735737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2854bd2e93ffa353be4c4af010c11b6015af14d8a01fd44caecd27f005eae`  
		Last Modified: Sat, 16 Mar 2024 09:02:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a98638c22a31753067775956551e83e71b5ff2492436692542809e3b1fdaa601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380a6fb69f6060cd614ddf88be41e93bc4524de186877df85fa546422a8b866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:14 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:14 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437ceea7b75ae735791dbc150afc3c2b26d4b431ac5ced56cf805dc8d154199a`  
		Last Modified: Sat, 16 Mar 2024 06:38:52 GMT  
		Size: 38.3 MB (38330899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87966e6d71b48984faa23eab03ff499a107931cbad2b1706e61e0d40a4023f03`  
		Last Modified: Sat, 16 Mar 2024 06:38:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5582b38228735e42e3fe1dd3fb49a2cc139cb1d19908c01de8ef0e53ca0372f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41660229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159525f47b70184553832cc3b646d48d2332462c674682d816707461d47c6965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:38 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:38 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ec8d4c0d6b39d6ac772df1a381c54b5ebdb0684a410a3b4b7ab1f8c0c822f5`  
		Last Modified: Sat, 16 Mar 2024 02:44:13 GMT  
		Size: 37.7 MB (37689392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9404f9e59a2c0cb69ba89ce113f9619427ba2d0367deef6e4f972c6b1afc86`  
		Last Modified: Sat, 16 Mar 2024 02:44:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:efba7027881dc510d374099389b6fce438104f92fcbe138111d6bbf962a3a37c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b813ffcb52083c55280ab73b23a8959359b21911352dc99841977ffbddb2566`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:10:00 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:10:01 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:10:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6724621d9ac1c4db5f182eebf62e6acdae57a70ba04d78722643af376dcfc8`  
		Last Modified: Sat, 16 Mar 2024 07:10:42 GMT  
		Size: 36.7 MB (36651920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fba92839f2ee812037158b91abd37cfdcc5d3ad9de09c6e89590d6dc517ca0b`  
		Last Modified: Sat, 16 Mar 2024 07:10:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:1d0f4e79aff6ff4b564fb2292af4e11eebe6b9d3b9d4ac77e417a46547654fca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43543560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d62fa36bfbf517be29ac764fe9ecd768c79ed91997ac822d4366c9176913d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:55:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:55:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:55:27 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:55:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:55:27 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:55:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee11a4c1b9e5b32b4cbd7ab4b6b2476c247fead47a16cecae7df62ed85faa9`  
		Last Modified: Sat, 16 Mar 2024 22:56:58 GMT  
		Size: 39.7 MB (39679543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629032b546364a1aa7b1ed4eb597d0e0feb5e38dda13289fc414edebb3bbeeb8`  
		Last Modified: Sat, 16 Mar 2024 22:56:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:68f280958b91c3ad020661f9d8dfcdc2937e23bb906301bc70d74f58412b7d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:6c5955d8c7d640ef1e953033bfe26e8446361c887e850375f77a328d6c5b1a9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206657579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617262a4ea137484e609ac8a8a11f20bbcfa9814a6efaa6e14a4933b07ce9aa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:47:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:47:58 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:47:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:48:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aacf44a3b14b8a83aef647a55a384882381ac41332f8dd2ef1c98c17b2f7acb`  
		Last Modified: Wed, 10 Apr 2024 03:50:00 GMT  
		Size: 42.2 MB (42223956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b263b54faf1ee656a3aebca88c4e3149b74fa9ea9f0da62f0696ab77cdb78c`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e280c61423acf1dd14d8703c15995d019ed30d6861fa81b56d74ac76cd963011`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dcbeb77a8df85630996daf57474e78c714c6149ba840b4419b5d7587d718bf`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d0b4d7c2b58fb45cae594447e61aa75eb6af746c3b3049c4de395f366102dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:3a49fb5b2da8093efb0ce0c81508cbd0da2094ad86ab54211a9d795409d46fd1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041584646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33031be9b8289d6354979333b3469cb1c2caf98f54ff84ddbb9bd0355bce8e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:46:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:46:05 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:46:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:46:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da328a847e4abad0f2877e248def5be636cb88ab9c263d476c4c0324ada9aa57`  
		Last Modified: Wed, 10 Apr 2024 03:49:34 GMT  
		Size: 42.2 MB (42205404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1871eb9258c0b7ed2735a70a2004c355e79c1c23e77067b50f9dc006660ab6c`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1279d1342efb5efb211769e19e67d9f012252ee5ea3c9c3d2a55a5c7defd5fa0`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d9e3e2a3252feeed2131f724369a572d22b136c23636ce651e302fac336e5`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:0a5157f742d2900389da6ce60ea80cc476801dc951917a993cd848d982f58265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v2.11` - linux; amd64

```console
$ docker pull traefik@sha256:903f89ddacc3059657565d3e5b3b8e8dcba4cc3b8af08183dad6fdc415459111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44764460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef9171e9d171746404b3deec2a4c9902a34ab090be5e0af6292cf46d578b35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:23 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:23 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f89104cf675aa8f174193c769467325e9ad59468b56c24f1e06873996e837`  
		Last Modified: Sat, 16 Mar 2024 09:02:59 GMT  
		Size: 40.7 MB (40735737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2854bd2e93ffa353be4c4af010c11b6015af14d8a01fd44caecd27f005eae`  
		Last Modified: Sat, 16 Mar 2024 09:02:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a98638c22a31753067775956551e83e71b5ff2492436692542809e3b1fdaa601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380a6fb69f6060cd614ddf88be41e93bc4524de186877df85fa546422a8b866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:14 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:14 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437ceea7b75ae735791dbc150afc3c2b26d4b431ac5ced56cf805dc8d154199a`  
		Last Modified: Sat, 16 Mar 2024 06:38:52 GMT  
		Size: 38.3 MB (38330899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87966e6d71b48984faa23eab03ff499a107931cbad2b1706e61e0d40a4023f03`  
		Last Modified: Sat, 16 Mar 2024 06:38:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5582b38228735e42e3fe1dd3fb49a2cc139cb1d19908c01de8ef0e53ca0372f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41660229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159525f47b70184553832cc3b646d48d2332462c674682d816707461d47c6965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:38 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:38 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ec8d4c0d6b39d6ac772df1a381c54b5ebdb0684a410a3b4b7ab1f8c0c822f5`  
		Last Modified: Sat, 16 Mar 2024 02:44:13 GMT  
		Size: 37.7 MB (37689392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9404f9e59a2c0cb69ba89ce113f9619427ba2d0367deef6e4f972c6b1afc86`  
		Last Modified: Sat, 16 Mar 2024 02:44:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:efba7027881dc510d374099389b6fce438104f92fcbe138111d6bbf962a3a37c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b813ffcb52083c55280ab73b23a8959359b21911352dc99841977ffbddb2566`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:10:00 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:10:01 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:10:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6724621d9ac1c4db5f182eebf62e6acdae57a70ba04d78722643af376dcfc8`  
		Last Modified: Sat, 16 Mar 2024 07:10:42 GMT  
		Size: 36.7 MB (36651920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fba92839f2ee812037158b91abd37cfdcc5d3ad9de09c6e89590d6dc517ca0b`  
		Last Modified: Sat, 16 Mar 2024 07:10:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:1d0f4e79aff6ff4b564fb2292af4e11eebe6b9d3b9d4ac77e417a46547654fca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43543560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d62fa36bfbf517be29ac764fe9ecd768c79ed91997ac822d4366c9176913d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:55:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:55:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:55:27 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:55:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:55:27 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:55:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee11a4c1b9e5b32b4cbd7ab4b6b2476c247fead47a16cecae7df62ed85faa9`  
		Last Modified: Sat, 16 Mar 2024 22:56:58 GMT  
		Size: 39.7 MB (39679543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629032b546364a1aa7b1ed4eb597d0e0feb5e38dda13289fc414edebb3bbeeb8`  
		Last Modified: Sat, 16 Mar 2024 22:56:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-1809`

```console
$ docker pull traefik@sha256:68f280958b91c3ad020661f9d8dfcdc2937e23bb906301bc70d74f58412b7d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:v2.11-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:6c5955d8c7d640ef1e953033bfe26e8446361c887e850375f77a328d6c5b1a9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206657579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617262a4ea137484e609ac8a8a11f20bbcfa9814a6efaa6e14a4933b07ce9aa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:47:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:47:58 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:47:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:48:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aacf44a3b14b8a83aef647a55a384882381ac41332f8dd2ef1c98c17b2f7acb`  
		Last Modified: Wed, 10 Apr 2024 03:50:00 GMT  
		Size: 42.2 MB (42223956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b263b54faf1ee656a3aebca88c4e3149b74fa9ea9f0da62f0696ab77cdb78c`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e280c61423acf1dd14d8703c15995d019ed30d6861fa81b56d74ac76cd963011`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dcbeb77a8df85630996daf57474e78c714c6149ba840b4419b5d7587d718bf`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d0b4d7c2b58fb45cae594447e61aa75eb6af746c3b3049c4de395f366102dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:3a49fb5b2da8093efb0ce0c81508cbd0da2094ad86ab54211a9d795409d46fd1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041584646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33031be9b8289d6354979333b3469cb1c2caf98f54ff84ddbb9bd0355bce8e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:46:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:46:05 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:46:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:46:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da328a847e4abad0f2877e248def5be636cb88ab9c263d476c4c0324ada9aa57`  
		Last Modified: Wed, 10 Apr 2024 03:49:34 GMT  
		Size: 42.2 MB (42205404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1871eb9258c0b7ed2735a70a2004c355e79c1c23e77067b50f9dc006660ab6c`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1279d1342efb5efb211769e19e67d9f012252ee5ea3c9c3d2a55a5c7defd5fa0`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d9e3e2a3252feeed2131f724369a572d22b136c23636ce651e302fac336e5`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0`

```console
$ docker pull traefik@sha256:0a5157f742d2900389da6ce60ea80cc476801dc951917a993cd848d982f58265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v2.11.0` - linux; amd64

```console
$ docker pull traefik@sha256:903f89ddacc3059657565d3e5b3b8e8dcba4cc3b8af08183dad6fdc415459111
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44764460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ef9171e9d171746404b3deec2a4c9902a34ab090be5e0af6292cf46d578b35`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:23 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:23 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:23 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3f89104cf675aa8f174193c769467325e9ad59468b56c24f1e06873996e837`  
		Last Modified: Sat, 16 Mar 2024 09:02:59 GMT  
		Size: 40.7 MB (40735737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb2854bd2e93ffa353be4c4af010c11b6015af14d8a01fd44caecd27f005eae`  
		Last Modified: Sat, 16 Mar 2024 09:02:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:a98638c22a31753067775956551e83e71b5ff2492436692542809e3b1fdaa601
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42117667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5380a6fb69f6060cd614ddf88be41e93bc4524de186877df85fa546422a8b866`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:14 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:14 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:14 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437ceea7b75ae735791dbc150afc3c2b26d4b431ac5ced56cf805dc8d154199a`  
		Last Modified: Sat, 16 Mar 2024 06:38:52 GMT  
		Size: 38.3 MB (38330899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87966e6d71b48984faa23eab03ff499a107931cbad2b1706e61e0d40a4023f03`  
		Last Modified: Sat, 16 Mar 2024 06:38:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:5582b38228735e42e3fe1dd3fb49a2cc139cb1d19908c01de8ef0e53ca0372f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41660229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159525f47b70184553832cc3b646d48d2332462c674682d816707461d47c6965`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:38 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:38 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:38 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:38 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ec8d4c0d6b39d6ac772df1a381c54b5ebdb0684a410a3b4b7ab1f8c0c822f5`  
		Last Modified: Sat, 16 Mar 2024 02:44:13 GMT  
		Size: 37.7 MB (37689392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9404f9e59a2c0cb69ba89ce113f9619427ba2d0367deef6e4f972c6b1afc86`  
		Last Modified: Sat, 16 Mar 2024 02:44:08 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:efba7027881dc510d374099389b6fce438104f92fcbe138111d6bbf962a3a37c
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40633810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b813ffcb52083c55280ab73b23a8959359b21911352dc99841977ffbddb2566`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:57 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:59 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:10:00 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:10:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:10:01 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:10:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6724621d9ac1c4db5f182eebf62e6acdae57a70ba04d78722643af376dcfc8`  
		Last Modified: Sat, 16 Mar 2024 07:10:42 GMT  
		Size: 36.7 MB (36651920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fba92839f2ee812037158b91abd37cfdcc5d3ad9de09c6e89590d6dc517ca0b`  
		Last Modified: Sat, 16 Mar 2024 07:10:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.0` - linux; s390x

```console
$ docker pull traefik@sha256:1d0f4e79aff6ff4b564fb2292af4e11eebe6b9d3b9d4ac77e417a46547654fca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43543560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d62fa36bfbf517be29ac764fe9ecd768c79ed91997ac822d4366c9176913d09`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:55:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:55:27 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:55:27 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:55:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:55:27 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:55:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ee11a4c1b9e5b32b4cbd7ab4b6b2476c247fead47a16cecae7df62ed85faa9`  
		Last Modified: Sat, 16 Mar 2024 22:56:58 GMT  
		Size: 39.7 MB (39679543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629032b546364a1aa7b1ed4eb597d0e0feb5e38dda13289fc414edebb3bbeeb8`  
		Last Modified: Sat, 16 Mar 2024 22:56:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:68f280958b91c3ad020661f9d8dfcdc2937e23bb906301bc70d74f58412b7d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:v2.11.0-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:6c5955d8c7d640ef1e953033bfe26e8446361c887e850375f77a328d6c5b1a9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206657579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617262a4ea137484e609ac8a8a11f20bbcfa9814a6efaa6e14a4933b07ce9aa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:47:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:47:58 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:47:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:48:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aacf44a3b14b8a83aef647a55a384882381ac41332f8dd2ef1c98c17b2f7acb`  
		Last Modified: Wed, 10 Apr 2024 03:50:00 GMT  
		Size: 42.2 MB (42223956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b263b54faf1ee656a3aebca88c4e3149b74fa9ea9f0da62f0696ab77cdb78c`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e280c61423acf1dd14d8703c15995d019ed30d6861fa81b56d74ac76cd963011`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dcbeb77a8df85630996daf57474e78c714c6149ba840b4419b5d7587d718bf`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d0b4d7c2b58fb45cae594447e61aa75eb6af746c3b3049c4de395f366102dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:v2.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:3a49fb5b2da8093efb0ce0c81508cbd0da2094ad86ab54211a9d795409d46fd1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041584646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33031be9b8289d6354979333b3469cb1c2caf98f54ff84ddbb9bd0355bce8e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:46:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:46:05 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:46:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:46:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da328a847e4abad0f2877e248def5be636cb88ab9c263d476c4c0324ada9aa57`  
		Last Modified: Wed, 10 Apr 2024 03:49:34 GMT  
		Size: 42.2 MB (42205404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1871eb9258c0b7ed2735a70a2004c355e79c1c23e77067b50f9dc006660ab6c`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1279d1342efb5efb211769e19e67d9f012252ee5ea3c9c3d2a55a5c7defd5fa0`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d9e3e2a3252feeed2131f724369a572d22b136c23636ce651e302fac336e5`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:940b0c3dd5468fb2dbc26eb6180a213e2f05ea5d10eeec4373abee136a159652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v3.0` - linux; amd64

```console
$ docker pull traefik@sha256:8b5a00052b4a25122b79e261d58f2bbf87937a0b11cbe62e9dc73394bbd3ed88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45167757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e595ae387b49f63c46bf7c0df3e3a1ade691546b8807fc90194f4a49e3dcaf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:15 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:15 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c86d42c6ee19def22cfadf30c6270aaac42a1c52c96179fc0ada179978ee0`  
		Last Modified: Sat, 16 Mar 2024 09:02:40 GMT  
		Size: 41.1 MB (41139034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad5694bc6f8a623b0eb1d57dc0a088f293870691c7e47310f5a18c0cde7674a`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:90d8997366af2b199b6f072ef057b01fe586dd0823a95846926fa174291c157c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42390472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6485015395492e18c678e74352403c96e5c0bb05aa7ec53a6f8a517bc9cf67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:07 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:07 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08fc1b14a3d3556165bedf1d94c8630dc1d0c7b33e4cd65a677907b5bba6cc1`  
		Last Modified: Sat, 16 Mar 2024 06:38:32 GMT  
		Size: 38.6 MB (38603704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8eb8e998597054adc242b95b60bdeb2e8e7020acf9f054b54fdc5e0d584ae4`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e68604ff497f79d9522e437ee66a3645de33494a2767872371a803212039993
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42043483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1f8efc9eb622c56f587602b707c3238b25d6f32d32d008b9a33cd7ac516216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:32 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:32 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e9487662ce49d04a55c69f1640870789f94bfd6e0dc32a28c511ddd3489b71`  
		Last Modified: Sat, 16 Mar 2024 02:43:55 GMT  
		Size: 38.1 MB (38072646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c15ff70d10a381654357ae74e33269071ee5380f03f4e11119fb2c8b79fb51d`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:edf5a96c035e0f6e682fff437a86d64199346ac4053e0286c1a823e7bc848a70
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dcb125de975065559e7f4373f2446f91076c02cdd79b57001543bed8db41a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:09:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:09:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:09:45 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:09:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07e78c4c5c1b86e845ed8a0fb75da1329adbc4fe731a0ee8b03ae71446ba1fd`  
		Last Modified: Sat, 16 Mar 2024 07:10:20 GMT  
		Size: 36.9 MB (36929870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d024b32c9d738039d6f452d8dbad3ae0d3faeb42c48460138da619c23164b4`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; s390x

```console
$ docker pull traefik@sha256:0bf8cfc60d3bc736604925e6047e58069ffbeeb39badbf495482a0ebbe91fb6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43797288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc3a16e2b34522b6f52599f397c5dc56a3a3b85400b6b88d908c98b35ac29d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:54:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:54:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:54:04 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:54:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:54:04 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:54:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc322c0721e5037c2543b6dd0f8d2414a757ad55ed5e16a9ace5f22c8428b9`  
		Last Modified: Sat, 16 Mar 2024 22:56:39 GMT  
		Size: 39.9 MB (39933271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e7a3d560876dfda34b978cf1250873cc7d723c8f46a77feedf1849e388f42`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a0357d92202a7e0fcaae4dd3cc728417289f51f1d8d21ec1c92ab6fbcab5133a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:75b5ef91faf5391e02263555071c35a5fc363874e2059ff151a933d04ceb64f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207243489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3dc00cb417c957e75a19010044938884a685c80da9d420089e1b77f83af88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:45:08 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:45:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:45:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688fe15c79b7db926c9e01771f49e6967e652ff34f7d3cc9421e16274bdabdf8`  
		Last Modified: Wed, 10 Apr 2024 03:49:11 GMT  
		Size: 42.8 MB (42809933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ca6e2850a6cfdf104e40c31579893a55030554c6b9507cad3756bdeaed1f5`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039938c2016338255e75112d1d20fe2f2a0421c222e9429a2e08335e0d882b1c`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fef8b7c7c9bed557697ce2c9abd90a94a06c108a3afb420fd7435856f43026`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:3a1fdc89de455b9c22251ffab5f844a259045b3de5a809d11d393886f9f2d263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:v3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:fca33031dd6909250cf0beaf5b81ebe87b40bb8e04697a184ce2f72fe6ffea6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042199913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89955d6980fa4a5298483012509b0098e371ecd53371e2969d3e939117d5b1d0`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:43:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:43:17 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:43:18 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16dca97b74396719506a92c84457e45ebb658e173a0581aad8debfc58de6690`  
		Last Modified: Wed, 10 Apr 2024 03:48:47 GMT  
		Size: 42.8 MB (42821001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31eee5a20b340589cc77b66bd8bdf6ceab83dd4dc68e337a42ef920eb20905d0`  
		Last Modified: Wed, 10 Apr 2024 03:48:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a5f2e153db15d696864529c6bb50afcb6527159a6e03879328350dd5b7b88`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca516aa541cd69f8936f5e586b58f6d9fc0135990cc558de86ab5ababf963b29`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3`

```console
$ docker pull traefik@sha256:940b0c3dd5468fb2dbc26eb6180a213e2f05ea5d10eeec4373abee136a159652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v3.0.0-rc3` - linux; amd64

```console
$ docker pull traefik@sha256:8b5a00052b4a25122b79e261d58f2bbf87937a0b11cbe62e9dc73394bbd3ed88
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45167757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e595ae387b49f63c46bf7c0df3e3a1ade691546b8807fc90194f4a49e3dcaf1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 09:02:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 09:02:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 09:02:15 GMT
EXPOSE 80
# Sat, 16 Mar 2024 09:02:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 09:02:15 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 09:02:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43642c84faa0177dd56ccef5d516b3a2884d2f7a43db9bd96fa0b3e959aad61d`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 619.6 KB (619626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c86d42c6ee19def22cfadf30c6270aaac42a1c52c96179fc0ada179978ee0`  
		Last Modified: Sat, 16 Mar 2024 09:02:40 GMT  
		Size: 41.1 MB (41139034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ad5694bc6f8a623b0eb1d57dc0a088f293870691c7e47310f5a18c0cde7674a`  
		Last Modified: Sat, 16 Mar 2024 09:02:34 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:90d8997366af2b199b6f072ef057b01fe586dd0823a95846926fa174291c157c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42390472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6485015395492e18c678e74352403c96e5c0bb05aa7ec53a6f8a517bc9cf67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 06:38:06 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 06:38:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 06:38:07 GMT
EXPOSE 80
# Sat, 16 Mar 2024 06:38:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 06:38:07 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 06:38:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef9cf5763ccd74ec71d4cc9e68ee015d1cff1fc34f48eb2999f662164849ef`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 621.0 KB (621004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08fc1b14a3d3556165bedf1d94c8630dc1d0c7b33e4cd65a677907b5bba6cc1`  
		Last Modified: Sat, 16 Mar 2024 06:38:32 GMT  
		Size: 38.6 MB (38603704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8eb8e998597054adc242b95b60bdeb2e8e7020acf9f054b54fdc5e0d584ae4`  
		Last Modified: Sat, 16 Mar 2024 06:38:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e68604ff497f79d9522e437ee66a3645de33494a2767872371a803212039993
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42043483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1f8efc9eb622c56f587602b707c3238b25d6f32d32d008b9a33cd7ac516216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 02:43:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 02:43:32 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 02:43:32 GMT
EXPOSE 80
# Sat, 16 Mar 2024 02:43:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:43:32 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 02:43:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4baaba5180ceea9ad8168fce68ccb099e3d162bd72481c825e648a20108e51`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 622.8 KB (622754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e9487662ce49d04a55c69f1640870789f94bfd6e0dc32a28c511ddd3489b71`  
		Last Modified: Sat, 16 Mar 2024 02:43:55 GMT  
		Size: 38.1 MB (38072646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c15ff70d10a381654357ae74e33269071ee5380f03f4e11119fb2c8b79fb51d`  
		Last Modified: Sat, 16 Mar 2024 02:43:51 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc3` - linux; ppc64le

```console
$ docker pull traefik@sha256:edf5a96c035e0f6e682fff437a86d64199346ac4053e0286c1a823e7bc848a70
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40911759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dcb125de975065559e7f4373f2446f91076c02cdd79b57001543bed8db41a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 07:09:41 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 07:09:44 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 07:09:44 GMT
EXPOSE 80
# Sat, 16 Mar 2024 07:09:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 07:09:45 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 07:09:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b469ea1332f58fc3525100cfcacbd0b8aa5906c661c76c8c0c6dc22a05a004f`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 623.2 KB (623168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07e78c4c5c1b86e845ed8a0fb75da1329adbc4fe731a0ee8b03ae71446ba1fd`  
		Last Modified: Sat, 16 Mar 2024 07:10:20 GMT  
		Size: 36.9 MB (36929870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d024b32c9d738039d6f452d8dbad3ae0d3faeb42c48460138da619c23164b4`  
		Last Modified: Sat, 16 Mar 2024 07:10:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc3` - linux; s390x

```console
$ docker pull traefik@sha256:0bf8cfc60d3bc736604925e6047e58069ffbeeb39badbf495482a0ebbe91fb6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43797288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cc3a16e2b34522b6f52599f397c5dc56a3a3b85400b6b88d908c98b35ac29d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Sat, 16 Mar 2024 22:54:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Sat, 16 Mar 2024 22:54:04 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Sat, 16 Mar 2024 22:54:04 GMT
EXPOSE 80
# Sat, 16 Mar 2024 22:54:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 22:54:04 GMT
CMD ["traefik"]
# Sat, 16 Mar 2024 22:54:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13631cdd38935d6cfedacf127605825835d2d9968a03d25fdca49f163f929286`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 621.0 KB (621014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01cc322c0721e5037c2543b6dd0f8d2414a757ad55ed5e16a9ace5f22c8428b9`  
		Last Modified: Sat, 16 Mar 2024 22:56:39 GMT  
		Size: 39.9 MB (39933271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508e7a3d560876dfda34b978cf1250873cc7d723c8f46a77feedf1849e388f42`  
		Last Modified: Sat, 16 Mar 2024 22:56:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:a0357d92202a7e0fcaae4dd3cc728417289f51f1d8d21ec1c92ab6fbcab5133a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:v3.0.0-rc3-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:75b5ef91faf5391e02263555071c35a5fc363874e2059ff151a933d04ceb64f0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207243489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b3dc00cb417c957e75a19010044938884a685c80da9d420089e1b77f83af88`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:45:07 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:45:08 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:45:08 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:45:09 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688fe15c79b7db926c9e01771f49e6967e652ff34f7d3cc9421e16274bdabdf8`  
		Last Modified: Wed, 10 Apr 2024 03:49:11 GMT  
		Size: 42.8 MB (42809933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7ca6e2850a6cfdf104e40c31579893a55030554c6b9507cad3756bdeaed1f5`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039938c2016338255e75112d1d20fe2f2a0421c222e9429a2e08335e0d882b1c`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fef8b7c7c9bed557697ce2c9abd90a94a06c108a3afb420fd7435856f43026`  
		Last Modified: Wed, 10 Apr 2024 03:49:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:3a1fdc89de455b9c22251ffab5f844a259045b3de5a809d11d393886f9f2d263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:v3.0.0-rc3-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:fca33031dd6909250cf0beaf5b81ebe87b40bb8e04697a184ce2f72fe6ffea6b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042199913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89955d6980fa4a5298483012509b0098e371ecd53371e2969d3e939117d5b1d0`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:43:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:43:17 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:43:18 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:43:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16dca97b74396719506a92c84457e45ebb658e173a0581aad8debfc58de6690`  
		Last Modified: Wed, 10 Apr 2024 03:48:47 GMT  
		Size: 42.8 MB (42821001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31eee5a20b340589cc77b66bd8bdf6ceab83dd4dc68e337a42ef920eb20905d0`  
		Last Modified: Wed, 10 Apr 2024 03:48:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0a5f2e153db15d696864529c6bb50afcb6527159a6e03879328350dd5b7b88`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca516aa541cd69f8936f5e586b58f6d9fc0135990cc558de86ab5ababf963b29`  
		Last Modified: Wed, 10 Apr 2024 03:48:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:68f280958b91c3ad020661f9d8dfcdc2937e23bb906301bc70d74f58412b7d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:6c5955d8c7d640ef1e953033bfe26e8446361c887e850375f77a328d6c5b1a9a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206657579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0617262a4ea137484e609ac8a8a11f20bbcfa9814a6efaa6e14a4933b07ce9aa`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:47:57 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:47:58 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:47:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:48:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aacf44a3b14b8a83aef647a55a384882381ac41332f8dd2ef1c98c17b2f7acb`  
		Last Modified: Wed, 10 Apr 2024 03:50:00 GMT  
		Size: 42.2 MB (42223956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b263b54faf1ee656a3aebca88c4e3149b74fa9ea9f0da62f0696ab77cdb78c`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e280c61423acf1dd14d8703c15995d019ed30d6861fa81b56d74ac76cd963011`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dcbeb77a8df85630996daf57474e78c714c6149ba840b4419b5d7587d718bf`  
		Last Modified: Wed, 10 Apr 2024 03:49:51 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:d0b4d7c2b58fb45cae594447e61aa75eb6af746c3b3049c4de395f366102dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:3a49fb5b2da8093efb0ce0c81508cbd0da2094ad86ab54211a9d795409d46fd1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041584646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33031be9b8289d6354979333b3469cb1c2caf98f54ff84ddbb9bd0355bce8e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 03:46:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Apr 2024 03:46:05 GMT
EXPOSE 80
# Wed, 10 Apr 2024 03:46:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Apr 2024 03:46:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da328a847e4abad0f2877e248def5be636cb88ab9c263d476c4c0324ada9aa57`  
		Last Modified: Wed, 10 Apr 2024 03:49:34 GMT  
		Size: 42.2 MB (42205404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1871eb9258c0b7ed2735a70a2004c355e79c1c23e77067b50f9dc006660ab6c`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1279d1342efb5efb211769e19e67d9f012252ee5ea3c9c3d2a55a5c7defd5fa0`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86d9e3e2a3252feeed2131f724369a572d22b136c23636ce651e302fac336e5`  
		Last Modified: Wed, 10 Apr 2024 03:49:25 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
