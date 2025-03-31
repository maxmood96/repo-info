## `traefik:saintnectaire`

```console
$ docker pull traefik@sha256:104204dadedf5d1284f8ef8f97f705649ac81aa6f7a6c9abf13e2c59245b8abc
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

### `traefik:saintnectaire` - linux; amd64

```console
$ docker pull traefik@sha256:8bb299b8b197e63658d3150e28cc6637970e9788698b88e269552c78295d5f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57517681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c037adf0b4eeeb4b1dbcbfc7520eae76ce967e73f02e1d569808930129ab3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
COPY entrypoint.sh / # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 31 Mar 2025 08:55:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
CMD ["traefik"]
# Mon, 31 Mar 2025 08:55:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1600f8cecfd444899afd69b681a02879ce5607d0278fefa5f8747744c75cc6`  
		Last Modified: Mon, 31 Mar 2025 17:29:14 GMT  
		Size: 460.2 KB (460188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc8cd112e3beb9d5fb4b1bcf11d884caeb7e5e00fefe1d07fab43ebc40386e9`  
		Last Modified: Mon, 31 Mar 2025 17:29:15 GMT  
		Size: 53.4 MB (53414876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3726c0c457c1ef0b6f1451755983ad25f602ecf58be4c89254ea1eddd17376a4`  
		Last Modified: Mon, 31 Mar 2025 17:29:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:13c5e2b3fb0a240652fcb49849fbae02879e6a554ea02fc9c2c9d2d41d0d4f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.7 KB (837676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43dfb28b35269c83d2f26f8eec581863604c6930f2f4ff9e4c43e5043cd4b0b`

```dockerfile
```

-	Layers:
	-	`sha256:2622978453a371b516c5ef088f3396419a4826f6ce7e03562245dbc123edaa53`  
		Last Modified: Mon, 31 Mar 2025 17:29:14 GMT  
		Size: 824.9 KB (824857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d427ba28761459274fd51d9ef966e2db0a56d0e53001e1745907b692d809ed5a`  
		Last Modified: Mon, 31 Mar 2025 17:29:13 GMT  
		Size: 12.8 KB (12819 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; arm variant v6

```console
$ docker pull traefik@sha256:fdc51bc1c209e3f06c602577ac92b3a8d33d2142e065e93495aa888f9e8560b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52936700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5912f7e53068702dbea6fc3148f0e0e168df77bc6baad0c01a89a25a851d8f87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
COPY entrypoint.sh / # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 31 Mar 2025 08:55:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
CMD ["traefik"]
# Mon, 31 Mar 2025 08:55:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:ecb539f6ffba96a70897a616774e0cf5e72d8fa9f45c9bea301994d4c7eea3ba`  
		Last Modified: Mon, 31 Mar 2025 17:28:52 GMT  
		Size: 49.1 MB (49112175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82280c277788ff30ffe2893282bf1e848d0f6f09d33b6566df438f79bdd897e8`  
		Last Modified: Mon, 31 Mar 2025 17:28:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:a9e578c19559a910c2cbf8d9fd16e6c8b526ec6a2bede18b24e335f19b9801c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ed327d7fae37d00adb4d1df4669360dbe7c4b78acada0f2992fd858b6d93fa`

```dockerfile
```

-	Layers:
	-	`sha256:987742cabb35a1ebc9f1ec34094a4eff7ef823feaeede8e449187f3926f7d22d`  
		Last Modified: Mon, 31 Mar 2025 17:28:51 GMT  
		Size: 12.7 KB (12725 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:842e5e3cf27887bcf6b519c70611dd16f8ea558c9432d09623ab794a6708aa23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53752315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b3c1e958e5327776ee51325e632c9eac6f69b596f4f38cc8b79cd7f8062f9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
COPY entrypoint.sh / # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 31 Mar 2025 08:55:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
CMD ["traefik"]
# Mon, 31 Mar 2025 08:55:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a232171547fa4f346637c134b74340d0a38ee59bf86696f832384914f2caf7d`  
		Last Modified: Mon, 31 Mar 2025 17:50:24 GMT  
		Size: 462.1 KB (462050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927346b37a21104f15027b51ca7e66515d2d4f4a79b2dd7680ace594f7c5aa7b`  
		Last Modified: Mon, 31 Mar 2025 17:51:09 GMT  
		Size: 49.3 MB (49296866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90d9c45889c9e1f672760cd3c7b664ba6ed5f579944de07a09469c1d9704ac4`  
		Last Modified: Mon, 31 Mar 2025 17:51:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:d1421f400df02be69a53c8f1cf206d611f829ce0c6bff5fbd5f1990694b1b338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.9 KB (837947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffdd68d8b833c98e6d8cb417fff485bc1c173cb12015db8c421c03f4d2423f8`

```dockerfile
```

-	Layers:
	-	`sha256:5d148137f501f8bdac305ae76f79d132398bf8e9aeae7a830e5f3cbfd6c843f6`  
		Last Modified: Mon, 31 Mar 2025 17:51:07 GMT  
		Size: 825.0 KB (824961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d1ff087d462da8134d9dd4034aba9dbf3593905574c7dd23298c7be5df7d8c1`  
		Last Modified: Mon, 31 Mar 2025 17:51:07 GMT  
		Size: 13.0 KB (12986 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; ppc64le

```console
$ docker pull traefik@sha256:91bac9ca5a67d697b90bd1d93648df8fd6e97b571aa7252f5df050ee78e340b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51092689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5c4c1ac879e81cd167b407870dacffb25c97ae21e6e2ff1538b158761f73d2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
COPY entrypoint.sh / # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 31 Mar 2025 08:55:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
CMD ["traefik"]
# Mon, 31 Mar 2025 08:55:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8ba39a6117bccb2affd6a0153a4a5540dfdb58bcad9bfabb285c2aacb2b8a1`  
		Last Modified: Mon, 31 Mar 2025 19:16:44 GMT  
		Size: 462.5 KB (462544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcb9f2f784aaf2a935b66385240561904ac5f4c5b4eb4d2b995da2f35afe568`  
		Last Modified: Mon, 31 Mar 2025 19:17:54 GMT  
		Size: 47.1 MB (47055430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f741620293cba7c94ff7540be265d77d0d7bdce9c811af344be60652df162b9b`  
		Last Modified: Mon, 31 Mar 2025 19:17:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:4fc77ffc83df1db545071b20ea6fa8515f1762f38d70f61c61da497d4e4bcae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.9 KB (835853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9169bd20bddf1ae38019199f44bbe3ddf1f689eec021517145b357361ad584`

```dockerfile
```

-	Layers:
	-	`sha256:86101326cbd0a642b1f0cad06356fcf616043de38a72ddb6430bb258116f7967`  
		Last Modified: Mon, 31 Mar 2025 19:17:51 GMT  
		Size: 823.0 KB (822964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7fcd4067f07fbc76ef3352563b41ba28c39a17e79be123d71534da6672d1229`  
		Last Modified: Mon, 31 Mar 2025 19:17:51 GMT  
		Size: 12.9 KB (12889 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; riscv64

```console
$ docker pull traefik@sha256:69e08e22629d25e16d677eddc7ef06577579c284952002df0eeef70e169e9d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55704755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2da20f92700275bb4dac0e4e93b982eabe127b5a746e85149ae5cbeb0abb632`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
COPY entrypoint.sh / # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 31 Mar 2025 08:55:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
CMD ["traefik"]
# Mon, 31 Mar 2025 08:55:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4eced17a08f17aadf47e5493c593c559d3e47d882ea352556a54ad16ef3a56b`  
		Last Modified: Mon, 31 Mar 2025 17:56:46 GMT  
		Size: 460.5 KB (460531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0e33ee4076b6b03f5c9a4081e75470dee41c4ae9bc8c1465dbe00dfb6c283d`  
		Last Modified: Mon, 31 Mar 2025 18:05:16 GMT  
		Size: 51.9 MB (51892416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bcc42c166f9d5f2a9d82095431c3e611dffbd088bc227c309759f437f72fb7`  
		Last Modified: Mon, 31 Mar 2025 18:05:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:2c5f00b00a2ea11954638e277c2370967c132630570db02b61aecee1c0cbf211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.8 KB (835848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9dbf723d214e1ed394ed992778476fe04f34ffa0de9090aeb206882c9f5ba5`

```dockerfile
```

-	Layers:
	-	`sha256:864fa8fdf30161e9696927a609847d0a75759971a8fcc1315eca48c6e54ccedb`  
		Last Modified: Mon, 31 Mar 2025 18:05:08 GMT  
		Size: 823.0 KB (822960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1c028a6a5a232c48e668eb87ff442ee08722cbc0f4aa13a00938b48149212a`  
		Last Modified: Mon, 31 Mar 2025 18:05:08 GMT  
		Size: 12.9 KB (12888 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:saintnectaire` - linux; s390x

```console
$ docker pull traefik@sha256:789c0c4ac279e3e074fcaf1bba5fb9048ea062ddee3616af85d0a87892bc9aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55502426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1271e5df30a8bed761ef152710b1f0acd166609507fb35cda02d6589f8433ba8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.3.5/traefik_v3.3.5_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
COPY entrypoint.sh / # buildkit
# Mon, 31 Mar 2025 08:55:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 31 Mar 2025 08:55:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 31 Mar 2025 08:55:13 GMT
CMD ["traefik"]
# Mon, 31 Mar 2025 08:55:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.3.5 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdbe029f4ab9521c647ec8cc3067628e9585501147e42cc3280c9ad73cfbf97`  
		Last Modified: Mon, 31 Mar 2025 19:05:58 GMT  
		Size: 461.1 KB (461133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a7b75771f85b540306cfa4e22505f7e1a394c3a26bbdaab0e9dd8eb3fab6aa`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 51.6 MB (51573356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c372fdf2ac328f26d671cc9a581efe58159d94b0b529f6f02d7152bdc8e5e6`  
		Last Modified: Mon, 31 Mar 2025 19:07:07 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:saintnectaire` - unknown; unknown

```console
$ docker pull traefik@sha256:32e20f9a2916bd42760d4d33789504699e15aa145acd80d836bfe33d4481a529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.7 KB (835723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814c2b3b33526c32bb6a2f3830caf8c749ecf3494010267397b2dbc850eaf3fa`

```dockerfile
```

-	Layers:
	-	`sha256:8bd63f093e50775119db74fbc32b6b43556a3b0daea1717634af4dce63d88192`  
		Last Modified: Mon, 31 Mar 2025 19:07:07 GMT  
		Size: 822.9 KB (822906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03fc8e89639cd6b959ae374e227032fb52d7287c11932cbdd87ba280d1a1b179`  
		Last Modified: Mon, 31 Mar 2025 19:07:08 GMT  
		Size: 12.8 KB (12817 bytes)  
		MIME: application/vnd.in-toto+json
