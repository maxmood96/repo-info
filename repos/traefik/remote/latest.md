## `traefik:latest`

```console
$ docker pull traefik@sha256:d9390743f669c0725186576b5af88a3ee9c4f545fc9d57938aec15b351015d1c
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
$ docker pull traefik@sha256:c54196e3a12a08b63db742c6a4c2038335c2d52cb639508476c59ce20a66ce44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59056569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f33a9ff29b57ff11b669f0aec8bc41d6bad9a4b8986c70ecfbaa8f5fd430cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.4/traefik_v3.4.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
COPY entrypoint.sh / # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 11 Jul 2025 08:41:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
CMD ["traefik"]
# Fri, 11 Jul 2025 08:41:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccc0c85e8e04e11f3ee8d90313f40398e9bcafeb1b2b85b417b38f08e378240`  
		Last Modified: Fri, 11 Jul 2025 22:56:52 GMT  
		Size: 460.2 KB (460225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5914f5f27be8057d72e09917bb09641995b3a9db947867ebf1f8c420e47665dc`  
		Last Modified: Sat, 12 Jul 2025 00:10:10 GMT  
		Size: 54.8 MB (54799129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec274304f2930bf30de69cf756b36149fef00dbebd24f282e6c15cad1aceadc`  
		Last Modified: Fri, 11 Jul 2025 22:56:47 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:a82241f1b423b927c4fa0a6e2ac966794733327384dda3b6215975813359ec48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23ea433eec5638da6343fd87ef4ead0eafd245c94c4318fe265679055b21db2`

```dockerfile
```

-	Layers:
	-	`sha256:6a6cb0e918125f3f0cdbec11a8902fe592aaccaead302a839fe54ccac88c2bf2`  
		Last Modified: Sat, 12 Jul 2025 00:10:01 GMT  
		Size: 828.0 KB (828045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4608d7df7b06b94d65819219f4d30600baffe7841142e5a569e465f18809fae`  
		Last Modified: Sat, 12 Jul 2025 00:10:01 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f0fecf2864ef2e625f8f3fc6fdb6a5b6dc606dd0cbc81f20c35a763f0af89e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54186618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c7f3aafc2a93745f41e6912c8d14dac004b63cbe4ad6f06617f6d209257be8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.4/traefik_v3.4.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
COPY entrypoint.sh / # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 11 Jul 2025 08:41:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
CMD ["traefik"]
# Fri, 11 Jul 2025 08:41:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080d5c6b3cfca4f94a04dd42bae669d939e00eff07555d118e7107c1ca48e6a9`  
		Last Modified: Fri, 11 Jul 2025 22:56:14 GMT  
		Size: 461.0 KB (461000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0b80947eb95adb425863e69316cc8b7c39fc147ebf6d620eafbde1abb0f3df`  
		Last Modified: Fri, 11 Jul 2025 22:57:03 GMT  
		Size: 50.2 MB (50224321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5295a48e84bed8d3829c48ac77340681224db55599bef9871b9b4125efcb16`  
		Last Modified: Fri, 11 Jul 2025 22:56:41 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:be270e9bf27dcd4697ab31f31faed24be9bbc36700195f8dc91f88f6a611599c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd2f81b6c2c9433c0ec7b9de09c5a30aa1221b2c4c1e2446a53d89bd7060f4c`

```dockerfile
```

-	Layers:
	-	`sha256:d0917753d503a416b01b174bb6fb9bd0d014d3724b47a8672d3a3cec3af4039a`  
		Last Modified: Sat, 12 Jul 2025 00:10:06 GMT  
		Size: 12.7 KB (12715 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8501288938cf24f1ca00137560d681c6eccb4d55c4f5882419d2b459e363717a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54910233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a169ea29de42a308589379cf7b12d51817fa5fca033cbb0dd659c63214f795f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.4/traefik_v3.4.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
COPY entrypoint.sh / # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 11 Jul 2025 08:41:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
CMD ["traefik"]
# Fri, 11 Jul 2025 08:41:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e75ea73684b64255949a2c7bc0380e1491ad950a0bee01b4f93de783de6591`  
		Last Modified: Fri, 11 Jul 2025 23:28:43 GMT  
		Size: 462.1 KB (462113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6de622dec20d882cacdfbd0f4f7fb08fde13dc4071d9a1bd7e10523fedbe15`  
		Last Modified: Fri, 11 Jul 2025 23:29:30 GMT  
		Size: 50.3 MB (50311810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cce7cc7ce47051e94fc8a4f04e68970a972622121dfca1f25db9363bdf43c88`  
		Last Modified: Fri, 11 Jul 2025 23:29:14 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6451623594b14d81d710d834353c8b39aa84525dab58851de81ceded134507a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.1 KB (841125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c463ccfe948d78afbc8b106360a8583ac72e129d77ad0922585d0413bee314d`

```dockerfile
```

-	Layers:
	-	`sha256:6065f581b1f0442ff65b050f39fb1dcdaed10c1ead474b3edd5a4dd49004ed32`  
		Last Modified: Sat, 12 Jul 2025 00:10:09 GMT  
		Size: 828.1 KB (828149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a91e0ec6b435306b9bfc337f8055956e9b50dd913de125c529238a1b1ecaffd9`  
		Last Modified: Sat, 12 Jul 2025 00:10:10 GMT  
		Size: 13.0 KB (12976 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:05078c357f40d1b1b22f8b5ca45428a68cd2d81eeebb4a9aba3c6e18afd36c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52307805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064ed921f1966ab77e5b1e344dae3ac5c3c752c930dbd8ec50c4dadccf44b3a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.4/traefik_v3.4.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
COPY entrypoint.sh / # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 11 Jul 2025 08:41:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
CMD ["traefik"]
# Fri, 11 Jul 2025 08:41:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7648f00a5e3a13f442e2251ee0d1726f8edba6d43d6b702e3927391d2b49916d`  
		Last Modified: Fri, 11 Jul 2025 23:31:10 GMT  
		Size: 462.6 KB (462611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8baf24cca7cb5fb03f79de9250e6bc9d5d4ee3a94a464523d59c15173a6cb86`  
		Last Modified: Fri, 11 Jul 2025 23:32:45 GMT  
		Size: 48.1 MB (48114640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08147c1d762a88acb54bb28931a5f7d4b336cb78f43fe6d285f44f1ddbaeb29b`  
		Last Modified: Fri, 11 Jul 2025 23:32:41 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:87b960953ad9595107d89fad955d5b7df83ec0b4b9f2d8cbecca8a892df50f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.0 KB (839030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ba4372e3c01157bba0b4e2fa16ad2a3426782f4886fad89c710878e8d519b2`

```dockerfile
```

-	Layers:
	-	`sha256:4a706a234e2f6ae99f8a828e71cf02f88c57106498b349fb6d0dd0b39dc7786c`  
		Last Modified: Sat, 12 Jul 2025 00:10:14 GMT  
		Size: 826.2 KB (826152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad542d25d11a17681b58a241b79b54a5807ae5e2a3dd2e91a4e46bd363f51fe`  
		Last Modified: Sat, 12 Jul 2025 00:10:15 GMT  
		Size: 12.9 KB (12878 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:12e056814e8dea0a59223b7ec3997228a38e1020eca05713db44ec47cd778b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57112706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca4f6f9461aeb967287c8e0576c25f0a7558686a699ab4c45f933b291525cb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Thu, 26 Jun 2025 13:34:32 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Thu, 26 Jun 2025 13:34:32 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.3/traefik_v3.4.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Thu, 26 Jun 2025 13:34:32 GMT
COPY entrypoint.sh / # buildkit
# Thu, 26 Jun 2025 13:34:32 GMT
EXPOSE map[80/tcp:{}]
# Thu, 26 Jun 2025 13:34:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 26 Jun 2025 13:34:32 GMT
CMD ["traefik"]
# Thu, 26 Jun 2025 13:34:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.3 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:dcb25b58b1b1e5d1caabdf4660b80d71f8310a6b3bbbf3a1b8bb982b3bc6f996`  
		Last Modified: Thu, 26 Jun 2025 18:59:16 GMT  
		Size: 53.3 MB (53300364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a29e551ddd9fe8fd81a4ce6ece0974f14d40bbddfa0b6edd44314fb50c474f`  
		Last Modified: Thu, 26 Jun 2025 18:59:10 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:c1c6e785c8906b4916f5bee7dddd6af5ebdc88118fba6af812b728bfccd245dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.2 KB (838250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d22d78d6e536662f765eb430303b4a098b133b2e3815f66466e3341f848679`

```dockerfile
```

-	Layers:
	-	`sha256:deaf15b72c844261a1b9e47f8ec1802f872c6e077867f59b02ecd2941fd53c49`  
		Last Modified: Thu, 26 Jun 2025 21:10:20 GMT  
		Size: 825.4 KB (825371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e93ca9ec192fe5efeee884c95e9023440d7db45ba3687de56a745cb4ed5b55e`  
		Last Modified: Thu, 26 Jun 2025 21:10:21 GMT  
		Size: 12.9 KB (12879 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:1683477ace6b3044517804e15d54ea6121e14eab4468eef5ad7843baea527b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57039630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fd54b2b5d726766a4f500ccca146a578c1e618c115654a2c87c0302030e302`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.4.4/traefik_v3.4.4_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
COPY entrypoint.sh / # buildkit
# Fri, 11 Jul 2025 08:41:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 11 Jul 2025 08:41:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 11 Jul 2025 08:41:35 GMT
CMD ["traefik"]
# Fri, 11 Jul 2025 08:41:35 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.4.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e7973250a029ffe8f660b5402fd5a0ce6434f23975b7f6f8b86103021bf93e`  
		Last Modified: Fri, 11 Jul 2025 23:17:02 GMT  
		Size: 461.2 KB (461180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0459e2e156449b8a837697c5927cba7214b8a34fde8b3ac49bb4f9e3353512`  
		Last Modified: Fri, 11 Jul 2025 23:18:22 GMT  
		Size: 52.9 MB (52930552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851447b62e478eb677d260579c7bab5ed0e69ea1ea16e0fc7e778f4a8320181e`  
		Last Modified: Fri, 11 Jul 2025 23:18:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:417c91eb9a03a3650bc25a41129e277a102661265451a6aa6619df000d0cea3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.9 KB (838903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be99c15083e8f459ed9677ca4d4e9b769e198aaaed051bb19c8bbfabb30792c4`

```dockerfile
```

-	Layers:
	-	`sha256:f76169a8230c94cc54e918a4334d7c9e08e763ae9d3a291367ea81043bff7bb2`  
		Last Modified: Sat, 12 Jul 2025 00:10:21 GMT  
		Size: 826.1 KB (826094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:084ebd957253d73fb574071997a28da667de396b2658e058094742cea4d572a9`  
		Last Modified: Sat, 12 Jul 2025 00:10:21 GMT  
		Size: 12.8 KB (12809 bytes)  
		MIME: application/vnd.in-toto+json
