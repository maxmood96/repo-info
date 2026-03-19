## `traefik:ramequin`

```console
$ docker pull traefik@sha256:3b6196024c3926041fc7d1398126bb2d9851e1befd0526ec58fa16d908f02a59
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
$ docker pull traefik@sha256:2b6506fde98570702dd026bc70ed307a0f22c2cf693329e91b46f94d371097a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52505747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0807f7197e0f14a9b997d8916b6487413d65d774b99a585b9ff023c4e8fd54e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:04:59 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:05:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.11/traefik_v3.6.11_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:05:02 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:05:02 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:05:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:05:02 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:05:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.11 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa991c6c731f7a73175879b7e3ffddd262a3dcda98d7a0ed0e7cde8b789f496a`  
		Last Modified: Thu, 19 Mar 2026 19:05:27 GMT  
		Size: 460.7 KB (460748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d531dd002746af30bf5eb9c3d3e47fae2cb45d4cbc8decc05fd2b03d418d60c`  
		Last Modified: Thu, 19 Mar 2026 19:05:28 GMT  
		Size: 48.2 MB (48182809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc70dc090f30f98f3019be55657425c66b1ce682d79d1214f1f78e71623fda7`  
		Last Modified: Thu, 19 Mar 2026 19:05:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:3dfe0f70c4f34ea82d7a8f7bf11add19457bea717e81cfce5ec6275ae0d2a241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.0 KB (856000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed317451d8fe3dd738341a0b7a2fde0f3a20b9cb6231c7645dcdba9bd3886958`

```dockerfile
```

-	Layers:
	-	`sha256:fae76c52bbe605ebfcefc09c192faadf6a9e017b5e90acf752c206fa892e421c`  
		Last Modified: Thu, 19 Mar 2026 19:05:27 GMT  
		Size: 843.1 KB (843110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c05730d20c2f85bc49534876b080b2dc6996808853ba769a4354730b53da2e`  
		Last Modified: Thu, 19 Mar 2026 19:05:27 GMT  
		Size: 12.9 KB (12890 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm variant v6

```console
$ docker pull traefik@sha256:3759bd90d79080263e0734976a7393983545724e37d226aee3c0cd484784bf64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47768090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aee900ab271a25fa684c107057cfebed98941d2ea8e14338155697b787105a0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:04:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:04:28 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.11/traefik_v3.6.11_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:04:28 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:04:28 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:04:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:04:28 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:04:28 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.11 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e34d1757ce2d016f7a483de23248b30365dea90fa551882704d3aaebd631b5`  
		Last Modified: Thu, 19 Mar 2026 19:04:37 GMT  
		Size: 461.3 KB (461255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3769a21df89bb0d3af6cdc6915becb4419a2956e2bf7820e5b514bc6e736d8e`  
		Last Modified: Thu, 19 Mar 2026 19:04:38 GMT  
		Size: 43.7 MB (43736644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7281d21a0460fbe6dd2f3a3e2d023637e66cb73b1873b3062711305333e10e18`  
		Last Modified: Thu, 19 Mar 2026 19:04:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:c9410ca485256a9776c512c68905b65f884be83e981f46044b5fca8b289526cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 KB (12801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ee34055e85e38cfa552a5e80d8272dedc2879846f16187d3328be065dccd58`

```dockerfile
```

-	Layers:
	-	`sha256:87e2b70eb94cc1039396a7f455f0a4ba2108517f8026bad0944cd9335d312577`  
		Last Modified: Thu, 19 Mar 2026 19:04:37 GMT  
		Size: 12.8 KB (12801 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:0a30da0c8091b62b9014e38bd6f29b01c9651e8b4e51e981e109b065bb9e493a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47706852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb5eca0f48bd30862920ce73344fbc53765b1f28fbdc6fb68a0c0cc15534189`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:03:49 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:04:27 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.11/traefik_v3.6.11_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:04:27 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:04:27 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:04:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:04:27 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:04:27 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.11 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad50546172361585197df1a64e87c13184f6be6fa3eee69e6470838f9d11107`  
		Last Modified: Thu, 19 Mar 2026 19:04:17 GMT  
		Size: 462.8 KB (462767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d8e38f4d00f1a76ca371d985f0698915e626f6f869ef0ce5345e51649fdd65`  
		Last Modified: Thu, 19 Mar 2026 19:04:53 GMT  
		Size: 43.0 MB (43046625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7013b218a7facbf5f2bd89dc0c07535301fc09f4b19a0b594064ea18fea1270`  
		Last Modified: Thu, 19 Mar 2026 19:04:52 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:f736c2d70c25245c2b511b6e4524847fc7daef8b14ac9d8473ac50e4439ca5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.6 KB (855622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a5b7e1150e21787241e77ebeb9267b89a40222d9d3ef8f921d6beab9c34007`

```dockerfile
```

-	Layers:
	-	`sha256:dd7661a12c3a3cd10caab9760fa803167f120a291f1e884eb20cb26a59ed03a4`  
		Last Modified: Thu, 19 Mar 2026 19:04:52 GMT  
		Size: 842.6 KB (842564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7919f4f1fd4745e85b5051f3de7a04a12259bd8d652232cc21963ab8a2444c9a`  
		Last Modified: Thu, 19 Mar 2026 19:04:52 GMT  
		Size: 13.1 KB (13058 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; ppc64le

```console
$ docker pull traefik@sha256:3f5dc7cb025230d3a23b46c721e3e51320102fe15531fe923902d57d35003ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45919291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9288cf09bfecf9ab22c1262031d31199123e48d3eb9cded31c3cd0bc76db243a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:03:06 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:03:10 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.11/traefik_v3.6.11_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:03:11 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:03:11 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:03:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:03:11 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:03:11 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.11 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af51bc42354da8eb1ff8345f831b3ea10ce113a35ee36906dcc5802964dca33a`  
		Last Modified: Thu, 19 Mar 2026 19:03:56 GMT  
		Size: 463.3 KB (463256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c571717c3464f9af4ab29d50ceac21bcb7343f1589bfcbcb28be5514a1243a`  
		Last Modified: Thu, 19 Mar 2026 19:03:58 GMT  
		Size: 41.6 MB (41626023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7091330080b984abd6035818d91de2a457ffc6edd9b91c710c9c89300727177`  
		Last Modified: Thu, 19 Mar 2026 19:03:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:b04eb468bac4f8c8ac155d9cb2fb51e8badf344915988350b9dac015c3c037e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.5 KB (855478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a50929074171c339b6c5ca5b01d4f590012e3203ff6a4140dde1f901a56911`

```dockerfile
```

-	Layers:
	-	`sha256:e92600a94453508fa7d840de3c0d7365024752fd1b9cca2ae15c00aaa82c2816`  
		Last Modified: Thu, 19 Mar 2026 19:03:57 GMT  
		Size: 842.5 KB (842517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c5bf63b860c91597a0be64ac3a1bbd5929d13bfaf8332ccc950d31429d61568`  
		Last Modified: Thu, 19 Mar 2026 19:03:57 GMT  
		Size: 13.0 KB (12961 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; riscv64

```console
$ docker pull traefik@sha256:0e4fcbf7ed1091713319f14f8a3d1d9dafe6033e5b576a8cf05c622467bb71d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50590207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faea0bb97a39fabe4a109ee21f0a5fd043993afee0f9cdbc1c51f2453b462e3e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2026 18:25:25 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 06 Mar 2026 18:25:37 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.10/traefik_v3.6.10_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 06 Mar 2026 18:25:37 GMT
COPY entrypoint.sh / # buildkit
# Fri, 06 Mar 2026 18:25:37 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Mar 2026 18:25:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 06 Mar 2026 18:25:37 GMT
CMD ["traefik"]
# Fri, 06 Mar 2026 18:25:37 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.10 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec88275a3670771fd674e819c3babae468414d19fd462f8c27bdeeffa991b1e8`  
		Last Modified: Fri, 06 Mar 2026 18:31:00 GMT  
		Size: 461.0 KB (460989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c5359bde538f89fefed3b414f36f0904d4214e578595ca775ef0d46aa7f0aa`  
		Last Modified: Fri, 06 Mar 2026 18:31:07 GMT  
		Size: 46.5 MB (46543563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010aa2f0eca64f187df02593ea786e5302d9487a279ac592785ffa1feba29780`  
		Last Modified: Fri, 06 Mar 2026 18:31:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:154f42a120c495b32e4953473d9fb108671978829320d4469dee70610746cbe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.4 KB (855359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11376ea76026e24bd04eeebd5d726dc16d38b057eb670c29b0afdd424d132849`

```dockerfile
```

-	Layers:
	-	`sha256:517ed2873d77d1380b2ebbc584a097636f91d4d6574d7947a3c0e9a22ca5bd69`  
		Last Modified: Fri, 06 Mar 2026 18:31:00 GMT  
		Size: 842.5 KB (842513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab71e2d8d3c409b3e81a4039410f50b04b7870e9efde64340daf4e8025a60a87`  
		Last Modified: Fri, 06 Mar 2026 18:31:00 GMT  
		Size: 12.8 KB (12846 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:ramequin` - linux; s390x

```console
$ docker pull traefik@sha256:f4dd794fbfba6f38360a5d3eee8683aff8a6a3f0ffd900475a7d54bb9225b0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50563809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e507bef0fcd88a81d47af9b4dc04b551dbb7d95b2196b7c348ea12a2147a2d6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 19 Mar 2026 19:03:17 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 19 Mar 2026 19:03:22 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;;         armv7) arch='armv7' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.6.11/traefik_v3.6.11_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 19 Mar 2026 19:03:23 GMT
COPY entrypoint.sh / # buildkit
# Thu, 19 Mar 2026 19:03:23 GMT
EXPOSE map[80/tcp:{}]
# Thu, 19 Mar 2026 19:03:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Mar 2026 19:03:23 GMT
CMD ["traefik"]
# Thu, 19 Mar 2026 19:03:23 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.6.11 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae977ba6d09124dd4b37527a4df183dc77405d05ca492b3252c125ea47df5155`  
		Last Modified: Thu, 19 Mar 2026 19:04:31 GMT  
		Size: 461.5 KB (461544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf9766043396e3c2e09fc95d8f54ac4395dee9144b74d53665671e4074e5a20`  
		Last Modified: Thu, 19 Mar 2026 19:04:39 GMT  
		Size: 46.4 MB (46376563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600cf319c3ac06d9b73065abb113864566a7ad3940bb247936720d58f51b31a8`  
		Last Modified: Thu, 19 Mar 2026 19:04:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:ramequin` - unknown; unknown

```console
$ docker pull traefik@sha256:ac3356c5d449deca82229fbbcc912c3ec79036d6df12291180f13467412bf5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **855.3 KB (855348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4066102e8db6b49d314a889e29af5db26956d29c87f231544c77252c725e7553`

```dockerfile
```

-	Layers:
	-	`sha256:fc23a07650d24a863e72b24fca0d0cd68bfe9c07cb78558fd394038e4d71e73c`  
		Last Modified: Thu, 19 Mar 2026 19:04:36 GMT  
		Size: 842.5 KB (842457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cffc520e48fba089c7e0be754b23d2e4d9f0bfb66f26219540c45b68669f8c69`  
		Last Modified: Thu, 19 Mar 2026 19:04:36 GMT  
		Size: 12.9 KB (12891 bytes)  
		MIME: application/vnd.in-toto+json
