## `traefik:chaource`

```console
$ docker pull traefik@sha256:20feca842005a8c2810ccd914222de18d15424aab3671cc400c9c6e18767078f
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

### `traefik:chaource` - linux; amd64

```console
$ docker pull traefik@sha256:073102b02294284c4d3acc1d5f4739ffa95e534fb53ae3bce2e2c2210fe93943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58292447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb8766785638ae375790cd00e80b4d68b4340435d060c75d04f4fcdc409fa70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.0-rc2/traefik_v3.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 12:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 12:42:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e18b29ca28d6454443ad83f34264215d7756b7365cc56909a26f7754c06989`  
		Last Modified: Fri, 18 Apr 2025 14:00:10 GMT  
		Size: 460.2 KB (460203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375afb7137a64b4488b7e52dbf31debb368eef21b5c8830f9d528f939fff3b13`  
		Last Modified: Fri, 18 Apr 2025 14:00:11 GMT  
		Size: 54.2 MB (54189628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e8b0ee35d9944182623ec01845ea849dfea4db144625a1380f55146e68f94a`  
		Last Modified: Fri, 18 Apr 2025 14:00:09 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:12996b197139ef3e57e244ac3c5b645691cde9862d1f36912334be2ddee2f22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.6 KB (835602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc48b6fff099861c68981d4bfc503ff0e79dcf580bcbaae6c8e9d952445395c8`

```dockerfile
```

-	Layers:
	-	`sha256:18a5313608fef065f5680cd97685201d5807a745de8c7f4e79818e8945c2bbb2`  
		Last Modified: Fri, 18 Apr 2025 14:00:10 GMT  
		Size: 824.2 KB (824225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab75022b5d102dd1d862d85f61adc1245ef3222c0d3062986c34394fcf593823`  
		Last Modified: Fri, 18 Apr 2025 14:00:09 GMT  
		Size: 11.4 KB (11377 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3227359668057c36833ed29231c7c836d576bcc00fda4f56ea3faac2376f01ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53687774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b453aa8a1fc7238c0f846def6fe1c36880c12107d7aae40f771158d9573d63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 05 May 2025 13:59:24 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 05 May 2025 13:59:24 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.0/traefik_v3.4.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 05 May 2025 13:59:24 GMT
COPY entrypoint.sh / # buildkit
# Mon, 05 May 2025 13:59:24 GMT
EXPOSE map[80/tcp:{}]
# Mon, 05 May 2025 13:59:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 05 May 2025 13:59:24 GMT
CMD ["traefik"]
# Mon, 05 May 2025 13:59:24 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f151b7863e2fb434ea3dcaca468a02986e2de68b280fc64073e5a41a84fd087`  
		Last Modified: Fri, 14 Feb 2025 22:10:21 GMT  
		Size: 459.4 KB (459424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bbfcf2c427ec0f4dd8f4b13add61a1653df86e63fd30cd002442c4decb8510`  
		Last Modified: Mon, 05 May 2025 17:22:04 GMT  
		Size: 49.9 MB (49863250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05ae266f31253dad89638ef1f84825aaa489ab610b1b3bfd0b4595c27ef1b97`  
		Last Modified: Mon, 05 May 2025 17:22:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:6e5cfac5c86babf52a7c18efaf21902451c06160747b458f4ea679be8db5e699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fbccae1324ea7a67f48c186a7cd51672b3ad74377a99ba6ab5ddf56385e656`

```dockerfile
```

-	Layers:
	-	`sha256:80c6a77f1436589bd0b06424f715427ef5e316534d4e1aa0c17006ba272a5b05`  
		Last Modified: Mon, 05 May 2025 17:22:02 GMT  
		Size: 12.7 KB (12714 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e4177202f8c5fc72a26743e279738f91901ebd6d24dc81179dfc8e64b9943ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54478632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd1797347083b7c27a67b308785c345d99fefce51876ff17290655217e46673`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.0-rc2/traefik_v3.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 12:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 12:42:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767a026dafabae556cd462be7925c367eda59c781152c498b6703f4aed3f2b8`  
		Last Modified: Fri, 18 Apr 2025 13:59:56 GMT  
		Size: 462.1 KB (462068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a60f07eb461fcf9450be33e41736e7734a5f0f5aea476946677c1b7908ad31e`  
		Last Modified: Fri, 18 Apr 2025 13:59:58 GMT  
		Size: 50.0 MB (50023166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9537506029b9498617e28edefcfa8fdd756abc836974d12c51e1944c12a04f11`  
		Last Modified: Fri, 18 Apr 2025 13:59:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:61b8d38ca14800886a2dbe267ccec301a036c874728f36fb0dbbef9497aea0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.8 KB (835752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2e3a0b49c4937e9519d64e94358f3be373d935a25f24283b094f1d07106abc`

```dockerfile
```

-	Layers:
	-	`sha256:a5c4ee4e336736a4cfe367656ef8fd6f7c58c7b8158b874a79137d6573ecc432`  
		Last Modified: Fri, 18 Apr 2025 13:59:57 GMT  
		Size: 824.3 KB (824269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27481eb7ebdc31918a85540476d4b41fdb7d5a4b695593c40fcd5ac5a588316e`  
		Last Modified: Fri, 18 Apr 2025 13:59:56 GMT  
		Size: 11.5 KB (11483 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; ppc64le

```console
$ docker pull traefik@sha256:829f3b8d726e41c40e8a0b533e0dadbfed186e3fa9d051bd093f4d392478fcbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51787142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069af736c08b380e48674d10b914527dab0db4bff7113129f2e0138034a0fd61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.0-rc2/traefik_v3.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 12:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 12:42:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e071b328b50063f749f347ba8d94858140ac210384e481fbb657c3ed08fa7`  
		Last Modified: Fri, 18 Apr 2025 14:00:22 GMT  
		Size: 462.6 KB (462561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07feaa0ede2da72cb2b4d9e80e8965d5cb1e7a946eb1132aa24c7e6b2702be39`  
		Last Modified: Fri, 18 Apr 2025 14:00:23 GMT  
		Size: 47.7 MB (47749867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01010dd638ed9610e5a5310d776416c9af84dc5b92c98ee9c2a073880b448e6e`  
		Last Modified: Fri, 18 Apr 2025 14:00:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:cfff4cd353597d00ffe5b0b63e07af7ab6e753a1acf70330a6acbe59f67a65ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **833.7 KB (833719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02c79ad3139c75166b900481cc5f7268c0952857a7e92be751b5a77723c51a6`

```dockerfile
```

-	Layers:
	-	`sha256:50586ece593125579dee1117f3e766129afff3b966239fb6f22104a0aed84ad4`  
		Last Modified: Fri, 18 Apr 2025 14:00:21 GMT  
		Size: 822.3 KB (822302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68bce3a632803b213fc82831ebf8dd750b5a476d0a41a4a62a74f2d3ac72615c`  
		Last Modified: Fri, 18 Apr 2025 14:00:21 GMT  
		Size: 11.4 KB (11417 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; riscv64

```console
$ docker pull traefik@sha256:e888af95bcc083fcc1f6df7c39222de8bf29c98d7f5d6f6b802343d05ab7355c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56449426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a86201b588eeaab48d878ca5170e11ca455a1b62569d2d0730d7cdfd502bdb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.0-rc2/traefik_v3.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 12:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 12:42:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786ed68a7bdb8d6cbb892f36c5788bd24eade8a9ab923e332fadb031b5c122a5`  
		Last Modified: Fri, 18 Apr 2025 14:06:56 GMT  
		Size: 460.5 KB (460548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa02d055f4575b3789d7d7aa4f5803ac8610c38b0ef90f107a159bdc2b8836e`  
		Last Modified: Fri, 18 Apr 2025 14:07:04 GMT  
		Size: 52.6 MB (52637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df23408dc5450b58b27ba2cd8a7d3dc7351df06ad4ef4b7c89e021fc9b8c93c2`  
		Last Modified: Fri, 18 Apr 2025 14:06:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:aee684ef351b198da179154271162fca9b7a719bfd4fb8d91782417f156fc355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **833.7 KB (833715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a06ac74451ce3b7d858f9450032f63e7cb144204b0d007fd8274cc998bd7fb`

```dockerfile
```

-	Layers:
	-	`sha256:fa3f252748e363ec3034eb648d110a30bc978045431453244fa28b1ba9ff3783`  
		Last Modified: Fri, 18 Apr 2025 14:06:56 GMT  
		Size: 822.3 KB (822298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d0bc5e8a4869876622ac8313c89f9ee2ef1158c3843ffa6c5b993c009e1bda3`  
		Last Modified: Fri, 18 Apr 2025 14:06:56 GMT  
		Size: 11.4 KB (11417 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chaource` - linux; s390x

```console
$ docker pull traefik@sha256:ee5af616bfc98cc1a1d44dbfdcccf1ea46b0ee5eecbf6b249dd3117a81bb15cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56267440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9972c5d0d36a5e22e9a1e5c88dfde57972b193c3a95ce3836ac9bdbe95ea936`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.0-rc2/traefik_v3.4.0-rc2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
COPY entrypoint.sh / # buildkit
# Fri, 18 Apr 2025 12:42:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 18 Apr 2025 12:42:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Apr 2025 12:42:44 GMT
CMD ["traefik"]
# Fri, 18 Apr 2025 12:42:44 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.0-rc2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6a1015bb7420b3fd750318ddcce5e18cbf629e4f8c83a0baeceb24b6a523be`  
		Last Modified: Fri, 18 Apr 2025 14:00:35 GMT  
		Size: 461.2 KB (461157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69450309bfbca32232f9f5c87ed96cbade89cbe990a4107e5980c63773952376`  
		Last Modified: Fri, 18 Apr 2025 14:00:36 GMT  
		Size: 52.3 MB (52338347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df378c18fb668abdff7fecc26c1ad8e7ba1552b716d8465670dd0b756f9759e7`  
		Last Modified: Fri, 18 Apr 2025 14:00:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chaource` - unknown; unknown

```console
$ docker pull traefik@sha256:f697b4f1f6bb6267e8ae2419a5593888d17f05148b7b153e2a3bc1e5980defb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **833.6 KB (833649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45dc4ec79561c81ad71005fe0d46bc8c2d4b92775cda5c6526298a86c20b014c`

```dockerfile
```

-	Layers:
	-	`sha256:fe1ea9f60a4a02210e237293aa0a8901469cc5fb5be9837c3de643034b2dd3b3`  
		Last Modified: Fri, 18 Apr 2025 14:00:35 GMT  
		Size: 822.3 KB (822272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f20663e6c00cb92b840c4037fe5c543672eeea540cd1961df314f36fd4db52`  
		Last Modified: Fri, 18 Apr 2025 14:00:35 GMT  
		Size: 11.4 KB (11377 bytes)  
		MIME: application/vnd.in-toto+json
