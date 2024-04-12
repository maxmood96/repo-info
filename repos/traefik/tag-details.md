<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-windowsservercore-1809`](#traefik211-windowsservercore-1809)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.2`](#traefik2112)
-	[`traefik:2.11.2-windowsservercore-1809`](#traefik2112-windowsservercore-1809)
-	[`traefik:2.11.2-windowsservercore-ltsc2022`](#traefik2112-windowsservercore-ltsc2022)
-	[`traefik:3.0`](#traefik30)
-	[`traefik:3.0-windowsservercore-1809`](#traefik30-windowsservercore-1809)
-	[`traefik:3.0-windowsservercore-ltsc2022`](#traefik30-windowsservercore-ltsc2022)
-	[`traefik:3.0.0-rc5`](#traefik300-rc5)
-	[`traefik:3.0.0-rc5-windowsservercore-1809`](#traefik300-rc5-windowsservercore-1809)
-	[`traefik:3.0.0-rc5-windowsservercore-ltsc2022`](#traefik300-rc5-windowsservercore-ltsc2022)
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
-	[`traefik:v2.11.2`](#traefikv2112)
-	[`traefik:v2.11.2-windowsservercore-1809`](#traefikv2112-windowsservercore-1809)
-	[`traefik:v2.11.2-windowsservercore-ltsc2022`](#traefikv2112-windowsservercore-ltsc2022)
-	[`traefik:v3.0`](#traefikv30)
-	[`traefik:v3.0-windowsservercore-1809`](#traefikv30-windowsservercore-1809)
-	[`traefik:v3.0-windowsservercore-ltsc2022`](#traefikv30-windowsservercore-ltsc2022)
-	[`traefik:v3.0.0-rc5`](#traefikv300-rc5)
-	[`traefik:v3.0.0-rc5-windowsservercore-1809`](#traefikv300-rc5-windowsservercore-1809)
-	[`traefik:v3.0.0-rc5-windowsservercore-ltsc2022`](#traefikv300-rc5-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-1809`](#traefikwindowsservercore-1809)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2.11`

```console
$ docker pull traefik@sha256:c6f6001dd1fc09fb0ae47ad2198102c40a8d9586c02d6040d561fd4fb7e91f45
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
$ docker pull traefik@sha256:c0577b65f0800c7be7e9b651917f22cda98cc2cca4167e546936a26dfe016aa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44867579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe0021cb966a1eaeffb1cd79f490edb9a9b90a129f32f2caddf3764f70417a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:34 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:34 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:34770c1f816cac86b87c016e6cb4b72caea0eea51842af9870f2eecb35a4c7e8`  
		Last Modified: Fri, 12 Apr 2024 00:20:17 GMT  
		Size: 40.8 MB (40838856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea386b2b17283914c6ebe44480fe40ee91b08c0a9ddc27bb7b8f097bfbceef`  
		Last Modified: Fri, 12 Apr 2024 00:20:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c7165daad921ed6b75c1cef1b5831d220ab3c0a750fb7be0e27e4566d4f3b95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42187860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0061acd2b3cdd995fc3287002e485c024cfb0fadbd88c0f2798fef0284afa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:54 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:deca64fcf678c659625190e96315652a3ef578e7fffd5c87242fbac7be415b6f`  
		Last Modified: Thu, 11 Apr 2024 22:16:35 GMT  
		Size: 38.4 MB (38401093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d971034897344b507410608ec8a5570229d17c7a20fdcd21362791f5931e1209`  
		Last Modified: Thu, 11 Apr 2024 22:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4bc25533b4285a21d9b604585f9f885c6266ce8cde580d71c73d5898225c7ff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41728821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8797b64f9893a7c58cb49ad999a05cf9dfa9ad6522dc8d3a6ebb9508ad5e8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:43 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:43 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a137a48e42fc346d8bf6dbd1e65022475f8f3e76a940d792928975bb13213d4e`  
		Last Modified: Fri, 12 Apr 2024 00:36:19 GMT  
		Size: 37.8 MB (37757985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44edc1b33556d0d40eb96f6fbb5f49c61fbc4bdc81fbeb6eb8adb7d802005633`  
		Last Modified: Fri, 12 Apr 2024 00:36:15 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:73f9d90421d5b14c9e31ad0ab396c3b8a7b945e5bd2a55cd7fb326fb156a14eb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40682778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb0a0cfaa13df8808d9d297e37f44e92dcaea892411eefaee5557a5547bf356`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:18 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:19 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6c0d6d632c3f66f7fe17cfdb8fa5895a4e52750e521c9e499e43ce52b04f4ba6`  
		Last Modified: Thu, 11 Apr 2024 23:06:02 GMT  
		Size: 36.7 MB (36700889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03df793315cfbd9e5d5ee7d84c2d5dac2c4ebe774463c52eefc1fb50d48df413`  
		Last Modified: Thu, 11 Apr 2024 23:05:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:0554ae58e67a53a32f7af2872d5f74aca2d7ec967946ba4345b95fe9e3bea2ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938e00aeb9b6705aed9bbb1f8d81b3a92a29003f176428ed3614764769d9fd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:42:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:42:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:42:10 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:42:10 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:42:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:50e55c64a74695c6158dabaa3b27d45e64f228e132a7eb4d192462c6ba2f5591`  
		Last Modified: Fri, 12 Apr 2024 06:43:45 GMT  
		Size: 39.8 MB (39759420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435cc6e849aff1c03d18fcddacb0924f0b87224cc6ebe2fee32e3e45b28ffcd2`  
		Last Modified: Fri, 12 Apr 2024 06:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5d57d565ce4f25e74dbfc998a3f8de1af92daddb7c06c4d544448144e84e2ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:2.11-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:871d1af1df46bdda93b932b6e0770fc3d2b7f359951ee4fb54c89659ed5fa03c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206777082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4accfc3034b31010b1f4989d82f4d5174cbe809ffab2144ac826438135d8e7dd`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:21:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:21:48 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:21:49 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:21:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3b0a68a91dddfdc645b9de3f12d157f1dfed7d4edb4bbe9d1cc59545560584c4`  
		Last Modified: Thu, 11 Apr 2024 21:23:59 GMT  
		Size: 42.3 MB (42343526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1184798168b8404b4fda09ac4d335419be9a2059ada2596ca580be1657d126`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc12a18bfcd6781649c9a02cf80cf3ce12e46e04a341287dc41d81892b16aab4`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6b6d4310ace0ce7630667449f47ad3c2d8289df90035f2f938905e65bbdcf`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:687a1167833ca51063a6df2a2ec1f1280db747e8df4a6039d8401d8d985b6076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:b18fb55ced49ba23d4385c70fc8000daca16763cdabf7ba902de16f14f6b85bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041715577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65367681edbfa0e5830a00186c79eeff6a82400a1c199c163d28daff7a57935`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:20:01 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:20:01 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a38a6ed2f2919e4d3a456722f80f2cc5189317b5f8206a1800abf8e4e2c340ee`  
		Last Modified: Thu, 11 Apr 2024 21:23:32 GMT  
		Size: 42.3 MB (42336305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a694512e13f4ca5ec422cca0abc98c942d10cd38b7bd4065ec2953da84ed12`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956c9331d98b50bab5553b6539c0754d2dd6caa97629e82c9ee54eb1c96d19f9`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38013d67d8e0708d512269850d6bf12744eb70848f1564ec713004271262a24d`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.2`

```console
$ docker pull traefik@sha256:c6f6001dd1fc09fb0ae47ad2198102c40a8d9586c02d6040d561fd4fb7e91f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:2.11.2` - linux; amd64

```console
$ docker pull traefik@sha256:c0577b65f0800c7be7e9b651917f22cda98cc2cca4167e546936a26dfe016aa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44867579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe0021cb966a1eaeffb1cd79f490edb9a9b90a129f32f2caddf3764f70417a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:34 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:34 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:34770c1f816cac86b87c016e6cb4b72caea0eea51842af9870f2eecb35a4c7e8`  
		Last Modified: Fri, 12 Apr 2024 00:20:17 GMT  
		Size: 40.8 MB (40838856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea386b2b17283914c6ebe44480fe40ee91b08c0a9ddc27bb7b8f097bfbceef`  
		Last Modified: Fri, 12 Apr 2024 00:20:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c7165daad921ed6b75c1cef1b5831d220ab3c0a750fb7be0e27e4566d4f3b95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42187860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0061acd2b3cdd995fc3287002e485c024cfb0fadbd88c0f2798fef0284afa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:54 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:deca64fcf678c659625190e96315652a3ef578e7fffd5c87242fbac7be415b6f`  
		Last Modified: Thu, 11 Apr 2024 22:16:35 GMT  
		Size: 38.4 MB (38401093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d971034897344b507410608ec8a5570229d17c7a20fdcd21362791f5931e1209`  
		Last Modified: Thu, 11 Apr 2024 22:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4bc25533b4285a21d9b604585f9f885c6266ce8cde580d71c73d5898225c7ff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41728821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8797b64f9893a7c58cb49ad999a05cf9dfa9ad6522dc8d3a6ebb9508ad5e8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:43 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:43 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a137a48e42fc346d8bf6dbd1e65022475f8f3e76a940d792928975bb13213d4e`  
		Last Modified: Fri, 12 Apr 2024 00:36:19 GMT  
		Size: 37.8 MB (37757985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44edc1b33556d0d40eb96f6fbb5f49c61fbc4bdc81fbeb6eb8adb7d802005633`  
		Last Modified: Fri, 12 Apr 2024 00:36:15 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.2` - linux; ppc64le

```console
$ docker pull traefik@sha256:73f9d90421d5b14c9e31ad0ab396c3b8a7b945e5bd2a55cd7fb326fb156a14eb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40682778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb0a0cfaa13df8808d9d297e37f44e92dcaea892411eefaee5557a5547bf356`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:18 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:19 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6c0d6d632c3f66f7fe17cfdb8fa5895a4e52750e521c9e499e43ce52b04f4ba6`  
		Last Modified: Thu, 11 Apr 2024 23:06:02 GMT  
		Size: 36.7 MB (36700889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03df793315cfbd9e5d5ee7d84c2d5dac2c4ebe774463c52eefc1fb50d48df413`  
		Last Modified: Thu, 11 Apr 2024 23:05:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:2.11.2` - linux; s390x

```console
$ docker pull traefik@sha256:0554ae58e67a53a32f7af2872d5f74aca2d7ec967946ba4345b95fe9e3bea2ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938e00aeb9b6705aed9bbb1f8d81b3a92a29003f176428ed3614764769d9fd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:42:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:42:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:42:10 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:42:10 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:42:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:50e55c64a74695c6158dabaa3b27d45e64f228e132a7eb4d192462c6ba2f5591`  
		Last Modified: Fri, 12 Apr 2024 06:43:45 GMT  
		Size: 39.8 MB (39759420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435cc6e849aff1c03d18fcddacb0924f0b87224cc6ebe2fee32e3e45b28ffcd2`  
		Last Modified: Fri, 12 Apr 2024 06:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5d57d565ce4f25e74dbfc998a3f8de1af92daddb7c06c4d544448144e84e2ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:2.11.2-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:871d1af1df46bdda93b932b6e0770fc3d2b7f359951ee4fb54c89659ed5fa03c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206777082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4accfc3034b31010b1f4989d82f4d5174cbe809ffab2144ac826438135d8e7dd`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:21:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:21:48 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:21:49 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:21:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3b0a68a91dddfdc645b9de3f12d157f1dfed7d4edb4bbe9d1cc59545560584c4`  
		Last Modified: Thu, 11 Apr 2024 21:23:59 GMT  
		Size: 42.3 MB (42343526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1184798168b8404b4fda09ac4d335419be9a2059ada2596ca580be1657d126`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc12a18bfcd6781649c9a02cf80cf3ce12e46e04a341287dc41d81892b16aab4`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6b6d4310ace0ce7630667449f47ad3c2d8289df90035f2f938905e65bbdcf`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:687a1167833ca51063a6df2a2ec1f1280db747e8df4a6039d8401d8d985b6076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:2.11.2-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:b18fb55ced49ba23d4385c70fc8000daca16763cdabf7ba902de16f14f6b85bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041715577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65367681edbfa0e5830a00186c79eeff6a82400a1c199c163d28daff7a57935`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:20:01 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:20:01 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a38a6ed2f2919e4d3a456722f80f2cc5189317b5f8206a1800abf8e4e2c340ee`  
		Last Modified: Thu, 11 Apr 2024 21:23:32 GMT  
		Size: 42.3 MB (42336305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a694512e13f4ca5ec422cca0abc98c942d10cd38b7bd4065ec2953da84ed12`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956c9331d98b50bab5553b6539c0754d2dd6caa97629e82c9ee54eb1c96d19f9`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38013d67d8e0708d512269850d6bf12744eb70848f1564ec713004271262a24d`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0`

```console
$ docker pull traefik@sha256:7138e0a962d4fd9dc7c6389ded6846faa63fc2e45605330224d07bdb8caff7b1
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
$ docker pull traefik@sha256:811bbf1194cc52d236a473e917a0aee3f528e2f79f5833c74b48a9bfca2ddb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45277036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcff26917f9848748f3eed01731a6251205f485c34c69cc657a6f1821e957d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:26 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:26 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:42c4476942763ad3acd156d084a6011f3ec9538f7f0bd06ee1b54ea651ecdfd3`  
		Last Modified: Fri, 12 Apr 2024 00:19:55 GMT  
		Size: 41.2 MB (41248314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a6ff87b7d1c9c00a294b40b2af6131149970a6845b438bfb94a7798cd728df`  
		Last Modified: Fri, 12 Apr 2024 00:19:48 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0ca78a7bfcfaa4b4b962ca8198d7cd718f999490eee95176b3126abdc0acb631
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42490608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b68cf3460b1aff598f3904b330fe77f9290a78809785c8c6dc655b8fb96df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:46 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:46 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:c4e1eaacb3adb0332f0bd4ae4ee8ffe2cdd1bd80a2d7158a2b0a0e074be8a8e4`  
		Last Modified: Thu, 11 Apr 2024 22:16:14 GMT  
		Size: 38.7 MB (38703841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bdd6895ca4693d1a62fb4acd8baeb1ea5e6cfc930de09fa08cc23a6ccaf1b9`  
		Last Modified: Thu, 11 Apr 2024 22:16:07 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f1ddb043d3389732070023942cee9af0c4e2af84f92fb93c986e381dd861a14a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42138445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe93f715ec4ec96091012f395a26084e26927a4564ccf8e346bd96939b22c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:36 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:36 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:906ac0d7801aef2db2bb0c095bec3e7d6b41315f531000d6afe70505cea778d8`  
		Last Modified: Fri, 12 Apr 2024 00:36:00 GMT  
		Size: 38.2 MB (38167609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf09b12869a3f35bf9bf4d2c6472ab2ec43091b612174bb3b2b16a761a2e1a70`  
		Last Modified: Fri, 12 Apr 2024 00:35:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:f95456451595948a332eec78d79092e8765e23edf00b3d037fa61e9a2d4a7607
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40991951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdb1bbea94694699731c1a9fd8d11a8dc3c39a1dd5bb49b0bf796d9c81b0d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:06 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:07 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a0c88713362d99d5028e665ae366ab1e963d5d2e92db4fcb9fa06e0517b0ae2f`  
		Last Modified: Thu, 11 Apr 2024 23:05:41 GMT  
		Size: 37.0 MB (37010062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5bf9f1638add89e28a3fe9df71add265483c883e1aadbb132835e672443652`  
		Last Modified: Thu, 11 Apr 2024 23:05:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0` - linux; s390x

```console
$ docker pull traefik@sha256:6210e091220dfd6b3b4a652e0909ddbbd0871054725dc3ea1e21b944b9cf076a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43897663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8619facbd82bb64ddb383e80f31d13eaa7e223eb3c21b287781c6a7ac5bda4a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:41:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:41:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:41:02 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:41:03 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:41:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d548252488ee7f731d13613eabb54583823befa4eb28774874cc3274da346d28`  
		Last Modified: Fri, 12 Apr 2024 06:43:28 GMT  
		Size: 40.0 MB (40033646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc937e642c6d4639ae3f93e9954ea1e90235e741f95e779d3f06f710617a611`  
		Last Modified: Fri, 12 Apr 2024 06:43:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:97586d9a8a9db5f083de589b53dffbf8e436157bc8cc472fad3cc970051fc618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:3.0-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:9047bddb7042f6a473bce099f717ee8e4b3afbfc6e5badcb2df7f10ba9f25c57
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b3bf18198ea0ee471f179e32368d15c01255fb14c3584839bd15f05692e5a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:19:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:19:13 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:19:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:19:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:51a3b8e9e274bbf363b9d0e073901c305443e40e2b0e2649f65da07a4d6dc581`  
		Last Modified: Thu, 11 Apr 2024 21:23:07 GMT  
		Size: 42.9 MB (42910903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f0d6e81290baec2a487b78551461710c2bab324308eba6c91050f74aa95879`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80aa336fd11f44b27038a0303eac3277ea18cbd9782d39d3bbeb2ffb3904db8b`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d7c6605e759ac002ed7705630608cce2f82bc7a3dc6c3691f8e181337b850`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8a1409c1139bff4179bc607456ee860a67a1985ffddf3217bb168c91a05de7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:a23258d2869ea0d2aaa6b83f19b288d98300429670dfc94aaf6738c446d83c03
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042309262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25c53563fc535cea74aaa8e22d32cfa2fc889814114bdb8b61a98d2668f5cbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:16:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:16:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:16:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:16:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:db875a8b9343f6d61f6cbe5d89b252c72175cffde0b5a4d5d20a2304ea060388`  
		Last Modified: Thu, 11 Apr 2024 21:22:42 GMT  
		Size: 42.9 MB (42929981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4d452c27d55f73dc1a4477d30fd09267a202627ec82c61a82f6fbdb59d8a6f`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7a84505488da92902d96856c92e8dd39e57a00bfeba904b088192b945d1261`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bf9dd26cc7e4fd1b3422c528d78ee6da3b248e99ce70f379f5cb6a62ce4892`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc5`

```console
$ docker pull traefik@sha256:7138e0a962d4fd9dc7c6389ded6846faa63fc2e45605330224d07bdb8caff7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:3.0.0-rc5` - linux; amd64

```console
$ docker pull traefik@sha256:811bbf1194cc52d236a473e917a0aee3f528e2f79f5833c74b48a9bfca2ddb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45277036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcff26917f9848748f3eed01731a6251205f485c34c69cc657a6f1821e957d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:26 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:26 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:42c4476942763ad3acd156d084a6011f3ec9538f7f0bd06ee1b54ea651ecdfd3`  
		Last Modified: Fri, 12 Apr 2024 00:19:55 GMT  
		Size: 41.2 MB (41248314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a6ff87b7d1c9c00a294b40b2af6131149970a6845b438bfb94a7798cd728df`  
		Last Modified: Fri, 12 Apr 2024 00:19:48 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0ca78a7bfcfaa4b4b962ca8198d7cd718f999490eee95176b3126abdc0acb631
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42490608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b68cf3460b1aff598f3904b330fe77f9290a78809785c8c6dc655b8fb96df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:46 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:46 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:c4e1eaacb3adb0332f0bd4ae4ee8ffe2cdd1bd80a2d7158a2b0a0e074be8a8e4`  
		Last Modified: Thu, 11 Apr 2024 22:16:14 GMT  
		Size: 38.7 MB (38703841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bdd6895ca4693d1a62fb4acd8baeb1ea5e6cfc930de09fa08cc23a6ccaf1b9`  
		Last Modified: Thu, 11 Apr 2024 22:16:07 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f1ddb043d3389732070023942cee9af0c4e2af84f92fb93c986e381dd861a14a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42138445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe93f715ec4ec96091012f395a26084e26927a4564ccf8e346bd96939b22c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:36 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:36 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:906ac0d7801aef2db2bb0c095bec3e7d6b41315f531000d6afe70505cea778d8`  
		Last Modified: Fri, 12 Apr 2024 00:36:00 GMT  
		Size: 38.2 MB (38167609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf09b12869a3f35bf9bf4d2c6472ab2ec43091b612174bb3b2b16a761a2e1a70`  
		Last Modified: Fri, 12 Apr 2024 00:35:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc5` - linux; ppc64le

```console
$ docker pull traefik@sha256:f95456451595948a332eec78d79092e8765e23edf00b3d037fa61e9a2d4a7607
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40991951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdb1bbea94694699731c1a9fd8d11a8dc3c39a1dd5bb49b0bf796d9c81b0d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:06 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:07 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a0c88713362d99d5028e665ae366ab1e963d5d2e92db4fcb9fa06e0517b0ae2f`  
		Last Modified: Thu, 11 Apr 2024 23:05:41 GMT  
		Size: 37.0 MB (37010062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5bf9f1638add89e28a3fe9df71add265483c883e1aadbb132835e672443652`  
		Last Modified: Thu, 11 Apr 2024 23:05:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:3.0.0-rc5` - linux; s390x

```console
$ docker pull traefik@sha256:6210e091220dfd6b3b4a652e0909ddbbd0871054725dc3ea1e21b944b9cf076a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43897663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8619facbd82bb64ddb383e80f31d13eaa7e223eb3c21b287781c6a7ac5bda4a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:41:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:41:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:41:02 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:41:03 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:41:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d548252488ee7f731d13613eabb54583823befa4eb28774874cc3274da346d28`  
		Last Modified: Fri, 12 Apr 2024 06:43:28 GMT  
		Size: 40.0 MB (40033646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc937e642c6d4639ae3f93e9954ea1e90235e741f95e779d3f06f710617a611`  
		Last Modified: Fri, 12 Apr 2024 06:43:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:97586d9a8a9db5f083de589b53dffbf8e436157bc8cc472fad3cc970051fc618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:3.0.0-rc5-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:9047bddb7042f6a473bce099f717ee8e4b3afbfc6e5badcb2df7f10ba9f25c57
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b3bf18198ea0ee471f179e32368d15c01255fb14c3584839bd15f05692e5a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:19:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:19:13 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:19:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:19:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:51a3b8e9e274bbf363b9d0e073901c305443e40e2b0e2649f65da07a4d6dc581`  
		Last Modified: Thu, 11 Apr 2024 21:23:07 GMT  
		Size: 42.9 MB (42910903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f0d6e81290baec2a487b78551461710c2bab324308eba6c91050f74aa95879`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80aa336fd11f44b27038a0303eac3277ea18cbd9782d39d3bbeb2ffb3904db8b`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d7c6605e759ac002ed7705630608cce2f82bc7a3dc6c3691f8e181337b850`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.0.0-rc5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8a1409c1139bff4179bc607456ee860a67a1985ffddf3217bb168c91a05de7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:3.0.0-rc5-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:a23258d2869ea0d2aaa6b83f19b288d98300429670dfc94aaf6738c446d83c03
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042309262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25c53563fc535cea74aaa8e22d32cfa2fc889814114bdb8b61a98d2668f5cbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:16:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:16:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:16:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:16:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:db875a8b9343f6d61f6cbe5d89b252c72175cffde0b5a4d5d20a2304ea060388`  
		Last Modified: Thu, 11 Apr 2024 21:22:42 GMT  
		Size: 42.9 MB (42929981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4d452c27d55f73dc1a4477d30fd09267a202627ec82c61a82f6fbdb59d8a6f`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7a84505488da92902d96856c92e8dd39e57a00bfeba904b088192b945d1261`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bf9dd26cc7e4fd1b3422c528d78ee6da3b248e99ce70f379f5cb6a62ce4892`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort`

```console
$ docker pull traefik@sha256:7138e0a962d4fd9dc7c6389ded6846faa63fc2e45605330224d07bdb8caff7b1
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
$ docker pull traefik@sha256:811bbf1194cc52d236a473e917a0aee3f528e2f79f5833c74b48a9bfca2ddb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45277036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcff26917f9848748f3eed01731a6251205f485c34c69cc657a6f1821e957d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:26 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:26 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:42c4476942763ad3acd156d084a6011f3ec9538f7f0bd06ee1b54ea651ecdfd3`  
		Last Modified: Fri, 12 Apr 2024 00:19:55 GMT  
		Size: 41.2 MB (41248314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a6ff87b7d1c9c00a294b40b2af6131149970a6845b438bfb94a7798cd728df`  
		Last Modified: Fri, 12 Apr 2024 00:19:48 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0ca78a7bfcfaa4b4b962ca8198d7cd718f999490eee95176b3126abdc0acb631
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42490608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b68cf3460b1aff598f3904b330fe77f9290a78809785c8c6dc655b8fb96df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:46 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:46 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:c4e1eaacb3adb0332f0bd4ae4ee8ffe2cdd1bd80a2d7158a2b0a0e074be8a8e4`  
		Last Modified: Thu, 11 Apr 2024 22:16:14 GMT  
		Size: 38.7 MB (38703841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bdd6895ca4693d1a62fb4acd8baeb1ea5e6cfc930de09fa08cc23a6ccaf1b9`  
		Last Modified: Thu, 11 Apr 2024 22:16:07 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f1ddb043d3389732070023942cee9af0c4e2af84f92fb93c986e381dd861a14a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42138445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe93f715ec4ec96091012f395a26084e26927a4564ccf8e346bd96939b22c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:36 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:36 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:906ac0d7801aef2db2bb0c095bec3e7d6b41315f531000d6afe70505cea778d8`  
		Last Modified: Fri, 12 Apr 2024 00:36:00 GMT  
		Size: 38.2 MB (38167609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf09b12869a3f35bf9bf4d2c6472ab2ec43091b612174bb3b2b16a761a2e1a70`  
		Last Modified: Fri, 12 Apr 2024 00:35:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; ppc64le

```console
$ docker pull traefik@sha256:f95456451595948a332eec78d79092e8765e23edf00b3d037fa61e9a2d4a7607
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40991951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdb1bbea94694699731c1a9fd8d11a8dc3c39a1dd5bb49b0bf796d9c81b0d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:06 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:07 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a0c88713362d99d5028e665ae366ab1e963d5d2e92db4fcb9fa06e0517b0ae2f`  
		Last Modified: Thu, 11 Apr 2024 23:05:41 GMT  
		Size: 37.0 MB (37010062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5bf9f1638add89e28a3fe9df71add265483c883e1aadbb132835e672443652`  
		Last Modified: Thu, 11 Apr 2024 23:05:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:beaufort` - linux; s390x

```console
$ docker pull traefik@sha256:6210e091220dfd6b3b4a652e0909ddbbd0871054725dc3ea1e21b944b9cf076a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43897663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8619facbd82bb64ddb383e80f31d13eaa7e223eb3c21b287781c6a7ac5bda4a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:41:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:41:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:41:02 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:41:03 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:41:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d548252488ee7f731d13613eabb54583823befa4eb28774874cc3274da346d28`  
		Last Modified: Fri, 12 Apr 2024 06:43:28 GMT  
		Size: 40.0 MB (40033646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc937e642c6d4639ae3f93e9954ea1e90235e741f95e779d3f06f710617a611`  
		Last Modified: Fri, 12 Apr 2024 06:43:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-1809`

```console
$ docker pull traefik@sha256:97586d9a8a9db5f083de589b53dffbf8e436157bc8cc472fad3cc970051fc618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:beaufort-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:9047bddb7042f6a473bce099f717ee8e4b3afbfc6e5badcb2df7f10ba9f25c57
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b3bf18198ea0ee471f179e32368d15c01255fb14c3584839bd15f05692e5a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:19:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:19:13 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:19:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:19:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:51a3b8e9e274bbf363b9d0e073901c305443e40e2b0e2649f65da07a4d6dc581`  
		Last Modified: Thu, 11 Apr 2024 21:23:07 GMT  
		Size: 42.9 MB (42910903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f0d6e81290baec2a487b78551461710c2bab324308eba6c91050f74aa95879`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80aa336fd11f44b27038a0303eac3277ea18cbd9782d39d3bbeb2ffb3904db8b`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d7c6605e759ac002ed7705630608cce2f82bc7a3dc6c3691f8e181337b850`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:beaufort-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8a1409c1139bff4179bc607456ee860a67a1985ffddf3217bb168c91a05de7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:beaufort-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:a23258d2869ea0d2aaa6b83f19b288d98300429670dfc94aaf6738c446d83c03
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042309262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25c53563fc535cea74aaa8e22d32cfa2fc889814114bdb8b61a98d2668f5cbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:16:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:16:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:16:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:16:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:db875a8b9343f6d61f6cbe5d89b252c72175cffde0b5a4d5d20a2304ea060388`  
		Last Modified: Thu, 11 Apr 2024 21:22:42 GMT  
		Size: 42.9 MB (42929981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4d452c27d55f73dc1a4477d30fd09267a202627ec82c61a82f6fbdb59d8a6f`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7a84505488da92902d96856c92e8dd39e57a00bfeba904b088192b945d1261`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bf9dd26cc7e4fd1b3422c528d78ee6da3b248e99ce70f379f5cb6a62ce4892`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:c6f6001dd1fc09fb0ae47ad2198102c40a8d9586c02d6040d561fd4fb7e91f45
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
$ docker pull traefik@sha256:c0577b65f0800c7be7e9b651917f22cda98cc2cca4167e546936a26dfe016aa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44867579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe0021cb966a1eaeffb1cd79f490edb9a9b90a129f32f2caddf3764f70417a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:34 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:34 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:34770c1f816cac86b87c016e6cb4b72caea0eea51842af9870f2eecb35a4c7e8`  
		Last Modified: Fri, 12 Apr 2024 00:20:17 GMT  
		Size: 40.8 MB (40838856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea386b2b17283914c6ebe44480fe40ee91b08c0a9ddc27bb7b8f097bfbceef`  
		Last Modified: Fri, 12 Apr 2024 00:20:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c7165daad921ed6b75c1cef1b5831d220ab3c0a750fb7be0e27e4566d4f3b95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42187860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0061acd2b3cdd995fc3287002e485c024cfb0fadbd88c0f2798fef0284afa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:54 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:deca64fcf678c659625190e96315652a3ef578e7fffd5c87242fbac7be415b6f`  
		Last Modified: Thu, 11 Apr 2024 22:16:35 GMT  
		Size: 38.4 MB (38401093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d971034897344b507410608ec8a5570229d17c7a20fdcd21362791f5931e1209`  
		Last Modified: Thu, 11 Apr 2024 22:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4bc25533b4285a21d9b604585f9f885c6266ce8cde580d71c73d5898225c7ff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41728821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8797b64f9893a7c58cb49ad999a05cf9dfa9ad6522dc8d3a6ebb9508ad5e8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:43 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:43 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a137a48e42fc346d8bf6dbd1e65022475f8f3e76a940d792928975bb13213d4e`  
		Last Modified: Fri, 12 Apr 2024 00:36:19 GMT  
		Size: 37.8 MB (37757985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44edc1b33556d0d40eb96f6fbb5f49c61fbc4bdc81fbeb6eb8adb7d802005633`  
		Last Modified: Fri, 12 Apr 2024 00:36:15 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:73f9d90421d5b14c9e31ad0ab396c3b8a7b945e5bd2a55cd7fb326fb156a14eb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40682778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb0a0cfaa13df8808d9d297e37f44e92dcaea892411eefaee5557a5547bf356`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:18 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:19 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6c0d6d632c3f66f7fe17cfdb8fa5895a4e52750e521c9e499e43ce52b04f4ba6`  
		Last Modified: Thu, 11 Apr 2024 23:06:02 GMT  
		Size: 36.7 MB (36700889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03df793315cfbd9e5d5ee7d84c2d5dac2c4ebe774463c52eefc1fb50d48df413`  
		Last Modified: Thu, 11 Apr 2024 23:05:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:0554ae58e67a53a32f7af2872d5f74aca2d7ec967946ba4345b95fe9e3bea2ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938e00aeb9b6705aed9bbb1f8d81b3a92a29003f176428ed3614764769d9fd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:42:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:42:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:42:10 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:42:10 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:42:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:50e55c64a74695c6158dabaa3b27d45e64f228e132a7eb4d192462c6ba2f5591`  
		Last Modified: Fri, 12 Apr 2024 06:43:45 GMT  
		Size: 39.8 MB (39759420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435cc6e849aff1c03d18fcddacb0924f0b87224cc6ebe2fee32e3e45b28ffcd2`  
		Last Modified: Fri, 12 Apr 2024 06:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:c6f6001dd1fc09fb0ae47ad2198102c40a8d9586c02d6040d561fd4fb7e91f45
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
$ docker pull traefik@sha256:c0577b65f0800c7be7e9b651917f22cda98cc2cca4167e546936a26dfe016aa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44867579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe0021cb966a1eaeffb1cd79f490edb9a9b90a129f32f2caddf3764f70417a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:34 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:34 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:34770c1f816cac86b87c016e6cb4b72caea0eea51842af9870f2eecb35a4c7e8`  
		Last Modified: Fri, 12 Apr 2024 00:20:17 GMT  
		Size: 40.8 MB (40838856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea386b2b17283914c6ebe44480fe40ee91b08c0a9ddc27bb7b8f097bfbceef`  
		Last Modified: Fri, 12 Apr 2024 00:20:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c7165daad921ed6b75c1cef1b5831d220ab3c0a750fb7be0e27e4566d4f3b95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42187860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0061acd2b3cdd995fc3287002e485c024cfb0fadbd88c0f2798fef0284afa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:54 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:deca64fcf678c659625190e96315652a3ef578e7fffd5c87242fbac7be415b6f`  
		Last Modified: Thu, 11 Apr 2024 22:16:35 GMT  
		Size: 38.4 MB (38401093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d971034897344b507410608ec8a5570229d17c7a20fdcd21362791f5931e1209`  
		Last Modified: Thu, 11 Apr 2024 22:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4bc25533b4285a21d9b604585f9f885c6266ce8cde580d71c73d5898225c7ff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41728821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8797b64f9893a7c58cb49ad999a05cf9dfa9ad6522dc8d3a6ebb9508ad5e8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:43 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:43 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a137a48e42fc346d8bf6dbd1e65022475f8f3e76a940d792928975bb13213d4e`  
		Last Modified: Fri, 12 Apr 2024 00:36:19 GMT  
		Size: 37.8 MB (37757985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44edc1b33556d0d40eb96f6fbb5f49c61fbc4bdc81fbeb6eb8adb7d802005633`  
		Last Modified: Fri, 12 Apr 2024 00:36:15 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:73f9d90421d5b14c9e31ad0ab396c3b8a7b945e5bd2a55cd7fb326fb156a14eb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40682778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb0a0cfaa13df8808d9d297e37f44e92dcaea892411eefaee5557a5547bf356`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:18 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:19 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6c0d6d632c3f66f7fe17cfdb8fa5895a4e52750e521c9e499e43ce52b04f4ba6`  
		Last Modified: Thu, 11 Apr 2024 23:06:02 GMT  
		Size: 36.7 MB (36700889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03df793315cfbd9e5d5ee7d84c2d5dac2c4ebe774463c52eefc1fb50d48df413`  
		Last Modified: Thu, 11 Apr 2024 23:05:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:0554ae58e67a53a32f7af2872d5f74aca2d7ec967946ba4345b95fe9e3bea2ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938e00aeb9b6705aed9bbb1f8d81b3a92a29003f176428ed3614764769d9fd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:42:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:42:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:42:10 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:42:10 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:42:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:50e55c64a74695c6158dabaa3b27d45e64f228e132a7eb4d192462c6ba2f5591`  
		Last Modified: Fri, 12 Apr 2024 06:43:45 GMT  
		Size: 39.8 MB (39759420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435cc6e849aff1c03d18fcddacb0924f0b87224cc6ebe2fee32e3e45b28ffcd2`  
		Last Modified: Fri, 12 Apr 2024 06:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5d57d565ce4f25e74dbfc998a3f8de1af92daddb7c06c4d544448144e84e2ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:mimolette-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:871d1af1df46bdda93b932b6e0770fc3d2b7f359951ee4fb54c89659ed5fa03c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206777082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4accfc3034b31010b1f4989d82f4d5174cbe809ffab2144ac826438135d8e7dd`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:21:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:21:48 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:21:49 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:21:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3b0a68a91dddfdc645b9de3f12d157f1dfed7d4edb4bbe9d1cc59545560584c4`  
		Last Modified: Thu, 11 Apr 2024 21:23:59 GMT  
		Size: 42.3 MB (42343526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1184798168b8404b4fda09ac4d335419be9a2059ada2596ca580be1657d126`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc12a18bfcd6781649c9a02cf80cf3ce12e46e04a341287dc41d81892b16aab4`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6b6d4310ace0ce7630667449f47ad3c2d8289df90035f2f938905e65bbdcf`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:687a1167833ca51063a6df2a2ec1f1280db747e8df4a6039d8401d8d985b6076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:b18fb55ced49ba23d4385c70fc8000daca16763cdabf7ba902de16f14f6b85bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041715577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65367681edbfa0e5830a00186c79eeff6a82400a1c199c163d28daff7a57935`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:20:01 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:20:01 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a38a6ed2f2919e4d3a456722f80f2cc5189317b5f8206a1800abf8e4e2c340ee`  
		Last Modified: Thu, 11 Apr 2024 21:23:32 GMT  
		Size: 42.3 MB (42336305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a694512e13f4ca5ec422cca0abc98c942d10cd38b7bd4065ec2953da84ed12`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956c9331d98b50bab5553b6539c0754d2dd6caa97629e82c9ee54eb1c96d19f9`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38013d67d8e0708d512269850d6bf12744eb70848f1564ec713004271262a24d`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:c6f6001dd1fc09fb0ae47ad2198102c40a8d9586c02d6040d561fd4fb7e91f45
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
$ docker pull traefik@sha256:c0577b65f0800c7be7e9b651917f22cda98cc2cca4167e546936a26dfe016aa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44867579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe0021cb966a1eaeffb1cd79f490edb9a9b90a129f32f2caddf3764f70417a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:34 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:34 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:34770c1f816cac86b87c016e6cb4b72caea0eea51842af9870f2eecb35a4c7e8`  
		Last Modified: Fri, 12 Apr 2024 00:20:17 GMT  
		Size: 40.8 MB (40838856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea386b2b17283914c6ebe44480fe40ee91b08c0a9ddc27bb7b8f097bfbceef`  
		Last Modified: Fri, 12 Apr 2024 00:20:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c7165daad921ed6b75c1cef1b5831d220ab3c0a750fb7be0e27e4566d4f3b95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42187860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0061acd2b3cdd995fc3287002e485c024cfb0fadbd88c0f2798fef0284afa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:54 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:deca64fcf678c659625190e96315652a3ef578e7fffd5c87242fbac7be415b6f`  
		Last Modified: Thu, 11 Apr 2024 22:16:35 GMT  
		Size: 38.4 MB (38401093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d971034897344b507410608ec8a5570229d17c7a20fdcd21362791f5931e1209`  
		Last Modified: Thu, 11 Apr 2024 22:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4bc25533b4285a21d9b604585f9f885c6266ce8cde580d71c73d5898225c7ff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41728821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8797b64f9893a7c58cb49ad999a05cf9dfa9ad6522dc8d3a6ebb9508ad5e8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:43 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:43 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a137a48e42fc346d8bf6dbd1e65022475f8f3e76a940d792928975bb13213d4e`  
		Last Modified: Fri, 12 Apr 2024 00:36:19 GMT  
		Size: 37.8 MB (37757985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44edc1b33556d0d40eb96f6fbb5f49c61fbc4bdc81fbeb6eb8adb7d802005633`  
		Last Modified: Fri, 12 Apr 2024 00:36:15 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:73f9d90421d5b14c9e31ad0ab396c3b8a7b945e5bd2a55cd7fb326fb156a14eb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40682778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb0a0cfaa13df8808d9d297e37f44e92dcaea892411eefaee5557a5547bf356`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:18 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:19 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6c0d6d632c3f66f7fe17cfdb8fa5895a4e52750e521c9e499e43ce52b04f4ba6`  
		Last Modified: Thu, 11 Apr 2024 23:06:02 GMT  
		Size: 36.7 MB (36700889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03df793315cfbd9e5d5ee7d84c2d5dac2c4ebe774463c52eefc1fb50d48df413`  
		Last Modified: Thu, 11 Apr 2024 23:05:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:0554ae58e67a53a32f7af2872d5f74aca2d7ec967946ba4345b95fe9e3bea2ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938e00aeb9b6705aed9bbb1f8d81b3a92a29003f176428ed3614764769d9fd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:42:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:42:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:42:10 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:42:10 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:42:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:50e55c64a74695c6158dabaa3b27d45e64f228e132a7eb4d192462c6ba2f5591`  
		Last Modified: Fri, 12 Apr 2024 06:43:45 GMT  
		Size: 39.8 MB (39759420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435cc6e849aff1c03d18fcddacb0924f0b87224cc6ebe2fee32e3e45b28ffcd2`  
		Last Modified: Fri, 12 Apr 2024 06:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5d57d565ce4f25e74dbfc998a3f8de1af92daddb7c06c4d544448144e84e2ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:v2.11-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:871d1af1df46bdda93b932b6e0770fc3d2b7f359951ee4fb54c89659ed5fa03c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206777082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4accfc3034b31010b1f4989d82f4d5174cbe809ffab2144ac826438135d8e7dd`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:21:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:21:48 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:21:49 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:21:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3b0a68a91dddfdc645b9de3f12d157f1dfed7d4edb4bbe9d1cc59545560584c4`  
		Last Modified: Thu, 11 Apr 2024 21:23:59 GMT  
		Size: 42.3 MB (42343526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1184798168b8404b4fda09ac4d335419be9a2059ada2596ca580be1657d126`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc12a18bfcd6781649c9a02cf80cf3ce12e46e04a341287dc41d81892b16aab4`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6b6d4310ace0ce7630667449f47ad3c2d8289df90035f2f938905e65bbdcf`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:687a1167833ca51063a6df2a2ec1f1280db747e8df4a6039d8401d8d985b6076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:b18fb55ced49ba23d4385c70fc8000daca16763cdabf7ba902de16f14f6b85bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041715577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65367681edbfa0e5830a00186c79eeff6a82400a1c199c163d28daff7a57935`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:20:01 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:20:01 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a38a6ed2f2919e4d3a456722f80f2cc5189317b5f8206a1800abf8e4e2c340ee`  
		Last Modified: Thu, 11 Apr 2024 21:23:32 GMT  
		Size: 42.3 MB (42336305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a694512e13f4ca5ec422cca0abc98c942d10cd38b7bd4065ec2953da84ed12`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956c9331d98b50bab5553b6539c0754d2dd6caa97629e82c9ee54eb1c96d19f9`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38013d67d8e0708d512269850d6bf12744eb70848f1564ec713004271262a24d`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.2`

```console
$ docker pull traefik@sha256:c6f6001dd1fc09fb0ae47ad2198102c40a8d9586c02d6040d561fd4fb7e91f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v2.11.2` - linux; amd64

```console
$ docker pull traefik@sha256:c0577b65f0800c7be7e9b651917f22cda98cc2cca4167e546936a26dfe016aa1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44867579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbe0021cb966a1eaeffb1cd79f490edb9a9b90a129f32f2caddf3764f70417a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:34 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:34 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:34 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:34 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:34770c1f816cac86b87c016e6cb4b72caea0eea51842af9870f2eecb35a4c7e8`  
		Last Modified: Fri, 12 Apr 2024 00:20:17 GMT  
		Size: 40.8 MB (40838856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ea386b2b17283914c6ebe44480fe40ee91b08c0a9ddc27bb7b8f097bfbceef`  
		Last Modified: Fri, 12 Apr 2024 00:20:10 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0c7165daad921ed6b75c1cef1b5831d220ab3c0a750fb7be0e27e4566d4f3b95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42187860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0061acd2b3cdd995fc3287002e485c024cfb0fadbd88c0f2798fef0284afa3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:54 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:54 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:deca64fcf678c659625190e96315652a3ef578e7fffd5c87242fbac7be415b6f`  
		Last Modified: Thu, 11 Apr 2024 22:16:35 GMT  
		Size: 38.4 MB (38401093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d971034897344b507410608ec8a5570229d17c7a20fdcd21362791f5931e1209`  
		Last Modified: Thu, 11 Apr 2024 22:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4bc25533b4285a21d9b604585f9f885c6266ce8cde580d71c73d5898225c7ff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41728821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8797b64f9893a7c58cb49ad999a05cf9dfa9ad6522dc8d3a6ebb9508ad5e8c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:42 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:43 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:43 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:43 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:43 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a137a48e42fc346d8bf6dbd1e65022475f8f3e76a940d792928975bb13213d4e`  
		Last Modified: Fri, 12 Apr 2024 00:36:19 GMT  
		Size: 37.8 MB (37757985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44edc1b33556d0d40eb96f6fbb5f49c61fbc4bdc81fbeb6eb8adb7d802005633`  
		Last Modified: Fri, 12 Apr 2024 00:36:15 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.2` - linux; ppc64le

```console
$ docker pull traefik@sha256:73f9d90421d5b14c9e31ad0ab396c3b8a7b945e5bd2a55cd7fb326fb156a14eb
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40682778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb0a0cfaa13df8808d9d297e37f44e92dcaea892411eefaee5557a5547bf356`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:16 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:18 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:18 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:19 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:19 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:6c0d6d632c3f66f7fe17cfdb8fa5895a4e52750e521c9e499e43ce52b04f4ba6`  
		Last Modified: Thu, 11 Apr 2024 23:06:02 GMT  
		Size: 36.7 MB (36700889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03df793315cfbd9e5d5ee7d84c2d5dac2c4ebe774463c52eefc1fb50d48df413`  
		Last Modified: Thu, 11 Apr 2024 23:05:56 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v2.11.2` - linux; s390x

```console
$ docker pull traefik@sha256:0554ae58e67a53a32f7af2872d5f74aca2d7ec967946ba4345b95fe9e3bea2ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938e00aeb9b6705aed9bbb1f8d81b3a92a29003f176428ed3614764769d9fd0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:42:08 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:42:10 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:42:10 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:42:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:42:10 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:42:10 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:50e55c64a74695c6158dabaa3b27d45e64f228e132a7eb4d192462c6ba2f5591`  
		Last Modified: Fri, 12 Apr 2024 06:43:45 GMT  
		Size: 39.8 MB (39759420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435cc6e849aff1c03d18fcddacb0924f0b87224cc6ebe2fee32e3e45b28ffcd2`  
		Last Modified: Fri, 12 Apr 2024 06:43:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.2-windowsservercore-1809`

```console
$ docker pull traefik@sha256:5d57d565ce4f25e74dbfc998a3f8de1af92daddb7c06c4d544448144e84e2ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:v2.11.2-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:871d1af1df46bdda93b932b6e0770fc3d2b7f359951ee4fb54c89659ed5fa03c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206777082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4accfc3034b31010b1f4989d82f4d5174cbe809ffab2144ac826438135d8e7dd`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:21:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:21:48 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:21:49 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:21:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3b0a68a91dddfdc645b9de3f12d157f1dfed7d4edb4bbe9d1cc59545560584c4`  
		Last Modified: Thu, 11 Apr 2024 21:23:59 GMT  
		Size: 42.3 MB (42343526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1184798168b8404b4fda09ac4d335419be9a2059ada2596ca580be1657d126`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc12a18bfcd6781649c9a02cf80cf3ce12e46e04a341287dc41d81892b16aab4`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6b6d4310ace0ce7630667449f47ad3c2d8289df90035f2f938905e65bbdcf`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:687a1167833ca51063a6df2a2ec1f1280db747e8df4a6039d8401d8d985b6076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:v2.11.2-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:b18fb55ced49ba23d4385c70fc8000daca16763cdabf7ba902de16f14f6b85bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041715577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65367681edbfa0e5830a00186c79eeff6a82400a1c199c163d28daff7a57935`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:20:01 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:20:01 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a38a6ed2f2919e4d3a456722f80f2cc5189317b5f8206a1800abf8e4e2c340ee`  
		Last Modified: Thu, 11 Apr 2024 21:23:32 GMT  
		Size: 42.3 MB (42336305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a694512e13f4ca5ec422cca0abc98c942d10cd38b7bd4065ec2953da84ed12`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956c9331d98b50bab5553b6539c0754d2dd6caa97629e82c9ee54eb1c96d19f9`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38013d67d8e0708d512269850d6bf12744eb70848f1564ec713004271262a24d`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0`

```console
$ docker pull traefik@sha256:7138e0a962d4fd9dc7c6389ded6846faa63fc2e45605330224d07bdb8caff7b1
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
$ docker pull traefik@sha256:811bbf1194cc52d236a473e917a0aee3f528e2f79f5833c74b48a9bfca2ddb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45277036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcff26917f9848748f3eed01731a6251205f485c34c69cc657a6f1821e957d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:26 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:26 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:42c4476942763ad3acd156d084a6011f3ec9538f7f0bd06ee1b54ea651ecdfd3`  
		Last Modified: Fri, 12 Apr 2024 00:19:55 GMT  
		Size: 41.2 MB (41248314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a6ff87b7d1c9c00a294b40b2af6131149970a6845b438bfb94a7798cd728df`  
		Last Modified: Fri, 12 Apr 2024 00:19:48 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0ca78a7bfcfaa4b4b962ca8198d7cd718f999490eee95176b3126abdc0acb631
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42490608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b68cf3460b1aff598f3904b330fe77f9290a78809785c8c6dc655b8fb96df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:46 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:46 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:c4e1eaacb3adb0332f0bd4ae4ee8ffe2cdd1bd80a2d7158a2b0a0e074be8a8e4`  
		Last Modified: Thu, 11 Apr 2024 22:16:14 GMT  
		Size: 38.7 MB (38703841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bdd6895ca4693d1a62fb4acd8baeb1ea5e6cfc930de09fa08cc23a6ccaf1b9`  
		Last Modified: Thu, 11 Apr 2024 22:16:07 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f1ddb043d3389732070023942cee9af0c4e2af84f92fb93c986e381dd861a14a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42138445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe93f715ec4ec96091012f395a26084e26927a4564ccf8e346bd96939b22c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:36 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:36 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:906ac0d7801aef2db2bb0c095bec3e7d6b41315f531000d6afe70505cea778d8`  
		Last Modified: Fri, 12 Apr 2024 00:36:00 GMT  
		Size: 38.2 MB (38167609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf09b12869a3f35bf9bf4d2c6472ab2ec43091b612174bb3b2b16a761a2e1a70`  
		Last Modified: Fri, 12 Apr 2024 00:35:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; ppc64le

```console
$ docker pull traefik@sha256:f95456451595948a332eec78d79092e8765e23edf00b3d037fa61e9a2d4a7607
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40991951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdb1bbea94694699731c1a9fd8d11a8dc3c39a1dd5bb49b0bf796d9c81b0d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:06 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:07 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a0c88713362d99d5028e665ae366ab1e963d5d2e92db4fcb9fa06e0517b0ae2f`  
		Last Modified: Thu, 11 Apr 2024 23:05:41 GMT  
		Size: 37.0 MB (37010062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5bf9f1638add89e28a3fe9df71add265483c883e1aadbb132835e672443652`  
		Last Modified: Thu, 11 Apr 2024 23:05:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0` - linux; s390x

```console
$ docker pull traefik@sha256:6210e091220dfd6b3b4a652e0909ddbbd0871054725dc3ea1e21b944b9cf076a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43897663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8619facbd82bb64ddb383e80f31d13eaa7e223eb3c21b287781c6a7ac5bda4a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:41:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:41:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:41:02 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:41:03 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:41:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d548252488ee7f731d13613eabb54583823befa4eb28774874cc3274da346d28`  
		Last Modified: Fri, 12 Apr 2024 06:43:28 GMT  
		Size: 40.0 MB (40033646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc937e642c6d4639ae3f93e9954ea1e90235e741f95e779d3f06f710617a611`  
		Last Modified: Fri, 12 Apr 2024 06:43:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-1809`

```console
$ docker pull traefik@sha256:97586d9a8a9db5f083de589b53dffbf8e436157bc8cc472fad3cc970051fc618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:v3.0-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:9047bddb7042f6a473bce099f717ee8e4b3afbfc6e5badcb2df7f10ba9f25c57
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b3bf18198ea0ee471f179e32368d15c01255fb14c3584839bd15f05692e5a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:19:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:19:13 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:19:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:19:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:51a3b8e9e274bbf363b9d0e073901c305443e40e2b0e2649f65da07a4d6dc581`  
		Last Modified: Thu, 11 Apr 2024 21:23:07 GMT  
		Size: 42.9 MB (42910903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f0d6e81290baec2a487b78551461710c2bab324308eba6c91050f74aa95879`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80aa336fd11f44b27038a0303eac3277ea18cbd9782d39d3bbeb2ffb3904db8b`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d7c6605e759ac002ed7705630608cce2f82bc7a3dc6c3691f8e181337b850`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8a1409c1139bff4179bc607456ee860a67a1985ffddf3217bb168c91a05de7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:v3.0-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:a23258d2869ea0d2aaa6b83f19b288d98300429670dfc94aaf6738c446d83c03
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042309262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25c53563fc535cea74aaa8e22d32cfa2fc889814114bdb8b61a98d2668f5cbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:16:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:16:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:16:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:16:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:db875a8b9343f6d61f6cbe5d89b252c72175cffde0b5a4d5d20a2304ea060388`  
		Last Modified: Thu, 11 Apr 2024 21:22:42 GMT  
		Size: 42.9 MB (42929981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4d452c27d55f73dc1a4477d30fd09267a202627ec82c61a82f6fbdb59d8a6f`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7a84505488da92902d96856c92e8dd39e57a00bfeba904b088192b945d1261`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bf9dd26cc7e4fd1b3422c528d78ee6da3b248e99ce70f379f5cb6a62ce4892`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc5`

```console
$ docker pull traefik@sha256:7138e0a962d4fd9dc7c6389ded6846faa63fc2e45605330224d07bdb8caff7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `traefik:v3.0.0-rc5` - linux; amd64

```console
$ docker pull traefik@sha256:811bbf1194cc52d236a473e917a0aee3f528e2f79f5833c74b48a9bfca2ddb8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45277036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbcff26917f9848748f3eed01731a6251205f485c34c69cc657a6f1821e957d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:19:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:19:26 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:19:26 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:19:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:19:26 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:19:26 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:42c4476942763ad3acd156d084a6011f3ec9538f7f0bd06ee1b54ea651ecdfd3`  
		Last Modified: Fri, 12 Apr 2024 00:19:55 GMT  
		Size: 41.2 MB (41248314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a6ff87b7d1c9c00a294b40b2af6131149970a6845b438bfb94a7798cd728df`  
		Last Modified: Fri, 12 Apr 2024 00:19:48 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0ca78a7bfcfaa4b4b962ca8198d7cd718f999490eee95176b3126abdc0acb631
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42490608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b68cf3460b1aff598f3904b330fe77f9290a78809785c8c6dc655b8fb96df5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 22:15:45 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 22:15:46 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 22:15:46 GMT
EXPOSE 80
# Thu, 11 Apr 2024 22:15:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 22:15:46 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 22:15:46 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:c4e1eaacb3adb0332f0bd4ae4ee8ffe2cdd1bd80a2d7158a2b0a0e074be8a8e4`  
		Last Modified: Thu, 11 Apr 2024 22:16:14 GMT  
		Size: 38.7 MB (38703841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bdd6895ca4693d1a62fb4acd8baeb1ea5e6cfc930de09fa08cc23a6ccaf1b9`  
		Last Modified: Thu, 11 Apr 2024 22:16:07 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:f1ddb043d3389732070023942cee9af0c4e2af84f92fb93c986e381dd861a14a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42138445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe93f715ec4ec96091012f395a26084e26927a4564ccf8e346bd96939b22c44f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 00:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 00:35:35 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 00:35:36 GMT
EXPOSE 80
# Fri, 12 Apr 2024 00:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 00:35:36 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 00:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:906ac0d7801aef2db2bb0c095bec3e7d6b41315f531000d6afe70505cea778d8`  
		Last Modified: Fri, 12 Apr 2024 00:36:00 GMT  
		Size: 38.2 MB (38167609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf09b12869a3f35bf9bf4d2c6472ab2ec43091b612174bb3b2b16a761a2e1a70`  
		Last Modified: Fri, 12 Apr 2024 00:35:56 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc5` - linux; ppc64le

```console
$ docker pull traefik@sha256:f95456451595948a332eec78d79092e8765e23edf00b3d037fa61e9a2d4a7607
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (40991951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdb1bbea94694699731c1a9fd8d11a8dc3c39a1dd5bb49b0bf796d9c81b0d58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 23:05:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 23:05:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 23:05:06 GMT
EXPOSE 80
# Thu, 11 Apr 2024 23:05:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 23:05:07 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 23:05:07 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a0c88713362d99d5028e665ae366ab1e963d5d2e92db4fcb9fa06e0517b0ae2f`  
		Last Modified: Thu, 11 Apr 2024 23:05:41 GMT  
		Size: 37.0 MB (37010062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5bf9f1638add89e28a3fe9df71add265483c883e1aadbb132835e672443652`  
		Last Modified: Thu, 11 Apr 2024 23:05:35 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:v3.0.0-rc5` - linux; s390x

```console
$ docker pull traefik@sha256:6210e091220dfd6b3b4a652e0909ddbbd0871054725dc3ea1e21b944b9cf076a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43897663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8619facbd82bb64ddb383e80f31d13eaa7e223eb3c21b287781c6a7ac5bda4a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Fri, 12 Apr 2024 06:41:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Fri, 12 Apr 2024 06:41:02 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Fri, 12 Apr 2024 06:41:02 GMT
EXPOSE 80
# Fri, 12 Apr 2024 06:41:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Apr 2024 06:41:03 GMT
CMD ["traefik"]
# Fri, 12 Apr 2024 06:41:03 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d548252488ee7f731d13613eabb54583823befa4eb28774874cc3274da346d28`  
		Last Modified: Fri, 12 Apr 2024 06:43:28 GMT  
		Size: 40.0 MB (40033646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc937e642c6d4639ae3f93e9954ea1e90235e741f95e779d3f06f710617a611`  
		Last Modified: Fri, 12 Apr 2024 06:43:21 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc5-windowsservercore-1809`

```console
$ docker pull traefik@sha256:97586d9a8a9db5f083de589b53dffbf8e436157bc8cc472fad3cc970051fc618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:v3.0.0-rc5-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:9047bddb7042f6a473bce099f717ee8e4b3afbfc6e5badcb2df7f10ba9f25c57
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207344488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b3bf18198ea0ee471f179e32368d15c01255fb14c3584839bd15f05692e5a`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:19:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:19:13 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:19:14 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:19:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:51a3b8e9e274bbf363b9d0e073901c305443e40e2b0e2649f65da07a4d6dc581`  
		Last Modified: Thu, 11 Apr 2024 21:23:07 GMT  
		Size: 42.9 MB (42910903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f0d6e81290baec2a487b78551461710c2bab324308eba6c91050f74aa95879`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80aa336fd11f44b27038a0303eac3277ea18cbd9782d39d3bbeb2ffb3904db8b`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976d7c6605e759ac002ed7705630608cce2f82bc7a3dc6c3691f8e181337b850`  
		Last Modified: Thu, 11 Apr 2024 21:22:58 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.0.0-rc5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:8a1409c1139bff4179bc607456ee860a67a1985ffddf3217bb168c91a05de7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:v3.0.0-rc5-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:a23258d2869ea0d2aaa6b83f19b288d98300429670dfc94aaf6738c446d83c03
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2042309262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25c53563fc535cea74aaa8e22d32cfa2fc889814114bdb8b61a98d2668f5cbf`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:16:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.0.0-rc5/traefik_v3.0.0-rc5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:16:54 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:16:55 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:16:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.0.0-rc5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:db875a8b9343f6d61f6cbe5d89b252c72175cffde0b5a4d5d20a2304ea060388`  
		Last Modified: Thu, 11 Apr 2024 21:22:42 GMT  
		Size: 42.9 MB (42929981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4d452c27d55f73dc1a4477d30fd09267a202627ec82c61a82f6fbdb59d8a6f`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7a84505488da92902d96856c92e8dd39e57a00bfeba904b088192b945d1261`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16bf9dd26cc7e4fd1b3422c528d78ee6da3b248e99ce70f379f5cb6a62ce4892`  
		Last Modified: Thu, 11 Apr 2024 21:22:33 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:5d57d565ce4f25e74dbfc998a3f8de1af92daddb7c06c4d544448144e84e2ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull traefik@sha256:871d1af1df46bdda93b932b6e0770fc3d2b7f359951ee4fb54c89659ed5fa03c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206777082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4accfc3034b31010b1f4989d82f4d5174cbe809ffab2144ac826438135d8e7dd`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:21:47 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:21:48 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:21:49 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:21:49 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:3b0a68a91dddfdc645b9de3f12d157f1dfed7d4edb4bbe9d1cc59545560584c4`  
		Last Modified: Thu, 11 Apr 2024 21:23:59 GMT  
		Size: 42.3 MB (42343526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1184798168b8404b4fda09ac4d335419be9a2059ada2596ca580be1657d126`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc12a18bfcd6781649c9a02cf80cf3ce12e46e04a341287dc41d81892b16aab4`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d6b6d4310ace0ce7630667449f47ad3c2d8289df90035f2f938905e65bbdcf`  
		Last Modified: Thu, 11 Apr 2024 21:23:50 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:687a1167833ca51063a6df2a2ec1f1280db747e8df4a6039d8401d8d985b6076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull traefik@sha256:b18fb55ced49ba23d4385c70fc8000daca16763cdabf7ba902de16f14f6b85bf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2041715577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65367681edbfa0e5830a00186c79eeff6a82400a1c199c163d28daff7a57935`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Apr 2024 21:20:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.2/traefik_v2.11.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Thu, 11 Apr 2024 21:20:01 GMT
EXPOSE 80
# Thu, 11 Apr 2024 21:20:01 GMT
ENTRYPOINT ["/traefik"]
# Thu, 11 Apr 2024 21:20:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:a38a6ed2f2919e4d3a456722f80f2cc5189317b5f8206a1800abf8e4e2c340ee`  
		Last Modified: Thu, 11 Apr 2024 21:23:32 GMT  
		Size: 42.3 MB (42336305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a694512e13f4ca5ec422cca0abc98c942d10cd38b7bd4065ec2953da84ed12`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956c9331d98b50bab5553b6539c0754d2dd6caa97629e82c9ee54eb1c96d19f9`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38013d67d8e0708d512269850d6bf12744eb70848f1564ec713004271262a24d`  
		Last Modified: Thu, 11 Apr 2024 21:23:23 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
