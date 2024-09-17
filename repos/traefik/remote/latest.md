## `traefik:latest`

```console
$ docker pull traefik@sha256:aa0b5b366e198602e5aa507ec94dfee05c12dd0044796763f4606f6b7936c9a9
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
$ docker pull traefik@sha256:e6c09f834f7499657627356686be1fa714538597b8084d6b3a097242c4287fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48643823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba44932023acd862fab2ce2e73b77961bb31f4dc1c721a2e8508c7febf295c15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.3/traefik_v3.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Sep 2024 15:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
CMD ["traefik"]
# Mon, 16 Sep 2024 15:44:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a607613dece0eec2844b6e53c78d1888d0b81ab704211451489bbc231bae43bd`  
		Last Modified: Mon, 16 Sep 2024 18:57:48 GMT  
		Size: 455.1 KB (455107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd4486903050a6e0728d7ad1f9288313d72544a97d8de9640086d88b3ab9217`  
		Last Modified: Mon, 16 Sep 2024 18:57:50 GMT  
		Size: 44.6 MB (44564540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71e86df84e71be53bdcddb69c8e3352b99c0f5bf5a05f2fb2f863de21b9b569`  
		Last Modified: Mon, 16 Sep 2024 18:57:48 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6b7a4bc7d77bdebc64389c6364a094ec82664b083fe7d4914da2c6fc8ea95e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.3 KB (806287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194abb09194d5d0c64eabc49842eee1f4e3e45edf3dc22a42c444e39c0f81069`

```dockerfile
```

-	Layers:
	-	`sha256:67541c62124b221c2b4aacdc960b5bd1065b6888c3e05ba0731ec766bbc2efb6`  
		Last Modified: Mon, 16 Sep 2024 18:57:49 GMT  
		Size: 793.7 KB (793717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34353317fdb89ac94138fa4c579df90d5b830511bce070f03205d0cfe37603a6`  
		Last Modified: Mon, 16 Sep 2024 18:57:48 GMT  
		Size: 12.6 KB (12570 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:2221ee324eb42524bfc6e71edb1844ffea918beb554bf37d5974a597b961bfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45403454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c181fe31181779784abb18e63c2574391c7f8747de08cf9cee2d01bed26e354`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.3/traefik_v3.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Sep 2024 15:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
CMD ["traefik"]
# Mon, 16 Sep 2024 15:44:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b198b4fc88f9f784e0d33686fd52862fdf1fe7e03ec4b3262dead44b2cff91a`  
		Last Modified: Sat, 07 Sep 2024 12:44:50 GMT  
		Size: 456.0 KB (456007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a71374f9d0d57cff23b8a24f9a301c46e9c2260e5d313740724d381d7cca7aa`  
		Last Modified: Mon, 16 Sep 2024 18:57:52 GMT  
		Size: 41.6 MB (41580571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a54f413b1039aea6350d851d35f04985054319cf62a9d64efd9ec43d551bc57`  
		Last Modified: Mon, 16 Sep 2024 18:57:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:c712b56f7f2adce146d1253f595f4300e179a0d30f1c2a1a5360fb9f611a116c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 KB (12465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64194bd90b955890711d304647a461c924c678356fde3ed09214535452ff5d20`

```dockerfile
```

-	Layers:
	-	`sha256:f11bd5a70cc10eda0e82482ef14853bcd0d56b84e4feea1dd3bc0d249e223c31`  
		Last Modified: Mon, 16 Sep 2024 18:57:50 GMT  
		Size: 12.5 KB (12465 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:e7191667bda5590ec102966d1b0f4c4d5800962baeda112f008eb5ebfb217f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45770168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29121aa6a0fb63d58baac10c837b3df92b824ba8eaa773794ee47156af4d200b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.3/traefik_v3.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Sep 2024 15:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
CMD ["traefik"]
# Mon, 16 Sep 2024 15:44:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b78a77f39a248439b4a93ad376e3d3d9b5a93b30a162e0587dc5f2a162a5c3`  
		Last Modified: Mon, 16 Sep 2024 19:17:49 GMT  
		Size: 457.5 KB (457460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c368c415c57b9aa1ce69cc86c7d191db42cf4e3aeaf38474967b7abe65e645a3`  
		Last Modified: Mon, 16 Sep 2024 19:17:50 GMT  
		Size: 41.2 MB (41224694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4072fc55c5181627a5a89f7af76e19f696bbbfa92c2553c5f463d7afc1a9270`  
		Last Modified: Mon, 16 Sep 2024 19:17:48 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:f2b332fdc2f7f714996a2ce8e0f177c283e144c263051e98666313195165431d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.7 KB (806739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422d1be4931faf16b4f70ec561b5eb90c9b63c15b81233ab31cf07b62065c4bd`

```dockerfile
```

-	Layers:
	-	`sha256:9de7acf0cd721277f618e60e6b2b7c29d5b5289dce13fec2177b3f835a684eea`  
		Last Modified: Mon, 16 Sep 2024 19:17:49 GMT  
		Size: 793.8 KB (793821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3635576daca69946642720e26f5a7ec3128bdffb10bae39fa973c85cef91177b`  
		Last Modified: Mon, 16 Sep 2024 19:17:49 GMT  
		Size: 12.9 KB (12918 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:3367956982bb0ace394d327ba36b4afa457d97757ccdc8641fe570c864639166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43836570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe21083cbffa573e38a84b767f266605b6c207f35eea0044ab536efbaefe217`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.3/traefik_v3.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Sep 2024 15:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
CMD ["traefik"]
# Mon, 16 Sep 2024 15:44:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cde7be485f5fdb8bd2195149b20194640ff0440f43a4457ce7c63b72edc412b`  
		Last Modified: Mon, 16 Sep 2024 19:06:29 GMT  
		Size: 457.9 KB (457879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbbfdf1e6a77e1ce50cfd6ce1ccc072749f5306694a275f907c1f1bd1ae0a6bf`  
		Last Modified: Mon, 16 Sep 2024 19:06:31 GMT  
		Size: 39.8 MB (39805903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1833520dca9889e315c2b143d23eb4670ef4ce60f2c89773778c1906fb6c70a`  
		Last Modified: Mon, 16 Sep 2024 19:06:29 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:435a096476e43f871b5e2bec804d2ee79a9da78e97ea6573c9e5a458621267ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.5 KB (804454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226f385b1cfa5c9acf579d52276bb54947fb1a624825e912a3eb146ae2c02caf`

```dockerfile
```

-	Layers:
	-	`sha256:ff1383f2be34e08a07ff42c87d91be874d52c0aedf1b7e790d1596715edcb2e0`  
		Last Modified: Mon, 16 Sep 2024 19:06:29 GMT  
		Size: 791.8 KB (791821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd3dc0bbb6f50b198933b6e95dbb4e7a0f7c43fc3cdc770f353a2d3f58b7fd8`  
		Last Modified: Mon, 16 Sep 2024 19:06:29 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:2c4c40a33e2bbaec14a7f2fb9a1fb83b1d2765e87b9b8b336fbdb83371c33dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46648335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68888c64bd24660c3ab1b2cc5e7628ad943f0869dc55677e6c6be9b00efd11f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.3/traefik_v3.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Sep 2024 15:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
CMD ["traefik"]
# Mon, 16 Sep 2024 15:44:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9782d9bb651b7b80a5b6dc6b8aa5e197330e400020c92b9e4ba59c8dccfb52`  
		Last Modified: Sun, 08 Sep 2024 17:42:04 GMT  
		Size: 455.9 KB (455888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3662d988f51b99c7e6ff8919ccb2b7269c725acea6b6137b56c77feb6cded24`  
		Last Modified: Mon, 16 Sep 2024 19:02:12 GMT  
		Size: 42.8 MB (42820626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71e86df84e71be53bdcddb69c8e3352b99c0f5bf5a05f2fb2f863de21b9b569`  
		Last Modified: Mon, 16 Sep 2024 18:57:48 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:30096358187c0baba5256d75b4041173eec0702598e70d7f3cab7c0b8b53632d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.4 KB (804449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa72c1b43c5c321a5e2e58a6067cf0ed7f870caae15dd18c897a7b96590164e`

```dockerfile
```

-	Layers:
	-	`sha256:7a0e226d6cb48e45cd21f34d43f01bd71aac878f734d4d924eaf9fce5d4c8281`  
		Last Modified: Mon, 16 Sep 2024 19:02:06 GMT  
		Size: 791.8 KB (791817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79829f740652d920ab47f0bdea184cb40c9b0a9d48678f7794be77ed72e9ba10`  
		Last Modified: Mon, 16 Sep 2024 19:02:06 GMT  
		Size: 12.6 KB (12632 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:33dcca2c50c41e07d28054fd73db1529148e18a27864e5c363b9ca8f73b7e920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47020371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cb60f67e1304cd7545380d383dd88a929d00f7ddf83fc654d025f48cb2859f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.1.3/traefik_v3.1.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
COPY entrypoint.sh / # buildkit
# Mon, 16 Sep 2024 15:44:12 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Sep 2024 15:44:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 16 Sep 2024 15:44:12 GMT
CMD ["traefik"]
# Mon, 16 Sep 2024 15:44:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.1.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efba9168f557703d77bbd850ea2260e2a0a5553cf31a1153f77d3ac22b4d81f`  
		Last Modified: Mon, 16 Sep 2024 19:05:32 GMT  
		Size: 456.1 KB (456124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96de266dd8bc52bb1043736e9d210f7e3572f832f5e9abd8bb1ad1fc2895f174`  
		Last Modified: Mon, 16 Sep 2024 19:05:33 GMT  
		Size: 43.1 MB (43102280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d368d86be1336f2c2c9c9e8e4f0e08ec2eb794d9e3b7e7fda7954036f5bcdfb`  
		Last Modified: Mon, 16 Sep 2024 19:05:32 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:1b1809df216263478df7087bd23116002fa6f3569ed607bc34222a5001fe4fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.3 KB (804333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165201199aaa81c18eb1763063e4293050ba6e7ca4efca2f8cc6534a8fc213ca`

```dockerfile
```

-	Layers:
	-	`sha256:162adc8cd690d9c12d9b170b51daee102459ae09f540974bee2d795e23739b9a`  
		Last Modified: Mon, 16 Sep 2024 19:05:32 GMT  
		Size: 791.8 KB (791763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a21a082b7b70a0dfa14402519dae6d34563d667ab14a773db09c697fe97a1f`  
		Last Modified: Mon, 16 Sep 2024 19:05:32 GMT  
		Size: 12.6 KB (12570 bytes)  
		MIME: application/vnd.in-toto+json
