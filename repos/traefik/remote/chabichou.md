## `traefik:chabichou`

```console
$ docker pull traefik@sha256:4df0a50fcf71b454c0d7ad17675776dc8d37359deae3291895bdaa008c1b9972
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

### `traefik:chabichou` - linux; amd64

```console
$ docker pull traefik@sha256:7d0441d7b82d85362d169ab2f2adfa731e88373f635874ae1f235050f27432a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50620944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8113f16a03a3f01546afa0ac6312322d06294194357e108d819d35a682dfe0f2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:48:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:48:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.4/traefik_v3.5.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:48:22 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:48:22 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:48:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:48:22 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:48:22 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00939ba87b7449ce79fe30ee20b827d2e64994002fa5d4d9d72bbbea34ee90e`  
		Last Modified: Tue, 28 Oct 2025 17:48:57 GMT  
		Size: 456.9 KB (456932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60757a8b58e9bdad01986163dc884d35d4de71a151498417f78655f12dbe9ddf`  
		Last Modified: Tue, 28 Oct 2025 17:49:01 GMT  
		Size: 46.4 MB (46361191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a69748b0bf354f6571707c61a9ff3a061d64f56cbe3c6ce36c4019abe4a10`  
		Last Modified: Tue, 28 Oct 2025 17:48:57 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:c1e1d97ce875a356077320767c44c8e1a217f68dd7a20e65300a3401005141ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **850.3 KB (850322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d8df97efd19fff720a65c603c132fa1f721da676ba7784dbfc6acd653e6001`

```dockerfile
```

-	Layers:
	-	`sha256:965bb81123f90573ad4d8b8e4a43013d3472ce67b589bbc5e1bdf41b6e439fe0`  
		Last Modified: Tue, 28 Oct 2025 18:10:54 GMT  
		Size: 837.6 KB (837554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c957d0e4281c0f61a0028dbd7b7232a3ca4b1e3c98e0be7d10ed64504148883`  
		Last Modified: Tue, 28 Oct 2025 18:10:55 GMT  
		Size: 12.8 KB (12768 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm variant v6

```console
$ docker pull traefik@sha256:97ef9ea9c69ce13a3a1bfee193c24856cc41547dcef4566ccb27f61a0ae68d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45944129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04d9f66e8d850623f48cdb0425789f57e39cc4b30fee45fe4f45c1edd06b3a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:46:57 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.4/traefik_v3.5.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:20 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:20 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee012da75e6d19d90dcdb3dfa5c0e71e36337095ea8bb050a2331f4e9137a7`  
		Last Modified: Tue, 28 Oct 2025 17:47:21 GMT  
		Size: 457.7 KB (457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef924852f322fcbfd5f863576b6767e547dd8a68ea03d34f7dfe7692a39b34`  
		Last Modified: Tue, 28 Oct 2025 17:47:56 GMT  
		Size: 42.0 MB (41981937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9616c26ab57c85518ab7436caf6e0ab1656873d1472897d1e7aa0217d89a22`  
		Last Modified: Tue, 28 Oct 2025 17:47:39 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:0edc8841b13b1faf2869f07d81e0fdf1e9b5258000917439b4787ab838e3b924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e457ccacb10b2a8912a656491aab6bb35b88376c9b829196f956e82ffbac6e`

```dockerfile
```

-	Layers:
	-	`sha256:e109a0a032cc508f291abf69ab8fb02c8dcd9ffb29b7dc12b9581029fe854033`  
		Last Modified: Tue, 28 Oct 2025 18:10:58 GMT  
		Size: 12.7 KB (12676 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:38aa2228f32f3f484beb433fc70ebb0024ed9f0067a37009b82a3a00fadc3f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46788755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec94ecae4a631056bd20825e44eef55cc69864fbc5a0f48b2cf3c3708ab2d8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 28 Oct 2025 17:47:45 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:47:47 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.4/traefik_v3.5.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:47:47 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:47:47 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:47:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:47:47 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:47:47 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0021398a2f5b215fe281ca59c29074cc3e49041f719ed5647e4d3ff7a55128`  
		Last Modified: Tue, 28 Oct 2025 17:48:19 GMT  
		Size: 459.0 KB (459018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169731141c9b1ceca648b35ccdc7a724be9fd8369310c9abccd2ba183401348d`  
		Last Modified: Tue, 28 Oct 2025 17:48:23 GMT  
		Size: 42.2 MB (42191300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a873af3b6642aa4f82ed449868b5be5f3e51a1ae97d3f5bc6514afc66e028f`  
		Last Modified: Tue, 28 Oct 2025 17:48:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:4983ad0a599f3094064b116c2228b16bddadc2c3287269233f857ed5cd19fbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **850.6 KB (850591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ae8e97ad0f2c50523b8a6dd980eaffa34f32f336d16c4c6990eab18bd714f0`

```dockerfile
```

-	Layers:
	-	`sha256:98db2c29a470d7697f79a02536aeb134b124fac1b5b2b640c061c6392c713d31`  
		Last Modified: Tue, 28 Oct 2025 18:11:02 GMT  
		Size: 837.7 KB (837658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2372d935c34b92c0253478ce0bdea510a0d8eb1e5b1995a2c93c5e550e78db59`  
		Last Modified: Tue, 28 Oct 2025 18:11:03 GMT  
		Size: 12.9 KB (12933 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; ppc64le

```console
$ docker pull traefik@sha256:f01bd0a055bf50393f104276e13f46429446b1a2266a9364c19b27e8dd447b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44385463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e275f73109e2f99312ef98a562e7c8060db74c3964ff8604fcaa27a107032c80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 03:32:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:48:01 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.4/traefik_v3.5.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:48:02 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:48:02 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:48:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:48:02 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:48:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a476383bb2bb2988acf2098cf20bed14bd4441bc69c2acd614a2184dbd44d8a8`  
		Last Modified: Thu, 09 Oct 2025 03:33:23 GMT  
		Size: 459.4 KB (459426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fe9c3d492bcfd24b149c06eb4525caf2d8f77ce0855ca6c59405a3dab5e9c4`  
		Last Modified: Tue, 28 Oct 2025 17:49:27 GMT  
		Size: 40.2 MB (40193427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbad6ece6648f4b41ce8666b18e1e595a5e58a7cb2acc606a31545f11b72f13`  
		Last Modified: Tue, 28 Oct 2025 17:49:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:dc8df66a14605cd613f999b0625752a821c9d84d0de806d97782a9492a744322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **848.5 KB (848499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9adb4553b22b13f8ba13122e47e86231fc8734b537cfd9adf370838defa8cf24`

```dockerfile
```

-	Layers:
	-	`sha256:bbd77b7b539835a858d3b8354e3ca40663643f52b4bd5fed7ac02de93d277c81`  
		Last Modified: Tue, 28 Oct 2025 18:11:06 GMT  
		Size: 835.7 KB (835661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936032d94e57898282a27a683730d0c9d0261cf344950546b53433bfc4d05f75`  
		Last Modified: Tue, 28 Oct 2025 18:11:07 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; riscv64

```console
$ docker pull traefik@sha256:273abc4e705dff76827bb087535df0cb192846e567f2516127c26bded998c149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48651125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8838f5155f6cc560ec728150bd37127e6df2ea2572aac1706e8d6f24a1ba281`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 29 Oct 2025 15:02:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 29 Oct 2025 15:09:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.4/traefik_v3.5.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 29 Oct 2025 15:09:11 GMT
COPY entrypoint.sh / # buildkit
# Wed, 29 Oct 2025 15:09:11 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 Oct 2025 15:09:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 29 Oct 2025 15:09:11 GMT
CMD ["traefik"]
# Wed, 29 Oct 2025 15:09:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3734c19de58da4f3bd4df579f0943d0967f596e3a1e2aa541e119d14638340`  
		Last Modified: Wed, 29 Oct 2025 15:08:21 GMT  
		Size: 457.3 KB (457265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ae7b686743dfe820b2fdc84d5f2f13cd12cc79a7db71c20f208da14ffc3c32`  
		Last Modified: Wed, 29 Oct 2025 15:13:56 GMT  
		Size: 44.7 MB (44678252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436a0537d2dc9427f0256d09c36dbfbbc44fc61f700084ce76f7d1d6716e0ed7`  
		Last Modified: Wed, 29 Oct 2025 15:13:53 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:1b094d2eeec9f70708b5ac683a14cfaed7a401600aefddd79ce454e29cf4c229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **848.5 KB (848495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52519664692bd3647b8947d1ae6b86952663c85f227715e6dff9607834be8f74`

```dockerfile
```

-	Layers:
	-	`sha256:b2c5de76f3491e75bc56c43371f50f405dd5776835c7b37ee64d940977f2ed11`  
		Last Modified: Wed, 29 Oct 2025 18:09:40 GMT  
		Size: 835.7 KB (835657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa56cdf8b88ef3be9441b394fd4afd3f10b51095aa04ac3fa0b87f61b9a650e`  
		Last Modified: Wed, 29 Oct 2025 18:09:41 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; s390x

```console
$ docker pull traefik@sha256:31d9e2c543521b504a04af1970fb81ca733264eb9d373aa224a4d1637d9e7d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48617303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8e1c3f90fa404566e41c1a20dcb176006732b2424309c525a4c1359c500062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 02:26:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 28 Oct 2025 17:50:53 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.4/traefik_v3.5.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 28 Oct 2025 17:50:53 GMT
COPY entrypoint.sh / # buildkit
# Tue, 28 Oct 2025 17:50:53 GMT
EXPOSE map[80/tcp:{}]
# Tue, 28 Oct 2025 17:50:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 28 Oct 2025 17:50:53 GMT
CMD ["traefik"]
# Tue, 28 Oct 2025 17:50:53 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6155014a1d77a7bc8a35aaadb5baad965e9e640c5be73a93d70e92988712af6d`  
		Last Modified: Thu, 09 Oct 2025 02:27:09 GMT  
		Size: 457.9 KB (457905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be55c5df39c991115007d60c151f79b02c9b710ca268800e3d12a10b429aca28`  
		Last Modified: Tue, 28 Oct 2025 17:51:55 GMT  
		Size: 44.5 MB (44509786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a60e15872d831c243a2ee42049879400adce2df13d45f630dfb2772fea771df`  
		Last Modified: Tue, 28 Oct 2025 17:51:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:fa2002c4469015a3b405d17cae8f11c812d7fb90bed30d71bd751e3fa63fc9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **848.4 KB (848371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a570ca91c671e44183753b6e60b1ff3d8848c2613c916d13777b668350079d4`

```dockerfile
```

-	Layers:
	-	`sha256:ea2308cfbb522869218770dbfe671f16b2374f23a2a14c148c84096259b0613a`  
		Last Modified: Tue, 28 Oct 2025 18:11:13 GMT  
		Size: 835.6 KB (835603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5aa947e76fc01ff82e09c209db530b144ab277f5d4be35ff81cedfaab382f4`  
		Last Modified: Tue, 28 Oct 2025 18:11:13 GMT  
		Size: 12.8 KB (12768 bytes)  
		MIME: application/vnd.in-toto+json
