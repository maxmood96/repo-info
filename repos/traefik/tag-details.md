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
$ docker pull traefik@sha256:31798dbdea383c4e8000af1a0e0e6672ee67655b4e4fbc84a9f7991e1f539dd4
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
$ docker pull traefik@sha256:2288dfb2b1598e5f78a8fc195fa6e63ca6583d2dc6aa705195667c924f065d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43545936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f9f69a2c99970f7beec33266a119e580b233634ce1c93b82c55193b994bb84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 23:19:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 23:19:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 23:19:55 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 23:19:55 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 23:19:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3fd5e93fa0b1f81fe2e15f1b973ef18bc797e2253f5b44811d6fa77eda0315`  
		Last Modified: Mon, 12 Feb 2024 23:21:30 GMT  
		Size: 39.7 MB (39679541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87af5bb6339aa046d6d9be943b4b463189ae85db29687c681b99eb95423c0de`  
		Last Modified: Mon, 12 Feb 2024 23:21:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:2.11-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0`

```console
$ docker pull traefik@sha256:31798dbdea383c4e8000af1a0e0e6672ee67655b4e4fbc84a9f7991e1f539dd4
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
$ docker pull traefik@sha256:2288dfb2b1598e5f78a8fc195fa6e63ca6583d2dc6aa705195667c924f065d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43545936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f9f69a2c99970f7beec33266a119e580b233634ce1c93b82c55193b994bb84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 23:19:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 23:19:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 23:19:55 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 23:19:55 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 23:19:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3fd5e93fa0b1f81fe2e15f1b973ef18bc797e2253f5b44811d6fa77eda0315`  
		Last Modified: Mon, 12 Feb 2024 23:21:30 GMT  
		Size: 39.7 MB (39679541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87af5bb6339aa046d6d9be943b4b463189ae85db29687c681b99eb95423c0de`  
		Last Modified: Mon, 12 Feb 2024 23:21:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:2.11.0-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:2.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0`

```console
$ docker pull traefik@sha256:f4129f411fc99a025f901688ace7186e0933ba0271ae8d47aa060de134a36c80
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
$ docker pull traefik@sha256:b08d1fc83e10b985fec28bb86bba3038695d79cf623a1608b5ebe0a1ed88f17a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7229524bf9d634c12b6ca11f397249459cf0c6b6b73d599d45f8b237e7001854`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 20:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 20:29:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 20:29:12 GMT
EXPOSE 80
# Wed, 13 Mar 2024 20:29:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 20:29:13 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 20:29:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7947c294ec78d988aafdda154262ed90cfca050140faae69fb157fda0afe46e8`  
		Last Modified: Wed, 13 Mar 2024 20:32:14 GMT  
		Size: 39.9 MB (39933272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a82447626ce9aea1a2e5c7e6129e91ba0bf38d7f24139e53f5fb363c3b26f`  
		Last Modified: Wed, 13 Mar 2024 20:32:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3`

```console
$ docker pull traefik@sha256:f4129f411fc99a025f901688ace7186e0933ba0271ae8d47aa060de134a36c80
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
$ docker pull traefik@sha256:b08d1fc83e10b985fec28bb86bba3038695d79cf623a1608b5ebe0a1ed88f17a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7229524bf9d634c12b6ca11f397249459cf0c6b6b73d599d45f8b237e7001854`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 20:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 20:29:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 20:29:12 GMT
EXPOSE 80
# Wed, 13 Mar 2024 20:29:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 20:29:13 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 20:29:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7947c294ec78d988aafdda154262ed90cfca050140faae69fb157fda0afe46e8`  
		Last Modified: Wed, 13 Mar 2024 20:32:14 GMT  
		Size: 39.9 MB (39933272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a82447626ce9aea1a2e5c7e6129e91ba0bf38d7f24139e53f5fb363c3b26f`  
		Last Modified: Wed, 13 Mar 2024 20:32:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:3.0.0-rc3-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:3.0.0-rc3-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:f4129f411fc99a025f901688ace7186e0933ba0271ae8d47aa060de134a36c80
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
$ docker pull traefik@sha256:b08d1fc83e10b985fec28bb86bba3038695d79cf623a1608b5ebe0a1ed88f17a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7229524bf9d634c12b6ca11f397249459cf0c6b6b73d599d45f8b237e7001854`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 20:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 20:29:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 20:29:12 GMT
EXPOSE 80
# Wed, 13 Mar 2024 20:29:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 20:29:13 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 20:29:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7947c294ec78d988aafdda154262ed90cfca050140faae69fb157fda0afe46e8`  
		Last Modified: Wed, 13 Mar 2024 20:32:14 GMT  
		Size: 39.9 MB (39933272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a82447626ce9aea1a2e5c7e6129e91ba0bf38d7f24139e53f5fb363c3b26f`  
		Last Modified: Wed, 13 Mar 2024 20:32:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:31798dbdea383c4e8000af1a0e0e6672ee67655b4e4fbc84a9f7991e1f539dd4
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
$ docker pull traefik@sha256:2288dfb2b1598e5f78a8fc195fa6e63ca6583d2dc6aa705195667c924f065d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43545936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f9f69a2c99970f7beec33266a119e580b233634ce1c93b82c55193b994bb84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 23:19:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 23:19:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 23:19:55 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 23:19:55 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 23:19:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3fd5e93fa0b1f81fe2e15f1b973ef18bc797e2253f5b44811d6fa77eda0315`  
		Last Modified: Mon, 12 Feb 2024 23:21:30 GMT  
		Size: 39.7 MB (39679541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87af5bb6339aa046d6d9be943b4b463189ae85db29687c681b99eb95423c0de`  
		Last Modified: Mon, 12 Feb 2024 23:21:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:31798dbdea383c4e8000af1a0e0e6672ee67655b4e4fbc84a9f7991e1f539dd4
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
$ docker pull traefik@sha256:2288dfb2b1598e5f78a8fc195fa6e63ca6583d2dc6aa705195667c924f065d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43545936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f9f69a2c99970f7beec33266a119e580b233634ce1c93b82c55193b994bb84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 23:19:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 23:19:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 23:19:55 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 23:19:55 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 23:19:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3fd5e93fa0b1f81fe2e15f1b973ef18bc797e2253f5b44811d6fa77eda0315`  
		Last Modified: Mon, 12 Feb 2024 23:21:30 GMT  
		Size: 39.7 MB (39679541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87af5bb6339aa046d6d9be943b4b463189ae85db29687c681b99eb95423c0de`  
		Last Modified: Mon, 12 Feb 2024 23:21:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:31798dbdea383c4e8000af1a0e0e6672ee67655b4e4fbc84a9f7991e1f539dd4
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
$ docker pull traefik@sha256:2288dfb2b1598e5f78a8fc195fa6e63ca6583d2dc6aa705195667c924f065d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43545936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f9f69a2c99970f7beec33266a119e580b233634ce1c93b82c55193b994bb84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 23:19:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 23:19:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 23:19:55 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 23:19:55 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 23:19:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3fd5e93fa0b1f81fe2e15f1b973ef18bc797e2253f5b44811d6fa77eda0315`  
		Last Modified: Mon, 12 Feb 2024 23:21:30 GMT  
		Size: 39.7 MB (39679541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87af5bb6339aa046d6d9be943b4b463189ae85db29687c681b99eb95423c0de`  
		Last Modified: Mon, 12 Feb 2024 23:21:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:v2.11-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0`

```console
$ docker pull traefik@sha256:31798dbdea383c4e8000af1a0e0e6672ee67655b4e4fbc84a9f7991e1f539dd4
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
$ docker pull traefik@sha256:2288dfb2b1598e5f78a8fc195fa6e63ca6583d2dc6aa705195667c924f065d9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43545936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f9f69a2c99970f7beec33266a119e580b233634ce1c93b82c55193b994bb84`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Mon, 12 Feb 2024 23:19:52 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Mon, 12 Feb 2024 23:19:55 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Mon, 12 Feb 2024 23:19:55 GMT
EXPOSE 80
# Mon, 12 Feb 2024 23:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 12 Feb 2024 23:19:55 GMT
CMD ["traefik"]
# Mon, 12 Feb 2024 23:19:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3fd5e93fa0b1f81fe2e15f1b973ef18bc797e2253f5b44811d6fa77eda0315`  
		Last Modified: Mon, 12 Feb 2024 23:21:30 GMT  
		Size: 39.7 MB (39679541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87af5bb6339aa046d6d9be943b4b463189ae85db29687c681b99eb95423c0de`  
		Last Modified: Mon, 12 Feb 2024 23:21:24 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:v2.11.0-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:v2.11.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:f4129f411fc99a025f901688ace7186e0933ba0271ae8d47aa060de134a36c80
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
$ docker pull traefik@sha256:b08d1fc83e10b985fec28bb86bba3038695d79cf623a1608b5ebe0a1ed88f17a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7229524bf9d634c12b6ca11f397249459cf0c6b6b73d599d45f8b237e7001854`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 20:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 20:29:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 20:29:12 GMT
EXPOSE 80
# Wed, 13 Mar 2024 20:29:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 20:29:13 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 20:29:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7947c294ec78d988aafdda154262ed90cfca050140faae69fb157fda0afe46e8`  
		Last Modified: Wed, 13 Mar 2024 20:32:14 GMT  
		Size: 39.9 MB (39933272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a82447626ce9aea1a2e5c7e6129e91ba0bf38d7f24139e53f5fb363c3b26f`  
		Last Modified: Wed, 13 Mar 2024 20:32:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:v3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3`

```console
$ docker pull traefik@sha256:f4129f411fc99a025f901688ace7186e0933ba0271ae8d47aa060de134a36c80
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
$ docker pull traefik@sha256:b08d1fc83e10b985fec28bb86bba3038695d79cf623a1608b5ebe0a1ed88f17a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43799667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7229524bf9d634c12b6ca11f397249459cf0c6b6b73d599d45f8b237e7001854`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:20:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 13 Mar 2024 20:29:09 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 13 Mar 2024 20:29:12 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 13 Mar 2024 20:29:12 GMT
EXPOSE 80
# Wed, 13 Mar 2024 20:29:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 13 Mar 2024 20:29:13 GMT
CMD ["traefik"]
# Wed, 13 Mar 2024 20:29:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf27425c88e5cc0862fced0d047cf74b71578f98896c1a758dee8855f093d79`  
		Last Modified: Sat, 27 Jan 2024 04:23:32 GMT  
		Size: 623.4 KB (623391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7947c294ec78d988aafdda154262ed90cfca050140faae69fb157fda0afe46e8`  
		Last Modified: Wed, 13 Mar 2024 20:32:14 GMT  
		Size: 39.9 MB (39933272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760a82447626ce9aea1a2e5c7e6129e91ba0bf38d7f24139e53f5fb363c3b26f`  
		Last Modified: Wed, 13 Mar 2024 20:32:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3-windowsservercore-1809`

```console
$ docker pull traefik@sha256:8cd933505291271393e38dee7c95ad038c39aaad0a7e2f98e504fb1874effeb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:v3.0.0-rc3-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:1765dfc7a5bd9874ae38acda9135d4051f862f147f7c74b2f1a5adf5e4b7e453
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167946232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ae201a76bc79c7366a245a122af50968181c082a2565a45d9271d0d33ece1b`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:19:01 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:19:02 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:19:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:19:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0715f5907ace3ad301acdf493973e89a9b672116bac6afd2749e9ce4a44a8eb`  
		Last Modified: Wed, 13 Mar 2024 19:20:36 GMT  
		Size: 42.8 MB (42840623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4dae33104c82d0189cfd84d69f2eb1837501f5fa16fdc3ca5e2a5e8fb99253`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78ea15fee491549e4e912349cd2e5c59f95685186ab429b8245903ef3c8f436`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d5bf92c0a782bf09a681c092db045e7fd92ff41b97e6edef7c93db76378f68`  
		Last Modified: Wed, 13 Mar 2024 19:20:26 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:73e2c44013cf3dfa5f84a7b2243eac5c8dce9167463c4efb67cbe9a7a42e37ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:v3.0.0-rc3-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:ae569feeca4b45ed9255c22a65efb91c846f28365423687f193aa44c0e655102
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2000292492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0731b3bf072fcc8a146ae5c4ab1935bbc470841c7378a91a35649beace00a22`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 19:16:26 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc3/traefik_v3.0.0-rc3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 19:16:27 GMT
EXPOSE 80
# Wed, 13 Mar 2024 19:16:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 19:16:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8dcc153faf25844163e5b2f08f18f94ab93dcaaab8919038821ffde2a49021`  
		Last Modified: Wed, 13 Mar 2024 19:20:07 GMT  
		Size: 42.8 MB (42827825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d87838d656d80f32043c43304582529474e4fb8bcc682a3d0cf5c3699f30f`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdad8e3579fee6ea282c79f652abbf970849ca89071214d8027e16525fa3fa`  
		Last Modified: Wed, 13 Mar 2024 19:19:58 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b7429cd8653cca61b37ad619d4aa4a2e5fe763b829cf968d0be23b2f9612bed`  
		Last Modified: Wed, 13 Mar 2024 19:19:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:2aac8ebfad3ba904b4d3526df665da626873047f67c5342e1ed998989c43ea8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull traefik@sha256:bbe0a7db1135c5aa48369a4eda314906864f78383e7b1fe09431f98ee6ccd234
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167341162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f811c8f069782b8d45e62475a89a201832c48402d8133e1515c291182b26a502`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:25:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:25:48 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:25:49 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:25:50 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95ac7200a8e3a2c0ba493c179bc071869284c2508fd9bb2fe002278f0afcb18`  
		Last Modified: Wed, 13 Mar 2024 04:27:37 GMT  
		Size: 42.2 MB (42235535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd691174aab3bf358c4e8c04e2289a6417f9a218daef3f6b340becc6b0d3db0`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2031e082f306cfde918d303ec4b3c6b20fe28fa4e98bc75bdf94e6a16c3fc9`  
		Last Modified: Wed, 13 Mar 2024 04:27:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34956f4ae2a88ec16d6fc2161f4cf70d3f9a56e0fba9bec37bbadc0f11d1ef64`  
		Last Modified: Wed, 13 Mar 2024 04:27:27 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:21d300d8d72db35e94fd885be7873e66fdf9a50407378145a1e8c5df0ae6f1ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull traefik@sha256:698b27fe2f1a7d910141455723932f32b8c7cb729830eb791a0b9bb9e1dfc37b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1999700334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac748ff26ef4b15d8858f826b681d177e9546e01c1809c76064e4595ef8f622`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 04:24:04 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.0/traefik_v2.11.0_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 13 Mar 2024 04:24:05 GMT
EXPOSE 80
# Wed, 13 Mar 2024 04:24:06 GMT
ENTRYPOINT ["/traefik"]
# Wed, 13 Mar 2024 04:24:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3defa6c0936d429cc07a43d4c41e98fe9a563b22d6d47c2d4e8b26bb91fd09`  
		Last Modified: Wed, 13 Mar 2024 04:27:11 GMT  
		Size: 42.2 MB (42235665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90320aa66285218bea75d45b7a0ce6306af06d7590d55538d05bb2d86f92f8d`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff82c34f3abc3e251df983c86355fbe950801d6de486bdf2b7bc3ab052e92cce`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bffafb756604dddb7d508523e6b558dbb9907799b21e53718fda2e27125f2af`  
		Last Modified: Wed, 13 Mar 2024 04:27:02 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
