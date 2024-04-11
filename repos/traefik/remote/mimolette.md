## `traefik:mimolette`

```console
$ docker pull traefik@sha256:799276a30d994de8e8211aca14e7f9a775062e99eddd30b552e8ef00c0d62552
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
$ docker pull traefik@sha256:0ccd4d8fb7dd82324563cc9260c208779523b709eb2e2881b560ca6afff7a51a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44866475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc12b4a7ccda78ab86c73c09b41f24215929eee38aabdab8911b1a70aa8cf81c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:02:11 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 10 Apr 2024 20:54:05 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.1/traefik_v2.11.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 10 Apr 2024 20:54:06 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 10 Apr 2024 20:54:06 GMT
EXPOSE 80
# Wed, 10 Apr 2024 20:54:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 20:54:06 GMT
CMD ["traefik"]
# Wed, 10 Apr 2024 20:54:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:820ebb7891219aee312a3c13f673125cb402b1a379f6f0f3443f674d51e27f88`  
		Last Modified: Wed, 10 Apr 2024 20:54:45 GMT  
		Size: 40.8 MB (40837752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ebbbf54a51e5bc675a5a8519a4cb6ba004b31e034dd7664d7ead940e21e91e`  
		Last Modified: Wed, 10 Apr 2024 20:54:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:7cc48798a6458fff2020a9e5f1d310eb7c5cdb35d3c84a4cab872471e61c90d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42190305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d7db9664d62a56e47ce8f314708651d91b1ea99db775a2f9685b83ffb5a509`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:38:01 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 10 Apr 2024 20:35:48 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.1/traefik_v2.11.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 10 Apr 2024 20:35:48 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 10 Apr 2024 20:35:48 GMT
EXPOSE 80
# Wed, 10 Apr 2024 20:35:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 20:35:48 GMT
CMD ["traefik"]
# Wed, 10 Apr 2024 20:35:48 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:f7d37aab4bb59a3a820e6519e8b2551f7dec66b9edac174645dbbdd6063e2b0b`  
		Last Modified: Wed, 10 Apr 2024 20:36:29 GMT  
		Size: 38.4 MB (38403538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656bf21e62be399083b383ed3c85eccfdd93ecddc588593c19409d57f4f8c6d9`  
		Last Modified: Wed, 10 Apr 2024 20:36:22 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:33cfe52013bc7fe386e15e389b8886baca457e4adbe5d0711838a2761528b22b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41736633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2eac9c463b1ff6c6b41278700a62a51edc8713700c81859bf8c86dc8f5ef30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:43:26 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 10 Apr 2024 18:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.1/traefik_v2.11.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 10 Apr 2024 18:39:15 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 10 Apr 2024 18:39:15 GMT
EXPOSE 80
# Wed, 10 Apr 2024 18:39:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 18:39:15 GMT
CMD ["traefik"]
# Wed, 10 Apr 2024 18:39:15 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:5386a698d198ee1a091203cf716ce9bdaecce2c6478b7140a84b49e07ff08c4d`  
		Last Modified: Wed, 10 Apr 2024 18:39:51 GMT  
		Size: 37.8 MB (37765796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb2d57c27815bae641aa9476350886b2d70e9e8ee5e7729ddf0efb2c4ffebad`  
		Last Modified: Wed, 10 Apr 2024 18:39:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:5976fa97ee1a966cdc3c21a76881d725fe5df7005f9cc9069972ed34504a9e2e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40678393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad51ebcabae1fddea5d031e4ecef7b220218bf70b708782f9df66f3e72a90c7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 07:09:34 GMT
RUN apk --no-cache add ca-certificates tzdata
# Wed, 10 Apr 2024 18:52:11 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.1/traefik_v2.11.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Wed, 10 Apr 2024 18:52:13 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Wed, 10 Apr 2024 18:52:13 GMT
EXPOSE 80
# Wed, 10 Apr 2024 18:52:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 18:52:14 GMT
CMD ["traefik"]
# Wed, 10 Apr 2024 18:52:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:d0e10162fedd9a084eccbefa870e812d1055ff9f642bc29f240c578d71159cf9`  
		Last Modified: Wed, 10 Apr 2024 18:52:58 GMT  
		Size: 36.7 MB (36696504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e9f6277682bfe1b56665d918759170e0438e988af393943d4d0bee0dc3ed10`  
		Last Modified: Wed, 10 Apr 2024 18:52:52 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:f2c02bcba3cd516fa963e26b29f292f8414287440e3b1052a10e2e7c5e28b4b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43622309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1c438ef6c193136aa13482e24483e1710eb5df576bf405228f066b5428061b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 22:53:57 GMT
RUN apk --no-cache add ca-certificates tzdata
# Thu, 11 Apr 2024 04:15:46 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.1/traefik_v2.11.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik
# Thu, 11 Apr 2024 04:15:50 GMT
COPY file:59a219a1fb7a9dc894a7a9a4718fa97fd24adb0a4a6455240ec2ab0183da796e in / 
# Thu, 11 Apr 2024 04:15:50 GMT
EXPOSE 80
# Thu, 11 Apr 2024 04:15:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Apr 2024 04:15:51 GMT
CMD ["traefik"]
# Thu, 11 Apr 2024 04:15:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.1 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dd7790e7416b6d76ace01b5876ae359b981d2191a6cafd87bb979259a3b7f4d6`  
		Last Modified: Thu, 11 Apr 2024 04:17:39 GMT  
		Size: 39.8 MB (39758292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0faadcb56ee12dac8cac351a6868f437a71ffe2adc0394f7273fb9615662dd6d`  
		Last Modified: Thu, 11 Apr 2024 04:17:32 GMT  
		Size: 368.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
