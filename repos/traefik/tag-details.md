<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.33`](#traefik21133)
-	[`traefik:2.11.33-nanoserver-ltsc2022`](#traefik21133-nanoserver-ltsc2022)
-	[`traefik:2.11.33-windowsservercore-ltsc2022`](#traefik21133-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.6`](#traefik36)
-	[`traefik:3.6-nanoserver-ltsc2022`](#traefik36-nanoserver-ltsc2022)
-	[`traefik:3.6-windowsservercore-ltsc2022`](#traefik36-windowsservercore-ltsc2022)
-	[`traefik:3.6.5`](#traefik365)
-	[`traefik:3.6.5-nanoserver-ltsc2022`](#traefik365-nanoserver-ltsc2022)
-	[`traefik:3.6.5-windowsservercore-ltsc2022`](#traefik365-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:ramequin`](#traefikramequin)
-	[`traefik:ramequin-nanoserver-ltsc2022`](#traefikramequin-nanoserver-ltsc2022)
-	[`traefik:ramequin-windowsservercore-ltsc2022`](#traefikramequin-windowsservercore-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.33`](#traefikv21133)
-	[`traefik:v2.11.33-nanoserver-ltsc2022`](#traefikv21133-nanoserver-ltsc2022)
-	[`traefik:v2.11.33-windowsservercore-ltsc2022`](#traefikv21133-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.6`](#traefikv36)
-	[`traefik:v3.6-nanoserver-ltsc2022`](#traefikv36-nanoserver-ltsc2022)
-	[`traefik:v3.6-windowsservercore-ltsc2022`](#traefikv36-windowsservercore-ltsc2022)
-	[`traefik:v3.6.5`](#traefikv365)
-	[`traefik:v3.6.5-nanoserver-ltsc2022`](#traefikv365-nanoserver-ltsc2022)
-	[`traefik:v3.6.5-windowsservercore-ltsc2022`](#traefikv365-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:bb58a3046a925d974492f2a8d12af98b44a7ed039a46d3ade1ecf470a1af96c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2` - linux; amd64

```console
$ docker pull traefik@sha256:c9fc23758d3c09b5a8e97d5afc74f9affdcea35b49ebefa090c282cb7221e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0585c0174ce35e3b51078255df8c4bbf032a035b0bcd5d1f314fb74fb55eab74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:37 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5dae0d1940727b42d867b3209f02853f05720dde47a7ebe329f56c9e9b0a6`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 461.0 KB (460954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6168cb646a25a9cdc453b74cee1ce0858ec81602ff2cfe610d622162b897d`  
		Last Modified: Thu, 18 Dec 2025 00:38:12 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5121841f894ebf472fa208d1a3c2158dff03e65340dd3aa9ca29d379a4c114`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:ff5b79b15bf36250a2b4d4a7e21f10fd2075edb6035fc49a4580df6b1c1e482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e14b576062789d9f0b20eab9a463af99072602efef98ca3c0532e6e802a8d57`

```dockerfile
```

-	Layers:
	-	`sha256:767001a8883a7256101f6053ced15623e6200632343b45f1c4d535dae99034ab`  
		Last Modified: Thu, 18 Dec 2025 04:10:22 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b4654225acf7ee725ad1e861e54707caf6a0f7b38342f30cb04e7fe6e7ca11`  
		Last Modified: Thu, 18 Dec 2025 04:10:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4181c5fe1ea8dc7ca3d5bd4efbeff33e4288f669efbdfe57bbfb441bb4b99e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46823436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f44a3f50e52a4af869b39f3519d4f7a813621ccf6cacaeca4f6f3ef1f58435a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:48:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:25 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99378ff454de63b469978df2985803a8e574cfce746e9d83301f346b5044a5`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 461.5 KB (461451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138af728689bca4742d064a55f10930ef5d41f1cc001781ead4e4886d37cf66`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 42.8 MB (42793183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eb3473fb57831f0f13eaf728f113e93b369c0f9af26cf847850b4702c3902`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:30e4b7212f3765ed5e6d0b3d6d73e001f7b8bbac70ff4f80f1ef26eca3ffaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d2eb8ff0453823b8981f577b25c7d753978339866bf218313b238f19ef3b61`

```dockerfile
```

-	Layers:
	-	`sha256:b4f767790f9de664313048666f47024a86f9b276460c25673bc955d3a8e926d5`  
		Last Modified: Thu, 18 Dec 2025 04:10:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e51f93db0b17a2799c4581ecc42068bf6be4db36cdb96bde0491a39a600ec8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47294537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4c8495d19cd8540489695b630af9528dfb871f126428bf99d35a3be551b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:13 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73d6207c60aa10764a3ad0a664af3927b67597708348546560d24423427f959`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 42.6 MB (42635437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:734fe12d7bbe3eae7fdccb4b0bd7e7d28255eb03dc3931ce4a4144ca37f48918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be3d743f60cd5458a039660f04b83e61c36c41a994af175343602dd8490ea52`

```dockerfile
```

-	Layers:
	-	`sha256:783980b78710a6ea627cc4077b6fa5f7c377072ab916b55c4ccc415d16c06ba3`  
		Last Modified: Thu, 18 Dec 2025 04:10:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ba5a3551ae835ee366268051563035196c2072c6fd30c6e16596648483adda`  
		Last Modified: Thu, 18 Dec 2025 04:10:31 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:e32646c5052b0b611abb6be173532babb39d9260d1656f5084292db768e9cde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e6a4256c2946e32447aef8d2fc7707b682e62abfd2127e868d6734bf50c749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:36 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336300a7f5c554abee8386b767558f3bed8e7e1873062b733786765afdfdb99`  
		Last Modified: Thu, 18 Dec 2025 01:36:43 GMT  
		Size: 41.0 MB (40954982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10abf6cd1b69fb8c8a781b1420ea66868819194edacfd9f4b6795bf05e7efe5a`  
		Last Modified: Thu, 18 Dec 2025 01:36:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:eef8876bc857d08591fa49e46bec2152776718308c2a050b4c9e177df0963e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc23fba13ce49c6157ec521bd500da5ba721bae0d13118467da73738757d057e`

```dockerfile
```

-	Layers:
	-	`sha256:3afe5038e133ffab4adc253f337b1387bda92f29879d62cf0a57114690dc6d91`  
		Last Modified: Thu, 18 Dec 2025 04:10:34 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f6e730ee53229408d94802908716057a1850445d052d79dcda628c0a43d735`  
		Last Modified: Thu, 18 Dec 2025 04:10:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:30200fce5beb9e08c163b7810d2f6a5cb39bdca59fa5c7dbd5c0ba8ea1118568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49866d8a8721443b1a603b69899b0b953093c961da1c0d66d5df848afc0a7bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:42:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:42:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:42:27 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:42:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc13f83f0b87c8557a5b2154a47f0c9d974c15360754ead5af8dec5373f168`  
		Last Modified: Fri, 19 Dec 2025 05:47:33 GMT  
		Size: 45.3 MB (45323997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:7c7a13552833efd30b342c5b39ca3f44c7917da4354a3f504670f8be108d56e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69666deb1f6675c10e964a5a034e182641f4f42f9b1935e62d0b63bc8429d9f7`

```dockerfile
```

-	Layers:
	-	`sha256:2f8e08eafe1d8dc4b499f0ecc58ed54fa9254b1260499e706122d624a0689a94`  
		Last Modified: Fri, 19 Dec 2025 07:09:34 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c8d65b1207194a9024719e430b4b5c8e214f1301638e711a5df7d8c2585c47`  
		Last Modified: Fri, 19 Dec 2025 07:09:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:ddeda4089a26193575342c0931fb5762e4384c278102e3d956787cde673f951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e74521b9b925a71802c35cb1346284ecb7854c5f1963dd2724b6012f5e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:13:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:13:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:13:16 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:13:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d3f44e94737924cc971968c6169a7c7cfba62480b0e4b85c7491f35d93056`  
		Last Modified: Thu, 18 Dec 2025 01:14:30 GMT  
		Size: 45.3 MB (45254483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb6a157453d8b40c1eb2e3e0e99878463b56964abd0e9a925eedd6dc5ef51c7`  
		Last Modified: Thu, 18 Dec 2025 01:14:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:62bc10d9dbe1507cc836c7b43bafddfd84c64436c5200234ed9768dc9a4c5aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce641443c0ab290b21691e235a0addcf69be0b9f2182e2bf82b179bed6791b91`

```dockerfile
```

-	Layers:
	-	`sha256:fb849482243a1f3d0956b740762e64b0d8ca1a29d33e4a2e3c96a85fbbf249b2`  
		Last Modified: Thu, 18 Dec 2025 04:10:40 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9679fce549453252eb71fac70e8bae7e9aadc177074b8e27cec459239d8bce25`  
		Last Modified: Thu, 18 Dec 2025 04:10:41 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:bb58a3046a925d974492f2a8d12af98b44a7ed039a46d3ade1ecf470a1af96c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2.11` - linux; amd64

```console
$ docker pull traefik@sha256:c9fc23758d3c09b5a8e97d5afc74f9affdcea35b49ebefa090c282cb7221e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0585c0174ce35e3b51078255df8c4bbf032a035b0bcd5d1f314fb74fb55eab74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:37 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5dae0d1940727b42d867b3209f02853f05720dde47a7ebe329f56c9e9b0a6`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 461.0 KB (460954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6168cb646a25a9cdc453b74cee1ce0858ec81602ff2cfe610d622162b897d`  
		Last Modified: Thu, 18 Dec 2025 00:38:12 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5121841f894ebf472fa208d1a3c2158dff03e65340dd3aa9ca29d379a4c114`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:ff5b79b15bf36250a2b4d4a7e21f10fd2075edb6035fc49a4580df6b1c1e482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e14b576062789d9f0b20eab9a463af99072602efef98ca3c0532e6e802a8d57`

```dockerfile
```

-	Layers:
	-	`sha256:767001a8883a7256101f6053ced15623e6200632343b45f1c4d535dae99034ab`  
		Last Modified: Thu, 18 Dec 2025 04:10:22 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b4654225acf7ee725ad1e861e54707caf6a0f7b38342f30cb04e7fe6e7ca11`  
		Last Modified: Thu, 18 Dec 2025 04:10:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4181c5fe1ea8dc7ca3d5bd4efbeff33e4288f669efbdfe57bbfb441bb4b99e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46823436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f44a3f50e52a4af869b39f3519d4f7a813621ccf6cacaeca4f6f3ef1f58435a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:48:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:25 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99378ff454de63b469978df2985803a8e574cfce746e9d83301f346b5044a5`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 461.5 KB (461451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138af728689bca4742d064a55f10930ef5d41f1cc001781ead4e4886d37cf66`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 42.8 MB (42793183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eb3473fb57831f0f13eaf728f113e93b369c0f9af26cf847850b4702c3902`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:30e4b7212f3765ed5e6d0b3d6d73e001f7b8bbac70ff4f80f1ef26eca3ffaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d2eb8ff0453823b8981f577b25c7d753978339866bf218313b238f19ef3b61`

```dockerfile
```

-	Layers:
	-	`sha256:b4f767790f9de664313048666f47024a86f9b276460c25673bc955d3a8e926d5`  
		Last Modified: Thu, 18 Dec 2025 04:10:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e51f93db0b17a2799c4581ecc42068bf6be4db36cdb96bde0491a39a600ec8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47294537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4c8495d19cd8540489695b630af9528dfb871f126428bf99d35a3be551b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:13 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73d6207c60aa10764a3ad0a664af3927b67597708348546560d24423427f959`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 42.6 MB (42635437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:734fe12d7bbe3eae7fdccb4b0bd7e7d28255eb03dc3931ce4a4144ca37f48918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be3d743f60cd5458a039660f04b83e61c36c41a994af175343602dd8490ea52`

```dockerfile
```

-	Layers:
	-	`sha256:783980b78710a6ea627cc4077b6fa5f7c377072ab916b55c4ccc415d16c06ba3`  
		Last Modified: Thu, 18 Dec 2025 04:10:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ba5a3551ae835ee366268051563035196c2072c6fd30c6e16596648483adda`  
		Last Modified: Thu, 18 Dec 2025 04:10:31 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:e32646c5052b0b611abb6be173532babb39d9260d1656f5084292db768e9cde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e6a4256c2946e32447aef8d2fc7707b682e62abfd2127e868d6734bf50c749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:36 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336300a7f5c554abee8386b767558f3bed8e7e1873062b733786765afdfdb99`  
		Last Modified: Thu, 18 Dec 2025 01:36:43 GMT  
		Size: 41.0 MB (40954982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10abf6cd1b69fb8c8a781b1420ea66868819194edacfd9f4b6795bf05e7efe5a`  
		Last Modified: Thu, 18 Dec 2025 01:36:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:eef8876bc857d08591fa49e46bec2152776718308c2a050b4c9e177df0963e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc23fba13ce49c6157ec521bd500da5ba721bae0d13118467da73738757d057e`

```dockerfile
```

-	Layers:
	-	`sha256:3afe5038e133ffab4adc253f337b1387bda92f29879d62cf0a57114690dc6d91`  
		Last Modified: Thu, 18 Dec 2025 04:10:34 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f6e730ee53229408d94802908716057a1850445d052d79dcda628c0a43d735`  
		Last Modified: Thu, 18 Dec 2025 04:10:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:30200fce5beb9e08c163b7810d2f6a5cb39bdca59fa5c7dbd5c0ba8ea1118568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49866d8a8721443b1a603b69899b0b953093c961da1c0d66d5df848afc0a7bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:42:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:42:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:42:27 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:42:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc13f83f0b87c8557a5b2154a47f0c9d974c15360754ead5af8dec5373f168`  
		Last Modified: Fri, 19 Dec 2025 05:47:33 GMT  
		Size: 45.3 MB (45323997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7c7a13552833efd30b342c5b39ca3f44c7917da4354a3f504670f8be108d56e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69666deb1f6675c10e964a5a034e182641f4f42f9b1935e62d0b63bc8429d9f7`

```dockerfile
```

-	Layers:
	-	`sha256:2f8e08eafe1d8dc4b499f0ecc58ed54fa9254b1260499e706122d624a0689a94`  
		Last Modified: Fri, 19 Dec 2025 07:09:34 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c8d65b1207194a9024719e430b4b5c8e214f1301638e711a5df7d8c2585c47`  
		Last Modified: Fri, 19 Dec 2025 07:09:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:ddeda4089a26193575342c0931fb5762e4384c278102e3d956787cde673f951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e74521b9b925a71802c35cb1346284ecb7854c5f1963dd2724b6012f5e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:13:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:13:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:13:16 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:13:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d3f44e94737924cc971968c6169a7c7cfba62480b0e4b85c7491f35d93056`  
		Last Modified: Thu, 18 Dec 2025 01:14:30 GMT  
		Size: 45.3 MB (45254483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb6a157453d8b40c1eb2e3e0e99878463b56964abd0e9a925eedd6dc5ef51c7`  
		Last Modified: Thu, 18 Dec 2025 01:14:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:62bc10d9dbe1507cc836c7b43bafddfd84c64436c5200234ed9768dc9a4c5aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce641443c0ab290b21691e235a0addcf69be0b9f2182e2bf82b179bed6791b91`

```dockerfile
```

-	Layers:
	-	`sha256:fb849482243a1f3d0956b740762e64b0d8ca1a29d33e4a2e3c96a85fbbf249b2`  
		Last Modified: Thu, 18 Dec 2025 04:10:40 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9679fce549453252eb71fac70e8bae7e9aadc177074b8e27cec459239d8bce25`  
		Last Modified: Thu, 18 Dec 2025 04:10:41 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.33`

```console
$ docker pull traefik@sha256:bb58a3046a925d974492f2a8d12af98b44a7ed039a46d3ade1ecf470a1af96c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2.11.33` - linux; amd64

```console
$ docker pull traefik@sha256:c9fc23758d3c09b5a8e97d5afc74f9affdcea35b49ebefa090c282cb7221e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0585c0174ce35e3b51078255df8c4bbf032a035b0bcd5d1f314fb74fb55eab74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:37 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5dae0d1940727b42d867b3209f02853f05720dde47a7ebe329f56c9e9b0a6`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 461.0 KB (460954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6168cb646a25a9cdc453b74cee1ce0858ec81602ff2cfe610d622162b897d`  
		Last Modified: Thu, 18 Dec 2025 00:38:12 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5121841f894ebf472fa208d1a3c2158dff03e65340dd3aa9ca29d379a4c114`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:ff5b79b15bf36250a2b4d4a7e21f10fd2075edb6035fc49a4580df6b1c1e482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e14b576062789d9f0b20eab9a463af99072602efef98ca3c0532e6e802a8d57`

```dockerfile
```

-	Layers:
	-	`sha256:767001a8883a7256101f6053ced15623e6200632343b45f1c4d535dae99034ab`  
		Last Modified: Thu, 18 Dec 2025 04:10:22 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b4654225acf7ee725ad1e861e54707caf6a0f7b38342f30cb04e7fe6e7ca11`  
		Last Modified: Thu, 18 Dec 2025 04:10:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4181c5fe1ea8dc7ca3d5bd4efbeff33e4288f669efbdfe57bbfb441bb4b99e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46823436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f44a3f50e52a4af869b39f3519d4f7a813621ccf6cacaeca4f6f3ef1f58435a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:48:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:25 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99378ff454de63b469978df2985803a8e574cfce746e9d83301f346b5044a5`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 461.5 KB (461451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138af728689bca4742d064a55f10930ef5d41f1cc001781ead4e4886d37cf66`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 42.8 MB (42793183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eb3473fb57831f0f13eaf728f113e93b369c0f9af26cf847850b4702c3902`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:30e4b7212f3765ed5e6d0b3d6d73e001f7b8bbac70ff4f80f1ef26eca3ffaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d2eb8ff0453823b8981f577b25c7d753978339866bf218313b238f19ef3b61`

```dockerfile
```

-	Layers:
	-	`sha256:b4f767790f9de664313048666f47024a86f9b276460c25673bc955d3a8e926d5`  
		Last Modified: Thu, 18 Dec 2025 04:10:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e51f93db0b17a2799c4581ecc42068bf6be4db36cdb96bde0491a39a600ec8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47294537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4c8495d19cd8540489695b630af9528dfb871f126428bf99d35a3be551b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:13 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73d6207c60aa10764a3ad0a664af3927b67597708348546560d24423427f959`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 42.6 MB (42635437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:734fe12d7bbe3eae7fdccb4b0bd7e7d28255eb03dc3931ce4a4144ca37f48918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be3d743f60cd5458a039660f04b83e61c36c41a994af175343602dd8490ea52`

```dockerfile
```

-	Layers:
	-	`sha256:783980b78710a6ea627cc4077b6fa5f7c377072ab916b55c4ccc415d16c06ba3`  
		Last Modified: Thu, 18 Dec 2025 04:10:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ba5a3551ae835ee366268051563035196c2072c6fd30c6e16596648483adda`  
		Last Modified: Thu, 18 Dec 2025 04:10:31 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; ppc64le

```console
$ docker pull traefik@sha256:e32646c5052b0b611abb6be173532babb39d9260d1656f5084292db768e9cde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e6a4256c2946e32447aef8d2fc7707b682e62abfd2127e868d6734bf50c749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:36 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336300a7f5c554abee8386b767558f3bed8e7e1873062b733786765afdfdb99`  
		Last Modified: Thu, 18 Dec 2025 01:36:43 GMT  
		Size: 41.0 MB (40954982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10abf6cd1b69fb8c8a781b1420ea66868819194edacfd9f4b6795bf05e7efe5a`  
		Last Modified: Thu, 18 Dec 2025 01:36:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:eef8876bc857d08591fa49e46bec2152776718308c2a050b4c9e177df0963e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc23fba13ce49c6157ec521bd500da5ba721bae0d13118467da73738757d057e`

```dockerfile
```

-	Layers:
	-	`sha256:3afe5038e133ffab4adc253f337b1387bda92f29879d62cf0a57114690dc6d91`  
		Last Modified: Thu, 18 Dec 2025 04:10:34 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f6e730ee53229408d94802908716057a1850445d052d79dcda628c0a43d735`  
		Last Modified: Thu, 18 Dec 2025 04:10:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; riscv64

```console
$ docker pull traefik@sha256:30200fce5beb9e08c163b7810d2f6a5cb39bdca59fa5c7dbd5c0ba8ea1118568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49866d8a8721443b1a603b69899b0b953093c961da1c0d66d5df848afc0a7bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:42:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:42:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:42:27 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:42:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc13f83f0b87c8557a5b2154a47f0c9d974c15360754ead5af8dec5373f168`  
		Last Modified: Fri, 19 Dec 2025 05:47:33 GMT  
		Size: 45.3 MB (45323997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:7c7a13552833efd30b342c5b39ca3f44c7917da4354a3f504670f8be108d56e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69666deb1f6675c10e964a5a034e182641f4f42f9b1935e62d0b63bc8429d9f7`

```dockerfile
```

-	Layers:
	-	`sha256:2f8e08eafe1d8dc4b499f0ecc58ed54fa9254b1260499e706122d624a0689a94`  
		Last Modified: Fri, 19 Dec 2025 07:09:34 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c8d65b1207194a9024719e430b4b5c8e214f1301638e711a5df7d8c2585c47`  
		Last Modified: Fri, 19 Dec 2025 07:09:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.33` - linux; s390x

```console
$ docker pull traefik@sha256:ddeda4089a26193575342c0931fb5762e4384c278102e3d956787cde673f951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e74521b9b925a71802c35cb1346284ecb7854c5f1963dd2724b6012f5e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:13:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:13:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:13:16 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:13:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d3f44e94737924cc971968c6169a7c7cfba62480b0e4b85c7491f35d93056`  
		Last Modified: Thu, 18 Dec 2025 01:14:30 GMT  
		Size: 45.3 MB (45254483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb6a157453d8b40c1eb2e3e0e99878463b56964abd0e9a925eedd6dc5ef51c7`  
		Last Modified: Thu, 18 Dec 2025 01:14:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:62bc10d9dbe1507cc836c7b43bafddfd84c64436c5200234ed9768dc9a4c5aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce641443c0ab290b21691e235a0addcf69be0b9f2182e2bf82b179bed6791b91`

```dockerfile
```

-	Layers:
	-	`sha256:fb849482243a1f3d0956b740762e64b0d8ca1a29d33e4a2e3c96a85fbbf249b2`  
		Last Modified: Thu, 18 Dec 2025 04:10:40 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9679fce549453252eb71fac70e8bae7e9aadc177074b8e27cec459239d8bce25`  
		Last Modified: Thu, 18 Dec 2025 04:10:41 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.33-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11.33-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.33-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:2.11.33-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:67622638cd88dbfcfba40159bc652ecf0aea0e032f8a3c7e3134ae7c037b9910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3` - linux; amd64

```console
$ docker pull traefik@sha256:d944e3693bbf5a361ddd2e411bb713049cfb4f5ff3da200b30ee7a347dbd6abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb158a64eaac3b411525e180705dbb4e120d078150b6a795e120e6b80e81b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:33 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e627467d86762f7d43dc795a23361ae2c3f587d554d237f08e8b851a00bedd1`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489626b3f9620aab9962ec32de70229fb411c6304b6fa465f36501e2c9fb591`  
		Last Modified: Thu, 18 Dec 2025 00:38:13 GMT  
		Size: 47.5 MB (47508389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d82de1962f8aea587dc96507c61f4532e0492a7486c0464424909c9a287d4`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:04a3aa984984cc7e2e3063d865bf62b0f49d1c7ecb8aa1c3204717d38b115f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d3ff5908e1cdb4d0bff4368546e85af9f3da9117b657e2d14fcc7a8cc46df`

```dockerfile
```

-	Layers:
	-	`sha256:d974d7a987a8a2d1e72455e2e7281893be7e4de5980f6b05ef538d9525eac5ad`  
		Last Modified: Thu, 18 Dec 2025 04:10:44 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c127714cbcc3b651d10c37ff43afa00f119fb595dfa041cae741b5e6ed773`  
		Last Modified: Thu, 18 Dec 2025 04:10:45 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:088e42947073420f9ebde2eb5d8bab8f9181bca4aa2ce68489825f098bf8c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47125075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49ac065a809cf09a162068ca036c38f5628b53ce26a833f2a94cd2e5609fd9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:01 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f737350ac794161f26d63aadebc1bef9562e1b5145b8de73ef57db6afa0e07`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 461.4 KB (461443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bafdabef314d9c0aa348705c8e18f7c41ccaeb27138426e29133e0d94847`  
		Last Modified: Thu, 18 Dec 2025 00:48:24 GMT  
		Size: 43.1 MB (43094831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6064d2d82dbe21bc8205771bd41cf5fba61bc9662afdef68e431208574b3cb9`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:e1d5a37fc3d7604403838d16bd28b6aebecbc232f421cd887deb8b86d3ac022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b7b588d832edae2cc1791cf2822ed4e7ab9df8e0466a9b32ea438e42044a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2bbed655619f17a9a92d9c84e19b7bffd4d0ac0643f30961edf86b8fc64032f0`  
		Last Modified: Thu, 18 Dec 2025 04:10:49 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4df45c2d1101f440d989afb8d54ce557fda8c1028c63b4edb46e1387f20e252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73051e3972adbd5fd7ac7a30bf363b919b805fc5a85b0c184fecdc8aafc69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:14 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776aff3ebb03754e9132ac99fdd3d55913a018df4553600e28c9b49ccb9359d`  
		Last Modified: Thu, 18 Dec 2025 00:39:47 GMT  
		Size: 43.2 MB (43235898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:0235f3573f63d55abfba7e9261bf749903b82ceb1338599b1dad8a7457aaadda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31ba6077556b5e469a5042279cc8a5d05f7d569a572d96e0dee0eaa7bd8b32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8220b97c6c54a61453867e3810ee63c84d079615a999974bb4c1cad060c68b`  
		Last Modified: Thu, 18 Dec 2025 04:10:52 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d83b4e84773fd95b32005cacfcbf43bfc22a2454bf16bfb8fd74072b564c2b`  
		Last Modified: Thu, 18 Dec 2025 04:10:53 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:f1bb2c5a12839909a38cbf8956a86a7de79a037d555cc29f1ac5ee281cb394a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c62d1ceea76fe16ce12841e2c9bcfc6df89a0cefc88ced9f5775f0201b1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:34:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:30 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:34:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ae93456d87a4319c334c68d8fe973661c62477820d71cbe214b3e3cf1596`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 41.3 MB (41258571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf953c6ec94ddbc562a208b274133f72e6e82689b6a4b337026df0994d1f0`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:0c178d2363efe5881ba2974fd5e15298b184c9f8d5a796ddc386bae7933c6752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374a0d4f6058bebc837f4c842459d396c9e6019f0b7563916122e36541f2419`

```dockerfile
```

-	Layers:
	-	`sha256:12c32f74f9c3051a06ec488f6838aea96b398fdf6e4fc6b49e438432ea420060`  
		Last Modified: Thu, 18 Dec 2025 04:10:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe6e9400e9638d6fdbda5dc01ea957d910d9fc60572973c5dcd8fa3dfc53099`  
		Last Modified: Thu, 18 Dec 2025 04:10:57 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:76f8fd7ae4b31a0b6b2534fb2b8382cdc1d20c1bbb16b021752bff223e53c362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe4361adc8d61b5640d8c41b11d9f96aeb226edd04fafdc0e8f820cfb97cfd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:36:31 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:36:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3795c96879d916d2c0c23f5dbe72e6a8e975208f3ee6c8589eb580db38822df`  
		Last Modified: Fri, 19 Dec 2025 05:41:58 GMT  
		Size: 45.8 MB (45795470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:39fe38828762408de37a606fb37a23ec2f45786dbbe06be33bfa482427399ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efa933315fec9b05e8e114af019de92ac7ec9e847df1142ea3ed0ebeb1e98d`

```dockerfile
```

-	Layers:
	-	`sha256:5d163d50d63b3ac0863f070ba4ea01fc52cb951173af525823de84928f516e28`  
		Last Modified: Fri, 19 Dec 2025 07:09:46 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01bf93423650c650bc0a55016bc1ea02e2d9cdb068f8689e2f84217908071ee3`  
		Last Modified: Fri, 19 Dec 2025 07:09:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:06d55534e41116deeffadfa188514bf9e1f842e76aef6cee98d881377914b349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49845032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b6cc6713d31eb6184651ce332a7209009863e54eb9fbdbc0e4255a9219543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:12:51 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:12:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b16a0de9ead22663a13405f975f967ff4dbd8fa6266070a070f9ba99948182`  
		Last Modified: Thu, 18 Dec 2025 01:14:11 GMT  
		Size: 45.7 MB (45658610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac41c55a8b3896d166b9c150fcf8cdd21d465e6db49bbcdf4d43b499a0adaa6`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:6f7736f1bcf95ddae038700b2f1e3a3392fd727d4ecd85b1103479a67fe82b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce3fef82d410be2a6681ee56f228ad9a602bf53f0786c5830c57b38b7624b4`

```dockerfile
```

-	Layers:
	-	`sha256:52bcbcbf682af9f97e31167002fd644577bfe589100690db9a0b7e618fa4b5cb`  
		Last Modified: Thu, 18 Dec 2025 04:11:02 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28153da3bfe5ff9102d0509bdd95f0ef8662f190b8e03b68eaa9e1bfc6075b3c`  
		Last Modified: Thu, 18 Dec 2025 04:11:03 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6`

```console
$ docker pull traefik@sha256:67622638cd88dbfcfba40159bc652ecf0aea0e032f8a3c7e3134ae7c037b9910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3.6` - linux; amd64

```console
$ docker pull traefik@sha256:d944e3693bbf5a361ddd2e411bb713049cfb4f5ff3da200b30ee7a347dbd6abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb158a64eaac3b411525e180705dbb4e120d078150b6a795e120e6b80e81b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:33 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e627467d86762f7d43dc795a23361ae2c3f587d554d237f08e8b851a00bedd1`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489626b3f9620aab9962ec32de70229fb411c6304b6fa465f36501e2c9fb591`  
		Last Modified: Thu, 18 Dec 2025 00:38:13 GMT  
		Size: 47.5 MB (47508389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d82de1962f8aea587dc96507c61f4532e0492a7486c0464424909c9a287d4`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:04a3aa984984cc7e2e3063d865bf62b0f49d1c7ecb8aa1c3204717d38b115f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d3ff5908e1cdb4d0bff4368546e85af9f3da9117b657e2d14fcc7a8cc46df`

```dockerfile
```

-	Layers:
	-	`sha256:d974d7a987a8a2d1e72455e2e7281893be7e4de5980f6b05ef538d9525eac5ad`  
		Last Modified: Thu, 18 Dec 2025 04:10:44 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c127714cbcc3b651d10c37ff43afa00f119fb595dfa041cae741b5e6ed773`  
		Last Modified: Thu, 18 Dec 2025 04:10:45 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:088e42947073420f9ebde2eb5d8bab8f9181bca4aa2ce68489825f098bf8c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47125075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49ac065a809cf09a162068ca036c38f5628b53ce26a833f2a94cd2e5609fd9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:01 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f737350ac794161f26d63aadebc1bef9562e1b5145b8de73ef57db6afa0e07`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 461.4 KB (461443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bafdabef314d9c0aa348705c8e18f7c41ccaeb27138426e29133e0d94847`  
		Last Modified: Thu, 18 Dec 2025 00:48:24 GMT  
		Size: 43.1 MB (43094831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6064d2d82dbe21bc8205771bd41cf5fba61bc9662afdef68e431208574b3cb9`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:e1d5a37fc3d7604403838d16bd28b6aebecbc232f421cd887deb8b86d3ac022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b7b588d832edae2cc1791cf2822ed4e7ab9df8e0466a9b32ea438e42044a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2bbed655619f17a9a92d9c84e19b7bffd4d0ac0643f30961edf86b8fc64032f0`  
		Last Modified: Thu, 18 Dec 2025 04:10:49 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4df45c2d1101f440d989afb8d54ce557fda8c1028c63b4edb46e1387f20e252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73051e3972adbd5fd7ac7a30bf363b919b805fc5a85b0c184fecdc8aafc69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:14 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776aff3ebb03754e9132ac99fdd3d55913a018df4553600e28c9b49ccb9359d`  
		Last Modified: Thu, 18 Dec 2025 00:39:47 GMT  
		Size: 43.2 MB (43235898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0235f3573f63d55abfba7e9261bf749903b82ceb1338599b1dad8a7457aaadda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31ba6077556b5e469a5042279cc8a5d05f7d569a572d96e0dee0eaa7bd8b32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8220b97c6c54a61453867e3810ee63c84d079615a999974bb4c1cad060c68b`  
		Last Modified: Thu, 18 Dec 2025 04:10:52 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d83b4e84773fd95b32005cacfcbf43bfc22a2454bf16bfb8fd74072b564c2b`  
		Last Modified: Thu, 18 Dec 2025 04:10:53 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:f1bb2c5a12839909a38cbf8956a86a7de79a037d555cc29f1ac5ee281cb394a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c62d1ceea76fe16ce12841e2c9bcfc6df89a0cefc88ced9f5775f0201b1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:34:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:30 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:34:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ae93456d87a4319c334c68d8fe973661c62477820d71cbe214b3e3cf1596`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 41.3 MB (41258571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf953c6ec94ddbc562a208b274133f72e6e82689b6a4b337026df0994d1f0`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0c178d2363efe5881ba2974fd5e15298b184c9f8d5a796ddc386bae7933c6752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374a0d4f6058bebc837f4c842459d396c9e6019f0b7563916122e36541f2419`

```dockerfile
```

-	Layers:
	-	`sha256:12c32f74f9c3051a06ec488f6838aea96b398fdf6e4fc6b49e438432ea420060`  
		Last Modified: Thu, 18 Dec 2025 04:10:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe6e9400e9638d6fdbda5dc01ea957d910d9fc60572973c5dcd8fa3dfc53099`  
		Last Modified: Thu, 18 Dec 2025 04:10:57 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:76f8fd7ae4b31a0b6b2534fb2b8382cdc1d20c1bbb16b021752bff223e53c362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe4361adc8d61b5640d8c41b11d9f96aeb226edd04fafdc0e8f820cfb97cfd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:36:31 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:36:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3795c96879d916d2c0c23f5dbe72e6a8e975208f3ee6c8589eb580db38822df`  
		Last Modified: Fri, 19 Dec 2025 05:41:58 GMT  
		Size: 45.8 MB (45795470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:39fe38828762408de37a606fb37a23ec2f45786dbbe06be33bfa482427399ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efa933315fec9b05e8e114af019de92ac7ec9e847df1142ea3ed0ebeb1e98d`

```dockerfile
```

-	Layers:
	-	`sha256:5d163d50d63b3ac0863f070ba4ea01fc52cb951173af525823de84928f516e28`  
		Last Modified: Fri, 19 Dec 2025 07:09:46 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01bf93423650c650bc0a55016bc1ea02e2d9cdb068f8689e2f84217908071ee3`  
		Last Modified: Fri, 19 Dec 2025 07:09:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6` - linux; s390x

```console
$ docker pull traefik@sha256:06d55534e41116deeffadfa188514bf9e1f842e76aef6cee98d881377914b349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49845032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b6cc6713d31eb6184651ce332a7209009863e54eb9fbdbc0e4255a9219543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:12:51 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:12:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b16a0de9ead22663a13405f975f967ff4dbd8fa6266070a070f9ba99948182`  
		Last Modified: Thu, 18 Dec 2025 01:14:11 GMT  
		Size: 45.7 MB (45658610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac41c55a8b3896d166b9c150fcf8cdd21d465e6db49bbcdf4d43b499a0adaa6`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:6f7736f1bcf95ddae038700b2f1e3a3392fd727d4ecd85b1103479a67fe82b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce3fef82d410be2a6681ee56f228ad9a602bf53f0786c5830c57b38b7624b4`

```dockerfile
```

-	Layers:
	-	`sha256:52bcbcbf682af9f97e31167002fd644577bfe589100690db9a0b7e618fa4b5cb`  
		Last Modified: Thu, 18 Dec 2025 04:11:02 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28153da3bfe5ff9102d0509bdd95f0ef8662f190b8e03b68eaa9e1bfc6075b3c`  
		Last Modified: Thu, 18 Dec 2025 04:11:03 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.5`

```console
$ docker pull traefik@sha256:67622638cd88dbfcfba40159bc652ecf0aea0e032f8a3c7e3134ae7c037b9910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3.6.5` - linux; amd64

```console
$ docker pull traefik@sha256:d944e3693bbf5a361ddd2e411bb713049cfb4f5ff3da200b30ee7a347dbd6abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb158a64eaac3b411525e180705dbb4e120d078150b6a795e120e6b80e81b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:33 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e627467d86762f7d43dc795a23361ae2c3f587d554d237f08e8b851a00bedd1`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489626b3f9620aab9962ec32de70229fb411c6304b6fa465f36501e2c9fb591`  
		Last Modified: Thu, 18 Dec 2025 00:38:13 GMT  
		Size: 47.5 MB (47508389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d82de1962f8aea587dc96507c61f4532e0492a7486c0464424909c9a287d4`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:04a3aa984984cc7e2e3063d865bf62b0f49d1c7ecb8aa1c3204717d38b115f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d3ff5908e1cdb4d0bff4368546e85af9f3da9117b657e2d14fcc7a8cc46df`

```dockerfile
```

-	Layers:
	-	`sha256:d974d7a987a8a2d1e72455e2e7281893be7e4de5980f6b05ef538d9525eac5ad`  
		Last Modified: Thu, 18 Dec 2025 04:10:44 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c127714cbcc3b651d10c37ff43afa00f119fb595dfa041cae741b5e6ed773`  
		Last Modified: Thu, 18 Dec 2025 04:10:45 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:088e42947073420f9ebde2eb5d8bab8f9181bca4aa2ce68489825f098bf8c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47125075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49ac065a809cf09a162068ca036c38f5628b53ce26a833f2a94cd2e5609fd9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:01 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f737350ac794161f26d63aadebc1bef9562e1b5145b8de73ef57db6afa0e07`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 461.4 KB (461443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bafdabef314d9c0aa348705c8e18f7c41ccaeb27138426e29133e0d94847`  
		Last Modified: Thu, 18 Dec 2025 00:48:24 GMT  
		Size: 43.1 MB (43094831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6064d2d82dbe21bc8205771bd41cf5fba61bc9662afdef68e431208574b3cb9`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:e1d5a37fc3d7604403838d16bd28b6aebecbc232f421cd887deb8b86d3ac022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b7b588d832edae2cc1791cf2822ed4e7ab9df8e0466a9b32ea438e42044a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2bbed655619f17a9a92d9c84e19b7bffd4d0ac0643f30961edf86b8fc64032f0`  
		Last Modified: Thu, 18 Dec 2025 04:10:49 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4df45c2d1101f440d989afb8d54ce557fda8c1028c63b4edb46e1387f20e252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73051e3972adbd5fd7ac7a30bf363b919b805fc5a85b0c184fecdc8aafc69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:14 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776aff3ebb03754e9132ac99fdd3d55913a018df4553600e28c9b49ccb9359d`  
		Last Modified: Thu, 18 Dec 2025 00:39:47 GMT  
		Size: 43.2 MB (43235898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:0235f3573f63d55abfba7e9261bf749903b82ceb1338599b1dad8a7457aaadda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31ba6077556b5e469a5042279cc8a5d05f7d569a572d96e0dee0eaa7bd8b32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8220b97c6c54a61453867e3810ee63c84d079615a999974bb4c1cad060c68b`  
		Last Modified: Thu, 18 Dec 2025 04:10:52 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d83b4e84773fd95b32005cacfcbf43bfc22a2454bf16bfb8fd74072b564c2b`  
		Last Modified: Thu, 18 Dec 2025 04:10:53 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:f1bb2c5a12839909a38cbf8956a86a7de79a037d555cc29f1ac5ee281cb394a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c62d1ceea76fe16ce12841e2c9bcfc6df89a0cefc88ced9f5775f0201b1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:34:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:30 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:34:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ae93456d87a4319c334c68d8fe973661c62477820d71cbe214b3e3cf1596`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 41.3 MB (41258571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf953c6ec94ddbc562a208b274133f72e6e82689b6a4b337026df0994d1f0`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:0c178d2363efe5881ba2974fd5e15298b184c9f8d5a796ddc386bae7933c6752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374a0d4f6058bebc837f4c842459d396c9e6019f0b7563916122e36541f2419`

```dockerfile
```

-	Layers:
	-	`sha256:12c32f74f9c3051a06ec488f6838aea96b398fdf6e4fc6b49e438432ea420060`  
		Last Modified: Thu, 18 Dec 2025 04:10:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe6e9400e9638d6fdbda5dc01ea957d910d9fc60572973c5dcd8fa3dfc53099`  
		Last Modified: Thu, 18 Dec 2025 04:10:57 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; riscv64

```console
$ docker pull traefik@sha256:76f8fd7ae4b31a0b6b2534fb2b8382cdc1d20c1bbb16b021752bff223e53c362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe4361adc8d61b5640d8c41b11d9f96aeb226edd04fafdc0e8f820cfb97cfd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:36:31 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:36:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3795c96879d916d2c0c23f5dbe72e6a8e975208f3ee6c8589eb580db38822df`  
		Last Modified: Fri, 19 Dec 2025 05:41:58 GMT  
		Size: 45.8 MB (45795470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:39fe38828762408de37a606fb37a23ec2f45786dbbe06be33bfa482427399ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efa933315fec9b05e8e114af019de92ac7ec9e847df1142ea3ed0ebeb1e98d`

```dockerfile
```

-	Layers:
	-	`sha256:5d163d50d63b3ac0863f070ba4ea01fc52cb951173af525823de84928f516e28`  
		Last Modified: Fri, 19 Dec 2025 07:09:46 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01bf93423650c650bc0a55016bc1ea02e2d9cdb068f8689e2f84217908071ee3`  
		Last Modified: Fri, 19 Dec 2025 07:09:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.6.5` - linux; s390x

```console
$ docker pull traefik@sha256:06d55534e41116deeffadfa188514bf9e1f842e76aef6cee98d881377914b349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49845032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b6cc6713d31eb6184651ce332a7209009863e54eb9fbdbc0e4255a9219543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:12:51 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:12:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b16a0de9ead22663a13405f975f967ff4dbd8fa6266070a070f9ba99948182`  
		Last Modified: Thu, 18 Dec 2025 01:14:11 GMT  
		Size: 45.7 MB (45658610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac41c55a8b3896d166b9c150fcf8cdd21d465e6db49bbcdf4d43b499a0adaa6`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6f7736f1bcf95ddae038700b2f1e3a3392fd727d4ecd85b1103479a67fe82b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce3fef82d410be2a6681ee56f228ad9a602bf53f0786c5830c57b38b7624b4`

```dockerfile
```

-	Layers:
	-	`sha256:52bcbcbf682af9f97e31167002fd644577bfe589100690db9a0b7e618fa4b5cb`  
		Last Modified: Thu, 18 Dec 2025 04:11:02 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28153da3bfe5ff9102d0509bdd95f0ef8662f190b8e03b68eaa9e1bfc6075b3c`  
		Last Modified: Thu, 18 Dec 2025 04:11:03 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.6.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6.5-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.6.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:3.6.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:67622638cd88dbfcfba40159bc652ecf0aea0e032f8a3c7e3134ae7c037b9910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:latest` - linux; amd64

```console
$ docker pull traefik@sha256:d944e3693bbf5a361ddd2e411bb713049cfb4f5ff3da200b30ee7a347dbd6abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb158a64eaac3b411525e180705dbb4e120d078150b6a795e120e6b80e81b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:33 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e627467d86762f7d43dc795a23361ae2c3f587d554d237f08e8b851a00bedd1`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489626b3f9620aab9962ec32de70229fb411c6304b6fa465f36501e2c9fb591`  
		Last Modified: Thu, 18 Dec 2025 00:38:13 GMT  
		Size: 47.5 MB (47508389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d82de1962f8aea587dc96507c61f4532e0492a7486c0464424909c9a287d4`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:04a3aa984984cc7e2e3063d865bf62b0f49d1c7ecb8aa1c3204717d38b115f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d3ff5908e1cdb4d0bff4368546e85af9f3da9117b657e2d14fcc7a8cc46df`

```dockerfile
```

-	Layers:
	-	`sha256:d974d7a987a8a2d1e72455e2e7281893be7e4de5980f6b05ef538d9525eac5ad`  
		Last Modified: Thu, 18 Dec 2025 04:10:44 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c127714cbcc3b651d10c37ff43afa00f119fb595dfa041cae741b5e6ed773`  
		Last Modified: Thu, 18 Dec 2025 04:10:45 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:088e42947073420f9ebde2eb5d8bab8f9181bca4aa2ce68489825f098bf8c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47125075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49ac065a809cf09a162068ca036c38f5628b53ce26a833f2a94cd2e5609fd9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:01 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f737350ac794161f26d63aadebc1bef9562e1b5145b8de73ef57db6afa0e07`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 461.4 KB (461443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bafdabef314d9c0aa348705c8e18f7c41ccaeb27138426e29133e0d94847`  
		Last Modified: Thu, 18 Dec 2025 00:48:24 GMT  
		Size: 43.1 MB (43094831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6064d2d82dbe21bc8205771bd41cf5fba61bc9662afdef68e431208574b3cb9`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:e1d5a37fc3d7604403838d16bd28b6aebecbc232f421cd887deb8b86d3ac022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b7b588d832edae2cc1791cf2822ed4e7ab9df8e0466a9b32ea438e42044a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2bbed655619f17a9a92d9c84e19b7bffd4d0ac0643f30961edf86b8fc64032f0`  
		Last Modified: Thu, 18 Dec 2025 04:10:49 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4df45c2d1101f440d989afb8d54ce557fda8c1028c63b4edb46e1387f20e252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73051e3972adbd5fd7ac7a30bf363b919b805fc5a85b0c184fecdc8aafc69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:14 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776aff3ebb03754e9132ac99fdd3d55913a018df4553600e28c9b49ccb9359d`  
		Last Modified: Thu, 18 Dec 2025 00:39:47 GMT  
		Size: 43.2 MB (43235898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:0235f3573f63d55abfba7e9261bf749903b82ceb1338599b1dad8a7457aaadda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31ba6077556b5e469a5042279cc8a5d05f7d569a572d96e0dee0eaa7bd8b32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8220b97c6c54a61453867e3810ee63c84d079615a999974bb4c1cad060c68b`  
		Last Modified: Thu, 18 Dec 2025 04:10:52 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d83b4e84773fd95b32005cacfcbf43bfc22a2454bf16bfb8fd74072b564c2b`  
		Last Modified: Thu, 18 Dec 2025 04:10:53 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:f1bb2c5a12839909a38cbf8956a86a7de79a037d555cc29f1ac5ee281cb394a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c62d1ceea76fe16ce12841e2c9bcfc6df89a0cefc88ced9f5775f0201b1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:34:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:30 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:34:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ae93456d87a4319c334c68d8fe973661c62477820d71cbe214b3e3cf1596`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 41.3 MB (41258571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf953c6ec94ddbc562a208b274133f72e6e82689b6a4b337026df0994d1f0`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:0c178d2363efe5881ba2974fd5e15298b184c9f8d5a796ddc386bae7933c6752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374a0d4f6058bebc837f4c842459d396c9e6019f0b7563916122e36541f2419`

```dockerfile
```

-	Layers:
	-	`sha256:12c32f74f9c3051a06ec488f6838aea96b398fdf6e4fc6b49e438432ea420060`  
		Last Modified: Thu, 18 Dec 2025 04:10:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe6e9400e9638d6fdbda5dc01ea957d910d9fc60572973c5dcd8fa3dfc53099`  
		Last Modified: Thu, 18 Dec 2025 04:10:57 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:76f8fd7ae4b31a0b6b2534fb2b8382cdc1d20c1bbb16b021752bff223e53c362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe4361adc8d61b5640d8c41b11d9f96aeb226edd04fafdc0e8f820cfb97cfd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:36:31 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:36:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3795c96879d916d2c0c23f5dbe72e6a8e975208f3ee6c8589eb580db38822df`  
		Last Modified: Fri, 19 Dec 2025 05:41:58 GMT  
		Size: 45.8 MB (45795470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:39fe38828762408de37a606fb37a23ec2f45786dbbe06be33bfa482427399ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efa933315fec9b05e8e114af019de92ac7ec9e847df1142ea3ed0ebeb1e98d`

```dockerfile
```

-	Layers:
	-	`sha256:5d163d50d63b3ac0863f070ba4ea01fc52cb951173af525823de84928f516e28`  
		Last Modified: Fri, 19 Dec 2025 07:09:46 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01bf93423650c650bc0a55016bc1ea02e2d9cdb068f8689e2f84217908071ee3`  
		Last Modified: Fri, 19 Dec 2025 07:09:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:06d55534e41116deeffadfa188514bf9e1f842e76aef6cee98d881377914b349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49845032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b6cc6713d31eb6184651ce332a7209009863e54eb9fbdbc0e4255a9219543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:12:51 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:12:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b16a0de9ead22663a13405f975f967ff4dbd8fa6266070a070f9ba99948182`  
		Last Modified: Thu, 18 Dec 2025 01:14:11 GMT  
		Size: 45.7 MB (45658610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac41c55a8b3896d166b9c150fcf8cdd21d465e6db49bbcdf4d43b499a0adaa6`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6f7736f1bcf95ddae038700b2f1e3a3392fd727d4ecd85b1103479a67fe82b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce3fef82d410be2a6681ee56f228ad9a602bf53f0786c5830c57b38b7624b4`

```dockerfile
```

-	Layers:
	-	`sha256:52bcbcbf682af9f97e31167002fd644577bfe589100690db9a0b7e618fa4b5cb`  
		Last Modified: Thu, 18 Dec 2025 04:11:02 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28153da3bfe5ff9102d0509bdd95f0ef8662f190b8e03b68eaa9e1bfc6075b3c`  
		Last Modified: Thu, 18 Dec 2025 04:11:03 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:bb58a3046a925d974492f2a8d12af98b44a7ed039a46d3ade1ecf470a1af96c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:mimolette` - linux; amd64

```console
$ docker pull traefik@sha256:c9fc23758d3c09b5a8e97d5afc74f9affdcea35b49ebefa090c282cb7221e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0585c0174ce35e3b51078255df8c4bbf032a035b0bcd5d1f314fb74fb55eab74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:37 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5dae0d1940727b42d867b3209f02853f05720dde47a7ebe329f56c9e9b0a6`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 461.0 KB (460954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6168cb646a25a9cdc453b74cee1ce0858ec81602ff2cfe610d622162b897d`  
		Last Modified: Thu, 18 Dec 2025 00:38:12 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5121841f894ebf472fa208d1a3c2158dff03e65340dd3aa9ca29d379a4c114`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:ff5b79b15bf36250a2b4d4a7e21f10fd2075edb6035fc49a4580df6b1c1e482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e14b576062789d9f0b20eab9a463af99072602efef98ca3c0532e6e802a8d57`

```dockerfile
```

-	Layers:
	-	`sha256:767001a8883a7256101f6053ced15623e6200632343b45f1c4d535dae99034ab`  
		Last Modified: Thu, 18 Dec 2025 04:10:22 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b4654225acf7ee725ad1e861e54707caf6a0f7b38342f30cb04e7fe6e7ca11`  
		Last Modified: Thu, 18 Dec 2025 04:10:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4181c5fe1ea8dc7ca3d5bd4efbeff33e4288f669efbdfe57bbfb441bb4b99e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46823436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f44a3f50e52a4af869b39f3519d4f7a813621ccf6cacaeca4f6f3ef1f58435a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:48:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:25 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99378ff454de63b469978df2985803a8e574cfce746e9d83301f346b5044a5`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 461.5 KB (461451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138af728689bca4742d064a55f10930ef5d41f1cc001781ead4e4886d37cf66`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 42.8 MB (42793183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eb3473fb57831f0f13eaf728f113e93b369c0f9af26cf847850b4702c3902`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:30e4b7212f3765ed5e6d0b3d6d73e001f7b8bbac70ff4f80f1ef26eca3ffaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d2eb8ff0453823b8981f577b25c7d753978339866bf218313b238f19ef3b61`

```dockerfile
```

-	Layers:
	-	`sha256:b4f767790f9de664313048666f47024a86f9b276460c25673bc955d3a8e926d5`  
		Last Modified: Thu, 18 Dec 2025 04:10:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e51f93db0b17a2799c4581ecc42068bf6be4db36cdb96bde0491a39a600ec8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47294537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4c8495d19cd8540489695b630af9528dfb871f126428bf99d35a3be551b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:13 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73d6207c60aa10764a3ad0a664af3927b67597708348546560d24423427f959`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 42.6 MB (42635437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:734fe12d7bbe3eae7fdccb4b0bd7e7d28255eb03dc3931ce4a4144ca37f48918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be3d743f60cd5458a039660f04b83e61c36c41a994af175343602dd8490ea52`

```dockerfile
```

-	Layers:
	-	`sha256:783980b78710a6ea627cc4077b6fa5f7c377072ab916b55c4ccc415d16c06ba3`  
		Last Modified: Thu, 18 Dec 2025 04:10:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ba5a3551ae835ee366268051563035196c2072c6fd30c6e16596648483adda`  
		Last Modified: Thu, 18 Dec 2025 04:10:31 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:e32646c5052b0b611abb6be173532babb39d9260d1656f5084292db768e9cde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e6a4256c2946e32447aef8d2fc7707b682e62abfd2127e868d6734bf50c749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:36 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336300a7f5c554abee8386b767558f3bed8e7e1873062b733786765afdfdb99`  
		Last Modified: Thu, 18 Dec 2025 01:36:43 GMT  
		Size: 41.0 MB (40954982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10abf6cd1b69fb8c8a781b1420ea66868819194edacfd9f4b6795bf05e7efe5a`  
		Last Modified: Thu, 18 Dec 2025 01:36:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:eef8876bc857d08591fa49e46bec2152776718308c2a050b4c9e177df0963e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc23fba13ce49c6157ec521bd500da5ba721bae0d13118467da73738757d057e`

```dockerfile
```

-	Layers:
	-	`sha256:3afe5038e133ffab4adc253f337b1387bda92f29879d62cf0a57114690dc6d91`  
		Last Modified: Thu, 18 Dec 2025 04:10:34 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f6e730ee53229408d94802908716057a1850445d052d79dcda628c0a43d735`  
		Last Modified: Thu, 18 Dec 2025 04:10:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:30200fce5beb9e08c163b7810d2f6a5cb39bdca59fa5c7dbd5c0ba8ea1118568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49866d8a8721443b1a603b69899b0b953093c961da1c0d66d5df848afc0a7bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:42:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:42:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:42:27 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:42:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc13f83f0b87c8557a5b2154a47f0c9d974c15360754ead5af8dec5373f168`  
		Last Modified: Fri, 19 Dec 2025 05:47:33 GMT  
		Size: 45.3 MB (45323997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:7c7a13552833efd30b342c5b39ca3f44c7917da4354a3f504670f8be108d56e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69666deb1f6675c10e964a5a034e182641f4f42f9b1935e62d0b63bc8429d9f7`

```dockerfile
```

-	Layers:
	-	`sha256:2f8e08eafe1d8dc4b499f0ecc58ed54fa9254b1260499e706122d624a0689a94`  
		Last Modified: Fri, 19 Dec 2025 07:09:34 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c8d65b1207194a9024719e430b4b5c8e214f1301638e711a5df7d8c2585c47`  
		Last Modified: Fri, 19 Dec 2025 07:09:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:ddeda4089a26193575342c0931fb5762e4384c278102e3d956787cde673f951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e74521b9b925a71802c35cb1346284ecb7854c5f1963dd2724b6012f5e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:13:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:13:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:13:16 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:13:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d3f44e94737924cc971968c6169a7c7cfba62480b0e4b85c7491f35d93056`  
		Last Modified: Thu, 18 Dec 2025 01:14:30 GMT  
		Size: 45.3 MB (45254483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb6a157453d8b40c1eb2e3e0e99878463b56964abd0e9a925eedd6dc5ef51c7`  
		Last Modified: Thu, 18 Dec 2025 01:14:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:62bc10d9dbe1507cc836c7b43bafddfd84c64436c5200234ed9768dc9a4c5aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce641443c0ab290b21691e235a0addcf69be0b9f2182e2bf82b179bed6791b91`

```dockerfile
```

-	Layers:
	-	`sha256:fb849482243a1f3d0956b740762e64b0d8ca1a29d33e4a2e3c96a85fbbf249b2`  
		Last Modified: Thu, 18 Dec 2025 04:10:40 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9679fce549453252eb71fac70e8bae7e9aadc177074b8e27cec459239d8bce25`  
		Last Modified: Thu, 18 Dec 2025 04:10:41 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin`

```console
$ docker pull traefik@sha256:67622638cd88dbfcfba40159bc652ecf0aea0e032f8a3c7e3134ae7c037b9910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:ramequin` - linux; amd64

```console
$ docker pull traefik@sha256:d944e3693bbf5a361ddd2e411bb713049cfb4f5ff3da200b30ee7a347dbd6abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb158a64eaac3b411525e180705dbb4e120d078150b6a795e120e6b80e81b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:33 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e627467d86762f7d43dc795a23361ae2c3f587d554d237f08e8b851a00bedd1`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489626b3f9620aab9962ec32de70229fb411c6304b6fa465f36501e2c9fb591`  
		Last Modified: Thu, 18 Dec 2025 00:38:13 GMT  
		Size: 47.5 MB (47508389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d82de1962f8aea587dc96507c61f4532e0492a7486c0464424909c9a287d4`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:04a3aa984984cc7e2e3063d865bf62b0f49d1c7ecb8aa1c3204717d38b115f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d3ff5908e1cdb4d0bff4368546e85af9f3da9117b657e2d14fcc7a8cc46df`

```dockerfile
```

-	Layers:
	-	`sha256:d974d7a987a8a2d1e72455e2e7281893be7e4de5980f6b05ef538d9525eac5ad`  
		Last Modified: Thu, 18 Dec 2025 04:10:44 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c127714cbcc3b651d10c37ff43afa00f119fb595dfa041cae741b5e6ed773`  
		Last Modified: Thu, 18 Dec 2025 04:10:45 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:088e42947073420f9ebde2eb5d8bab8f9181bca4aa2ce68489825f098bf8c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47125075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49ac065a809cf09a162068ca036c38f5628b53ce26a833f2a94cd2e5609fd9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:01 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f737350ac794161f26d63aadebc1bef9562e1b5145b8de73ef57db6afa0e07`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 461.4 KB (461443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bafdabef314d9c0aa348705c8e18f7c41ccaeb27138426e29133e0d94847`  
		Last Modified: Thu, 18 Dec 2025 00:48:24 GMT  
		Size: 43.1 MB (43094831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6064d2d82dbe21bc8205771bd41cf5fba61bc9662afdef68e431208574b3cb9`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:e1d5a37fc3d7604403838d16bd28b6aebecbc232f421cd887deb8b86d3ac022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b7b588d832edae2cc1791cf2822ed4e7ab9df8e0466a9b32ea438e42044a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2bbed655619f17a9a92d9c84e19b7bffd4d0ac0643f30961edf86b8fc64032f0`  
		Last Modified: Thu, 18 Dec 2025 04:10:49 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4df45c2d1101f440d989afb8d54ce557fda8c1028c63b4edb46e1387f20e252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73051e3972adbd5fd7ac7a30bf363b919b805fc5a85b0c184fecdc8aafc69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:14 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776aff3ebb03754e9132ac99fdd3d55913a018df4553600e28c9b49ccb9359d`  
		Last Modified: Thu, 18 Dec 2025 00:39:47 GMT  
		Size: 43.2 MB (43235898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0235f3573f63d55abfba7e9261bf749903b82ceb1338599b1dad8a7457aaadda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31ba6077556b5e469a5042279cc8a5d05f7d569a572d96e0dee0eaa7bd8b32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8220b97c6c54a61453867e3810ee63c84d079615a999974bb4c1cad060c68b`  
		Last Modified: Thu, 18 Dec 2025 04:10:52 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d83b4e84773fd95b32005cacfcbf43bfc22a2454bf16bfb8fd74072b564c2b`  
		Last Modified: Thu, 18 Dec 2025 04:10:53 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:f1bb2c5a12839909a38cbf8956a86a7de79a037d555cc29f1ac5ee281cb394a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c62d1ceea76fe16ce12841e2c9bcfc6df89a0cefc88ced9f5775f0201b1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:34:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:30 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:34:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ae93456d87a4319c334c68d8fe973661c62477820d71cbe214b3e3cf1596`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 41.3 MB (41258571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf953c6ec94ddbc562a208b274133f72e6e82689b6a4b337026df0994d1f0`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:0c178d2363efe5881ba2974fd5e15298b184c9f8d5a796ddc386bae7933c6752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374a0d4f6058bebc837f4c842459d396c9e6019f0b7563916122e36541f2419`

```dockerfile
```

-	Layers:
	-	`sha256:12c32f74f9c3051a06ec488f6838aea96b398fdf6e4fc6b49e438432ea420060`  
		Last Modified: Thu, 18 Dec 2025 04:10:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe6e9400e9638d6fdbda5dc01ea957d910d9fc60572973c5dcd8fa3dfc53099`  
		Last Modified: Thu, 18 Dec 2025 04:10:57 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:76f8fd7ae4b31a0b6b2534fb2b8382cdc1d20c1bbb16b021752bff223e53c362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe4361adc8d61b5640d8c41b11d9f96aeb226edd04fafdc0e8f820cfb97cfd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:36:31 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:36:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3795c96879d916d2c0c23f5dbe72e6a8e975208f3ee6c8589eb580db38822df`  
		Last Modified: Fri, 19 Dec 2025 05:41:58 GMT  
		Size: 45.8 MB (45795470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:39fe38828762408de37a606fb37a23ec2f45786dbbe06be33bfa482427399ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efa933315fec9b05e8e114af019de92ac7ec9e847df1142ea3ed0ebeb1e98d`

```dockerfile
```

-	Layers:
	-	`sha256:5d163d50d63b3ac0863f070ba4ea01fc52cb951173af525823de84928f516e28`  
		Last Modified: Fri, 19 Dec 2025 07:09:46 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01bf93423650c650bc0a55016bc1ea02e2d9cdb068f8689e2f84217908071ee3`  
		Last Modified: Fri, 19 Dec 2025 07:09:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:06d55534e41116deeffadfa188514bf9e1f842e76aef6cee98d881377914b349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49845032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b6cc6713d31eb6184651ce332a7209009863e54eb9fbdbc0e4255a9219543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:12:51 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:12:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b16a0de9ead22663a13405f975f967ff4dbd8fa6266070a070f9ba99948182`  
		Last Modified: Thu, 18 Dec 2025 01:14:11 GMT  
		Size: 45.7 MB (45658610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac41c55a8b3896d166b9c150fcf8cdd21d465e6db49bbcdf4d43b499a0adaa6`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:6f7736f1bcf95ddae038700b2f1e3a3392fd727d4ecd85b1103479a67fe82b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce3fef82d410be2a6681ee56f228ad9a602bf53f0786c5830c57b38b7624b4`

```dockerfile
```

-	Layers:
	-	`sha256:52bcbcbf682af9f97e31167002fd644577bfe589100690db9a0b7e618fa4b5cb`  
		Last Modified: Thu, 18 Dec 2025 04:11:02 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28153da3bfe5ff9102d0509bdd95f0ef8662f190b8e03b68eaa9e1bfc6075b3c`  
		Last Modified: Thu, 18 Dec 2025 04:11:03 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:ramequin-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:ramequin-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:ramequin-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:ramequin-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:bb58a3046a925d974492f2a8d12af98b44a7ed039a46d3ade1ecf470a1af96c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2` - linux; amd64

```console
$ docker pull traefik@sha256:c9fc23758d3c09b5a8e97d5afc74f9affdcea35b49ebefa090c282cb7221e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0585c0174ce35e3b51078255df8c4bbf032a035b0bcd5d1f314fb74fb55eab74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:37 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5dae0d1940727b42d867b3209f02853f05720dde47a7ebe329f56c9e9b0a6`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 461.0 KB (460954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6168cb646a25a9cdc453b74cee1ce0858ec81602ff2cfe610d622162b897d`  
		Last Modified: Thu, 18 Dec 2025 00:38:12 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5121841f894ebf472fa208d1a3c2158dff03e65340dd3aa9ca29d379a4c114`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:ff5b79b15bf36250a2b4d4a7e21f10fd2075edb6035fc49a4580df6b1c1e482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e14b576062789d9f0b20eab9a463af99072602efef98ca3c0532e6e802a8d57`

```dockerfile
```

-	Layers:
	-	`sha256:767001a8883a7256101f6053ced15623e6200632343b45f1c4d535dae99034ab`  
		Last Modified: Thu, 18 Dec 2025 04:10:22 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b4654225acf7ee725ad1e861e54707caf6a0f7b38342f30cb04e7fe6e7ca11`  
		Last Modified: Thu, 18 Dec 2025 04:10:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4181c5fe1ea8dc7ca3d5bd4efbeff33e4288f669efbdfe57bbfb441bb4b99e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46823436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f44a3f50e52a4af869b39f3519d4f7a813621ccf6cacaeca4f6f3ef1f58435a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:48:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:25 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99378ff454de63b469978df2985803a8e574cfce746e9d83301f346b5044a5`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 461.5 KB (461451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138af728689bca4742d064a55f10930ef5d41f1cc001781ead4e4886d37cf66`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 42.8 MB (42793183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eb3473fb57831f0f13eaf728f113e93b369c0f9af26cf847850b4702c3902`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:30e4b7212f3765ed5e6d0b3d6d73e001f7b8bbac70ff4f80f1ef26eca3ffaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d2eb8ff0453823b8981f577b25c7d753978339866bf218313b238f19ef3b61`

```dockerfile
```

-	Layers:
	-	`sha256:b4f767790f9de664313048666f47024a86f9b276460c25673bc955d3a8e926d5`  
		Last Modified: Thu, 18 Dec 2025 04:10:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e51f93db0b17a2799c4581ecc42068bf6be4db36cdb96bde0491a39a600ec8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47294537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4c8495d19cd8540489695b630af9528dfb871f126428bf99d35a3be551b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:13 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73d6207c60aa10764a3ad0a664af3927b67597708348546560d24423427f959`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 42.6 MB (42635437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:734fe12d7bbe3eae7fdccb4b0bd7e7d28255eb03dc3931ce4a4144ca37f48918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be3d743f60cd5458a039660f04b83e61c36c41a994af175343602dd8490ea52`

```dockerfile
```

-	Layers:
	-	`sha256:783980b78710a6ea627cc4077b6fa5f7c377072ab916b55c4ccc415d16c06ba3`  
		Last Modified: Thu, 18 Dec 2025 04:10:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ba5a3551ae835ee366268051563035196c2072c6fd30c6e16596648483adda`  
		Last Modified: Thu, 18 Dec 2025 04:10:31 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:e32646c5052b0b611abb6be173532babb39d9260d1656f5084292db768e9cde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e6a4256c2946e32447aef8d2fc7707b682e62abfd2127e868d6734bf50c749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:36 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336300a7f5c554abee8386b767558f3bed8e7e1873062b733786765afdfdb99`  
		Last Modified: Thu, 18 Dec 2025 01:36:43 GMT  
		Size: 41.0 MB (40954982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10abf6cd1b69fb8c8a781b1420ea66868819194edacfd9f4b6795bf05e7efe5a`  
		Last Modified: Thu, 18 Dec 2025 01:36:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:eef8876bc857d08591fa49e46bec2152776718308c2a050b4c9e177df0963e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc23fba13ce49c6157ec521bd500da5ba721bae0d13118467da73738757d057e`

```dockerfile
```

-	Layers:
	-	`sha256:3afe5038e133ffab4adc253f337b1387bda92f29879d62cf0a57114690dc6d91`  
		Last Modified: Thu, 18 Dec 2025 04:10:34 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f6e730ee53229408d94802908716057a1850445d052d79dcda628c0a43d735`  
		Last Modified: Thu, 18 Dec 2025 04:10:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:30200fce5beb9e08c163b7810d2f6a5cb39bdca59fa5c7dbd5c0ba8ea1118568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49866d8a8721443b1a603b69899b0b953093c961da1c0d66d5df848afc0a7bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:42:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:42:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:42:27 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:42:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc13f83f0b87c8557a5b2154a47f0c9d974c15360754ead5af8dec5373f168`  
		Last Modified: Fri, 19 Dec 2025 05:47:33 GMT  
		Size: 45.3 MB (45323997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:7c7a13552833efd30b342c5b39ca3f44c7917da4354a3f504670f8be108d56e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69666deb1f6675c10e964a5a034e182641f4f42f9b1935e62d0b63bc8429d9f7`

```dockerfile
```

-	Layers:
	-	`sha256:2f8e08eafe1d8dc4b499f0ecc58ed54fa9254b1260499e706122d624a0689a94`  
		Last Modified: Fri, 19 Dec 2025 07:09:34 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c8d65b1207194a9024719e430b4b5c8e214f1301638e711a5df7d8c2585c47`  
		Last Modified: Fri, 19 Dec 2025 07:09:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:ddeda4089a26193575342c0931fb5762e4384c278102e3d956787cde673f951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e74521b9b925a71802c35cb1346284ecb7854c5f1963dd2724b6012f5e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:13:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:13:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:13:16 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:13:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d3f44e94737924cc971968c6169a7c7cfba62480b0e4b85c7491f35d93056`  
		Last Modified: Thu, 18 Dec 2025 01:14:30 GMT  
		Size: 45.3 MB (45254483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb6a157453d8b40c1eb2e3e0e99878463b56964abd0e9a925eedd6dc5ef51c7`  
		Last Modified: Thu, 18 Dec 2025 01:14:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:62bc10d9dbe1507cc836c7b43bafddfd84c64436c5200234ed9768dc9a4c5aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce641443c0ab290b21691e235a0addcf69be0b9f2182e2bf82b179bed6791b91`

```dockerfile
```

-	Layers:
	-	`sha256:fb849482243a1f3d0956b740762e64b0d8ca1a29d33e4a2e3c96a85fbbf249b2`  
		Last Modified: Thu, 18 Dec 2025 04:10:40 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9679fce549453252eb71fac70e8bae7e9aadc177074b8e27cec459239d8bce25`  
		Last Modified: Thu, 18 Dec 2025 04:10:41 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:bb58a3046a925d974492f2a8d12af98b44a7ed039a46d3ade1ecf470a1af96c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2.11` - linux; amd64

```console
$ docker pull traefik@sha256:c9fc23758d3c09b5a8e97d5afc74f9affdcea35b49ebefa090c282cb7221e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0585c0174ce35e3b51078255df8c4bbf032a035b0bcd5d1f314fb74fb55eab74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:37 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5dae0d1940727b42d867b3209f02853f05720dde47a7ebe329f56c9e9b0a6`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 461.0 KB (460954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6168cb646a25a9cdc453b74cee1ce0858ec81602ff2cfe610d622162b897d`  
		Last Modified: Thu, 18 Dec 2025 00:38:12 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5121841f894ebf472fa208d1a3c2158dff03e65340dd3aa9ca29d379a4c114`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:ff5b79b15bf36250a2b4d4a7e21f10fd2075edb6035fc49a4580df6b1c1e482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e14b576062789d9f0b20eab9a463af99072602efef98ca3c0532e6e802a8d57`

```dockerfile
```

-	Layers:
	-	`sha256:767001a8883a7256101f6053ced15623e6200632343b45f1c4d535dae99034ab`  
		Last Modified: Thu, 18 Dec 2025 04:10:22 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b4654225acf7ee725ad1e861e54707caf6a0f7b38342f30cb04e7fe6e7ca11`  
		Last Modified: Thu, 18 Dec 2025 04:10:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4181c5fe1ea8dc7ca3d5bd4efbeff33e4288f669efbdfe57bbfb441bb4b99e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46823436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f44a3f50e52a4af869b39f3519d4f7a813621ccf6cacaeca4f6f3ef1f58435a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:48:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:25 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99378ff454de63b469978df2985803a8e574cfce746e9d83301f346b5044a5`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 461.5 KB (461451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138af728689bca4742d064a55f10930ef5d41f1cc001781ead4e4886d37cf66`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 42.8 MB (42793183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eb3473fb57831f0f13eaf728f113e93b369c0f9af26cf847850b4702c3902`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:30e4b7212f3765ed5e6d0b3d6d73e001f7b8bbac70ff4f80f1ef26eca3ffaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d2eb8ff0453823b8981f577b25c7d753978339866bf218313b238f19ef3b61`

```dockerfile
```

-	Layers:
	-	`sha256:b4f767790f9de664313048666f47024a86f9b276460c25673bc955d3a8e926d5`  
		Last Modified: Thu, 18 Dec 2025 04:10:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e51f93db0b17a2799c4581ecc42068bf6be4db36cdb96bde0491a39a600ec8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47294537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4c8495d19cd8540489695b630af9528dfb871f126428bf99d35a3be551b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:13 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73d6207c60aa10764a3ad0a664af3927b67597708348546560d24423427f959`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 42.6 MB (42635437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:734fe12d7bbe3eae7fdccb4b0bd7e7d28255eb03dc3931ce4a4144ca37f48918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be3d743f60cd5458a039660f04b83e61c36c41a994af175343602dd8490ea52`

```dockerfile
```

-	Layers:
	-	`sha256:783980b78710a6ea627cc4077b6fa5f7c377072ab916b55c4ccc415d16c06ba3`  
		Last Modified: Thu, 18 Dec 2025 04:10:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ba5a3551ae835ee366268051563035196c2072c6fd30c6e16596648483adda`  
		Last Modified: Thu, 18 Dec 2025 04:10:31 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:e32646c5052b0b611abb6be173532babb39d9260d1656f5084292db768e9cde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e6a4256c2946e32447aef8d2fc7707b682e62abfd2127e868d6734bf50c749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:36 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336300a7f5c554abee8386b767558f3bed8e7e1873062b733786765afdfdb99`  
		Last Modified: Thu, 18 Dec 2025 01:36:43 GMT  
		Size: 41.0 MB (40954982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10abf6cd1b69fb8c8a781b1420ea66868819194edacfd9f4b6795bf05e7efe5a`  
		Last Modified: Thu, 18 Dec 2025 01:36:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:eef8876bc857d08591fa49e46bec2152776718308c2a050b4c9e177df0963e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc23fba13ce49c6157ec521bd500da5ba721bae0d13118467da73738757d057e`

```dockerfile
```

-	Layers:
	-	`sha256:3afe5038e133ffab4adc253f337b1387bda92f29879d62cf0a57114690dc6d91`  
		Last Modified: Thu, 18 Dec 2025 04:10:34 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f6e730ee53229408d94802908716057a1850445d052d79dcda628c0a43d735`  
		Last Modified: Thu, 18 Dec 2025 04:10:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:30200fce5beb9e08c163b7810d2f6a5cb39bdca59fa5c7dbd5c0ba8ea1118568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49866d8a8721443b1a603b69899b0b953093c961da1c0d66d5df848afc0a7bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:42:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:42:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:42:27 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:42:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc13f83f0b87c8557a5b2154a47f0c9d974c15360754ead5af8dec5373f168`  
		Last Modified: Fri, 19 Dec 2025 05:47:33 GMT  
		Size: 45.3 MB (45323997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:7c7a13552833efd30b342c5b39ca3f44c7917da4354a3f504670f8be108d56e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69666deb1f6675c10e964a5a034e182641f4f42f9b1935e62d0b63bc8429d9f7`

```dockerfile
```

-	Layers:
	-	`sha256:2f8e08eafe1d8dc4b499f0ecc58ed54fa9254b1260499e706122d624a0689a94`  
		Last Modified: Fri, 19 Dec 2025 07:09:34 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c8d65b1207194a9024719e430b4b5c8e214f1301638e711a5df7d8c2585c47`  
		Last Modified: Fri, 19 Dec 2025 07:09:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:ddeda4089a26193575342c0931fb5762e4384c278102e3d956787cde673f951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e74521b9b925a71802c35cb1346284ecb7854c5f1963dd2724b6012f5e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:13:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:13:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:13:16 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:13:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d3f44e94737924cc971968c6169a7c7cfba62480b0e4b85c7491f35d93056`  
		Last Modified: Thu, 18 Dec 2025 01:14:30 GMT  
		Size: 45.3 MB (45254483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb6a157453d8b40c1eb2e3e0e99878463b56964abd0e9a925eedd6dc5ef51c7`  
		Last Modified: Thu, 18 Dec 2025 01:14:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:62bc10d9dbe1507cc836c7b43bafddfd84c64436c5200234ed9768dc9a4c5aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce641443c0ab290b21691e235a0addcf69be0b9f2182e2bf82b179bed6791b91`

```dockerfile
```

-	Layers:
	-	`sha256:fb849482243a1f3d0956b740762e64b0d8ca1a29d33e4a2e3c96a85fbbf249b2`  
		Last Modified: Thu, 18 Dec 2025 04:10:40 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9679fce549453252eb71fac70e8bae7e9aadc177074b8e27cec459239d8bce25`  
		Last Modified: Thu, 18 Dec 2025 04:10:41 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.33`

```console
$ docker pull traefik@sha256:bb58a3046a925d974492f2a8d12af98b44a7ed039a46d3ade1ecf470a1af96c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2.11.33` - linux; amd64

```console
$ docker pull traefik@sha256:c9fc23758d3c09b5a8e97d5afc74f9affdcea35b49ebefa090c282cb7221e3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51047889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0585c0174ce35e3b51078255df8c4bbf032a035b0bcd5d1f314fb74fb55eab74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:37 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d5dae0d1940727b42d867b3209f02853f05720dde47a7ebe329f56c9e9b0a6`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 461.0 KB (460954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd6168cb646a25a9cdc453b74cee1ce0858ec81602ff2cfe610d622162b897d`  
		Last Modified: Thu, 18 Dec 2025 00:38:12 GMT  
		Size: 46.7 MB (46726462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5121841f894ebf472fa208d1a3c2158dff03e65340dd3aa9ca29d379a4c114`  
		Last Modified: Thu, 18 Dec 2025 00:38:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:ff5b79b15bf36250a2b4d4a7e21f10fd2075edb6035fc49a4580df6b1c1e482d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.5 KB (867455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e14b576062789d9f0b20eab9a463af99072602efef98ca3c0532e6e802a8d57`

```dockerfile
```

-	Layers:
	-	`sha256:767001a8883a7256101f6053ced15623e6200632343b45f1c4d535dae99034ab`  
		Last Modified: Thu, 18 Dec 2025 04:10:22 GMT  
		Size: 855.0 KB (854960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b4654225acf7ee725ad1e861e54707caf6a0f7b38342f30cb04e7fe6e7ca11`  
		Last Modified: Thu, 18 Dec 2025 04:10:23 GMT  
		Size: 12.5 KB (12495 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; arm variant v6

```console
$ docker pull traefik@sha256:4181c5fe1ea8dc7ca3d5bd4efbeff33e4288f669efbdfe57bbfb441bb4b99e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46823436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f44a3f50e52a4af869b39f3519d4f7a813621ccf6cacaeca4f6f3ef1f58435a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:48:22 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:25 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:25 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:25 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f99378ff454de63b469978df2985803a8e574cfce746e9d83301f346b5044a5`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 461.5 KB (461451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138af728689bca4742d064a55f10930ef5d41f1cc001781ead4e4886d37cf66`  
		Last Modified: Thu, 18 Dec 2025 00:48:43 GMT  
		Size: 42.8 MB (42793183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933eb3473fb57831f0f13eaf728f113e93b369c0f9af26cf847850b4702c3902`  
		Last Modified: Thu, 18 Dec 2025 00:48:39 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:30e4b7212f3765ed5e6d0b3d6d73e001f7b8bbac70ff4f80f1ef26eca3ffaeb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d2eb8ff0453823b8981f577b25c7d753978339866bf218313b238f19ef3b61`

```dockerfile
```

-	Layers:
	-	`sha256:b4f767790f9de664313048666f47024a86f9b276460c25673bc955d3a8e926d5`  
		Last Modified: Thu, 18 Dec 2025 04:10:27 GMT  
		Size: 12.4 KB (12397 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e51f93db0b17a2799c4581ecc42068bf6be4db36cdb96bde0491a39a600ec8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47294537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4c8495d19cd8540489695b630af9528dfb871f126428bf99d35a3be551b0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:13 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:13 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73d6207c60aa10764a3ad0a664af3927b67597708348546560d24423427f959`  
		Last Modified: Thu, 18 Dec 2025 00:39:48 GMT  
		Size: 42.6 MB (42635437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:734fe12d7bbe3eae7fdccb4b0bd7e7d28255eb03dc3931ce4a4144ca37f48918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.1 KB (867052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be3d743f60cd5458a039660f04b83e61c36c41a994af175343602dd8490ea52`

```dockerfile
```

-	Layers:
	-	`sha256:783980b78710a6ea627cc4077b6fa5f7c377072ab916b55c4ccc415d16c06ba3`  
		Last Modified: Thu, 18 Dec 2025 04:10:30 GMT  
		Size: 854.4 KB (854402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ba5a3551ae835ee366268051563035196c2072c6fd30c6e16596648483adda`  
		Last Modified: Thu, 18 Dec 2025 04:10:31 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; ppc64le

```console
$ docker pull traefik@sha256:e32646c5052b0b611abb6be173532babb39d9260d1656f5084292db768e9cde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45246617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e6a4256c2946e32447aef8d2fc7707b682e62abfd2127e868d6734bf50c749`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:35:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:35:36 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:35:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:35:36 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:35:36 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1336300a7f5c554abee8386b767558f3bed8e7e1873062b733786765afdfdb99`  
		Last Modified: Thu, 18 Dec 2025 01:36:43 GMT  
		Size: 41.0 MB (40954982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10abf6cd1b69fb8c8a781b1420ea66868819194edacfd9f4b6795bf05e7efe5a`  
		Last Modified: Thu, 18 Dec 2025 01:36:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:eef8876bc857d08591fa49e46bec2152776718308c2a050b4c9e177df0963e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc23fba13ce49c6157ec521bd500da5ba721bae0d13118467da73738757d057e`

```dockerfile
```

-	Layers:
	-	`sha256:3afe5038e133ffab4adc253f337b1387bda92f29879d62cf0a57114690dc6d91`  
		Last Modified: Thu, 18 Dec 2025 04:10:34 GMT  
		Size: 854.4 KB (854361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61f6e730ee53229408d94802908716057a1850445d052d79dcda628c0a43d735`  
		Last Modified: Thu, 18 Dec 2025 04:10:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; riscv64

```console
$ docker pull traefik@sha256:30200fce5beb9e08c163b7810d2f6a5cb39bdca59fa5c7dbd5c0ba8ea1118568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49369496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49866d8a8721443b1a603b69899b0b953093c961da1c0d66d5df848afc0a7bf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:42:26 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:42:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:42:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:42:27 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:42:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc13f83f0b87c8557a5b2154a47f0c9d974c15360754ead5af8dec5373f168`  
		Last Modified: Fri, 19 Dec 2025 05:47:33 GMT  
		Size: 45.3 MB (45323997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8977c8b131b21d9ec50d6656430c551cc2e185878f8b17a0f62b17befb467f`  
		Last Modified: Wed, 17 Dec 2025 18:46:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:7c7a13552833efd30b342c5b39ca3f44c7917da4354a3f504670f8be108d56e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.9 KB (866916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69666deb1f6675c10e964a5a034e182641f4f42f9b1935e62d0b63bc8429d9f7`

```dockerfile
```

-	Layers:
	-	`sha256:2f8e08eafe1d8dc4b499f0ecc58ed54fa9254b1260499e706122d624a0689a94`  
		Last Modified: Fri, 19 Dec 2025 07:09:34 GMT  
		Size: 854.4 KB (854357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c8d65b1207194a9024719e430b4b5c8e214f1301638e711a5df7d8c2585c47`  
		Last Modified: Fri, 19 Dec 2025 07:09:35 GMT  
		Size: 12.6 KB (12559 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.33` - linux; s390x

```console
$ docker pull traefik@sha256:ddeda4089a26193575342c0931fb5762e4384c278102e3d956787cde673f951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0e74521b9b925a71802c35cb1346284ecb7854c5f1963dd2724b6012f5e5b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:13:15 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:13:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:13:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:13:16 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:13:16 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77d3f44e94737924cc971968c6169a7c7cfba62480b0e4b85c7491f35d93056`  
		Last Modified: Thu, 18 Dec 2025 01:14:30 GMT  
		Size: 45.3 MB (45254483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb6a157453d8b40c1eb2e3e0e99878463b56964abd0e9a925eedd6dc5ef51c7`  
		Last Modified: Thu, 18 Dec 2025 01:14:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.33` - unknown; unknown

```console
$ docker pull traefik@sha256:62bc10d9dbe1507cc836c7b43bafddfd84c64436c5200234ed9768dc9a4c5aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.8 KB (866799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce641443c0ab290b21691e235a0addcf69be0b9f2182e2bf82b179bed6791b91`

```dockerfile
```

-	Layers:
	-	`sha256:fb849482243a1f3d0956b740762e64b0d8ca1a29d33e4a2e3c96a85fbbf249b2`  
		Last Modified: Thu, 18 Dec 2025 04:10:40 GMT  
		Size: 854.3 KB (854305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9679fce549453252eb71fac70e8bae7e9aadc177074b8e27cec459239d8bce25`  
		Last Modified: Thu, 18 Dec 2025 04:10:41 GMT  
		Size: 12.5 KB (12494 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.33-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e8d541c311d86693ff5f52e9c1ce648156945b44a451ee85f98c42d652c7f060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11.33-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:de21e6fe59df83e96ebafda135a9104679608e2399b0aa1395505a9294709282
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173873786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d4de94b35d1536b389c47d06499dde53622a1595c43d837be62fe8ba15d99c`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 17 Dec 2025 19:09:44 GMT
RUN cmd /S /C #(nop) COPY file:e8b1825093bb50331d5da901c0d3bf30d38175a00b778d3702b5af5222065b37 in \ 
# Wed, 17 Dec 2025 19:09:46 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 17 Dec 2025 19:09:47 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 19:09:48 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befcbd32a5211d51eb78a8ffca0e9b5bd6a75fee459f44159afcc14d3c4f151f`  
		Last Modified: Wed, 17 Dec 2025 19:10:34 GMT  
		Size: 47.5 MB (47512297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b480417a477dc90f73e0ab07421c2f1c1ec08188c53e6375bdbe817180690052`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ffcd38b04538c79ba8c042cf83d128ff2d87e80eb4fc873b70febff370f02a`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83898e481fc2498a43872864ca26b5ba80ae64cb26a6448d9c80cd2da2b7c271`  
		Last Modified: Wed, 17 Dec 2025 19:10:29 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.33-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:7ae28f047fde3a06e8b3298bf5428663d8bb18c6ef3368bca3e5618ec0350b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v2.11.33-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:588a262be8d65ea220f8345e54351a309632da4996a473e9e5cc1ace9ed0b8f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828025786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43006f6a17317bf56066d41186e9ad383afb8f5ce64ae6f562bca271439c40ff`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 18:45:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 18:46:27 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.33/traefik_v2.11.33_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 17 Dec 2025 18:46:28 GMT
EXPOSE 80
# Wed, 17 Dec 2025 18:46:28 GMT
ENTRYPOINT ["/traefik"]
# Wed, 17 Dec 2025 18:46:29 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.33 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b570d5a52b273296486a82d56ed1fb607dc2d48c2a2141dd8682f7db3f31d65`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d61c3ac562a95bbce347308e2fc3cf5cae31e9a694fae9a10ca85fd176a2a0e`  
		Last Modified: Wed, 17 Dec 2025 18:55:26 GMT  
		Size: 48.1 MB (48141264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32528f135a3c4bc8e0cc0bcc3ccaf09a0e109296a655107dc4defd21fc9c790a`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa9f2c653102db08561dd4f3c42a71f6ec3f75a5a80043d2cc0f634909056f5`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cdc4662a7739a2ff80051bd8ae9de9ef796b9a7433f69a8bd7cb6d4fa7a1ca`  
		Last Modified: Wed, 17 Dec 2025 18:55:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:67622638cd88dbfcfba40159bc652ecf0aea0e032f8a3c7e3134ae7c037b9910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3` - linux; amd64

```console
$ docker pull traefik@sha256:d944e3693bbf5a361ddd2e411bb713049cfb4f5ff3da200b30ee7a347dbd6abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb158a64eaac3b411525e180705dbb4e120d078150b6a795e120e6b80e81b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:33 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e627467d86762f7d43dc795a23361ae2c3f587d554d237f08e8b851a00bedd1`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489626b3f9620aab9962ec32de70229fb411c6304b6fa465f36501e2c9fb591`  
		Last Modified: Thu, 18 Dec 2025 00:38:13 GMT  
		Size: 47.5 MB (47508389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d82de1962f8aea587dc96507c61f4532e0492a7486c0464424909c9a287d4`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:04a3aa984984cc7e2e3063d865bf62b0f49d1c7ecb8aa1c3204717d38b115f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d3ff5908e1cdb4d0bff4368546e85af9f3da9117b657e2d14fcc7a8cc46df`

```dockerfile
```

-	Layers:
	-	`sha256:d974d7a987a8a2d1e72455e2e7281893be7e4de5980f6b05ef538d9525eac5ad`  
		Last Modified: Thu, 18 Dec 2025 04:10:44 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c127714cbcc3b651d10c37ff43afa00f119fb595dfa041cae741b5e6ed773`  
		Last Modified: Thu, 18 Dec 2025 04:10:45 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:088e42947073420f9ebde2eb5d8bab8f9181bca4aa2ce68489825f098bf8c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47125075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49ac065a809cf09a162068ca036c38f5628b53ce26a833f2a94cd2e5609fd9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:01 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f737350ac794161f26d63aadebc1bef9562e1b5145b8de73ef57db6afa0e07`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 461.4 KB (461443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bafdabef314d9c0aa348705c8e18f7c41ccaeb27138426e29133e0d94847`  
		Last Modified: Thu, 18 Dec 2025 00:48:24 GMT  
		Size: 43.1 MB (43094831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6064d2d82dbe21bc8205771bd41cf5fba61bc9662afdef68e431208574b3cb9`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:e1d5a37fc3d7604403838d16bd28b6aebecbc232f421cd887deb8b86d3ac022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b7b588d832edae2cc1791cf2822ed4e7ab9df8e0466a9b32ea438e42044a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2bbed655619f17a9a92d9c84e19b7bffd4d0ac0643f30961edf86b8fc64032f0`  
		Last Modified: Thu, 18 Dec 2025 04:10:49 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4df45c2d1101f440d989afb8d54ce557fda8c1028c63b4edb46e1387f20e252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73051e3972adbd5fd7ac7a30bf363b919b805fc5a85b0c184fecdc8aafc69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:14 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776aff3ebb03754e9132ac99fdd3d55913a018df4553600e28c9b49ccb9359d`  
		Last Modified: Thu, 18 Dec 2025 00:39:47 GMT  
		Size: 43.2 MB (43235898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:0235f3573f63d55abfba7e9261bf749903b82ceb1338599b1dad8a7457aaadda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31ba6077556b5e469a5042279cc8a5d05f7d569a572d96e0dee0eaa7bd8b32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8220b97c6c54a61453867e3810ee63c84d079615a999974bb4c1cad060c68b`  
		Last Modified: Thu, 18 Dec 2025 04:10:52 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d83b4e84773fd95b32005cacfcbf43bfc22a2454bf16bfb8fd74072b564c2b`  
		Last Modified: Thu, 18 Dec 2025 04:10:53 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:f1bb2c5a12839909a38cbf8956a86a7de79a037d555cc29f1ac5ee281cb394a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c62d1ceea76fe16ce12841e2c9bcfc6df89a0cefc88ced9f5775f0201b1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:34:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:30 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:34:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ae93456d87a4319c334c68d8fe973661c62477820d71cbe214b3e3cf1596`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 41.3 MB (41258571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf953c6ec94ddbc562a208b274133f72e6e82689b6a4b337026df0994d1f0`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:0c178d2363efe5881ba2974fd5e15298b184c9f8d5a796ddc386bae7933c6752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374a0d4f6058bebc837f4c842459d396c9e6019f0b7563916122e36541f2419`

```dockerfile
```

-	Layers:
	-	`sha256:12c32f74f9c3051a06ec488f6838aea96b398fdf6e4fc6b49e438432ea420060`  
		Last Modified: Thu, 18 Dec 2025 04:10:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe6e9400e9638d6fdbda5dc01ea957d910d9fc60572973c5dcd8fa3dfc53099`  
		Last Modified: Thu, 18 Dec 2025 04:10:57 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:76f8fd7ae4b31a0b6b2534fb2b8382cdc1d20c1bbb16b021752bff223e53c362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe4361adc8d61b5640d8c41b11d9f96aeb226edd04fafdc0e8f820cfb97cfd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:36:31 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:36:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3795c96879d916d2c0c23f5dbe72e6a8e975208f3ee6c8589eb580db38822df`  
		Last Modified: Fri, 19 Dec 2025 05:41:58 GMT  
		Size: 45.8 MB (45795470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:39fe38828762408de37a606fb37a23ec2f45786dbbe06be33bfa482427399ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efa933315fec9b05e8e114af019de92ac7ec9e847df1142ea3ed0ebeb1e98d`

```dockerfile
```

-	Layers:
	-	`sha256:5d163d50d63b3ac0863f070ba4ea01fc52cb951173af525823de84928f516e28`  
		Last Modified: Fri, 19 Dec 2025 07:09:46 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01bf93423650c650bc0a55016bc1ea02e2d9cdb068f8689e2f84217908071ee3`  
		Last Modified: Fri, 19 Dec 2025 07:09:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:06d55534e41116deeffadfa188514bf9e1f842e76aef6cee98d881377914b349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49845032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b6cc6713d31eb6184651ce332a7209009863e54eb9fbdbc0e4255a9219543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:12:51 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:12:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b16a0de9ead22663a13405f975f967ff4dbd8fa6266070a070f9ba99948182`  
		Last Modified: Thu, 18 Dec 2025 01:14:11 GMT  
		Size: 45.7 MB (45658610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac41c55a8b3896d166b9c150fcf8cdd21d465e6db49bbcdf4d43b499a0adaa6`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:6f7736f1bcf95ddae038700b2f1e3a3392fd727d4ecd85b1103479a67fe82b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce3fef82d410be2a6681ee56f228ad9a602bf53f0786c5830c57b38b7624b4`

```dockerfile
```

-	Layers:
	-	`sha256:52bcbcbf682af9f97e31167002fd644577bfe589100690db9a0b7e618fa4b5cb`  
		Last Modified: Thu, 18 Dec 2025 04:11:02 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28153da3bfe5ff9102d0509bdd95f0ef8662f190b8e03b68eaa9e1bfc6075b3c`  
		Last Modified: Thu, 18 Dec 2025 04:11:03 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6`

```console
$ docker pull traefik@sha256:67622638cd88dbfcfba40159bc652ecf0aea0e032f8a3c7e3134ae7c037b9910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3.6` - linux; amd64

```console
$ docker pull traefik@sha256:d944e3693bbf5a361ddd2e411bb713049cfb4f5ff3da200b30ee7a347dbd6abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb158a64eaac3b411525e180705dbb4e120d078150b6a795e120e6b80e81b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:33 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e627467d86762f7d43dc795a23361ae2c3f587d554d237f08e8b851a00bedd1`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489626b3f9620aab9962ec32de70229fb411c6304b6fa465f36501e2c9fb591`  
		Last Modified: Thu, 18 Dec 2025 00:38:13 GMT  
		Size: 47.5 MB (47508389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d82de1962f8aea587dc96507c61f4532e0492a7486c0464424909c9a287d4`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:04a3aa984984cc7e2e3063d865bf62b0f49d1c7ecb8aa1c3204717d38b115f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d3ff5908e1cdb4d0bff4368546e85af9f3da9117b657e2d14fcc7a8cc46df`

```dockerfile
```

-	Layers:
	-	`sha256:d974d7a987a8a2d1e72455e2e7281893be7e4de5980f6b05ef538d9525eac5ad`  
		Last Modified: Thu, 18 Dec 2025 04:10:44 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c127714cbcc3b651d10c37ff43afa00f119fb595dfa041cae741b5e6ed773`  
		Last Modified: Thu, 18 Dec 2025 04:10:45 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm variant v6

```console
$ docker pull traefik@sha256:088e42947073420f9ebde2eb5d8bab8f9181bca4aa2ce68489825f098bf8c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47125075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49ac065a809cf09a162068ca036c38f5628b53ce26a833f2a94cd2e5609fd9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:01 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f737350ac794161f26d63aadebc1bef9562e1b5145b8de73ef57db6afa0e07`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 461.4 KB (461443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bafdabef314d9c0aa348705c8e18f7c41ccaeb27138426e29133e0d94847`  
		Last Modified: Thu, 18 Dec 2025 00:48:24 GMT  
		Size: 43.1 MB (43094831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6064d2d82dbe21bc8205771bd41cf5fba61bc9662afdef68e431208574b3cb9`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:e1d5a37fc3d7604403838d16bd28b6aebecbc232f421cd887deb8b86d3ac022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b7b588d832edae2cc1791cf2822ed4e7ab9df8e0466a9b32ea438e42044a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2bbed655619f17a9a92d9c84e19b7bffd4d0ac0643f30961edf86b8fc64032f0`  
		Last Modified: Thu, 18 Dec 2025 04:10:49 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4df45c2d1101f440d989afb8d54ce557fda8c1028c63b4edb46e1387f20e252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73051e3972adbd5fd7ac7a30bf363b919b805fc5a85b0c184fecdc8aafc69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:14 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776aff3ebb03754e9132ac99fdd3d55913a018df4553600e28c9b49ccb9359d`  
		Last Modified: Thu, 18 Dec 2025 00:39:47 GMT  
		Size: 43.2 MB (43235898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0235f3573f63d55abfba7e9261bf749903b82ceb1338599b1dad8a7457aaadda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31ba6077556b5e469a5042279cc8a5d05f7d569a572d96e0dee0eaa7bd8b32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8220b97c6c54a61453867e3810ee63c84d079615a999974bb4c1cad060c68b`  
		Last Modified: Thu, 18 Dec 2025 04:10:52 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d83b4e84773fd95b32005cacfcbf43bfc22a2454bf16bfb8fd74072b564c2b`  
		Last Modified: Thu, 18 Dec 2025 04:10:53 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; ppc64le

```console
$ docker pull traefik@sha256:f1bb2c5a12839909a38cbf8956a86a7de79a037d555cc29f1ac5ee281cb394a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c62d1ceea76fe16ce12841e2c9bcfc6df89a0cefc88ced9f5775f0201b1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:34:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:30 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:34:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ae93456d87a4319c334c68d8fe973661c62477820d71cbe214b3e3cf1596`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 41.3 MB (41258571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf953c6ec94ddbc562a208b274133f72e6e82689b6a4b337026df0994d1f0`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:0c178d2363efe5881ba2974fd5e15298b184c9f8d5a796ddc386bae7933c6752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374a0d4f6058bebc837f4c842459d396c9e6019f0b7563916122e36541f2419`

```dockerfile
```

-	Layers:
	-	`sha256:12c32f74f9c3051a06ec488f6838aea96b398fdf6e4fc6b49e438432ea420060`  
		Last Modified: Thu, 18 Dec 2025 04:10:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe6e9400e9638d6fdbda5dc01ea957d910d9fc60572973c5dcd8fa3dfc53099`  
		Last Modified: Thu, 18 Dec 2025 04:10:57 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; riscv64

```console
$ docker pull traefik@sha256:76f8fd7ae4b31a0b6b2534fb2b8382cdc1d20c1bbb16b021752bff223e53c362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe4361adc8d61b5640d8c41b11d9f96aeb226edd04fafdc0e8f820cfb97cfd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:36:31 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:36:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3795c96879d916d2c0c23f5dbe72e6a8e975208f3ee6c8589eb580db38822df`  
		Last Modified: Fri, 19 Dec 2025 05:41:58 GMT  
		Size: 45.8 MB (45795470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:39fe38828762408de37a606fb37a23ec2f45786dbbe06be33bfa482427399ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efa933315fec9b05e8e114af019de92ac7ec9e847df1142ea3ed0ebeb1e98d`

```dockerfile
```

-	Layers:
	-	`sha256:5d163d50d63b3ac0863f070ba4ea01fc52cb951173af525823de84928f516e28`  
		Last Modified: Fri, 19 Dec 2025 07:09:46 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01bf93423650c650bc0a55016bc1ea02e2d9cdb068f8689e2f84217908071ee3`  
		Last Modified: Fri, 19 Dec 2025 07:09:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6` - linux; s390x

```console
$ docker pull traefik@sha256:06d55534e41116deeffadfa188514bf9e1f842e76aef6cee98d881377914b349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49845032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b6cc6713d31eb6184651ce332a7209009863e54eb9fbdbc0e4255a9219543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:12:51 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:12:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b16a0de9ead22663a13405f975f967ff4dbd8fa6266070a070f9ba99948182`  
		Last Modified: Thu, 18 Dec 2025 01:14:11 GMT  
		Size: 45.7 MB (45658610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac41c55a8b3896d166b9c150fcf8cdd21d465e6db49bbcdf4d43b499a0adaa6`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6` - unknown; unknown

```console
$ docker pull traefik@sha256:6f7736f1bcf95ddae038700b2f1e3a3392fd727d4ecd85b1103479a67fe82b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce3fef82d410be2a6681ee56f228ad9a602bf53f0786c5830c57b38b7624b4`

```dockerfile
```

-	Layers:
	-	`sha256:52bcbcbf682af9f97e31167002fd644577bfe589100690db9a0b7e618fa4b5cb`  
		Last Modified: Thu, 18 Dec 2025 04:11:02 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28153da3bfe5ff9102d0509bdd95f0ef8662f190b8e03b68eaa9e1bfc6075b3c`  
		Last Modified: Thu, 18 Dec 2025 04:11:03 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.5`

```console
$ docker pull traefik@sha256:67622638cd88dbfcfba40159bc652ecf0aea0e032f8a3c7e3134ae7c037b9910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3.6.5` - linux; amd64

```console
$ docker pull traefik@sha256:d944e3693bbf5a361ddd2e411bb713049cfb4f5ff3da200b30ee7a347dbd6abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51829800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb158a64eaac3b411525e180705dbb4e120d078150b6a795e120e6b80e81b02`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:37:31 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:37:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:37:33 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:37:33 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e627467d86762f7d43dc795a23361ae2c3f587d554d237f08e8b851a00bedd1`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 460.9 KB (460938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9489626b3f9620aab9962ec32de70229fb411c6304b6fa465f36501e2c9fb591`  
		Last Modified: Thu, 18 Dec 2025 00:38:13 GMT  
		Size: 47.5 MB (47508389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d82de1962f8aea587dc96507c61f4532e0492a7486c0464424909c9a287d4`  
		Last Modified: Thu, 18 Dec 2025 00:38:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:04a3aa984984cc7e2e3063d865bf62b0f49d1c7ecb8aa1c3204717d38b115f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.9 KB (855900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44d3ff5908e1cdb4d0bff4368546e85af9f3da9117b657e2d14fcc7a8cc46df`

```dockerfile
```

-	Layers:
	-	`sha256:d974d7a987a8a2d1e72455e2e7281893be7e4de5980f6b05ef538d9525eac5ad`  
		Last Modified: Thu, 18 Dec 2025 04:10:44 GMT  
		Size: 843.1 KB (843134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c127714cbcc3b651d10c37ff43afa00f119fb595dfa041cae741b5e6ed773`  
		Last Modified: Thu, 18 Dec 2025 04:10:45 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:088e42947073420f9ebde2eb5d8bab8f9181bca4aa2ce68489825f098bf8c162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47125075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49ac065a809cf09a162068ca036c38f5628b53ce26a833f2a94cd2e5609fd9c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:47:58 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:48:00 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:48:01 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:48:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:48:01 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:48:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f737350ac794161f26d63aadebc1bef9562e1b5145b8de73ef57db6afa0e07`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 461.4 KB (461443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2bafdabef314d9c0aa348705c8e18f7c41ccaeb27138426e29133e0d94847`  
		Last Modified: Thu, 18 Dec 2025 00:48:24 GMT  
		Size: 43.1 MB (43094831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6064d2d82dbe21bc8205771bd41cf5fba61bc9662afdef68e431208574b3cb9`  
		Last Modified: Thu, 18 Dec 2025 00:48:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:e1d5a37fc3d7604403838d16bd28b6aebecbc232f421cd887deb8b86d3ac022e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b7b588d832edae2cc1791cf2822ed4e7ab9df8e0466a9b32ea438e42044a3a`

```dockerfile
```

-	Layers:
	-	`sha256:2bbed655619f17a9a92d9c84e19b7bffd4d0ac0643f30961edf86b8fc64032f0`  
		Last Modified: Thu, 18 Dec 2025 04:10:49 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:4df45c2d1101f440d989afb8d54ce557fda8c1028c63b4edb46e1387f20e252d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47894998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d73051e3972adbd5fd7ac7a30bf363b919b805fc5a85b0c184fecdc8aafc69c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:39:11 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:39:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:39:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 00:39:14 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 00:39:14 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa85ac6768b81add38b2157853ff07f4244c4430f913c15f1fd951590a92038e`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 463.0 KB (462991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1776aff3ebb03754e9132ac99fdd3d55913a018df4553600e28c9b49ccb9359d`  
		Last Modified: Thu, 18 Dec 2025 00:39:47 GMT  
		Size: 43.2 MB (43235898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e4731fd100ca4a239094f921710cc63383a6025594d450d9f6b88d72339710`  
		Last Modified: Thu, 18 Dec 2025 00:39:44 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:0235f3573f63d55abfba7e9261bf749903b82ceb1338599b1dad8a7457aaadda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac31ba6077556b5e469a5042279cc8a5d05f7d569a572d96e0dee0eaa7bd8b32`

```dockerfile
```

-	Layers:
	-	`sha256:8f8220b97c6c54a61453867e3810ee63c84d079615a999974bb4c1cad060c68b`  
		Last Modified: Thu, 18 Dec 2025 04:10:52 GMT  
		Size: 842.6 KB (842588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79d83b4e84773fd95b32005cacfcbf43bfc22a2454bf16bfb8fd74072b564c2b`  
		Last Modified: Thu, 18 Dec 2025 04:10:53 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:f1bb2c5a12839909a38cbf8956a86a7de79a037d555cc29f1ac5ee281cb394a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4670c62d1ceea76fe16ce12841e2c9bcfc6df89a0cefc88ced9f5775f0201b1c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:34:23 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:34:29 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:34:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:34:30 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:34:30 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58d90cbc798211f739b91be6d27031a0efce31b2fc966844549b707f0bf2182`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 463.5 KB (463511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd46ae93456d87a4319c334c68d8fe973661c62477820d71cbe214b3e3cf1596`  
		Last Modified: Thu, 18 Dec 2025 01:35:34 GMT  
		Size: 41.3 MB (41258571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fcf953c6ec94ddbc562a208b274133f72e6e82689b6a4b337026df0994d1f0`  
		Last Modified: Thu, 18 Dec 2025 01:35:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:0c178d2363efe5881ba2974fd5e15298b184c9f8d5a796ddc386bae7933c6752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7374a0d4f6058bebc837f4c842459d396c9e6019f0b7563916122e36541f2419`

```dockerfile
```

-	Layers:
	-	`sha256:12c32f74f9c3051a06ec488f6838aea96b398fdf6e4fc6b49e438432ea420060`  
		Last Modified: Thu, 18 Dec 2025 04:10:56 GMT  
		Size: 842.5 KB (842541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe6e9400e9638d6fdbda5dc01ea957d910d9fc60572973c5dcd8fa3dfc53099`  
		Last Modified: Thu, 18 Dec 2025 04:10:57 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; riscv64

```console
$ docker pull traefik@sha256:76f8fd7ae4b31a0b6b2534fb2b8382cdc1d20c1bbb16b021752bff223e53c362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49840968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe4361adc8d61b5640d8c41b11d9f96aeb226edd04fafdc0e8f820cfb97cfd4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 05:36:19 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
COPY entrypoint.sh / # buildkit
# Fri, 19 Dec 2025 05:36:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Dec 2025 05:36:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 19 Dec 2025 05:36:31 GMT
CMD ["traefik"]
# Fri, 19 Dec 2025 05:36:31 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e01ca8591dbea77d9ad65c846f0bfe88790e18d13b37bcceca11b8b2258890`  
		Last Modified: Fri, 19 Dec 2025 05:41:52 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3795c96879d916d2c0c23f5dbe72e6a8e975208f3ee6c8589eb580db38822df`  
		Last Modified: Fri, 19 Dec 2025 05:41:58 GMT  
		Size: 45.8 MB (45795470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdd9265ad12000df0608cc572b22a51c5724734e08cc803d3ff263679d3c53d`  
		Last Modified: Tue, 16 Dec 2025 22:02:26 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:39fe38828762408de37a606fb37a23ec2f45786dbbe06be33bfa482427399ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efa933315fec9b05e8e114af019de92ac7ec9e847df1142ea3ed0ebeb1e98d`

```dockerfile
```

-	Layers:
	-	`sha256:5d163d50d63b3ac0863f070ba4ea01fc52cb951173af525823de84928f516e28`  
		Last Modified: Fri, 19 Dec 2025 07:09:46 GMT  
		Size: 842.5 KB (842537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01bf93423650c650bc0a55016bc1ea02e2d9cdb068f8689e2f84217908071ee3`  
		Last Modified: Fri, 19 Dec 2025 07:09:47 GMT  
		Size: 12.8 KB (12836 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.6.5` - linux; s390x

```console
$ docker pull traefik@sha256:06d55534e41116deeffadfa188514bf9e1f842e76aef6cee98d881377914b349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49845032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5b6cc6713d31eb6184651ce332a7209009863e54eb9fbdbc0e4255a9219543`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 01:12:47 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
COPY entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 01:12:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 01:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 18 Dec 2025 01:12:51 GMT
CMD ["traefik"]
# Thu, 18 Dec 2025 01:12:51 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe513b91d35261d41996463d097ba18535d3059637882deb700bbc747e5a3e4`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 461.7 KB (461742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b16a0de9ead22663a13405f975f967ff4dbd8fa6266070a070f9ba99948182`  
		Last Modified: Thu, 18 Dec 2025 01:14:11 GMT  
		Size: 45.7 MB (45658610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac41c55a8b3896d166b9c150fcf8cdd21d465e6db49bbcdf4d43b499a0adaa6`  
		Last Modified: Thu, 18 Dec 2025 01:14:06 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.6.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6f7736f1bcf95ddae038700b2f1e3a3392fd727d4ecd85b1103479a67fe82b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.2 KB (855249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ce3fef82d410be2a6681ee56f228ad9a602bf53f0786c5830c57b38b7624b4`

```dockerfile
```

-	Layers:
	-	`sha256:52bcbcbf682af9f97e31167002fd644577bfe589100690db9a0b7e618fa4b5cb`  
		Last Modified: Thu, 18 Dec 2025 04:11:02 GMT  
		Size: 842.5 KB (842483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28153da3bfe5ff9102d0509bdd95f0ef8662f190b8e03b68eaa9e1bfc6075b3c`  
		Last Modified: Thu, 18 Dec 2025 04:11:03 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.6.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:691b0525f33a4cdabfbc55a8bf7c5cf662beeec9d4adb86f4f4b2af86287cadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6.5-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:99ac9b41a47169bbfdeec08d9503d34cd651c25a0e727f3096c1b8f8eede8015
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174626007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce84bb67b36812be78f4295025e25f1e5525d3b77c4f31d16914d8c749eae231`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Tue, 16 Dec 2025 22:10:30 GMT
RUN cmd /S /C #(nop) COPY file:e715893758111c86ceaf8cc73bc45b1d3daa199fa85a47fac868aef4abefc1d6 in \ 
# Tue, 16 Dec 2025 22:10:32 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 16 Dec 2025 22:10:33 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 22:10:34 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aef87f7f4a0a1be913e4f3a551c412dbde57684b2194d3d3999124b8cd2636`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 48.3 MB (48264487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de1335b2f2e242c2a1c9178d5421026b0254fca0c70106be56d31142516e0218`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb92daa195f64ea506c1df56e258fd13a28d26b52b39f84c62351625f6f3991`  
		Last Modified: Tue, 16 Dec 2025 22:11:17 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736a7f8b7a26a2d8c940bf0649e1745e8bc2040d935aa91983fb1ce8917d82a4`  
		Last Modified: Tue, 16 Dec 2025 22:11:24 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.6.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:v3.6.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:42621e95e357a9ace77c10ce9dabc9d14a193791e6d649a73008e6bbb49139ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull traefik@sha256:0545aeec9a3cfc0a3e70f5f362d809fb2162a447e7238f40fbd6d2c9d19e2079
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828809739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2e2809930be7fd01d91031e730a89281f1ed5179aac935be3475863bf14747`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 21:57:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 21:58:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.6.5/traefik_v3.6.5_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 16 Dec 2025 21:58:22 GMT
EXPOSE 80
# Tue, 16 Dec 2025 21:58:23 GMT
ENTRYPOINT ["/traefik"]
# Tue, 16 Dec 2025 21:58:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:734674e5f0cd9d7f13ac2e704e3f6f0f7a7d97a698d98452896b32a1cf07d3d9`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9606d00de0777137c10f2b6026d808f89a3610c0d28d4f9afa55f4c7444065f2`  
		Last Modified: Tue, 16 Dec 2025 22:03:47 GMT  
		Size: 48.9 MB (48925234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad753c5e5799c3f2f9d6865c6d596246904756be4831b3ceec105d0a1248d46`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415324d16bc9e0268972e3b49de0b1f0a305eb079af37bb1ebced1011bc2315c`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0178f297a05f0dacd0465df7f7b08b50fbeb1625864e5d1e425b97eff6cba1c5`  
		Last Modified: Tue, 16 Dec 2025 22:03:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
