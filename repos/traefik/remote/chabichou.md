## `traefik:chabichou`

```console
$ docker pull traefik@sha256:ec3cddc799808d091b1143615a872f89b25c9c8893a2a358cfeea59d2d058d14
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
$ docker pull traefik@sha256:2bddf078a1b4c7308c71b3a33a9828c4e4041175c53adedf0b870aafb98793a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58067544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43bea882a18132089137e58f836cb7d407dc40918dcb2ee1366e0f66e6f2c77`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0-rc1/traefik_v3.5.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
COPY entrypoint.sh / # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Jun 2025 15:08:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
CMD ["traefik"]
# Thu, 26 Jun 2025 15:08:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebf1c046be3dec331ad29a52d8b632867a9ee0abcf7520884c5402db2adcb5d`  
		Last Modified: Thu, 26 Jun 2025 21:13:21 GMT  
		Size: 460.2 KB (460211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06aa9609ddc8be1a1c3d861440f2e4b79d1dfb5005b9ef6d2358b2f9fddcf6f`  
		Last Modified: Thu, 26 Jun 2025 21:13:24 GMT  
		Size: 54.0 MB (53964717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2372675007c3cdc89321250054f8e348f6f5e282c35b35abd91f809c4bea63b`  
		Last Modified: Thu, 26 Jun 2025 21:13:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:347f8310fe67ec78c31de669cfc6b7eb87bae4adf763c94bd9cc0efb6f7fb0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.0 KB (838004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f762ba8e54f2745170f027a849d84b2afba00c0b8e00bc99bb3b7486245a7f5f`

```dockerfile
```

-	Layers:
	-	`sha256:feff80e1d77e1a17d072f6fe9fc28eae95fdb1e52f580322300f1b990eea80d7`  
		Last Modified: Thu, 26 Jun 2025 21:10:34 GMT  
		Size: 826.6 KB (826625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c79b7b1b432837ecb3564c33e9d9cc04816e24409820e2fb6f7ac5afe0a48b9`  
		Last Modified: Thu, 26 Jun 2025 21:10:35 GMT  
		Size: 11.4 KB (11379 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm variant v6

```console
$ docker pull traefik@sha256:49b286d44e4ec5b0270c25b76062738e453889118565d512ace24e19e4e31994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53196695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c302bddf8ca3671b0c12d18640fee2420ce1b48a488c59aefff5b5a8a715660`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0-rc1/traefik_v3.5.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
COPY entrypoint.sh / # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Jun 2025 15:08:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
CMD ["traefik"]
# Thu, 26 Jun 2025 15:08:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Sat, 15 Feb 2025 01:09:48 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7548da87e9d7f6fb4a4425b868ec112761ab1860a065e734f8701930c6cf65`  
		Last Modified: Thu, 26 Jun 2025 18:45:21 GMT  
		Size: 49.4 MB (49372171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4108224622f48820d39c987571979fb2986d8c3836bff3a06b6d8c56f7b57db0`  
		Last Modified: Thu, 26 Jun 2025 18:45:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:fd74302c161999ebf7f998390641f55d0072cb3b3d6703b5db8b35ee3c23568a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 KB (11245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58aee3067c594d158ea215fb7babe14e03059be4e79fcbce1c01265280e5a38e`

```dockerfile
```

-	Layers:
	-	`sha256:866b3a120f1fad3494926fbbbd598e640a8d4e5c79c2c0db9d47fbf25f14c5b8`  
		Last Modified: Thu, 26 Jun 2025 21:10:38 GMT  
		Size: 11.2 KB (11245 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:644fd859b2e8be17d825034006be0f2ada1c6534381c54d19d3773835dd22097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53902589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0941f86c8ccd36a46eab0877572020b0ddc589c1c4109b65ae8eb480548fca6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0-rc1/traefik_v3.5.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
COPY entrypoint.sh / # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Jun 2025 15:08:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
CMD ["traefik"]
# Thu, 26 Jun 2025 15:08:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a753a32681602147167204e80ea784846efb10c32651855619d7703b6bf35b56`  
		Last Modified: Thu, 26 Jun 2025 19:06:22 GMT  
		Size: 462.1 KB (462074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846d6effcfe505f32e694136bcc61c02b4cecfd54781a473a1f61564edd6a539`  
		Last Modified: Thu, 26 Jun 2025 21:25:15 GMT  
		Size: 49.4 MB (49447117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4108224622f48820d39c987571979fb2986d8c3836bff3a06b6d8c56f7b57db0`  
		Last Modified: Thu, 26 Jun 2025 18:45:15 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:7a838c33d7f0901fee35308159f06eb14de7e4e925ad652f6763e1ed31378924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.2 KB (838155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586fc8933c61e012a266a21c4c58cbc982edcb8019b6eb5b5a2f1d6af74de1b0`

```dockerfile
```

-	Layers:
	-	`sha256:c4bb9f7f00f106b788d2b684f85ea3a63799e62c87fe9c3482da8a1c8d5a4398`  
		Last Modified: Thu, 26 Jun 2025 21:10:41 GMT  
		Size: 826.7 KB (826669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d27921720662ec53a5e68e3121dd5d61c6a7def5652698299e80b3238d94d71`  
		Last Modified: Thu, 26 Jun 2025 21:10:42 GMT  
		Size: 11.5 KB (11486 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; ppc64le

```console
$ docker pull traefik@sha256:b50f0796898691bc20eddb1e6d710471debf041f7f08b254e6addf2a9c97b8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51270508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b5c13a81cd6be08a67d532554bfd92ff5b18e9d1a65032bf29e5b5ffea502f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0-rc1/traefik_v3.5.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
COPY entrypoint.sh / # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Jun 2025 15:08:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
CMD ["traefik"]
# Thu, 26 Jun 2025 15:08:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d08a3034249c395b56cdbf5260622c9cbd32d023750a27e1c5522b91048d57`  
		Last Modified: Thu, 26 Jun 2025 18:46:35 GMT  
		Size: 462.6 KB (462579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cabfec5197fd5578c503c6853b19ff8af3a500ea2f06b898787d049551396c`  
		Last Modified: Thu, 26 Jun 2025 18:46:40 GMT  
		Size: 47.2 MB (47233214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b107445821ebc9ee181f00b1510cc4e2c7b8cab8c8d85174eaa6c13af7b9543`  
		Last Modified: Thu, 26 Jun 2025 18:46:35 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:96ce92bbdf7a9ca0fc48a5ba497be024aaf87de78dd7513501d2c201d5b49fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.1 KB (836121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beefbc1b808fc44979b765301c168a3bf685dafd6f2ed63a9c3ea0357b253c6`

```dockerfile
```

-	Layers:
	-	`sha256:558e10cfaf00d5dd913fe70e48295a0854f58afe8f6074036fea01d804262904`  
		Last Modified: Thu, 26 Jun 2025 21:10:46 GMT  
		Size: 824.7 KB (824702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170df01bf5ca80db9d48141e35d2b47dcf4a0a0c781253035899d0d74c123cfd`  
		Last Modified: Thu, 26 Jun 2025 21:10:46 GMT  
		Size: 11.4 KB (11419 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; riscv64

```console
$ docker pull traefik@sha256:03492ee8f37790110d9d3bb5f2a0878fa0914419e474eefb8fc72e7f2b85e783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56264597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a20813bb82f6a7dd944361e47ecd98665ba283377699e33364695874ce0074`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0-rc1/traefik_v3.5.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
COPY entrypoint.sh / # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Jun 2025 15:08:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
CMD ["traefik"]
# Thu, 26 Jun 2025 15:08:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02ad2790f990f3b2679508be0024e34a070f1c0fc3340739067a3f7f345d8a5`  
		Last Modified: Thu, 26 Jun 2025 18:52:29 GMT  
		Size: 460.5 KB (460534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19d2220c2bc75049e19daa2f4318eb41263440f9a312c25c33a5a6af2bf3379`  
		Last Modified: Thu, 26 Jun 2025 18:52:34 GMT  
		Size: 52.5 MB (52452255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924aa26bc72ab22f6d59d54703e00246cd2d114c8e394bf14ef4867df557492a`  
		Last Modified: Thu, 26 Jun 2025 18:52:28 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:35515481e1f1deebc54282af0116e9defaa2d520b8712e772c1d60652c7aa908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.1 KB (836117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b4ef4cbd65fb1ec5a39fbcce57d249c4c16ab58c00a8c612589b005553b053`

```dockerfile
```

-	Layers:
	-	`sha256:536c4542e5f53489db5d07a2d287b7f2d20e95cd5bb6b234d5eca50139df32f0`  
		Last Modified: Thu, 26 Jun 2025 21:10:50 GMT  
		Size: 824.7 KB (824698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75959d5a25e31c147e8c77064756f97284ce817275cbe09f3a2a48f524b77e40`  
		Last Modified: Thu, 26 Jun 2025 21:10:51 GMT  
		Size: 11.4 KB (11419 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; s390x

```console
$ docker pull traefik@sha256:842bf7bb17383fc2549d1379e55ff855a336a0bc425b0ed03988443dde7f9c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56015417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d183bc550e0c2bd1bf4e2e52f6259f49ff7756921442b94fc4ee56b4563cf650`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0-rc1/traefik_v3.5.0-rc1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
COPY entrypoint.sh / # buildkit
# Thu, 26 Jun 2025 15:08:44 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Jun 2025 15:08:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 Jun 2025 15:08:44 GMT
CMD ["traefik"]
# Thu, 26 Jun 2025 15:08:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0-rc1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4df7d491336b12db12aeb4fd18ed87e7c83236947e9cea4e93f5de3429adc0d`  
		Last Modified: Thu, 26 Jun 2025 18:47:20 GMT  
		Size: 461.2 KB (461160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6b23afd2dcc41c51c1d54f1fc880ac269152fcfbcf9e13d8c93102dbd03d4`  
		Last Modified: Thu, 26 Jun 2025 18:47:28 GMT  
		Size: 52.1 MB (52086321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1837885d01c50f2c0300e58c36676fa1bdbeeb19a88e518efa9575ed4085a3`  
		Last Modified: Thu, 26 Jun 2025 18:47:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:61f7f2189613d3942935cbd645fe0b169930f9587ea560b84313639274bd905e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **836.1 KB (836051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ce1f7b33d0099f7d53ad8aede4c6b41ec351fee68365437166ba9be8253ab1`

```dockerfile
```

-	Layers:
	-	`sha256:7b46f6064df194e2d527396e0b15ace33a25d4aba62a95048ec390483f271209`  
		Last Modified: Thu, 26 Jun 2025 21:10:54 GMT  
		Size: 824.7 KB (824672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b971b75978ef5ccb8f7f96ceacf86562487dcbae0cd34163e5c235fc5447e357`  
		Last Modified: Thu, 26 Jun 2025 21:10:55 GMT  
		Size: 11.4 KB (11379 bytes)  
		MIME: application/vnd.in-toto+json
