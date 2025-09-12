## `traefik:latest`

```console
$ docker pull traefik@sha256:f0abbbd11ced29754d4d188c29e9320b613481ec162b6ea5d3a8b6bdd8e5fa54
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
$ docker pull traefik@sha256:3b6e38a0ff33b612462af48f1cb8b43bf26ba7fa3c2aae10ce3c85269edb5905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49727678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fe7ceeba1174ea926c08d03b8163a6a3908b12ce68ed4fde3fb9cb4f3f60bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Sep 2025 10:28:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
CMD ["traefik"]
# Tue, 09 Sep 2025 10:28:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb80887cf619e590e6f2b23c6ee9d3e83685bc7609ed45abd55d465d5b30bb3b`  
		Last Modified: Tue, 09 Sep 2025 20:20:00 GMT  
		Size: 447.7 KB (447743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacb9cc999f73782044a58de56592bcb324bc679513123c0a7883c6fbb1ddd8e`  
		Last Modified: Tue, 09 Sep 2025 20:20:05 GMT  
		Size: 45.5 MB (45479877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06eb2b935e7458794f5715d4e8c477bf8a87098eceb518221956e78ee343f747`  
		Last Modified: Tue, 09 Sep 2025 20:20:00 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:325fa4d572d00f6cbd8619394e2e5af3ed4c20040bd26540b723db86361c36e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec365f7502e120d702e09d1154996b7a83b590ddb3accf2eab8c483135b8aa2`

```dockerfile
```

-	Layers:
	-	`sha256:2bbebc28a9de40977001592e5b2d820528cd6742ca84c6abc83b62c977a5cdf7`  
		Last Modified: Tue, 09 Sep 2025 21:09:31 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a5d5464872ba346a27c25276dad695f9e1ca69ca1bbf614e7591d4471a02cde`  
		Last Modified: Tue, 09 Sep 2025 21:09:32 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:6fbe648591f74f7a28668f9b106b299b69348dea2f2a4e7d6431092a4098a3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45181409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6804d228ef4703144099d3d274921ec5df1ceed52f2b1e2ac0a1661119dd2ec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Sep 2025 10:28:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
CMD ["traefik"]
# Tue, 09 Sep 2025 10:28:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dc90d7748f980f3099ac9da688ed0e14e2e6f836b7c608f30794e057cabbb3`  
		Last Modified: Tue, 09 Sep 2025 21:43:05 GMT  
		Size: 448.3 KB (448274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aa2b8d486c9a6a13067c214fd030fb2f27564c7294b220969880e83092c280`  
		Last Modified: Tue, 09 Sep 2025 21:43:07 GMT  
		Size: 41.2 MB (41231856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17959942174a6be67ab1cf611b285ed34b8d60a6bbef6f565aff3f7ee61e79b0`  
		Last Modified: Tue, 09 Sep 2025 21:43:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4f43623d25fff57c7ed6e28c7f3fb6e7ba531ddd4c8e7a714cc293f16dea1f9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a4b27e2a79f09264e206ba8b244676883e9f1dc6c02a61d1ec140154d8d3c9`

```dockerfile
```

-	Layers:
	-	`sha256:649cae3f9490e3d561f49c4232a2f520ee1ed5e83ca37e19b00057593d8b9c39`  
		Last Modified: Wed, 10 Sep 2025 00:09:36 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:65886fcfc7b19f3ba93eac95adebf09709aa32bfa5fa55fc846c3f46efa1e561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45966902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b711030bcb6e8376a9ba0910509565c5821c961fb9d813133b09ab229cfdd36d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Sep 2025 10:28:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
CMD ["traefik"]
# Tue, 09 Sep 2025 10:28:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e9b88aad5c2b4859dcc5e1a2581d380f9ffb1fbca0e8485dca2072bed654cd`  
		Last Modified: Tue, 09 Sep 2025 20:23:47 GMT  
		Size: 449.6 KB (449555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc727fbf92c213f1e4130a340f3f1246b974778f33b525437f8ca59ceff106f0`  
		Last Modified: Tue, 09 Sep 2025 20:23:52 GMT  
		Size: 41.4 MB (41386229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b6e04d4e3ec1a6e5601df054baa4c39d010ac363bfa054cd030ab1401010de`  
		Last Modified: Tue, 09 Sep 2025 20:23:47 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:f17b893f21618a6b23c84c71318246c08057aaa745b47dabc096bf3c0c9c4f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba3477ff4540fb39d381f26fe78468d4c0fc86c6a6ade96c4dcd90bb084aca5`

```dockerfile
```

-	Layers:
	-	`sha256:e290c9ce8485a7d3b476719cdb85181c85b68d1013102c2809999420e806c8aa`  
		Last Modified: Tue, 09 Sep 2025 21:09:37 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8d7ee7686c4fb1d58a127b9ad6e23f46afe6892243392a5a08caf7ab6333d8c`  
		Last Modified: Tue, 09 Sep 2025 21:09:38 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:329bead73bdf68006d69bda2e242e300b6b330661540d571d56bb35900f9fd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43621592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f1bc9c1b315f41f0ac2e87f46b653af58984ffbb9e1625b40d2c39bf010cc24`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Sep 2025 10:28:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
CMD ["traefik"]
# Tue, 09 Sep 2025 10:28:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf98098d751c3b40ed9d43b92282b9dd397805861915cf1d20b9d63d081c698c`  
		Last Modified: Tue, 09 Sep 2025 21:21:39 GMT  
		Size: 450.0 KB (449974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d4cda68b49c2101be29e4aaf108b661e3907a8e203238348977e092873072d`  
		Last Modified: Tue, 09 Sep 2025 21:21:47 GMT  
		Size: 39.4 MB (39444139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245cb3383627167a84feffd950129a21300907d3c40921048b2e8297e8796eb6`  
		Last Modified: Tue, 09 Sep 2025 21:21:39 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:04c1486b3f267951aee6ee11d9f8a17d24c578d6b1f507710ff5782315798f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85afdc7dfbbafd797a312f3abaead7c155e0006d5377ca08b42bc898403ae8d3`

```dockerfile
```

-	Layers:
	-	`sha256:0d127516afe655ee12cd4d0644d7a42fa70e8836679a649a67b3591fe0fcf2aa`  
		Last Modified: Wed, 10 Sep 2025 00:09:42 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667dca0b515ef75b711a8cb8a09e21f20a0ba46b26376929d1f6fa383477847c`  
		Last Modified: Wed, 10 Sep 2025 00:09:43 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:c0b5a9e2aca1cb9965af37c3ba51d98f23c48c92b13916a55c51c7f7ee1cd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47765406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e76e7f45cbdf50a1ff332cedee2020a2de32ccd1778d8aa59e81cf653fc3b9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Sep 2025 10:28:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
CMD ["traefik"]
# Tue, 09 Sep 2025 10:28:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca3755609efb27f08c4323dd67f4bf924bdbeee5d4b53c2a60384a09c05b75`  
		Last Modified: Thu, 11 Sep 2025 21:47:27 GMT  
		Size: 43.8 MB (43804180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248ee51e5244bea6c9960d2fcad9fb401b29ae740054dcf63ccc09cf888e18c7`  
		Last Modified: Thu, 11 Sep 2025 21:47:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:bf1c4de926bf4e74a8fcd726ccd167c7dc22148ffd98e9e17fd838bee4643161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7780495703aa16be4eaabb899602b99107727e7db622e952bf342c321ec2ccf8`

```dockerfile
```

-	Layers:
	-	`sha256:c6ba26cc8fc7e9709454ade234af5626b5193b9a52edf957fc651e3a1ecfc8a2`  
		Last Modified: Fri, 12 Sep 2025 00:10:00 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b938d661cdf9758f6e6101d63d4cfdb4a47715527dbcbce7e5924e9283fd9a47`  
		Last Modified: Fri, 12 Sep 2025 00:10:01 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:61436d4fd3100b4b601df0df2da668f3d3bddc1b6c68bcdad10e9784e3c77cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47749362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095ef3aaecfffd5e3b16549c99f57233d93481617a4288d44be86cb489041403`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
COPY entrypoint.sh / # buildkit
# Tue, 09 Sep 2025 10:28:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Sep 2025 10:28:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Sep 2025 10:28:12 GMT
CMD ["traefik"]
# Tue, 09 Sep 2025 10:28:12 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcb5c832d0cc06bd64a93847b9bdd492e65332ecc30a0e79255cf39a27586ac`  
		Last Modified: Tue, 09 Sep 2025 23:36:33 GMT  
		Size: 448.6 KB (448588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c855e793c10cc83564aafea3e774dba33c17f0969eb401b9fe5b5410f8cc33`  
		Last Modified: Tue, 09 Sep 2025 23:36:39 GMT  
		Size: 43.7 MB (43655434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed70d5b95173a27d1e242c68105c4b0bd496c1d1ae0775cdf8406cb2de781490`  
		Last Modified: Tue, 09 Sep 2025 23:36:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:c0b067a51b2e5080cd849adcb18c6e9fd50190ecd66b216d4f2ba688a42e35f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db38114f57915f9e7d243424c568b238d8a4e897accaa30ec717287779f7a20`

```dockerfile
```

-	Layers:
	-	`sha256:992f29b3f50db6740b214dcdafbf608614138e23ac338702b7f50f0806141e75`  
		Last Modified: Wed, 10 Sep 2025 00:09:49 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c8b5db48695a42b434defac52fd6975db3b225c9fd61dc9f860dfc86323b93`  
		Last Modified: Wed, 10 Sep 2025 00:09:50 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json
