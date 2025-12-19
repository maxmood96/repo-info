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
