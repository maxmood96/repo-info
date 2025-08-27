<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `traefik`

-	[`traefik:2`](#traefik2)
-	[`traefik:2-nanoserver-ltsc2022`](#traefik2-nanoserver-ltsc2022)
-	[`traefik:2-windowsservercore-ltsc2022`](#traefik2-windowsservercore-ltsc2022)
-	[`traefik:2.11`](#traefik211)
-	[`traefik:2.11-nanoserver-ltsc2022`](#traefik211-nanoserver-ltsc2022)
-	[`traefik:2.11-windowsservercore-ltsc2022`](#traefik211-windowsservercore-ltsc2022)
-	[`traefik:2.11.29`](#traefik21129)
-	[`traefik:2.11.29-nanoserver-ltsc2022`](#traefik21129-nanoserver-ltsc2022)
-	[`traefik:2.11.29-windowsservercore-ltsc2022`](#traefik21129-windowsservercore-ltsc2022)
-	[`traefik:3`](#traefik3)
-	[`traefik:3-nanoserver-ltsc2022`](#traefik3-nanoserver-ltsc2022)
-	[`traefik:3-windowsservercore-ltsc2022`](#traefik3-windowsservercore-ltsc2022)
-	[`traefik:3.5`](#traefik35)
-	[`traefik:3.5-nanoserver-ltsc2022`](#traefik35-nanoserver-ltsc2022)
-	[`traefik:3.5-windowsservercore-ltsc2022`](#traefik35-windowsservercore-ltsc2022)
-	[`traefik:3.5.1`](#traefik351)
-	[`traefik:3.5.1-nanoserver-ltsc2022`](#traefik351-nanoserver-ltsc2022)
-	[`traefik:3.5.1-windowsservercore-ltsc2022`](#traefik351-windowsservercore-ltsc2022)
-	[`traefik:chabichou`](#traefikchabichou)
-	[`traefik:chabichou-nanoserver-ltsc2022`](#traefikchabichou-nanoserver-ltsc2022)
-	[`traefik:chabichou-windowsservercore-ltsc2022`](#traefikchabichou-windowsservercore-ltsc2022)
-	[`traefik:latest`](#traefiklatest)
-	[`traefik:mimolette`](#traefikmimolette)
-	[`traefik:mimolette-nanoserver-ltsc2022`](#traefikmimolette-nanoserver-ltsc2022)
-	[`traefik:mimolette-windowsservercore-ltsc2022`](#traefikmimolette-windowsservercore-ltsc2022)
-	[`traefik:nanoserver-ltsc2022`](#traefiknanoserver-ltsc2022)
-	[`traefik:v2`](#traefikv2)
-	[`traefik:v2-nanoserver-ltsc2022`](#traefikv2-nanoserver-ltsc2022)
-	[`traefik:v2-windowsservercore-ltsc2022`](#traefikv2-windowsservercore-ltsc2022)
-	[`traefik:v2.11`](#traefikv211)
-	[`traefik:v2.11-nanoserver-ltsc2022`](#traefikv211-nanoserver-ltsc2022)
-	[`traefik:v2.11-windowsservercore-ltsc2022`](#traefikv211-windowsservercore-ltsc2022)
-	[`traefik:v2.11.29`](#traefikv21129)
-	[`traefik:v2.11.29-nanoserver-ltsc2022`](#traefikv21129-nanoserver-ltsc2022)
-	[`traefik:v2.11.29-windowsservercore-ltsc2022`](#traefikv21129-windowsservercore-ltsc2022)
-	[`traefik:v3`](#traefikv3)
-	[`traefik:v3-nanoserver-ltsc2022`](#traefikv3-nanoserver-ltsc2022)
-	[`traefik:v3-windowsservercore-ltsc2022`](#traefikv3-windowsservercore-ltsc2022)
-	[`traefik:v3.5`](#traefikv35)
-	[`traefik:v3.5-nanoserver-ltsc2022`](#traefikv35-nanoserver-ltsc2022)
-	[`traefik:v3.5-windowsservercore-ltsc2022`](#traefikv35-windowsservercore-ltsc2022)
-	[`traefik:v3.5.1`](#traefikv351)
-	[`traefik:v3.5.1-nanoserver-ltsc2022`](#traefikv351-nanoserver-ltsc2022)
-	[`traefik:v3.5.1-windowsservercore-ltsc2022`](#traefikv351-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:16f4ba0c10c496dfea966939e742c0e5dbbb03e03617247ff617054a78b25333
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
$ docker pull traefik@sha256:ef194b47cdffffd46578478691150abf5dac2137328baa8018d8bb9fa1d77aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48879165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f1ecf2373092bdd8e52a11f6691b2c41aa5f97040e235c54eefc011386062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0515b72f0cc67ea3ae08fdad1ad8beb0a8fd964c43f13e9752c67ba2a2b7366`  
		Last Modified: Wed, 27 Aug 2025 17:01:41 GMT  
		Size: 447.8 KB (447750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461195f44be0809defed6a87825edb85b164d5d0a264c96d1f4aff1ebbf2b574`  
		Last Modified: Wed, 27 Aug 2025 18:09:44 GMT  
		Size: 44.6 MB (44631356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:2ade12cf666ce72dc348e4e29569ea9033f9867f3e2861a9e8131c222d687593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 KB (856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48383883228500cfe7e71b8cc19385d963057e5930fb8a43822a6ffddd02c551`

```dockerfile
```

-	Layers:
	-	`sha256:693c3c28391cd2a31bb91ee19fbde369a09a9c44b84a00182c856970c35a301c`  
		Last Modified: Wed, 27 Aug 2025 18:09:34 GMT  
		Size: 844.0 KB (844040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc96ca71e0435fa78c0c3e7fc773f3035006e75bf7c9dcffcbb5df534e73e8a`  
		Last Modified: Wed, 27 Aug 2025 18:09:35 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f167694ccf4c99b36665a815414e69b72309a2ef440bc6541cde3a346dc8bc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44700698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370da53c00275152a1b8465452a8e0b8f17e918ca0f48db42597e110959c173c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f890fe69bca4ff8eb3489cb7f1ea54fa3b284ad5acd111963cf7c9106121c10`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 40.8 MB (40751135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:607349433ed7fc1091c03e1d0b8679699dff7aae431de92d3a2ac0573a3fe1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a398ce1d98641c17b9a5620e9d71faec34d8ddb267bb6343c4c8a113a7c007`

```dockerfile
```

-	Layers:
	-	`sha256:0ee433723b058d37f54c878a9f320b347c1d73eaa2e6ff724fb06ca8945c9821`  
		Last Modified: Wed, 27 Aug 2025 18:09:38 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1b47f982b405f9f9fa029b9f924a0683bb66395d4777255c0b29cf7edaf895ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1e751070a8fbc76f7dc4e3391251d178e580c7c9354b1388e7a652e362db5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b5ca0013c90545f931f3187ef25879415ef0686615303f4146c7471158646`  
		Last Modified: Wed, 27 Aug 2025 17:00:18 GMT  
		Size: 40.7 MB (40663126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fb4ccf9d8d0b4cf80443115894ed1cea94d95077076d89216cac9c855204f`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:15f1612fe326d61d989f3b80694a485c7b5397d0db83483071d880df0769c0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.8 KB (856825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a184b894974c6406390cbc238c9e25e87c99da427dcfb26ec6e3fb72765c4ac`

```dockerfile
```

-	Layers:
	-	`sha256:ebc9bf0be6405e6144c840de51890ae11e7cabea1d1e6397176728c8e9e49476`  
		Last Modified: Wed, 27 Aug 2025 18:09:41 GMT  
		Size: 844.1 KB (844132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28625b3d0d96bc20dfae94910da354762bad6d3c09869a4bd7a3456322ad5f3`  
		Last Modified: Wed, 27 Aug 2025 18:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; ppc64le

```console
$ docker pull traefik@sha256:fb4fb93c04b5579f3b837d2c031b6012d1ffcdda457de870c195e5d515f9e6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43245458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f930e177b128612c7b674cfc5210f2a88df32e1880425221d902f4571b157be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbc2968f8fd1eb17c3e7dae63497470b63757685a313a7e11ce58138ff539ae`  
		Last Modified: Wed, 27 Aug 2025 17:10:55 GMT  
		Size: 39.1 MB (39068019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e709bcd4a895201bdde2912728505809636956cc55bd68c2c24ca365a0a771`  
		Last Modified: Wed, 27 Aug 2025 17:10:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:e12687addd17aa37f76fe6b60a52ce0c555f08b9f334b34f9c0b1bb1af9f0ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e3912556e978a30d3e33a5a64963c9d9c6b0bc1689ecce2d4ad93021649e34`

```dockerfile
```

-	Layers:
	-	`sha256:c9b622ef5e884e63fe6490c69c8fc2c2825498e5286e44a527ef973efb82bfef`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 842.1 KB (842141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be376f9328eb13f6c07a50955cd0c75330c408076dc59985f47c4abc14a42ca`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2` - linux; s390x

```console
$ docker pull traefik@sha256:95af8372733c1683ab0ea00651d20c50342a102856b24c85dbdd6ac8f995a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f687e38c4046d74d1595cee6461218ddb7088048db04bb6c0321401e92c654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf539186cb47eb247f25a88398480d6a53353b16a9906ca97d56b8e9bf97aa`  
		Last Modified: Wed, 27 Aug 2025 17:09:44 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63217dd1feb81bce4d043ca9c5791559356450e5c84ec376455f59d4d8a303a8`  
		Last Modified: Wed, 27 Aug 2025 17:09:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:64197983ee7053f706e95e1f5d675fc65f2321195d3dff6ae582d4317907d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.6 KB (854623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7753786057c28ca160c0ffe1976efd1d38212427fd393d8086b03aa8132cff3`

```dockerfile
```

-	Layers:
	-	`sha256:e581aad51ab2b6ee24ab0e2f0c5edd3ed64599c8ea3a5d890b50efd8bf15a5b8`  
		Last Modified: Wed, 27 Aug 2025 18:09:52 GMT  
		Size: 842.1 KB (842085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22daa7b6a23e0e21ab5deb69f071a11b811bbe64446fc4688080588afc028aad`  
		Last Modified: Wed, 27 Aug 2025 18:09:53 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:0ec8bd037b27de09939c7b3da3775de4abb4677b0748055376120d7181504758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:531e7c4ddd99447e08351b4d6bc5c0422b1b4dc453bd512df3ff1dc05cf957d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168058665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b88dfbf738a9fd8533bbcbefd39c9bc28a03db9ab5c7c547cd2b04616302f2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:58:22 GMT
RUN cmd /S /C #(nop) COPY file:62077633f712881ec9f316398f13d332fdc2065b0651d9fa892a92e6c7058f8d in \ 
# Wed, 27 Aug 2025 16:58:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:58:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:58:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f80e4344df79fd556ec8244973291a15548667a8cb5a48c6fcd9de57d884bd8`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 45.4 MB (45395246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a74d6a766096699f51d62018f8c31ab2a10b26fb2c63b49349de7b71f15bc1`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7977da73453c1acfac358763f4d922c8f64483cac66b6ff81203b69b61cba7`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdee3b77fee893cc6a120448a348926b3f5d71a1d84772c4add6f11519f3edb`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:56b3a9b79e2def1df660deb6620148eb3320662430a29947b91e151b27588ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:73b564e82dbcce2a7fab889d42d97db3ff4239c2bef3c7821f03671f8ba0c562
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327575010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f30b119a6b6906ac0fb7c1f0c8f7de0acbf9a034583a9baedd5462ff2972b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:15 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:56:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9c2455f451781d20e3a57f975c5cf60b32a5ea9a2c0a84c54dfab11b206ce`  
		Last Modified: Wed, 27 Aug 2025 16:56:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a6fe3b02f5f443812f0440484b655a27006f973b661e061beee892f35131ca`  
		Last Modified: Wed, 27 Aug 2025 16:57:24 GMT  
		Size: 45.9 MB (45877907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98cf9c87c699ed396949c29973cdcb8a857cb2280cf4371a06a7e12ff1d022f`  
		Last Modified: Wed, 27 Aug 2025 16:56:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0d5bfcd1650a5d03e49c2647583651f231e28481d4ed01a60b83afbc6d207`  
		Last Modified: Wed, 27 Aug 2025 16:56:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670a3637fbb679e28052308ed6e48a33d01c96626d442e33f74c6f82695344cc`  
		Last Modified: Wed, 27 Aug 2025 16:56:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:16f4ba0c10c496dfea966939e742c0e5dbbb03e03617247ff617054a78b25333
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
$ docker pull traefik@sha256:ef194b47cdffffd46578478691150abf5dac2137328baa8018d8bb9fa1d77aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48879165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f1ecf2373092bdd8e52a11f6691b2c41aa5f97040e235c54eefc011386062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0515b72f0cc67ea3ae08fdad1ad8beb0a8fd964c43f13e9752c67ba2a2b7366`  
		Last Modified: Wed, 27 Aug 2025 17:01:41 GMT  
		Size: 447.8 KB (447750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461195f44be0809defed6a87825edb85b164d5d0a264c96d1f4aff1ebbf2b574`  
		Last Modified: Wed, 27 Aug 2025 18:09:44 GMT  
		Size: 44.6 MB (44631356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:2ade12cf666ce72dc348e4e29569ea9033f9867f3e2861a9e8131c222d687593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 KB (856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48383883228500cfe7e71b8cc19385d963057e5930fb8a43822a6ffddd02c551`

```dockerfile
```

-	Layers:
	-	`sha256:693c3c28391cd2a31bb91ee19fbde369a09a9c44b84a00182c856970c35a301c`  
		Last Modified: Wed, 27 Aug 2025 18:09:34 GMT  
		Size: 844.0 KB (844040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc96ca71e0435fa78c0c3e7fc773f3035006e75bf7c9dcffcbb5df534e73e8a`  
		Last Modified: Wed, 27 Aug 2025 18:09:35 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f167694ccf4c99b36665a815414e69b72309a2ef440bc6541cde3a346dc8bc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44700698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370da53c00275152a1b8465452a8e0b8f17e918ca0f48db42597e110959c173c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f890fe69bca4ff8eb3489cb7f1ea54fa3b284ad5acd111963cf7c9106121c10`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 40.8 MB (40751135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:607349433ed7fc1091c03e1d0b8679699dff7aae431de92d3a2ac0573a3fe1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a398ce1d98641c17b9a5620e9d71faec34d8ddb267bb6343c4c8a113a7c007`

```dockerfile
```

-	Layers:
	-	`sha256:0ee433723b058d37f54c878a9f320b347c1d73eaa2e6ff724fb06ca8945c9821`  
		Last Modified: Wed, 27 Aug 2025 18:09:38 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1b47f982b405f9f9fa029b9f924a0683bb66395d4777255c0b29cf7edaf895ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1e751070a8fbc76f7dc4e3391251d178e580c7c9354b1388e7a652e362db5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b5ca0013c90545f931f3187ef25879415ef0686615303f4146c7471158646`  
		Last Modified: Wed, 27 Aug 2025 17:00:18 GMT  
		Size: 40.7 MB (40663126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fb4ccf9d8d0b4cf80443115894ed1cea94d95077076d89216cac9c855204f`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:15f1612fe326d61d989f3b80694a485c7b5397d0db83483071d880df0769c0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.8 KB (856825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a184b894974c6406390cbc238c9e25e87c99da427dcfb26ec6e3fb72765c4ac`

```dockerfile
```

-	Layers:
	-	`sha256:ebc9bf0be6405e6144c840de51890ae11e7cabea1d1e6397176728c8e9e49476`  
		Last Modified: Wed, 27 Aug 2025 18:09:41 GMT  
		Size: 844.1 KB (844132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28625b3d0d96bc20dfae94910da354762bad6d3c09869a4bd7a3456322ad5f3`  
		Last Modified: Wed, 27 Aug 2025 18:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:fb4fb93c04b5579f3b837d2c031b6012d1ffcdda457de870c195e5d515f9e6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43245458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f930e177b128612c7b674cfc5210f2a88df32e1880425221d902f4571b157be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbc2968f8fd1eb17c3e7dae63497470b63757685a313a7e11ce58138ff539ae`  
		Last Modified: Wed, 27 Aug 2025 17:10:55 GMT  
		Size: 39.1 MB (39068019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e709bcd4a895201bdde2912728505809636956cc55bd68c2c24ca365a0a771`  
		Last Modified: Wed, 27 Aug 2025 17:10:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:e12687addd17aa37f76fe6b60a52ce0c555f08b9f334b34f9c0b1bb1af9f0ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e3912556e978a30d3e33a5a64963c9d9c6b0bc1689ecce2d4ad93021649e34`

```dockerfile
```

-	Layers:
	-	`sha256:c9b622ef5e884e63fe6490c69c8fc2c2825498e5286e44a527ef973efb82bfef`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 842.1 KB (842141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be376f9328eb13f6c07a50955cd0c75330c408076dc59985f47c4abc14a42ca`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11` - linux; s390x

```console
$ docker pull traefik@sha256:95af8372733c1683ab0ea00651d20c50342a102856b24c85dbdd6ac8f995a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f687e38c4046d74d1595cee6461218ddb7088048db04bb6c0321401e92c654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf539186cb47eb247f25a88398480d6a53353b16a9906ca97d56b8e9bf97aa`  
		Last Modified: Wed, 27 Aug 2025 17:09:44 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63217dd1feb81bce4d043ca9c5791559356450e5c84ec376455f59d4d8a303a8`  
		Last Modified: Wed, 27 Aug 2025 17:09:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:64197983ee7053f706e95e1f5d675fc65f2321195d3dff6ae582d4317907d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.6 KB (854623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7753786057c28ca160c0ffe1976efd1d38212427fd393d8086b03aa8132cff3`

```dockerfile
```

-	Layers:
	-	`sha256:e581aad51ab2b6ee24ab0e2f0c5edd3ed64599c8ea3a5d890b50efd8bf15a5b8`  
		Last Modified: Wed, 27 Aug 2025 18:09:52 GMT  
		Size: 842.1 KB (842085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22daa7b6a23e0e21ab5deb69f071a11b811bbe64446fc4688080588afc028aad`  
		Last Modified: Wed, 27 Aug 2025 18:09:53 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:0ec8bd037b27de09939c7b3da3775de4abb4677b0748055376120d7181504758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:531e7c4ddd99447e08351b4d6bc5c0422b1b4dc453bd512df3ff1dc05cf957d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168058665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b88dfbf738a9fd8533bbcbefd39c9bc28a03db9ab5c7c547cd2b04616302f2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:58:22 GMT
RUN cmd /S /C #(nop) COPY file:62077633f712881ec9f316398f13d332fdc2065b0651d9fa892a92e6c7058f8d in \ 
# Wed, 27 Aug 2025 16:58:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:58:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:58:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f80e4344df79fd556ec8244973291a15548667a8cb5a48c6fcd9de57d884bd8`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 45.4 MB (45395246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a74d6a766096699f51d62018f8c31ab2a10b26fb2c63b49349de7b71f15bc1`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7977da73453c1acfac358763f4d922c8f64483cac66b6ff81203b69b61cba7`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdee3b77fee893cc6a120448a348926b3f5d71a1d84772c4add6f11519f3edb`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:56b3a9b79e2def1df660deb6620148eb3320662430a29947b91e151b27588ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:73b564e82dbcce2a7fab889d42d97db3ff4239c2bef3c7821f03671f8ba0c562
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327575010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f30b119a6b6906ac0fb7c1f0c8f7de0acbf9a034583a9baedd5462ff2972b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:15 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:56:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9c2455f451781d20e3a57f975c5cf60b32a5ea9a2c0a84c54dfab11b206ce`  
		Last Modified: Wed, 27 Aug 2025 16:56:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a6fe3b02f5f443812f0440484b655a27006f973b661e061beee892f35131ca`  
		Last Modified: Wed, 27 Aug 2025 16:57:24 GMT  
		Size: 45.9 MB (45877907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98cf9c87c699ed396949c29973cdcb8a857cb2280cf4371a06a7e12ff1d022f`  
		Last Modified: Wed, 27 Aug 2025 16:56:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0d5bfcd1650a5d03e49c2647583651f231e28481d4ed01a60b83afbc6d207`  
		Last Modified: Wed, 27 Aug 2025 16:56:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670a3637fbb679e28052308ed6e48a33d01c96626d442e33f74c6f82695344cc`  
		Last Modified: Wed, 27 Aug 2025 16:56:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29`

```console
$ docker pull traefik@sha256:9d1f512777ee61a06e33e77021d50d66b8fcf313c5cb3fde3f5375eccf84f202
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:2.11.29` - linux; amd64

```console
$ docker pull traefik@sha256:ef194b47cdffffd46578478691150abf5dac2137328baa8018d8bb9fa1d77aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48879165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f1ecf2373092bdd8e52a11f6691b2c41aa5f97040e235c54eefc011386062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0515b72f0cc67ea3ae08fdad1ad8beb0a8fd964c43f13e9752c67ba2a2b7366`  
		Last Modified: Wed, 27 Aug 2025 17:01:41 GMT  
		Size: 447.8 KB (447750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461195f44be0809defed6a87825edb85b164d5d0a264c96d1f4aff1ebbf2b574`  
		Last Modified: Wed, 27 Aug 2025 18:09:44 GMT  
		Size: 44.6 MB (44631356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:2ade12cf666ce72dc348e4e29569ea9033f9867f3e2861a9e8131c222d687593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 KB (856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48383883228500cfe7e71b8cc19385d963057e5930fb8a43822a6ffddd02c551`

```dockerfile
```

-	Layers:
	-	`sha256:693c3c28391cd2a31bb91ee19fbde369a09a9c44b84a00182c856970c35a301c`  
		Last Modified: Wed, 27 Aug 2025 18:09:34 GMT  
		Size: 844.0 KB (844040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc96ca71e0435fa78c0c3e7fc773f3035006e75bf7c9dcffcbb5df534e73e8a`  
		Last Modified: Wed, 27 Aug 2025 18:09:35 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f167694ccf4c99b36665a815414e69b72309a2ef440bc6541cde3a346dc8bc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44700698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370da53c00275152a1b8465452a8e0b8f17e918ca0f48db42597e110959c173c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f890fe69bca4ff8eb3489cb7f1ea54fa3b284ad5acd111963cf7c9106121c10`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 40.8 MB (40751135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:607349433ed7fc1091c03e1d0b8679699dff7aae431de92d3a2ac0573a3fe1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a398ce1d98641c17b9a5620e9d71faec34d8ddb267bb6343c4c8a113a7c007`

```dockerfile
```

-	Layers:
	-	`sha256:0ee433723b058d37f54c878a9f320b347c1d73eaa2e6ff724fb06ca8945c9821`  
		Last Modified: Wed, 27 Aug 2025 18:09:38 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1b47f982b405f9f9fa029b9f924a0683bb66395d4777255c0b29cf7edaf895ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1e751070a8fbc76f7dc4e3391251d178e580c7c9354b1388e7a652e362db5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b5ca0013c90545f931f3187ef25879415ef0686615303f4146c7471158646`  
		Last Modified: Wed, 27 Aug 2025 17:00:18 GMT  
		Size: 40.7 MB (40663126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fb4ccf9d8d0b4cf80443115894ed1cea94d95077076d89216cac9c855204f`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:15f1612fe326d61d989f3b80694a485c7b5397d0db83483071d880df0769c0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.8 KB (856825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a184b894974c6406390cbc238c9e25e87c99da427dcfb26ec6e3fb72765c4ac`

```dockerfile
```

-	Layers:
	-	`sha256:ebc9bf0be6405e6144c840de51890ae11e7cabea1d1e6397176728c8e9e49476`  
		Last Modified: Wed, 27 Aug 2025 18:09:41 GMT  
		Size: 844.1 KB (844132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28625b3d0d96bc20dfae94910da354762bad6d3c09869a4bd7a3456322ad5f3`  
		Last Modified: Wed, 27 Aug 2025 18:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; ppc64le

```console
$ docker pull traefik@sha256:fb4fb93c04b5579f3b837d2c031b6012d1ffcdda457de870c195e5d515f9e6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43245458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f930e177b128612c7b674cfc5210f2a88df32e1880425221d902f4571b157be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbc2968f8fd1eb17c3e7dae63497470b63757685a313a7e11ce58138ff539ae`  
		Last Modified: Wed, 27 Aug 2025 17:10:55 GMT  
		Size: 39.1 MB (39068019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e709bcd4a895201bdde2912728505809636956cc55bd68c2c24ca365a0a771`  
		Last Modified: Wed, 27 Aug 2025 17:10:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:e12687addd17aa37f76fe6b60a52ce0c555f08b9f334b34f9c0b1bb1af9f0ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e3912556e978a30d3e33a5a64963c9d9c6b0bc1689ecce2d4ad93021649e34`

```dockerfile
```

-	Layers:
	-	`sha256:c9b622ef5e884e63fe6490c69c8fc2c2825498e5286e44a527ef973efb82bfef`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 842.1 KB (842141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be376f9328eb13f6c07a50955cd0c75330c408076dc59985f47c4abc14a42ca`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:2.11.29` - linux; s390x

```console
$ docker pull traefik@sha256:95af8372733c1683ab0ea00651d20c50342a102856b24c85dbdd6ac8f995a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f687e38c4046d74d1595cee6461218ddb7088048db04bb6c0321401e92c654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf539186cb47eb247f25a88398480d6a53353b16a9906ca97d56b8e9bf97aa`  
		Last Modified: Wed, 27 Aug 2025 17:09:44 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63217dd1feb81bce4d043ca9c5791559356450e5c84ec376455f59d4d8a303a8`  
		Last Modified: Wed, 27 Aug 2025 17:09:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:64197983ee7053f706e95e1f5d675fc65f2321195d3dff6ae582d4317907d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.6 KB (854623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7753786057c28ca160c0ffe1976efd1d38212427fd393d8086b03aa8132cff3`

```dockerfile
```

-	Layers:
	-	`sha256:e581aad51ab2b6ee24ab0e2f0c5edd3ed64599c8ea3a5d890b50efd8bf15a5b8`  
		Last Modified: Wed, 27 Aug 2025 18:09:52 GMT  
		Size: 842.1 KB (842085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22daa7b6a23e0e21ab5deb69f071a11b811bbe64446fc4688080588afc028aad`  
		Last Modified: Wed, 27 Aug 2025 18:09:53 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:2.11.29-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:0ec8bd037b27de09939c7b3da3775de4abb4677b0748055376120d7181504758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2.11.29-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:531e7c4ddd99447e08351b4d6bc5c0422b1b4dc453bd512df3ff1dc05cf957d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168058665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b88dfbf738a9fd8533bbcbefd39c9bc28a03db9ab5c7c547cd2b04616302f2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:58:22 GMT
RUN cmd /S /C #(nop) COPY file:62077633f712881ec9f316398f13d332fdc2065b0651d9fa892a92e6c7058f8d in \ 
# Wed, 27 Aug 2025 16:58:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:58:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:58:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f80e4344df79fd556ec8244973291a15548667a8cb5a48c6fcd9de57d884bd8`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 45.4 MB (45395246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a74d6a766096699f51d62018f8c31ab2a10b26fb2c63b49349de7b71f15bc1`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7977da73453c1acfac358763f4d922c8f64483cac66b6ff81203b69b61cba7`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdee3b77fee893cc6a120448a348926b3f5d71a1d84772c4add6f11519f3edb`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:56b3a9b79e2def1df660deb6620148eb3320662430a29947b91e151b27588ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:2.11.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:73b564e82dbcce2a7fab889d42d97db3ff4239c2bef3c7821f03671f8ba0c562
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327575010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f30b119a6b6906ac0fb7c1f0c8f7de0acbf9a034583a9baedd5462ff2972b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:15 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:56:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9c2455f451781d20e3a57f975c5cf60b32a5ea9a2c0a84c54dfab11b206ce`  
		Last Modified: Wed, 27 Aug 2025 16:56:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a6fe3b02f5f443812f0440484b655a27006f973b661e061beee892f35131ca`  
		Last Modified: Wed, 27 Aug 2025 16:57:24 GMT  
		Size: 45.9 MB (45877907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98cf9c87c699ed396949c29973cdcb8a857cb2280cf4371a06a7e12ff1d022f`  
		Last Modified: Wed, 27 Aug 2025 16:56:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0d5bfcd1650a5d03e49c2647583651f231e28481d4ed01a60b83afbc6d207`  
		Last Modified: Wed, 27 Aug 2025 16:56:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670a3637fbb679e28052308ed6e48a33d01c96626d442e33f74c6f82695344cc`  
		Last Modified: Wed, 27 Aug 2025 16:56:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:b79db93a75530d01ff4181ae6deabb0aa6c7269538bcab700f2eff197fb83722
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
$ docker pull traefik@sha256:81e9ae4b24d81dddaeec331607fb1f5c89e7722b7db301b26045337310b02ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df847a19b384a02d6815ad145d267438250a90a59f08679145b61f790c64f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04439cdf28f8e9472b2dd39bc8bf09b16bd92bfbe064bc91064f36ef8dedc40b`  
		Last Modified: Wed, 27 Aug 2025 17:01:44 GMT  
		Size: 447.7 KB (447749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6b58dcb295e3222dee05ea5f341a59fe9a3456fefdd5f066c5a05c150112c`  
		Last Modified: Wed, 27 Aug 2025 17:34:19 GMT  
		Size: 45.5 MB (45475022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100956301a3856c3fd51ece02c0cb3c8656a830d0e475b68f204db53cc63151`  
		Last Modified: Wed, 27 Aug 2025 17:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:b17b59feb849d0844281037f1a3c5b30fe0f50e11bd67ff3a22f3bc0a4ddb535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da769548d68e432c33900981f87b1737c090a104912801108fbf6531ddcc09a`

```dockerfile
```

-	Layers:
	-	`sha256:07cae4063a61746920f6eabe2f9de8b079279989d8d2989d1c5e8fd77fcc3ff0`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10704978db0bf22e2cc7700bc14cc2f1a0f9406f490058d7c25a90570e5affe7`  
		Last Modified: Wed, 27 Aug 2025 18:10:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:211f6902527b39b5bdc09b5062f7a16a2edd09acf83dfa3cf8ede88f2054ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd2d50600dbd898bd575f11fd667a8379022c92e299e53329eabe0af285fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88e126b141e8ffbd63dda0357515d9531a4e7eb4992e441498a832fbc6d167`  
		Last Modified: Wed, 27 Aug 2025 17:32:07 GMT  
		Size: 41.2 MB (41230533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a507179ca736b6c36eb3f38d7e68e441905f346d80849451149e9184307646a`  
		Last Modified: Wed, 27 Aug 2025 17:01:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:e2f547be4b22769a1e26bcc073afa9a9402adba4b6ce2c71487f0192583f865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a2ed378bb6fd197772d5fdf803ad041a945f4ee122925b78b9deed98ef99b`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb145a4285206f0fae905684820445e06dd8aba96d30880dba85b1cb1d2bcf`  
		Last Modified: Wed, 27 Aug 2025 18:10:11 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e523711822b129d1bf22dd50ae4345fa97d824976ead3084ee6ea9986db5ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f5bf38404e1e55976630aea2fd8335606e3b6149c5af25f883997ec604ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56dfb33904ecb5e55d4c49849b180e3febf05faaee3000af3515c8f4801d6c8`  
		Last Modified: Wed, 27 Aug 2025 17:07:41 GMT  
		Size: 41.4 MB (41398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02498b828d62c3a782051fd83062771dd64177a438b77e5b96af404d06853a11`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:9845802d0e80ffb1937df4a782b7e602a94f68a5134df439707fea7c55b9e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c64a72a93e68ed8f64d8c1c39ccc9ef9383d6a6cebf5937da51274c1c0c78`

```dockerfile
```

-	Layers:
	-	`sha256:cc845f89b64086e6ec7896a77ce5c2e44d28e9779cea84ffe0b004eb192d4417`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01178cfe74e88e9ab78e4dd9b8f5cfa44f26647a8003a310d85c4124101fb7`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:e6927b5405f6cba179d82078a9890783981a8a86e0bc7ee4902386279ac3f15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6dc72c0c5c9239fee2b7f6aaca26e64efda1308bfb37c7a67ce2f89425ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b1143603366e8524f93ec7f3de917b3e31fe27f96c49317ab958da940d844`  
		Last Modified: Wed, 27 Aug 2025 17:09:27 GMT  
		Size: 39.4 MB (39445747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de4741918ce13525480ffd91dc6b216b62082473a4562fb5265523ce87582e`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:c3ed616eb5072d01a686dbc0be70849b3790f972bee8fa91f7afdf66a4f4783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555dfe3dd12c79cdf713ad6cb75d9345274917ce3722c33ab1c5bcbe950985f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f22fe69081680a56629c47c776443d1b08408f9e142383d1ff7e2c5ce64412`  
		Last Modified: Wed, 27 Aug 2025 18:10:17 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31193bbec1ab84a355b5a2da10f92ea2692592ace73072e792fbfb3daba1ed`  
		Last Modified: Wed, 27 Aug 2025 18:10:18 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:bc8fd0bcbef96b11674a70d3f43a2b5a1bf6883b7a4fb2e6d5c008096e9ded9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda3a5bb317f4f331a8114277c58e6ebaf160e795164a508c03fd750769a1b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda85489cd9f2f30f94f1f3e7d431009ac97ba8e42352ede9b572633862d8adc`  
		Last Modified: Wed, 27 Aug 2025 17:08:10 GMT  
		Size: 43.7 MB (43660750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49270d38d651efb3f9113b69ff3a6d48e90266e6e3ed5e42576ed16a8d0593e4`  
		Last Modified: Wed, 27 Aug 2025 17:08:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:6b107cf683ea0df17071ad9ecd2abc9530828fa095e0499d2de91ce2f5ab7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e1dc33803d26f10070af62f90649ee9f35e68c12008603f1f5aa8086470e2`

```dockerfile
```

-	Layers:
	-	`sha256:4e793b9108e9dd2354537ae118dcd9f447610762d3531112105809237095c203`  
		Last Modified: Wed, 27 Aug 2025 18:10:23 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c587e47439872acb4deba3d3e52a9e70b727bfd6eac624aae349cab3593a983`  
		Last Modified: Wed, 27 Aug 2025 18:10:24 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e5922966178c631047e534d82f05fcca084a5f9eb086bf41a5f884057e2c5fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:d16fbba3a116ae9b605b641394b1cdfbe37f9ef5c6e8179d507255f9be853575
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3f6efca79296ba17e096dbb803f1f24607391d4983e2dd910265ff582d4d9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:59:49 GMT
RUN cmd /S /C #(nop) COPY file:abd9a8b820cc1b70a903e8293c4f75175a30ea1d20fc7b8259deacc8d8acb6e8 in \ 
# Wed, 27 Aug 2025 16:59:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:59:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:59:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8513503707a98f555015c891873c823cf765c7c91d4b5df66c73c9bf6778ce`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 46.2 MB (46223885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493ed9f0ad984d8d03c6abf141523f091e2746bf1ed9725b641bf2651855918`  
		Last Modified: Wed, 27 Aug 2025 17:00:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a2f341d8d4358dfa68c8bfb516a6b6c18989822e1372750cba9e1403a348ff`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6ec331bc39da54ef1e96ed28e53983c6908a221e6d7a542a6a757dd9b8822`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e4e7d77b6260491390bfd5085a4481640b2f0a0e8f653f28dbeeefe3b7073cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:c9bfe93694c87dbce8d8de8c90e58a5298be047ae5bfee82de9e6b2252a096fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328429380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd53247d0cbd73975920d06fe678a16f71974d3386d6d25a69423e0b7f3f6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:58 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:57:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983f838df296448d31c1c82c150b89bcae7404cdd75d0d1610baeea4cf5e2551`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959202625b9458dfcdc2761fcf90a6f1f2e08849ac802716a8c672ddc9af814c`  
		Last Modified: Wed, 27 Aug 2025 16:57:25 GMT  
		Size: 46.7 MB (46732219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19b9802aaf9f4dddfdf6b0a18f45fd6648a90dce24328df327692a176f3cd5`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a15cf6da19475e9ba544b5e5af0e4d1ba42dad4a29a0f383d0eb06c1828bdbf`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b0d24e3f75d640c4125d49fe8a8fa61ee0e46e50f36c3f4e989574cde314ed`  
		Last Modified: Wed, 27 Aug 2025 16:57:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5`

```console
$ docker pull traefik@sha256:b79db93a75530d01ff4181ae6deabb0aa6c7269538bcab700f2eff197fb83722
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

### `traefik:3.5` - linux; amd64

```console
$ docker pull traefik@sha256:81e9ae4b24d81dddaeec331607fb1f5c89e7722b7db301b26045337310b02ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df847a19b384a02d6815ad145d267438250a90a59f08679145b61f790c64f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04439cdf28f8e9472b2dd39bc8bf09b16bd92bfbe064bc91064f36ef8dedc40b`  
		Last Modified: Wed, 27 Aug 2025 17:01:44 GMT  
		Size: 447.7 KB (447749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6b58dcb295e3222dee05ea5f341a59fe9a3456fefdd5f066c5a05c150112c`  
		Last Modified: Wed, 27 Aug 2025 17:34:19 GMT  
		Size: 45.5 MB (45475022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100956301a3856c3fd51ece02c0cb3c8656a830d0e475b68f204db53cc63151`  
		Last Modified: Wed, 27 Aug 2025 17:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:b17b59feb849d0844281037f1a3c5b30fe0f50e11bd67ff3a22f3bc0a4ddb535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da769548d68e432c33900981f87b1737c090a104912801108fbf6531ddcc09a`

```dockerfile
```

-	Layers:
	-	`sha256:07cae4063a61746920f6eabe2f9de8b079279989d8d2989d1c5e8fd77fcc3ff0`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10704978db0bf22e2cc7700bc14cc2f1a0f9406f490058d7c25a90570e5affe7`  
		Last Modified: Wed, 27 Aug 2025 18:10:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:211f6902527b39b5bdc09b5062f7a16a2edd09acf83dfa3cf8ede88f2054ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd2d50600dbd898bd575f11fd667a8379022c92e299e53329eabe0af285fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88e126b141e8ffbd63dda0357515d9531a4e7eb4992e441498a832fbc6d167`  
		Last Modified: Wed, 27 Aug 2025 17:32:07 GMT  
		Size: 41.2 MB (41230533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a507179ca736b6c36eb3f38d7e68e441905f346d80849451149e9184307646a`  
		Last Modified: Wed, 27 Aug 2025 17:01:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:e2f547be4b22769a1e26bcc073afa9a9402adba4b6ce2c71487f0192583f865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a2ed378bb6fd197772d5fdf803ad041a945f4ee122925b78b9deed98ef99b`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb145a4285206f0fae905684820445e06dd8aba96d30880dba85b1cb1d2bcf`  
		Last Modified: Wed, 27 Aug 2025 18:10:11 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e523711822b129d1bf22dd50ae4345fa97d824976ead3084ee6ea9986db5ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f5bf38404e1e55976630aea2fd8335606e3b6149c5af25f883997ec604ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56dfb33904ecb5e55d4c49849b180e3febf05faaee3000af3515c8f4801d6c8`  
		Last Modified: Wed, 27 Aug 2025 17:07:41 GMT  
		Size: 41.4 MB (41398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02498b828d62c3a782051fd83062771dd64177a438b77e5b96af404d06853a11`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:9845802d0e80ffb1937df4a782b7e602a94f68a5134df439707fea7c55b9e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c64a72a93e68ed8f64d8c1c39ccc9ef9383d6a6cebf5937da51274c1c0c78`

```dockerfile
```

-	Layers:
	-	`sha256:cc845f89b64086e6ec7896a77ce5c2e44d28e9779cea84ffe0b004eb192d4417`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01178cfe74e88e9ab78e4dd9b8f5cfa44f26647a8003a310d85c4124101fb7`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:e6927b5405f6cba179d82078a9890783981a8a86e0bc7ee4902386279ac3f15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6dc72c0c5c9239fee2b7f6aaca26e64efda1308bfb37c7a67ce2f89425ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b1143603366e8524f93ec7f3de917b3e31fe27f96c49317ab958da940d844`  
		Last Modified: Wed, 27 Aug 2025 17:09:27 GMT  
		Size: 39.4 MB (39445747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de4741918ce13525480ffd91dc6b216b62082473a4562fb5265523ce87582e`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:c3ed616eb5072d01a686dbc0be70849b3790f972bee8fa91f7afdf66a4f4783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555dfe3dd12c79cdf713ad6cb75d9345274917ce3722c33ab1c5bcbe950985f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f22fe69081680a56629c47c776443d1b08408f9e142383d1ff7e2c5ce64412`  
		Last Modified: Wed, 27 Aug 2025 18:10:17 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31193bbec1ab84a355b5a2da10f92ea2692592ace73072e792fbfb3daba1ed`  
		Last Modified: Wed, 27 Aug 2025 18:10:18 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; s390x

```console
$ docker pull traefik@sha256:bc8fd0bcbef96b11674a70d3f43a2b5a1bf6883b7a4fb2e6d5c008096e9ded9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda3a5bb317f4f331a8114277c58e6ebaf160e795164a508c03fd750769a1b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda85489cd9f2f30f94f1f3e7d431009ac97ba8e42352ede9b572633862d8adc`  
		Last Modified: Wed, 27 Aug 2025 17:08:10 GMT  
		Size: 43.7 MB (43660750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49270d38d651efb3f9113b69ff3a6d48e90266e6e3ed5e42576ed16a8d0593e4`  
		Last Modified: Wed, 27 Aug 2025 17:08:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6b107cf683ea0df17071ad9ecd2abc9530828fa095e0499d2de91ce2f5ab7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e1dc33803d26f10070af62f90649ee9f35e68c12008603f1f5aa8086470e2`

```dockerfile
```

-	Layers:
	-	`sha256:4e793b9108e9dd2354537ae118dcd9f447610762d3531112105809237095c203`  
		Last Modified: Wed, 27 Aug 2025 18:10:23 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c587e47439872acb4deba3d3e52a9e70b727bfd6eac624aae349cab3593a983`  
		Last Modified: Wed, 27 Aug 2025 18:10:24 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e5922966178c631047e534d82f05fcca084a5f9eb086bf41a5f884057e2c5fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:d16fbba3a116ae9b605b641394b1cdfbe37f9ef5c6e8179d507255f9be853575
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3f6efca79296ba17e096dbb803f1f24607391d4983e2dd910265ff582d4d9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:59:49 GMT
RUN cmd /S /C #(nop) COPY file:abd9a8b820cc1b70a903e8293c4f75175a30ea1d20fc7b8259deacc8d8acb6e8 in \ 
# Wed, 27 Aug 2025 16:59:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:59:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:59:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8513503707a98f555015c891873c823cf765c7c91d4b5df66c73c9bf6778ce`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 46.2 MB (46223885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493ed9f0ad984d8d03c6abf141523f091e2746bf1ed9725b641bf2651855918`  
		Last Modified: Wed, 27 Aug 2025 17:00:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a2f341d8d4358dfa68c8bfb516a6b6c18989822e1372750cba9e1403a348ff`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6ec331bc39da54ef1e96ed28e53983c6908a221e6d7a542a6a757dd9b8822`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e4e7d77b6260491390bfd5085a4481640b2f0a0e8f653f28dbeeefe3b7073cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:c9bfe93694c87dbce8d8de8c90e58a5298be047ae5bfee82de9e6b2252a096fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328429380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd53247d0cbd73975920d06fe678a16f71974d3386d6d25a69423e0b7f3f6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:58 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:57:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983f838df296448d31c1c82c150b89bcae7404cdd75d0d1610baeea4cf5e2551`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959202625b9458dfcdc2761fcf90a6f1f2e08849ac802716a8c672ddc9af814c`  
		Last Modified: Wed, 27 Aug 2025 16:57:25 GMT  
		Size: 46.7 MB (46732219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19b9802aaf9f4dddfdf6b0a18f45fd6648a90dce24328df327692a176f3cd5`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a15cf6da19475e9ba544b5e5af0e4d1ba42dad4a29a0f383d0eb06c1828bdbf`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b0d24e3f75d640c4125d49fe8a8fa61ee0e46e50f36c3f4e989574cde314ed`  
		Last Modified: Wed, 27 Aug 2025 16:57:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.1`

```console
$ docker pull traefik@sha256:c56901603318ee375477ee5c3f50d175d3ec42dc102efc2f1158f0756ba4dffa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:3.5.1` - linux; amd64

```console
$ docker pull traefik@sha256:81e9ae4b24d81dddaeec331607fb1f5c89e7722b7db301b26045337310b02ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df847a19b384a02d6815ad145d267438250a90a59f08679145b61f790c64f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04439cdf28f8e9472b2dd39bc8bf09b16bd92bfbe064bc91064f36ef8dedc40b`  
		Last Modified: Wed, 27 Aug 2025 17:01:44 GMT  
		Size: 447.7 KB (447749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6b58dcb295e3222dee05ea5f341a59fe9a3456fefdd5f066c5a05c150112c`  
		Last Modified: Wed, 27 Aug 2025 17:34:19 GMT  
		Size: 45.5 MB (45475022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100956301a3856c3fd51ece02c0cb3c8656a830d0e475b68f204db53cc63151`  
		Last Modified: Wed, 27 Aug 2025 17:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:b17b59feb849d0844281037f1a3c5b30fe0f50e11bd67ff3a22f3bc0a4ddb535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da769548d68e432c33900981f87b1737c090a104912801108fbf6531ddcc09a`

```dockerfile
```

-	Layers:
	-	`sha256:07cae4063a61746920f6eabe2f9de8b079279989d8d2989d1c5e8fd77fcc3ff0`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10704978db0bf22e2cc7700bc14cc2f1a0f9406f490058d7c25a90570e5affe7`  
		Last Modified: Wed, 27 Aug 2025 18:10:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:211f6902527b39b5bdc09b5062f7a16a2edd09acf83dfa3cf8ede88f2054ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd2d50600dbd898bd575f11fd667a8379022c92e299e53329eabe0af285fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88e126b141e8ffbd63dda0357515d9531a4e7eb4992e441498a832fbc6d167`  
		Last Modified: Wed, 27 Aug 2025 17:32:07 GMT  
		Size: 41.2 MB (41230533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a507179ca736b6c36eb3f38d7e68e441905f346d80849451149e9184307646a`  
		Last Modified: Wed, 27 Aug 2025 17:01:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:e2f547be4b22769a1e26bcc073afa9a9402adba4b6ce2c71487f0192583f865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a2ed378bb6fd197772d5fdf803ad041a945f4ee122925b78b9deed98ef99b`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb145a4285206f0fae905684820445e06dd8aba96d30880dba85b1cb1d2bcf`  
		Last Modified: Wed, 27 Aug 2025 18:10:11 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e523711822b129d1bf22dd50ae4345fa97d824976ead3084ee6ea9986db5ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f5bf38404e1e55976630aea2fd8335606e3b6149c5af25f883997ec604ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56dfb33904ecb5e55d4c49849b180e3febf05faaee3000af3515c8f4801d6c8`  
		Last Modified: Wed, 27 Aug 2025 17:07:41 GMT  
		Size: 41.4 MB (41398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02498b828d62c3a782051fd83062771dd64177a438b77e5b96af404d06853a11`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:9845802d0e80ffb1937df4a782b7e602a94f68a5134df439707fea7c55b9e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c64a72a93e68ed8f64d8c1c39ccc9ef9383d6a6cebf5937da51274c1c0c78`

```dockerfile
```

-	Layers:
	-	`sha256:cc845f89b64086e6ec7896a77ce5c2e44d28e9779cea84ffe0b004eb192d4417`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01178cfe74e88e9ab78e4dd9b8f5cfa44f26647a8003a310d85c4124101fb7`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.1` - linux; ppc64le

```console
$ docker pull traefik@sha256:e6927b5405f6cba179d82078a9890783981a8a86e0bc7ee4902386279ac3f15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6dc72c0c5c9239fee2b7f6aaca26e64efda1308bfb37c7a67ce2f89425ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b1143603366e8524f93ec7f3de917b3e31fe27f96c49317ab958da940d844`  
		Last Modified: Wed, 27 Aug 2025 17:09:27 GMT  
		Size: 39.4 MB (39445747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de4741918ce13525480ffd91dc6b216b62082473a4562fb5265523ce87582e`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:c3ed616eb5072d01a686dbc0be70849b3790f972bee8fa91f7afdf66a4f4783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555dfe3dd12c79cdf713ad6cb75d9345274917ce3722c33ab1c5bcbe950985f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f22fe69081680a56629c47c776443d1b08408f9e142383d1ff7e2c5ce64412`  
		Last Modified: Wed, 27 Aug 2025 18:10:17 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31193bbec1ab84a355b5a2da10f92ea2692592ace73072e792fbfb3daba1ed`  
		Last Modified: Wed, 27 Aug 2025 18:10:18 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.1` - linux; s390x

```console
$ docker pull traefik@sha256:bc8fd0bcbef96b11674a70d3f43a2b5a1bf6883b7a4fb2e6d5c008096e9ded9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda3a5bb317f4f331a8114277c58e6ebaf160e795164a508c03fd750769a1b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda85489cd9f2f30f94f1f3e7d431009ac97ba8e42352ede9b572633862d8adc`  
		Last Modified: Wed, 27 Aug 2025 17:08:10 GMT  
		Size: 43.7 MB (43660750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49270d38d651efb3f9113b69ff3a6d48e90266e6e3ed5e42576ed16a8d0593e4`  
		Last Modified: Wed, 27 Aug 2025 17:08:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:6b107cf683ea0df17071ad9ecd2abc9530828fa095e0499d2de91ce2f5ab7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e1dc33803d26f10070af62f90649ee9f35e68c12008603f1f5aa8086470e2`

```dockerfile
```

-	Layers:
	-	`sha256:4e793b9108e9dd2354537ae118dcd9f447610762d3531112105809237095c203`  
		Last Modified: Wed, 27 Aug 2025 18:10:23 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c587e47439872acb4deba3d3e52a9e70b727bfd6eac624aae349cab3593a983`  
		Last Modified: Wed, 27 Aug 2025 18:10:24 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.5.1-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e5922966178c631047e534d82f05fcca084a5f9eb086bf41a5f884057e2c5fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5.1-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:d16fbba3a116ae9b605b641394b1cdfbe37f9ef5c6e8179d507255f9be853575
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3f6efca79296ba17e096dbb803f1f24607391d4983e2dd910265ff582d4d9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:59:49 GMT
RUN cmd /S /C #(nop) COPY file:abd9a8b820cc1b70a903e8293c4f75175a30ea1d20fc7b8259deacc8d8acb6e8 in \ 
# Wed, 27 Aug 2025 16:59:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:59:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:59:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8513503707a98f555015c891873c823cf765c7c91d4b5df66c73c9bf6778ce`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 46.2 MB (46223885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493ed9f0ad984d8d03c6abf141523f091e2746bf1ed9725b641bf2651855918`  
		Last Modified: Wed, 27 Aug 2025 17:00:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a2f341d8d4358dfa68c8bfb516a6b6c18989822e1372750cba9e1403a348ff`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6ec331bc39da54ef1e96ed28e53983c6908a221e6d7a542a6a757dd9b8822`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.1-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e4e7d77b6260491390bfd5085a4481640b2f0a0e8f653f28dbeeefe3b7073cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:c9bfe93694c87dbce8d8de8c90e58a5298be047ae5bfee82de9e6b2252a096fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328429380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd53247d0cbd73975920d06fe678a16f71974d3386d6d25a69423e0b7f3f6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:58 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:57:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983f838df296448d31c1c82c150b89bcae7404cdd75d0d1610baeea4cf5e2551`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959202625b9458dfcdc2761fcf90a6f1f2e08849ac802716a8c672ddc9af814c`  
		Last Modified: Wed, 27 Aug 2025 16:57:25 GMT  
		Size: 46.7 MB (46732219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19b9802aaf9f4dddfdf6b0a18f45fd6648a90dce24328df327692a176f3cd5`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a15cf6da19475e9ba544b5e5af0e4d1ba42dad4a29a0f383d0eb06c1828bdbf`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b0d24e3f75d640c4125d49fe8a8fa61ee0e46e50f36c3f4e989574cde314ed`  
		Last Modified: Wed, 27 Aug 2025 16:57:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou`

```console
$ docker pull traefik@sha256:b79db93a75530d01ff4181ae6deabb0aa6c7269538bcab700f2eff197fb83722
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
$ docker pull traefik@sha256:81e9ae4b24d81dddaeec331607fb1f5c89e7722b7db301b26045337310b02ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df847a19b384a02d6815ad145d267438250a90a59f08679145b61f790c64f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04439cdf28f8e9472b2dd39bc8bf09b16bd92bfbe064bc91064f36ef8dedc40b`  
		Last Modified: Wed, 27 Aug 2025 17:01:44 GMT  
		Size: 447.7 KB (447749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6b58dcb295e3222dee05ea5f341a59fe9a3456fefdd5f066c5a05c150112c`  
		Last Modified: Wed, 27 Aug 2025 17:34:19 GMT  
		Size: 45.5 MB (45475022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100956301a3856c3fd51ece02c0cb3c8656a830d0e475b68f204db53cc63151`  
		Last Modified: Wed, 27 Aug 2025 17:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:b17b59feb849d0844281037f1a3c5b30fe0f50e11bd67ff3a22f3bc0a4ddb535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da769548d68e432c33900981f87b1737c090a104912801108fbf6531ddcc09a`

```dockerfile
```

-	Layers:
	-	`sha256:07cae4063a61746920f6eabe2f9de8b079279989d8d2989d1c5e8fd77fcc3ff0`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10704978db0bf22e2cc7700bc14cc2f1a0f9406f490058d7c25a90570e5affe7`  
		Last Modified: Wed, 27 Aug 2025 18:10:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm variant v6

```console
$ docker pull traefik@sha256:211f6902527b39b5bdc09b5062f7a16a2edd09acf83dfa3cf8ede88f2054ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd2d50600dbd898bd575f11fd667a8379022c92e299e53329eabe0af285fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88e126b141e8ffbd63dda0357515d9531a4e7eb4992e441498a832fbc6d167`  
		Last Modified: Wed, 27 Aug 2025 17:32:07 GMT  
		Size: 41.2 MB (41230533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a507179ca736b6c36eb3f38d7e68e441905f346d80849451149e9184307646a`  
		Last Modified: Wed, 27 Aug 2025 17:01:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:e2f547be4b22769a1e26bcc073afa9a9402adba4b6ce2c71487f0192583f865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a2ed378bb6fd197772d5fdf803ad041a945f4ee122925b78b9deed98ef99b`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb145a4285206f0fae905684820445e06dd8aba96d30880dba85b1cb1d2bcf`  
		Last Modified: Wed, 27 Aug 2025 18:10:11 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e523711822b129d1bf22dd50ae4345fa97d824976ead3084ee6ea9986db5ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f5bf38404e1e55976630aea2fd8335606e3b6149c5af25f883997ec604ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56dfb33904ecb5e55d4c49849b180e3febf05faaee3000af3515c8f4801d6c8`  
		Last Modified: Wed, 27 Aug 2025 17:07:41 GMT  
		Size: 41.4 MB (41398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02498b828d62c3a782051fd83062771dd64177a438b77e5b96af404d06853a11`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:9845802d0e80ffb1937df4a782b7e602a94f68a5134df439707fea7c55b9e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c64a72a93e68ed8f64d8c1c39ccc9ef9383d6a6cebf5937da51274c1c0c78`

```dockerfile
```

-	Layers:
	-	`sha256:cc845f89b64086e6ec7896a77ce5c2e44d28e9779cea84ffe0b004eb192d4417`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01178cfe74e88e9ab78e4dd9b8f5cfa44f26647a8003a310d85c4124101fb7`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; ppc64le

```console
$ docker pull traefik@sha256:e6927b5405f6cba179d82078a9890783981a8a86e0bc7ee4902386279ac3f15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6dc72c0c5c9239fee2b7f6aaca26e64efda1308bfb37c7a67ce2f89425ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b1143603366e8524f93ec7f3de917b3e31fe27f96c49317ab958da940d844`  
		Last Modified: Wed, 27 Aug 2025 17:09:27 GMT  
		Size: 39.4 MB (39445747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de4741918ce13525480ffd91dc6b216b62082473a4562fb5265523ce87582e`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:c3ed616eb5072d01a686dbc0be70849b3790f972bee8fa91f7afdf66a4f4783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555dfe3dd12c79cdf713ad6cb75d9345274917ce3722c33ab1c5bcbe950985f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f22fe69081680a56629c47c776443d1b08408f9e142383d1ff7e2c5ce64412`  
		Last Modified: Wed, 27 Aug 2025 18:10:17 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31193bbec1ab84a355b5a2da10f92ea2692592ace73072e792fbfb3daba1ed`  
		Last Modified: Wed, 27 Aug 2025 18:10:18 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; s390x

```console
$ docker pull traefik@sha256:bc8fd0bcbef96b11674a70d3f43a2b5a1bf6883b7a4fb2e6d5c008096e9ded9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda3a5bb317f4f331a8114277c58e6ebaf160e795164a508c03fd750769a1b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda85489cd9f2f30f94f1f3e7d431009ac97ba8e42352ede9b572633862d8adc`  
		Last Modified: Wed, 27 Aug 2025 17:08:10 GMT  
		Size: 43.7 MB (43660750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49270d38d651efb3f9113b69ff3a6d48e90266e6e3ed5e42576ed16a8d0593e4`  
		Last Modified: Wed, 27 Aug 2025 17:08:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:6b107cf683ea0df17071ad9ecd2abc9530828fa095e0499d2de91ce2f5ab7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e1dc33803d26f10070af62f90649ee9f35e68c12008603f1f5aa8086470e2`

```dockerfile
```

-	Layers:
	-	`sha256:4e793b9108e9dd2354537ae118dcd9f447610762d3531112105809237095c203`  
		Last Modified: Wed, 27 Aug 2025 18:10:23 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c587e47439872acb4deba3d3e52a9e70b727bfd6eac624aae349cab3593a983`  
		Last Modified: Wed, 27 Aug 2025 18:10:24 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:chabichou-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e5922966178c631047e534d82f05fcca084a5f9eb086bf41a5f884057e2c5fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:chabichou-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:d16fbba3a116ae9b605b641394b1cdfbe37f9ef5c6e8179d507255f9be853575
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3f6efca79296ba17e096dbb803f1f24607391d4983e2dd910265ff582d4d9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:59:49 GMT
RUN cmd /S /C #(nop) COPY file:abd9a8b820cc1b70a903e8293c4f75175a30ea1d20fc7b8259deacc8d8acb6e8 in \ 
# Wed, 27 Aug 2025 16:59:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:59:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:59:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8513503707a98f555015c891873c823cf765c7c91d4b5df66c73c9bf6778ce`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 46.2 MB (46223885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493ed9f0ad984d8d03c6abf141523f091e2746bf1ed9725b641bf2651855918`  
		Last Modified: Wed, 27 Aug 2025 17:00:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a2f341d8d4358dfa68c8bfb516a6b6c18989822e1372750cba9e1403a348ff`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6ec331bc39da54ef1e96ed28e53983c6908a221e6d7a542a6a757dd9b8822`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e4e7d77b6260491390bfd5085a4481640b2f0a0e8f653f28dbeeefe3b7073cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:chabichou-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:c9bfe93694c87dbce8d8de8c90e58a5298be047ae5bfee82de9e6b2252a096fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328429380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd53247d0cbd73975920d06fe678a16f71974d3386d6d25a69423e0b7f3f6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:58 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:57:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983f838df296448d31c1c82c150b89bcae7404cdd75d0d1610baeea4cf5e2551`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959202625b9458dfcdc2761fcf90a6f1f2e08849ac802716a8c672ddc9af814c`  
		Last Modified: Wed, 27 Aug 2025 16:57:25 GMT  
		Size: 46.7 MB (46732219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19b9802aaf9f4dddfdf6b0a18f45fd6648a90dce24328df327692a176f3cd5`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a15cf6da19475e9ba544b5e5af0e4d1ba42dad4a29a0f383d0eb06c1828bdbf`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b0d24e3f75d640c4125d49fe8a8fa61ee0e46e50f36c3f4e989574cde314ed`  
		Last Modified: Wed, 27 Aug 2025 16:57:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:b79db93a75530d01ff4181ae6deabb0aa6c7269538bcab700f2eff197fb83722
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
$ docker pull traefik@sha256:81e9ae4b24d81dddaeec331607fb1f5c89e7722b7db301b26045337310b02ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df847a19b384a02d6815ad145d267438250a90a59f08679145b61f790c64f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04439cdf28f8e9472b2dd39bc8bf09b16bd92bfbe064bc91064f36ef8dedc40b`  
		Last Modified: Wed, 27 Aug 2025 17:01:44 GMT  
		Size: 447.7 KB (447749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6b58dcb295e3222dee05ea5f341a59fe9a3456fefdd5f066c5a05c150112c`  
		Last Modified: Wed, 27 Aug 2025 17:34:19 GMT  
		Size: 45.5 MB (45475022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100956301a3856c3fd51ece02c0cb3c8656a830d0e475b68f204db53cc63151`  
		Last Modified: Wed, 27 Aug 2025 17:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:b17b59feb849d0844281037f1a3c5b30fe0f50e11bd67ff3a22f3bc0a4ddb535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da769548d68e432c33900981f87b1737c090a104912801108fbf6531ddcc09a`

```dockerfile
```

-	Layers:
	-	`sha256:07cae4063a61746920f6eabe2f9de8b079279989d8d2989d1c5e8fd77fcc3ff0`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10704978db0bf22e2cc7700bc14cc2f1a0f9406f490058d7c25a90570e5affe7`  
		Last Modified: Wed, 27 Aug 2025 18:10:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:211f6902527b39b5bdc09b5062f7a16a2edd09acf83dfa3cf8ede88f2054ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd2d50600dbd898bd575f11fd667a8379022c92e299e53329eabe0af285fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88e126b141e8ffbd63dda0357515d9531a4e7eb4992e441498a832fbc6d167`  
		Last Modified: Wed, 27 Aug 2025 17:32:07 GMT  
		Size: 41.2 MB (41230533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a507179ca736b6c36eb3f38d7e68e441905f346d80849451149e9184307646a`  
		Last Modified: Wed, 27 Aug 2025 17:01:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:e2f547be4b22769a1e26bcc073afa9a9402adba4b6ce2c71487f0192583f865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a2ed378bb6fd197772d5fdf803ad041a945f4ee122925b78b9deed98ef99b`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb145a4285206f0fae905684820445e06dd8aba96d30880dba85b1cb1d2bcf`  
		Last Modified: Wed, 27 Aug 2025 18:10:11 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e523711822b129d1bf22dd50ae4345fa97d824976ead3084ee6ea9986db5ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f5bf38404e1e55976630aea2fd8335606e3b6149c5af25f883997ec604ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56dfb33904ecb5e55d4c49849b180e3febf05faaee3000af3515c8f4801d6c8`  
		Last Modified: Wed, 27 Aug 2025 17:07:41 GMT  
		Size: 41.4 MB (41398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02498b828d62c3a782051fd83062771dd64177a438b77e5b96af404d06853a11`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:9845802d0e80ffb1937df4a782b7e602a94f68a5134df439707fea7c55b9e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c64a72a93e68ed8f64d8c1c39ccc9ef9383d6a6cebf5937da51274c1c0c78`

```dockerfile
```

-	Layers:
	-	`sha256:cc845f89b64086e6ec7896a77ce5c2e44d28e9779cea84ffe0b004eb192d4417`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01178cfe74e88e9ab78e4dd9b8f5cfa44f26647a8003a310d85c4124101fb7`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:e6927b5405f6cba179d82078a9890783981a8a86e0bc7ee4902386279ac3f15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6dc72c0c5c9239fee2b7f6aaca26e64efda1308bfb37c7a67ce2f89425ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b1143603366e8524f93ec7f3de917b3e31fe27f96c49317ab958da940d844`  
		Last Modified: Wed, 27 Aug 2025 17:09:27 GMT  
		Size: 39.4 MB (39445747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de4741918ce13525480ffd91dc6b216b62082473a4562fb5265523ce87582e`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:c3ed616eb5072d01a686dbc0be70849b3790f972bee8fa91f7afdf66a4f4783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555dfe3dd12c79cdf713ad6cb75d9345274917ce3722c33ab1c5bcbe950985f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f22fe69081680a56629c47c776443d1b08408f9e142383d1ff7e2c5ce64412`  
		Last Modified: Wed, 27 Aug 2025 18:10:17 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31193bbec1ab84a355b5a2da10f92ea2692592ace73072e792fbfb3daba1ed`  
		Last Modified: Wed, 27 Aug 2025 18:10:18 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:bc8fd0bcbef96b11674a70d3f43a2b5a1bf6883b7a4fb2e6d5c008096e9ded9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda3a5bb317f4f331a8114277c58e6ebaf160e795164a508c03fd750769a1b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda85489cd9f2f30f94f1f3e7d431009ac97ba8e42352ede9b572633862d8adc`  
		Last Modified: Wed, 27 Aug 2025 17:08:10 GMT  
		Size: 43.7 MB (43660750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49270d38d651efb3f9113b69ff3a6d48e90266e6e3ed5e42576ed16a8d0593e4`  
		Last Modified: Wed, 27 Aug 2025 17:08:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6b107cf683ea0df17071ad9ecd2abc9530828fa095e0499d2de91ce2f5ab7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e1dc33803d26f10070af62f90649ee9f35e68c12008603f1f5aa8086470e2`

```dockerfile
```

-	Layers:
	-	`sha256:4e793b9108e9dd2354537ae118dcd9f447610762d3531112105809237095c203`  
		Last Modified: Wed, 27 Aug 2025 18:10:23 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c587e47439872acb4deba3d3e52a9e70b727bfd6eac624aae349cab3593a983`  
		Last Modified: Wed, 27 Aug 2025 18:10:24 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:16f4ba0c10c496dfea966939e742c0e5dbbb03e03617247ff617054a78b25333
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
$ docker pull traefik@sha256:ef194b47cdffffd46578478691150abf5dac2137328baa8018d8bb9fa1d77aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48879165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f1ecf2373092bdd8e52a11f6691b2c41aa5f97040e235c54eefc011386062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0515b72f0cc67ea3ae08fdad1ad8beb0a8fd964c43f13e9752c67ba2a2b7366`  
		Last Modified: Wed, 27 Aug 2025 17:01:41 GMT  
		Size: 447.8 KB (447750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461195f44be0809defed6a87825edb85b164d5d0a264c96d1f4aff1ebbf2b574`  
		Last Modified: Wed, 27 Aug 2025 18:09:44 GMT  
		Size: 44.6 MB (44631356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:2ade12cf666ce72dc348e4e29569ea9033f9867f3e2861a9e8131c222d687593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 KB (856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48383883228500cfe7e71b8cc19385d963057e5930fb8a43822a6ffddd02c551`

```dockerfile
```

-	Layers:
	-	`sha256:693c3c28391cd2a31bb91ee19fbde369a09a9c44b84a00182c856970c35a301c`  
		Last Modified: Wed, 27 Aug 2025 18:09:34 GMT  
		Size: 844.0 KB (844040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc96ca71e0435fa78c0c3e7fc773f3035006e75bf7c9dcffcbb5df534e73e8a`  
		Last Modified: Wed, 27 Aug 2025 18:09:35 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f167694ccf4c99b36665a815414e69b72309a2ef440bc6541cde3a346dc8bc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44700698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370da53c00275152a1b8465452a8e0b8f17e918ca0f48db42597e110959c173c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f890fe69bca4ff8eb3489cb7f1ea54fa3b284ad5acd111963cf7c9106121c10`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 40.8 MB (40751135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:607349433ed7fc1091c03e1d0b8679699dff7aae431de92d3a2ac0573a3fe1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a398ce1d98641c17b9a5620e9d71faec34d8ddb267bb6343c4c8a113a7c007`

```dockerfile
```

-	Layers:
	-	`sha256:0ee433723b058d37f54c878a9f320b347c1d73eaa2e6ff724fb06ca8945c9821`  
		Last Modified: Wed, 27 Aug 2025 18:09:38 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1b47f982b405f9f9fa029b9f924a0683bb66395d4777255c0b29cf7edaf895ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1e751070a8fbc76f7dc4e3391251d178e580c7c9354b1388e7a652e362db5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b5ca0013c90545f931f3187ef25879415ef0686615303f4146c7471158646`  
		Last Modified: Wed, 27 Aug 2025 17:00:18 GMT  
		Size: 40.7 MB (40663126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fb4ccf9d8d0b4cf80443115894ed1cea94d95077076d89216cac9c855204f`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:15f1612fe326d61d989f3b80694a485c7b5397d0db83483071d880df0769c0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.8 KB (856825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a184b894974c6406390cbc238c9e25e87c99da427dcfb26ec6e3fb72765c4ac`

```dockerfile
```

-	Layers:
	-	`sha256:ebc9bf0be6405e6144c840de51890ae11e7cabea1d1e6397176728c8e9e49476`  
		Last Modified: Wed, 27 Aug 2025 18:09:41 GMT  
		Size: 844.1 KB (844132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28625b3d0d96bc20dfae94910da354762bad6d3c09869a4bd7a3456322ad5f3`  
		Last Modified: Wed, 27 Aug 2025 18:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; ppc64le

```console
$ docker pull traefik@sha256:fb4fb93c04b5579f3b837d2c031b6012d1ffcdda457de870c195e5d515f9e6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43245458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f930e177b128612c7b674cfc5210f2a88df32e1880425221d902f4571b157be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbc2968f8fd1eb17c3e7dae63497470b63757685a313a7e11ce58138ff539ae`  
		Last Modified: Wed, 27 Aug 2025 17:10:55 GMT  
		Size: 39.1 MB (39068019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e709bcd4a895201bdde2912728505809636956cc55bd68c2c24ca365a0a771`  
		Last Modified: Wed, 27 Aug 2025 17:10:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:e12687addd17aa37f76fe6b60a52ce0c555f08b9f334b34f9c0b1bb1af9f0ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e3912556e978a30d3e33a5a64963c9d9c6b0bc1689ecce2d4ad93021649e34`

```dockerfile
```

-	Layers:
	-	`sha256:c9b622ef5e884e63fe6490c69c8fc2c2825498e5286e44a527ef973efb82bfef`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 842.1 KB (842141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be376f9328eb13f6c07a50955cd0c75330c408076dc59985f47c4abc14a42ca`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:mimolette` - linux; s390x

```console
$ docker pull traefik@sha256:95af8372733c1683ab0ea00651d20c50342a102856b24c85dbdd6ac8f995a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f687e38c4046d74d1595cee6461218ddb7088048db04bb6c0321401e92c654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf539186cb47eb247f25a88398480d6a53353b16a9906ca97d56b8e9bf97aa`  
		Last Modified: Wed, 27 Aug 2025 17:09:44 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63217dd1feb81bce4d043ca9c5791559356450e5c84ec376455f59d4d8a303a8`  
		Last Modified: Wed, 27 Aug 2025 17:09:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:64197983ee7053f706e95e1f5d675fc65f2321195d3dff6ae582d4317907d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.6 KB (854623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7753786057c28ca160c0ffe1976efd1d38212427fd393d8086b03aa8132cff3`

```dockerfile
```

-	Layers:
	-	`sha256:e581aad51ab2b6ee24ab0e2f0c5edd3ed64599c8ea3a5d890b50efd8bf15a5b8`  
		Last Modified: Wed, 27 Aug 2025 18:09:52 GMT  
		Size: 842.1 KB (842085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22daa7b6a23e0e21ab5deb69f071a11b811bbe64446fc4688080588afc028aad`  
		Last Modified: Wed, 27 Aug 2025 18:09:53 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:0ec8bd037b27de09939c7b3da3775de4abb4677b0748055376120d7181504758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:531e7c4ddd99447e08351b4d6bc5c0422b1b4dc453bd512df3ff1dc05cf957d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168058665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b88dfbf738a9fd8533bbcbefd39c9bc28a03db9ab5c7c547cd2b04616302f2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:58:22 GMT
RUN cmd /S /C #(nop) COPY file:62077633f712881ec9f316398f13d332fdc2065b0651d9fa892a92e6c7058f8d in \ 
# Wed, 27 Aug 2025 16:58:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:58:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:58:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f80e4344df79fd556ec8244973291a15548667a8cb5a48c6fcd9de57d884bd8`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 45.4 MB (45395246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a74d6a766096699f51d62018f8c31ab2a10b26fb2c63b49349de7b71f15bc1`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7977da73453c1acfac358763f4d922c8f64483cac66b6ff81203b69b61cba7`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdee3b77fee893cc6a120448a348926b3f5d71a1d84772c4add6f11519f3edb`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:56b3a9b79e2def1df660deb6620148eb3320662430a29947b91e151b27588ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:73b564e82dbcce2a7fab889d42d97db3ff4239c2bef3c7821f03671f8ba0c562
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327575010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f30b119a6b6906ac0fb7c1f0c8f7de0acbf9a034583a9baedd5462ff2972b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:15 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:56:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9c2455f451781d20e3a57f975c5cf60b32a5ea9a2c0a84c54dfab11b206ce`  
		Last Modified: Wed, 27 Aug 2025 16:56:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a6fe3b02f5f443812f0440484b655a27006f973b661e061beee892f35131ca`  
		Last Modified: Wed, 27 Aug 2025 16:57:24 GMT  
		Size: 45.9 MB (45877907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98cf9c87c699ed396949c29973cdcb8a857cb2280cf4371a06a7e12ff1d022f`  
		Last Modified: Wed, 27 Aug 2025 16:56:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0d5bfcd1650a5d03e49c2647583651f231e28481d4ed01a60b83afbc6d207`  
		Last Modified: Wed, 27 Aug 2025 16:56:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670a3637fbb679e28052308ed6e48a33d01c96626d442e33f74c6f82695344cc`  
		Last Modified: Wed, 27 Aug 2025 16:56:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e5922966178c631047e534d82f05fcca084a5f9eb086bf41a5f884057e2c5fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:d16fbba3a116ae9b605b641394b1cdfbe37f9ef5c6e8179d507255f9be853575
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3f6efca79296ba17e096dbb803f1f24607391d4983e2dd910265ff582d4d9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:59:49 GMT
RUN cmd /S /C #(nop) COPY file:abd9a8b820cc1b70a903e8293c4f75175a30ea1d20fc7b8259deacc8d8acb6e8 in \ 
# Wed, 27 Aug 2025 16:59:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:59:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:59:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8513503707a98f555015c891873c823cf765c7c91d4b5df66c73c9bf6778ce`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 46.2 MB (46223885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493ed9f0ad984d8d03c6abf141523f091e2746bf1ed9725b641bf2651855918`  
		Last Modified: Wed, 27 Aug 2025 17:00:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a2f341d8d4358dfa68c8bfb516a6b6c18989822e1372750cba9e1403a348ff`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6ec331bc39da54ef1e96ed28e53983c6908a221e6d7a542a6a757dd9b8822`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:16f4ba0c10c496dfea966939e742c0e5dbbb03e03617247ff617054a78b25333
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
$ docker pull traefik@sha256:ef194b47cdffffd46578478691150abf5dac2137328baa8018d8bb9fa1d77aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48879165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f1ecf2373092bdd8e52a11f6691b2c41aa5f97040e235c54eefc011386062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0515b72f0cc67ea3ae08fdad1ad8beb0a8fd964c43f13e9752c67ba2a2b7366`  
		Last Modified: Wed, 27 Aug 2025 17:01:41 GMT  
		Size: 447.8 KB (447750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461195f44be0809defed6a87825edb85b164d5d0a264c96d1f4aff1ebbf2b574`  
		Last Modified: Wed, 27 Aug 2025 18:09:44 GMT  
		Size: 44.6 MB (44631356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:2ade12cf666ce72dc348e4e29569ea9033f9867f3e2861a9e8131c222d687593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 KB (856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48383883228500cfe7e71b8cc19385d963057e5930fb8a43822a6ffddd02c551`

```dockerfile
```

-	Layers:
	-	`sha256:693c3c28391cd2a31bb91ee19fbde369a09a9c44b84a00182c856970c35a301c`  
		Last Modified: Wed, 27 Aug 2025 18:09:34 GMT  
		Size: 844.0 KB (844040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc96ca71e0435fa78c0c3e7fc773f3035006e75bf7c9dcffcbb5df534e73e8a`  
		Last Modified: Wed, 27 Aug 2025 18:09:35 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f167694ccf4c99b36665a815414e69b72309a2ef440bc6541cde3a346dc8bc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44700698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370da53c00275152a1b8465452a8e0b8f17e918ca0f48db42597e110959c173c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f890fe69bca4ff8eb3489cb7f1ea54fa3b284ad5acd111963cf7c9106121c10`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 40.8 MB (40751135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:607349433ed7fc1091c03e1d0b8679699dff7aae431de92d3a2ac0573a3fe1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a398ce1d98641c17b9a5620e9d71faec34d8ddb267bb6343c4c8a113a7c007`

```dockerfile
```

-	Layers:
	-	`sha256:0ee433723b058d37f54c878a9f320b347c1d73eaa2e6ff724fb06ca8945c9821`  
		Last Modified: Wed, 27 Aug 2025 18:09:38 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1b47f982b405f9f9fa029b9f924a0683bb66395d4777255c0b29cf7edaf895ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1e751070a8fbc76f7dc4e3391251d178e580c7c9354b1388e7a652e362db5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b5ca0013c90545f931f3187ef25879415ef0686615303f4146c7471158646`  
		Last Modified: Wed, 27 Aug 2025 17:00:18 GMT  
		Size: 40.7 MB (40663126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fb4ccf9d8d0b4cf80443115894ed1cea94d95077076d89216cac9c855204f`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:15f1612fe326d61d989f3b80694a485c7b5397d0db83483071d880df0769c0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.8 KB (856825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a184b894974c6406390cbc238c9e25e87c99da427dcfb26ec6e3fb72765c4ac`

```dockerfile
```

-	Layers:
	-	`sha256:ebc9bf0be6405e6144c840de51890ae11e7cabea1d1e6397176728c8e9e49476`  
		Last Modified: Wed, 27 Aug 2025 18:09:41 GMT  
		Size: 844.1 KB (844132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28625b3d0d96bc20dfae94910da354762bad6d3c09869a4bd7a3456322ad5f3`  
		Last Modified: Wed, 27 Aug 2025 18:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; ppc64le

```console
$ docker pull traefik@sha256:fb4fb93c04b5579f3b837d2c031b6012d1ffcdda457de870c195e5d515f9e6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43245458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f930e177b128612c7b674cfc5210f2a88df32e1880425221d902f4571b157be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbc2968f8fd1eb17c3e7dae63497470b63757685a313a7e11ce58138ff539ae`  
		Last Modified: Wed, 27 Aug 2025 17:10:55 GMT  
		Size: 39.1 MB (39068019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e709bcd4a895201bdde2912728505809636956cc55bd68c2c24ca365a0a771`  
		Last Modified: Wed, 27 Aug 2025 17:10:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:e12687addd17aa37f76fe6b60a52ce0c555f08b9f334b34f9c0b1bb1af9f0ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e3912556e978a30d3e33a5a64963c9d9c6b0bc1689ecce2d4ad93021649e34`

```dockerfile
```

-	Layers:
	-	`sha256:c9b622ef5e884e63fe6490c69c8fc2c2825498e5286e44a527ef973efb82bfef`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 842.1 KB (842141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be376f9328eb13f6c07a50955cd0c75330c408076dc59985f47c4abc14a42ca`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2` - linux; s390x

```console
$ docker pull traefik@sha256:95af8372733c1683ab0ea00651d20c50342a102856b24c85dbdd6ac8f995a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f687e38c4046d74d1595cee6461218ddb7088048db04bb6c0321401e92c654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf539186cb47eb247f25a88398480d6a53353b16a9906ca97d56b8e9bf97aa`  
		Last Modified: Wed, 27 Aug 2025 17:09:44 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63217dd1feb81bce4d043ca9c5791559356450e5c84ec376455f59d4d8a303a8`  
		Last Modified: Wed, 27 Aug 2025 17:09:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:64197983ee7053f706e95e1f5d675fc65f2321195d3dff6ae582d4317907d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.6 KB (854623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7753786057c28ca160c0ffe1976efd1d38212427fd393d8086b03aa8132cff3`

```dockerfile
```

-	Layers:
	-	`sha256:e581aad51ab2b6ee24ab0e2f0c5edd3ed64599c8ea3a5d890b50efd8bf15a5b8`  
		Last Modified: Wed, 27 Aug 2025 18:09:52 GMT  
		Size: 842.1 KB (842085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22daa7b6a23e0e21ab5deb69f071a11b811bbe64446fc4688080588afc028aad`  
		Last Modified: Wed, 27 Aug 2025 18:09:53 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:0ec8bd037b27de09939c7b3da3775de4abb4677b0748055376120d7181504758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:531e7c4ddd99447e08351b4d6bc5c0422b1b4dc453bd512df3ff1dc05cf957d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168058665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b88dfbf738a9fd8533bbcbefd39c9bc28a03db9ab5c7c547cd2b04616302f2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:58:22 GMT
RUN cmd /S /C #(nop) COPY file:62077633f712881ec9f316398f13d332fdc2065b0651d9fa892a92e6c7058f8d in \ 
# Wed, 27 Aug 2025 16:58:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:58:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:58:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f80e4344df79fd556ec8244973291a15548667a8cb5a48c6fcd9de57d884bd8`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 45.4 MB (45395246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a74d6a766096699f51d62018f8c31ab2a10b26fb2c63b49349de7b71f15bc1`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7977da73453c1acfac358763f4d922c8f64483cac66b6ff81203b69b61cba7`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdee3b77fee893cc6a120448a348926b3f5d71a1d84772c4add6f11519f3edb`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:56b3a9b79e2def1df660deb6620148eb3320662430a29947b91e151b27588ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:73b564e82dbcce2a7fab889d42d97db3ff4239c2bef3c7821f03671f8ba0c562
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327575010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f30b119a6b6906ac0fb7c1f0c8f7de0acbf9a034583a9baedd5462ff2972b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:15 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:56:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9c2455f451781d20e3a57f975c5cf60b32a5ea9a2c0a84c54dfab11b206ce`  
		Last Modified: Wed, 27 Aug 2025 16:56:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a6fe3b02f5f443812f0440484b655a27006f973b661e061beee892f35131ca`  
		Last Modified: Wed, 27 Aug 2025 16:57:24 GMT  
		Size: 45.9 MB (45877907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98cf9c87c699ed396949c29973cdcb8a857cb2280cf4371a06a7e12ff1d022f`  
		Last Modified: Wed, 27 Aug 2025 16:56:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0d5bfcd1650a5d03e49c2647583651f231e28481d4ed01a60b83afbc6d207`  
		Last Modified: Wed, 27 Aug 2025 16:56:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670a3637fbb679e28052308ed6e48a33d01c96626d442e33f74c6f82695344cc`  
		Last Modified: Wed, 27 Aug 2025 16:56:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:16f4ba0c10c496dfea966939e742c0e5dbbb03e03617247ff617054a78b25333
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
$ docker pull traefik@sha256:ef194b47cdffffd46578478691150abf5dac2137328baa8018d8bb9fa1d77aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48879165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f1ecf2373092bdd8e52a11f6691b2c41aa5f97040e235c54eefc011386062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0515b72f0cc67ea3ae08fdad1ad8beb0a8fd964c43f13e9752c67ba2a2b7366`  
		Last Modified: Wed, 27 Aug 2025 17:01:41 GMT  
		Size: 447.8 KB (447750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461195f44be0809defed6a87825edb85b164d5d0a264c96d1f4aff1ebbf2b574`  
		Last Modified: Wed, 27 Aug 2025 18:09:44 GMT  
		Size: 44.6 MB (44631356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:2ade12cf666ce72dc348e4e29569ea9033f9867f3e2861a9e8131c222d687593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 KB (856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48383883228500cfe7e71b8cc19385d963057e5930fb8a43822a6ffddd02c551`

```dockerfile
```

-	Layers:
	-	`sha256:693c3c28391cd2a31bb91ee19fbde369a09a9c44b84a00182c856970c35a301c`  
		Last Modified: Wed, 27 Aug 2025 18:09:34 GMT  
		Size: 844.0 KB (844040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc96ca71e0435fa78c0c3e7fc773f3035006e75bf7c9dcffcbb5df534e73e8a`  
		Last Modified: Wed, 27 Aug 2025 18:09:35 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f167694ccf4c99b36665a815414e69b72309a2ef440bc6541cde3a346dc8bc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44700698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370da53c00275152a1b8465452a8e0b8f17e918ca0f48db42597e110959c173c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f890fe69bca4ff8eb3489cb7f1ea54fa3b284ad5acd111963cf7c9106121c10`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 40.8 MB (40751135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:607349433ed7fc1091c03e1d0b8679699dff7aae431de92d3a2ac0573a3fe1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a398ce1d98641c17b9a5620e9d71faec34d8ddb267bb6343c4c8a113a7c007`

```dockerfile
```

-	Layers:
	-	`sha256:0ee433723b058d37f54c878a9f320b347c1d73eaa2e6ff724fb06ca8945c9821`  
		Last Modified: Wed, 27 Aug 2025 18:09:38 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1b47f982b405f9f9fa029b9f924a0683bb66395d4777255c0b29cf7edaf895ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1e751070a8fbc76f7dc4e3391251d178e580c7c9354b1388e7a652e362db5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b5ca0013c90545f931f3187ef25879415ef0686615303f4146c7471158646`  
		Last Modified: Wed, 27 Aug 2025 17:00:18 GMT  
		Size: 40.7 MB (40663126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fb4ccf9d8d0b4cf80443115894ed1cea94d95077076d89216cac9c855204f`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:15f1612fe326d61d989f3b80694a485c7b5397d0db83483071d880df0769c0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.8 KB (856825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a184b894974c6406390cbc238c9e25e87c99da427dcfb26ec6e3fb72765c4ac`

```dockerfile
```

-	Layers:
	-	`sha256:ebc9bf0be6405e6144c840de51890ae11e7cabea1d1e6397176728c8e9e49476`  
		Last Modified: Wed, 27 Aug 2025 18:09:41 GMT  
		Size: 844.1 KB (844132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28625b3d0d96bc20dfae94910da354762bad6d3c09869a4bd7a3456322ad5f3`  
		Last Modified: Wed, 27 Aug 2025 18:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; ppc64le

```console
$ docker pull traefik@sha256:fb4fb93c04b5579f3b837d2c031b6012d1ffcdda457de870c195e5d515f9e6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43245458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f930e177b128612c7b674cfc5210f2a88df32e1880425221d902f4571b157be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbc2968f8fd1eb17c3e7dae63497470b63757685a313a7e11ce58138ff539ae`  
		Last Modified: Wed, 27 Aug 2025 17:10:55 GMT  
		Size: 39.1 MB (39068019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e709bcd4a895201bdde2912728505809636956cc55bd68c2c24ca365a0a771`  
		Last Modified: Wed, 27 Aug 2025 17:10:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:e12687addd17aa37f76fe6b60a52ce0c555f08b9f334b34f9c0b1bb1af9f0ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e3912556e978a30d3e33a5a64963c9d9c6b0bc1689ecce2d4ad93021649e34`

```dockerfile
```

-	Layers:
	-	`sha256:c9b622ef5e884e63fe6490c69c8fc2c2825498e5286e44a527ef973efb82bfef`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 842.1 KB (842141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be376f9328eb13f6c07a50955cd0c75330c408076dc59985f47c4abc14a42ca`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; riscv64

```console
$ docker pull traefik@sha256:d4816acc44810fba63654937475ffa2a3320d3dbf4fe0f69518c19a0357b44f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55862931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6082542fb135d413a518baff2d7cd6e0ab1edae249f65d2e6c1c5eb613620d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.28/traefik_v2.11.28_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 08:56:13 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 08:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 08:56:13 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 08:56:13 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.28 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5657b9e6d8c6ac366b9737e7739428ab98bc44930e7283b19d13f1b09686ab`  
		Last Modified: Wed, 23 Jul 2025 17:10:27 GMT  
		Size: 51.9 MB (51901708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbb2dacade807dc677517fc2626970b5fe5a6fe782431bb591696d2ee259106`  
		Last Modified: Wed, 23 Jul 2025 17:10:01 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:3d18f0c1be0ba653a11e46bac75357d0ef33f376ee19da56f7d718102b6bf6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **847.6 KB (847592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70a1f42c119f7231a992340860d8e24d9baf4028f3c7e1ce26a182c1b255422`

```dockerfile
```

-	Layers:
	-	`sha256:8bd51c9c26c6186a2461d57d3cb59a68d18ed9403e8df0fa47c265cfb50d7386`  
		Last Modified: Wed, 23 Jul 2025 18:09:49 GMT  
		Size: 835.0 KB (834990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918345255b372e1cf74132bac8bc497bccef9253c02f0f68848f62c8fe7e778f`  
		Last Modified: Wed, 23 Jul 2025 18:09:50 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11` - linux; s390x

```console
$ docker pull traefik@sha256:95af8372733c1683ab0ea00651d20c50342a102856b24c85dbdd6ac8f995a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f687e38c4046d74d1595cee6461218ddb7088048db04bb6c0321401e92c654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf539186cb47eb247f25a88398480d6a53353b16a9906ca97d56b8e9bf97aa`  
		Last Modified: Wed, 27 Aug 2025 17:09:44 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63217dd1feb81bce4d043ca9c5791559356450e5c84ec376455f59d4d8a303a8`  
		Last Modified: Wed, 27 Aug 2025 17:09:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:64197983ee7053f706e95e1f5d675fc65f2321195d3dff6ae582d4317907d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.6 KB (854623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7753786057c28ca160c0ffe1976efd1d38212427fd393d8086b03aa8132cff3`

```dockerfile
```

-	Layers:
	-	`sha256:e581aad51ab2b6ee24ab0e2f0c5edd3ed64599c8ea3a5d890b50efd8bf15a5b8`  
		Last Modified: Wed, 27 Aug 2025 18:09:52 GMT  
		Size: 842.1 KB (842085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22daa7b6a23e0e21ab5deb69f071a11b811bbe64446fc4688080588afc028aad`  
		Last Modified: Wed, 27 Aug 2025 18:09:53 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:0ec8bd037b27de09939c7b3da3775de4abb4677b0748055376120d7181504758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:531e7c4ddd99447e08351b4d6bc5c0422b1b4dc453bd512df3ff1dc05cf957d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168058665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b88dfbf738a9fd8533bbcbefd39c9bc28a03db9ab5c7c547cd2b04616302f2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:58:22 GMT
RUN cmd /S /C #(nop) COPY file:62077633f712881ec9f316398f13d332fdc2065b0651d9fa892a92e6c7058f8d in \ 
# Wed, 27 Aug 2025 16:58:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:58:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:58:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f80e4344df79fd556ec8244973291a15548667a8cb5a48c6fcd9de57d884bd8`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 45.4 MB (45395246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a74d6a766096699f51d62018f8c31ab2a10b26fb2c63b49349de7b71f15bc1`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7977da73453c1acfac358763f4d922c8f64483cac66b6ff81203b69b61cba7`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdee3b77fee893cc6a120448a348926b3f5d71a1d84772c4add6f11519f3edb`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:56b3a9b79e2def1df660deb6620148eb3320662430a29947b91e151b27588ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:73b564e82dbcce2a7fab889d42d97db3ff4239c2bef3c7821f03671f8ba0c562
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327575010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f30b119a6b6906ac0fb7c1f0c8f7de0acbf9a034583a9baedd5462ff2972b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:15 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:56:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9c2455f451781d20e3a57f975c5cf60b32a5ea9a2c0a84c54dfab11b206ce`  
		Last Modified: Wed, 27 Aug 2025 16:56:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a6fe3b02f5f443812f0440484b655a27006f973b661e061beee892f35131ca`  
		Last Modified: Wed, 27 Aug 2025 16:57:24 GMT  
		Size: 45.9 MB (45877907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98cf9c87c699ed396949c29973cdcb8a857cb2280cf4371a06a7e12ff1d022f`  
		Last Modified: Wed, 27 Aug 2025 16:56:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0d5bfcd1650a5d03e49c2647583651f231e28481d4ed01a60b83afbc6d207`  
		Last Modified: Wed, 27 Aug 2025 16:56:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670a3637fbb679e28052308ed6e48a33d01c96626d442e33f74c6f82695344cc`  
		Last Modified: Wed, 27 Aug 2025 16:56:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29`

```console
$ docker pull traefik@sha256:9d1f512777ee61a06e33e77021d50d66b8fcf313c5cb3fde3f5375eccf84f202
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v2.11.29` - linux; amd64

```console
$ docker pull traefik@sha256:ef194b47cdffffd46578478691150abf5dac2137328baa8018d8bb9fa1d77aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48879165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f1ecf2373092bdd8e52a11f6691b2c41aa5f97040e235c54eefc011386062`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0515b72f0cc67ea3ae08fdad1ad8beb0a8fd964c43f13e9752c67ba2a2b7366`  
		Last Modified: Wed, 27 Aug 2025 17:01:41 GMT  
		Size: 447.8 KB (447750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461195f44be0809defed6a87825edb85b164d5d0a264c96d1f4aff1ebbf2b574`  
		Last Modified: Wed, 27 Aug 2025 18:09:44 GMT  
		Size: 44.6 MB (44631356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:2ade12cf666ce72dc348e4e29569ea9033f9867f3e2861a9e8131c222d687593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.6 KB (856577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48383883228500cfe7e71b8cc19385d963057e5930fb8a43822a6ffddd02c551`

```dockerfile
```

-	Layers:
	-	`sha256:693c3c28391cd2a31bb91ee19fbde369a09a9c44b84a00182c856970c35a301c`  
		Last Modified: Wed, 27 Aug 2025 18:09:34 GMT  
		Size: 844.0 KB (844040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc96ca71e0435fa78c0c3e7fc773f3035006e75bf7c9dcffcbb5df534e73e8a`  
		Last Modified: Wed, 27 Aug 2025 18:09:35 GMT  
		Size: 12.5 KB (12537 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; arm variant v6

```console
$ docker pull traefik@sha256:f167694ccf4c99b36665a815414e69b72309a2ef440bc6541cde3a346dc8bc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44700698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370da53c00275152a1b8465452a8e0b8f17e918ca0f48db42597e110959c173c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f890fe69bca4ff8eb3489cb7f1ea54fa3b284ad5acd111963cf7c9106121c10`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 40.8 MB (40751135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cb41e07c5aff532c35fd24386540cc4e97670d9c4dec4b52b1c61dd3ef5132`  
		Last Modified: Wed, 27 Aug 2025 17:01:48 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:607349433ed7fc1091c03e1d0b8679699dff7aae431de92d3a2ac0573a3fe1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.4 KB (12436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a398ce1d98641c17b9a5620e9d71faec34d8ddb267bb6343c4c8a113a7c007`

```dockerfile
```

-	Layers:
	-	`sha256:0ee433723b058d37f54c878a9f320b347c1d73eaa2e6ff724fb06ca8945c9821`  
		Last Modified: Wed, 27 Aug 2025 18:09:38 GMT  
		Size: 12.4 KB (12436 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:1b47f982b405f9f9fa029b9f924a0683bb66395d4777255c0b29cf7edaf895ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45243795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1e751070a8fbc76f7dc4e3391251d178e580c7c9354b1388e7a652e362db5d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b5ca0013c90545f931f3187ef25879415ef0686615303f4146c7471158646`  
		Last Modified: Wed, 27 Aug 2025 17:00:18 GMT  
		Size: 40.7 MB (40663126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16fb4ccf9d8d0b4cf80443115894ed1cea94d95077076d89216cac9c855204f`  
		Last Modified: Wed, 27 Aug 2025 17:00:16 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:15f1612fe326d61d989f3b80694a485c7b5397d0db83483071d880df0769c0c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.8 KB (856825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a184b894974c6406390cbc238c9e25e87c99da427dcfb26ec6e3fb72765c4ac`

```dockerfile
```

-	Layers:
	-	`sha256:ebc9bf0be6405e6144c840de51890ae11e7cabea1d1e6397176728c8e9e49476`  
		Last Modified: Wed, 27 Aug 2025 18:09:41 GMT  
		Size: 844.1 KB (844132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28625b3d0d96bc20dfae94910da354762bad6d3c09869a4bd7a3456322ad5f3`  
		Last Modified: Wed, 27 Aug 2025 18:09:42 GMT  
		Size: 12.7 KB (12693 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; ppc64le

```console
$ docker pull traefik@sha256:fb4fb93c04b5579f3b837d2c031b6012d1ffcdda457de870c195e5d515f9e6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43245458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f930e177b128612c7b674cfc5210f2a88df32e1880425221d902f4571b157be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbc2968f8fd1eb17c3e7dae63497470b63757685a313a7e11ce58138ff539ae`  
		Last Modified: Wed, 27 Aug 2025 17:10:55 GMT  
		Size: 39.1 MB (39068019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e709bcd4a895201bdde2912728505809636956cc55bd68c2c24ca365a0a771`  
		Last Modified: Wed, 27 Aug 2025 17:10:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:e12687addd17aa37f76fe6b60a52ce0c555f08b9f334b34f9c0b1bb1af9f0ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e3912556e978a30d3e33a5a64963c9d9c6b0bc1689ecce2d4ad93021649e34`

```dockerfile
```

-	Layers:
	-	`sha256:c9b622ef5e884e63fe6490c69c8fc2c2825498e5286e44a527ef973efb82bfef`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 842.1 KB (842141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be376f9328eb13f6c07a50955cd0c75330c408076dc59985f47c4abc14a42ca`  
		Last Modified: Wed, 27 Aug 2025 18:09:46 GMT  
		Size: 12.6 KB (12601 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v2.11.29` - linux; s390x

```console
$ docker pull traefik@sha256:95af8372733c1683ab0ea00651d20c50342a102856b24c85dbdd6ac8f995a77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47345879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f687e38c4046d74d1595cee6461218ddb7088048db04bb6c0321401e92c654`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
COPY entrypoint.sh / # buildkit
# Tue, 26 Aug 2025 13:14:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Aug 2025 13:14:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 26 Aug 2025 13:14:56 GMT
CMD ["traefik"]
# Tue, 26 Aug 2025 13:14:56 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf539186cb47eb247f25a88398480d6a53353b16a9906ca97d56b8e9bf97aa`  
		Last Modified: Wed, 27 Aug 2025 17:09:44 GMT  
		Size: 43.3 MB (43251940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63217dd1feb81bce4d043ca9c5791559356450e5c84ec376455f59d4d8a303a8`  
		Last Modified: Wed, 27 Aug 2025 17:09:38 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:64197983ee7053f706e95e1f5d675fc65f2321195d3dff6ae582d4317907d2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.6 KB (854623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7753786057c28ca160c0ffe1976efd1d38212427fd393d8086b03aa8132cff3`

```dockerfile
```

-	Layers:
	-	`sha256:e581aad51ab2b6ee24ab0e2f0c5edd3ed64599c8ea3a5d890b50efd8bf15a5b8`  
		Last Modified: Wed, 27 Aug 2025 18:09:52 GMT  
		Size: 842.1 KB (842085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22daa7b6a23e0e21ab5deb69f071a11b811bbe64446fc4688080588afc028aad`  
		Last Modified: Wed, 27 Aug 2025 18:09:53 GMT  
		Size: 12.5 KB (12538 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v2.11.29-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:0ec8bd037b27de09939c7b3da3775de4abb4677b0748055376120d7181504758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2.11.29-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:531e7c4ddd99447e08351b4d6bc5c0422b1b4dc453bd512df3ff1dc05cf957d5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168058665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b88dfbf738a9fd8533bbcbefd39c9bc28a03db9ab5c7c547cd2b04616302f2`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:58:22 GMT
RUN cmd /S /C #(nop) COPY file:62077633f712881ec9f316398f13d332fdc2065b0651d9fa892a92e6c7058f8d in \ 
# Wed, 27 Aug 2025 16:58:25 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:58:26 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:58:27 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f80e4344df79fd556ec8244973291a15548667a8cb5a48c6fcd9de57d884bd8`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 45.4 MB (45395246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a74d6a766096699f51d62018f8c31ab2a10b26fb2c63b49349de7b71f15bc1`  
		Last Modified: Wed, 27 Aug 2025 17:00:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7977da73453c1acfac358763f4d922c8f64483cac66b6ff81203b69b61cba7`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdee3b77fee893cc6a120448a348926b3f5d71a1d84772c4add6f11519f3edb`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:56b3a9b79e2def1df660deb6620148eb3320662430a29947b91e151b27588ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v2.11.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:73b564e82dbcce2a7fab889d42d97db3ff4239c2bef3c7821f03671f8ba0c562
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327575010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f30b119a6b6906ac0fb7c1f0c8f7de0acbf9a034583a9baedd5462ff2972b4`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:12 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:15 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:16 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:56:17 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd9c2455f451781d20e3a57f975c5cf60b32a5ea9a2c0a84c54dfab11b206ce`  
		Last Modified: Wed, 27 Aug 2025 16:56:45 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a6fe3b02f5f443812f0440484b655a27006f973b661e061beee892f35131ca`  
		Last Modified: Wed, 27 Aug 2025 16:57:24 GMT  
		Size: 45.9 MB (45877907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98cf9c87c699ed396949c29973cdcb8a857cb2280cf4371a06a7e12ff1d022f`  
		Last Modified: Wed, 27 Aug 2025 16:56:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0d5bfcd1650a5d03e49c2647583651f231e28481d4ed01a60b83afbc6d207`  
		Last Modified: Wed, 27 Aug 2025 16:56:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670a3637fbb679e28052308ed6e48a33d01c96626d442e33f74c6f82695344cc`  
		Last Modified: Wed, 27 Aug 2025 16:56:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:b79db93a75530d01ff4181ae6deabb0aa6c7269538bcab700f2eff197fb83722
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
$ docker pull traefik@sha256:81e9ae4b24d81dddaeec331607fb1f5c89e7722b7db301b26045337310b02ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df847a19b384a02d6815ad145d267438250a90a59f08679145b61f790c64f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04439cdf28f8e9472b2dd39bc8bf09b16bd92bfbe064bc91064f36ef8dedc40b`  
		Last Modified: Wed, 27 Aug 2025 17:01:44 GMT  
		Size: 447.7 KB (447749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6b58dcb295e3222dee05ea5f341a59fe9a3456fefdd5f066c5a05c150112c`  
		Last Modified: Wed, 27 Aug 2025 17:34:19 GMT  
		Size: 45.5 MB (45475022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100956301a3856c3fd51ece02c0cb3c8656a830d0e475b68f204db53cc63151`  
		Last Modified: Wed, 27 Aug 2025 17:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:b17b59feb849d0844281037f1a3c5b30fe0f50e11bd67ff3a22f3bc0a4ddb535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da769548d68e432c33900981f87b1737c090a104912801108fbf6531ddcc09a`

```dockerfile
```

-	Layers:
	-	`sha256:07cae4063a61746920f6eabe2f9de8b079279989d8d2989d1c5e8fd77fcc3ff0`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10704978db0bf22e2cc7700bc14cc2f1a0f9406f490058d7c25a90570e5affe7`  
		Last Modified: Wed, 27 Aug 2025 18:10:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:211f6902527b39b5bdc09b5062f7a16a2edd09acf83dfa3cf8ede88f2054ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd2d50600dbd898bd575f11fd667a8379022c92e299e53329eabe0af285fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88e126b141e8ffbd63dda0357515d9531a4e7eb4992e441498a832fbc6d167`  
		Last Modified: Wed, 27 Aug 2025 17:32:07 GMT  
		Size: 41.2 MB (41230533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a507179ca736b6c36eb3f38d7e68e441905f346d80849451149e9184307646a`  
		Last Modified: Wed, 27 Aug 2025 17:01:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:e2f547be4b22769a1e26bcc073afa9a9402adba4b6ce2c71487f0192583f865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a2ed378bb6fd197772d5fdf803ad041a945f4ee122925b78b9deed98ef99b`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb145a4285206f0fae905684820445e06dd8aba96d30880dba85b1cb1d2bcf`  
		Last Modified: Wed, 27 Aug 2025 18:10:11 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e523711822b129d1bf22dd50ae4345fa97d824976ead3084ee6ea9986db5ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f5bf38404e1e55976630aea2fd8335606e3b6149c5af25f883997ec604ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56dfb33904ecb5e55d4c49849b180e3febf05faaee3000af3515c8f4801d6c8`  
		Last Modified: Wed, 27 Aug 2025 17:07:41 GMT  
		Size: 41.4 MB (41398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02498b828d62c3a782051fd83062771dd64177a438b77e5b96af404d06853a11`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:9845802d0e80ffb1937df4a782b7e602a94f68a5134df439707fea7c55b9e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c64a72a93e68ed8f64d8c1c39ccc9ef9383d6a6cebf5937da51274c1c0c78`

```dockerfile
```

-	Layers:
	-	`sha256:cc845f89b64086e6ec7896a77ce5c2e44d28e9779cea84ffe0b004eb192d4417`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01178cfe74e88e9ab78e4dd9b8f5cfa44f26647a8003a310d85c4124101fb7`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:e6927b5405f6cba179d82078a9890783981a8a86e0bc7ee4902386279ac3f15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6dc72c0c5c9239fee2b7f6aaca26e64efda1308bfb37c7a67ce2f89425ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b1143603366e8524f93ec7f3de917b3e31fe27f96c49317ab958da940d844`  
		Last Modified: Wed, 27 Aug 2025 17:09:27 GMT  
		Size: 39.4 MB (39445747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de4741918ce13525480ffd91dc6b216b62082473a4562fb5265523ce87582e`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:c3ed616eb5072d01a686dbc0be70849b3790f972bee8fa91f7afdf66a4f4783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555dfe3dd12c79cdf713ad6cb75d9345274917ce3722c33ab1c5bcbe950985f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f22fe69081680a56629c47c776443d1b08408f9e142383d1ff7e2c5ce64412`  
		Last Modified: Wed, 27 Aug 2025 18:10:17 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31193bbec1ab84a355b5a2da10f92ea2692592ace73072e792fbfb3daba1ed`  
		Last Modified: Wed, 27 Aug 2025 18:10:18 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:bc8fd0bcbef96b11674a70d3f43a2b5a1bf6883b7a4fb2e6d5c008096e9ded9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda3a5bb317f4f331a8114277c58e6ebaf160e795164a508c03fd750769a1b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda85489cd9f2f30f94f1f3e7d431009ac97ba8e42352ede9b572633862d8adc`  
		Last Modified: Wed, 27 Aug 2025 17:08:10 GMT  
		Size: 43.7 MB (43660750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49270d38d651efb3f9113b69ff3a6d48e90266e6e3ed5e42576ed16a8d0593e4`  
		Last Modified: Wed, 27 Aug 2025 17:08:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:6b107cf683ea0df17071ad9ecd2abc9530828fa095e0499d2de91ce2f5ab7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e1dc33803d26f10070af62f90649ee9f35e68c12008603f1f5aa8086470e2`

```dockerfile
```

-	Layers:
	-	`sha256:4e793b9108e9dd2354537ae118dcd9f447610762d3531112105809237095c203`  
		Last Modified: Wed, 27 Aug 2025 18:10:23 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c587e47439872acb4deba3d3e52a9e70b727bfd6eac624aae349cab3593a983`  
		Last Modified: Wed, 27 Aug 2025 18:10:24 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e5922966178c631047e534d82f05fcca084a5f9eb086bf41a5f884057e2c5fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:d16fbba3a116ae9b605b641394b1cdfbe37f9ef5c6e8179d507255f9be853575
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3f6efca79296ba17e096dbb803f1f24607391d4983e2dd910265ff582d4d9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:59:49 GMT
RUN cmd /S /C #(nop) COPY file:abd9a8b820cc1b70a903e8293c4f75175a30ea1d20fc7b8259deacc8d8acb6e8 in \ 
# Wed, 27 Aug 2025 16:59:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:59:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:59:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8513503707a98f555015c891873c823cf765c7c91d4b5df66c73c9bf6778ce`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 46.2 MB (46223885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493ed9f0ad984d8d03c6abf141523f091e2746bf1ed9725b641bf2651855918`  
		Last Modified: Wed, 27 Aug 2025 17:00:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a2f341d8d4358dfa68c8bfb516a6b6c18989822e1372750cba9e1403a348ff`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6ec331bc39da54ef1e96ed28e53983c6908a221e6d7a542a6a757dd9b8822`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e4e7d77b6260491390bfd5085a4481640b2f0a0e8f653f28dbeeefe3b7073cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:c9bfe93694c87dbce8d8de8c90e58a5298be047ae5bfee82de9e6b2252a096fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328429380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd53247d0cbd73975920d06fe678a16f71974d3386d6d25a69423e0b7f3f6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:58 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:57:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983f838df296448d31c1c82c150b89bcae7404cdd75d0d1610baeea4cf5e2551`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959202625b9458dfcdc2761fcf90a6f1f2e08849ac802716a8c672ddc9af814c`  
		Last Modified: Wed, 27 Aug 2025 16:57:25 GMT  
		Size: 46.7 MB (46732219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19b9802aaf9f4dddfdf6b0a18f45fd6648a90dce24328df327692a176f3cd5`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a15cf6da19475e9ba544b5e5af0e4d1ba42dad4a29a0f383d0eb06c1828bdbf`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b0d24e3f75d640c4125d49fe8a8fa61ee0e46e50f36c3f4e989574cde314ed`  
		Last Modified: Wed, 27 Aug 2025 16:57:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5`

```console
$ docker pull traefik@sha256:b79db93a75530d01ff4181ae6deabb0aa6c7269538bcab700f2eff197fb83722
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

### `traefik:v3.5` - linux; amd64

```console
$ docker pull traefik@sha256:81e9ae4b24d81dddaeec331607fb1f5c89e7722b7db301b26045337310b02ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df847a19b384a02d6815ad145d267438250a90a59f08679145b61f790c64f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04439cdf28f8e9472b2dd39bc8bf09b16bd92bfbe064bc91064f36ef8dedc40b`  
		Last Modified: Wed, 27 Aug 2025 17:01:44 GMT  
		Size: 447.7 KB (447749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6b58dcb295e3222dee05ea5f341a59fe9a3456fefdd5f066c5a05c150112c`  
		Last Modified: Wed, 27 Aug 2025 17:34:19 GMT  
		Size: 45.5 MB (45475022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100956301a3856c3fd51ece02c0cb3c8656a830d0e475b68f204db53cc63151`  
		Last Modified: Wed, 27 Aug 2025 17:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:b17b59feb849d0844281037f1a3c5b30fe0f50e11bd67ff3a22f3bc0a4ddb535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da769548d68e432c33900981f87b1737c090a104912801108fbf6531ddcc09a`

```dockerfile
```

-	Layers:
	-	`sha256:07cae4063a61746920f6eabe2f9de8b079279989d8d2989d1c5e8fd77fcc3ff0`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10704978db0bf22e2cc7700bc14cc2f1a0f9406f490058d7c25a90570e5affe7`  
		Last Modified: Wed, 27 Aug 2025 18:10:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:211f6902527b39b5bdc09b5062f7a16a2edd09acf83dfa3cf8ede88f2054ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd2d50600dbd898bd575f11fd667a8379022c92e299e53329eabe0af285fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88e126b141e8ffbd63dda0357515d9531a4e7eb4992e441498a832fbc6d167`  
		Last Modified: Wed, 27 Aug 2025 17:32:07 GMT  
		Size: 41.2 MB (41230533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a507179ca736b6c36eb3f38d7e68e441905f346d80849451149e9184307646a`  
		Last Modified: Wed, 27 Aug 2025 17:01:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:e2f547be4b22769a1e26bcc073afa9a9402adba4b6ce2c71487f0192583f865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a2ed378bb6fd197772d5fdf803ad041a945f4ee122925b78b9deed98ef99b`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb145a4285206f0fae905684820445e06dd8aba96d30880dba85b1cb1d2bcf`  
		Last Modified: Wed, 27 Aug 2025 18:10:11 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e523711822b129d1bf22dd50ae4345fa97d824976ead3084ee6ea9986db5ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f5bf38404e1e55976630aea2fd8335606e3b6149c5af25f883997ec604ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56dfb33904ecb5e55d4c49849b180e3febf05faaee3000af3515c8f4801d6c8`  
		Last Modified: Wed, 27 Aug 2025 17:07:41 GMT  
		Size: 41.4 MB (41398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02498b828d62c3a782051fd83062771dd64177a438b77e5b96af404d06853a11`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:9845802d0e80ffb1937df4a782b7e602a94f68a5134df439707fea7c55b9e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c64a72a93e68ed8f64d8c1c39ccc9ef9383d6a6cebf5937da51274c1c0c78`

```dockerfile
```

-	Layers:
	-	`sha256:cc845f89b64086e6ec7896a77ce5c2e44d28e9779cea84ffe0b004eb192d4417`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01178cfe74e88e9ab78e4dd9b8f5cfa44f26647a8003a310d85c4124101fb7`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:e6927b5405f6cba179d82078a9890783981a8a86e0bc7ee4902386279ac3f15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6dc72c0c5c9239fee2b7f6aaca26e64efda1308bfb37c7a67ce2f89425ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b1143603366e8524f93ec7f3de917b3e31fe27f96c49317ab958da940d844`  
		Last Modified: Wed, 27 Aug 2025 17:09:27 GMT  
		Size: 39.4 MB (39445747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de4741918ce13525480ffd91dc6b216b62082473a4562fb5265523ce87582e`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:c3ed616eb5072d01a686dbc0be70849b3790f972bee8fa91f7afdf66a4f4783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555dfe3dd12c79cdf713ad6cb75d9345274917ce3722c33ab1c5bcbe950985f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f22fe69081680a56629c47c776443d1b08408f9e142383d1ff7e2c5ce64412`  
		Last Modified: Wed, 27 Aug 2025 18:10:17 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31193bbec1ab84a355b5a2da10f92ea2692592ace73072e792fbfb3daba1ed`  
		Last Modified: Wed, 27 Aug 2025 18:10:18 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:3d129b096cda6d4d8e7bed7eb574c19461dfec84289ed46dc67983bf9ef2ce56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56488220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37fe6797c653be54bf52c8cf083868955283277512ab714bd977e89e227ad301`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.0/traefik_v3.5.0_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
COPY entrypoint.sh / # buildkit
# Wed, 23 Jul 2025 14:06:55 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Jul 2025 14:06:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jul 2025 14:06:55 GMT
CMD ["traefik"]
# Wed, 23 Jul 2025 14:06:55 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.0 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84737325fa6ef3f916a1ff5eeddd40772e568530d306452b8dd60b85c179e558`  
		Last Modified: Wed, 23 Jul 2025 16:40:10 GMT  
		Size: 448.1 KB (448054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def266ba1e79d29f5e57bd284d16760ca78fb1435a77461fe5241ed3c33ed8cf`  
		Last Modified: Wed, 23 Jul 2025 16:40:21 GMT  
		Size: 52.5 MB (52526996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226680637c931a433ee307e8df1e2c3213341d70b97f6f616238435e45d91e3d`  
		Last Modified: Wed, 23 Jul 2025 16:40:08 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:4c21e005c0d4aa9797d9707d7e8784afe69d1441ebca6f1c0575bf01e06c05d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.3 KB (835298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f074aa9a8cdba1f7d68b97d02d2cbb4feb96f00e42f594f4a4c37be86fac937b`

```dockerfile
```

-	Layers:
	-	`sha256:26b44c741b41f51eb0d38339129d7e199ca9820acfdb5d8198ccb6352e5f4c76`  
		Last Modified: Wed, 23 Jul 2025 18:10:14 GMT  
		Size: 822.4 KB (822417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3396ae78c3f9c1d10dbe63f2252356beb6fe37dd0a2db29d755710b7f3944875`  
		Last Modified: Wed, 23 Jul 2025 18:10:15 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; s390x

```console
$ docker pull traefik@sha256:bc8fd0bcbef96b11674a70d3f43a2b5a1bf6883b7a4fb2e6d5c008096e9ded9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda3a5bb317f4f331a8114277c58e6ebaf160e795164a508c03fd750769a1b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda85489cd9f2f30f94f1f3e7d431009ac97ba8e42352ede9b572633862d8adc`  
		Last Modified: Wed, 27 Aug 2025 17:08:10 GMT  
		Size: 43.7 MB (43660750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49270d38d651efb3f9113b69ff3a6d48e90266e6e3ed5e42576ed16a8d0593e4`  
		Last Modified: Wed, 27 Aug 2025 17:08:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6b107cf683ea0df17071ad9ecd2abc9530828fa095e0499d2de91ce2f5ab7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e1dc33803d26f10070af62f90649ee9f35e68c12008603f1f5aa8086470e2`

```dockerfile
```

-	Layers:
	-	`sha256:4e793b9108e9dd2354537ae118dcd9f447610762d3531112105809237095c203`  
		Last Modified: Wed, 27 Aug 2025 18:10:23 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c587e47439872acb4deba3d3e52a9e70b727bfd6eac624aae349cab3593a983`  
		Last Modified: Wed, 27 Aug 2025 18:10:24 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e5922966178c631047e534d82f05fcca084a5f9eb086bf41a5f884057e2c5fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:d16fbba3a116ae9b605b641394b1cdfbe37f9ef5c6e8179d507255f9be853575
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3f6efca79296ba17e096dbb803f1f24607391d4983e2dd910265ff582d4d9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:59:49 GMT
RUN cmd /S /C #(nop) COPY file:abd9a8b820cc1b70a903e8293c4f75175a30ea1d20fc7b8259deacc8d8acb6e8 in \ 
# Wed, 27 Aug 2025 16:59:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:59:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:59:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8513503707a98f555015c891873c823cf765c7c91d4b5df66c73c9bf6778ce`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 46.2 MB (46223885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493ed9f0ad984d8d03c6abf141523f091e2746bf1ed9725b641bf2651855918`  
		Last Modified: Wed, 27 Aug 2025 17:00:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a2f341d8d4358dfa68c8bfb516a6b6c18989822e1372750cba9e1403a348ff`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6ec331bc39da54ef1e96ed28e53983c6908a221e6d7a542a6a757dd9b8822`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e4e7d77b6260491390bfd5085a4481640b2f0a0e8f653f28dbeeefe3b7073cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:c9bfe93694c87dbce8d8de8c90e58a5298be047ae5bfee82de9e6b2252a096fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328429380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd53247d0cbd73975920d06fe678a16f71974d3386d6d25a69423e0b7f3f6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:58 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:57:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983f838df296448d31c1c82c150b89bcae7404cdd75d0d1610baeea4cf5e2551`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959202625b9458dfcdc2761fcf90a6f1f2e08849ac802716a8c672ddc9af814c`  
		Last Modified: Wed, 27 Aug 2025 16:57:25 GMT  
		Size: 46.7 MB (46732219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19b9802aaf9f4dddfdf6b0a18f45fd6648a90dce24328df327692a176f3cd5`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a15cf6da19475e9ba544b5e5af0e4d1ba42dad4a29a0f383d0eb06c1828bdbf`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b0d24e3f75d640c4125d49fe8a8fa61ee0e46e50f36c3f4e989574cde314ed`  
		Last Modified: Wed, 27 Aug 2025 16:57:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.1`

```console
$ docker pull traefik@sha256:c56901603318ee375477ee5c3f50d175d3ec42dc102efc2f1158f0756ba4dffa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `traefik:v3.5.1` - linux; amd64

```console
$ docker pull traefik@sha256:81e9ae4b24d81dddaeec331607fb1f5c89e7722b7db301b26045337310b02ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49722829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8df847a19b384a02d6815ad145d267438250a90a59f08679145b61f790c64f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04439cdf28f8e9472b2dd39bc8bf09b16bd92bfbe064bc91064f36ef8dedc40b`  
		Last Modified: Wed, 27 Aug 2025 17:01:44 GMT  
		Size: 447.7 KB (447749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e6b58dcb295e3222dee05ea5f341a59fe9a3456fefdd5f066c5a05c150112c`  
		Last Modified: Wed, 27 Aug 2025 17:34:19 GMT  
		Size: 45.5 MB (45475022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7100956301a3856c3fd51ece02c0cb3c8656a830d0e475b68f204db53cc63151`  
		Last Modified: Wed, 27 Aug 2025 17:01:50 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:b17b59feb849d0844281037f1a3c5b30fe0f50e11bd67ff3a22f3bc0a4ddb535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da769548d68e432c33900981f87b1737c090a104912801108fbf6531ddcc09a`

```dockerfile
```

-	Layers:
	-	`sha256:07cae4063a61746920f6eabe2f9de8b079279989d8d2989d1c5e8fd77fcc3ff0`  
		Last Modified: Wed, 27 Aug 2025 18:10:07 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10704978db0bf22e2cc7700bc14cc2f1a0f9406f490058d7c25a90570e5affe7`  
		Last Modified: Wed, 27 Aug 2025 18:10:08 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.1` - linux; arm variant v6

```console
$ docker pull traefik@sha256:211f6902527b39b5bdc09b5062f7a16a2edd09acf83dfa3cf8ede88f2054ab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45180096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2dd2d50600dbd898bd575f11fd667a8379022c92e299e53329eabe0af285fc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c0e30c94e3b87e8495f73eb60c6c877005b636c6e0d5b83e900bf0b2deeb7`  
		Last Modified: Tue, 15 Jul 2025 22:49:24 GMT  
		Size: 448.3 KB (448283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88e126b141e8ffbd63dda0357515d9531a4e7eb4992e441498a832fbc6d167`  
		Last Modified: Wed, 27 Aug 2025 17:32:07 GMT  
		Size: 41.2 MB (41230533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a507179ca736b6c36eb3f38d7e68e441905f346d80849451149e9184307646a`  
		Last Modified: Wed, 27 Aug 2025 17:01:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:e2f547be4b22769a1e26bcc073afa9a9402adba4b6ce2c71487f0192583f865d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a2ed378bb6fd197772d5fdf803ad041a945f4ee122925b78b9deed98ef99b`

```dockerfile
```

-	Layers:
	-	`sha256:9ebb145a4285206f0fae905684820445e06dd8aba96d30880dba85b1cb1d2bcf`  
		Last Modified: Wed, 27 Aug 2025 18:10:11 GMT  
		Size: 12.7 KB (12717 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.1` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:8e523711822b129d1bf22dd50ae4345fa97d824976ead3084ee6ea9986db5ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f5bf38404e1e55976630aea2fd8335606e3b6149c5af25f883997ec604ee80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89f4a655d925f1f0810e4e6dad8cf5ee00a953bb997be55084efe899133bcc7`  
		Last Modified: Wed, 27 Aug 2025 17:00:15 GMT  
		Size: 449.6 KB (449550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56dfb33904ecb5e55d4c49849b180e3febf05faaee3000af3515c8f4801d6c8`  
		Last Modified: Wed, 27 Aug 2025 17:07:41 GMT  
		Size: 41.4 MB (41398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02498b828d62c3a782051fd83062771dd64177a438b77e5b96af404d06853a11`  
		Last Modified: Wed, 27 Aug 2025 17:07:37 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:9845802d0e80ffb1937df4a782b7e602a94f68a5134df439707fea7c55b9e4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c64a72a93e68ed8f64d8c1c39ccc9ef9383d6a6cebf5937da51274c1c0c78`

```dockerfile
```

-	Layers:
	-	`sha256:cc845f89b64086e6ec7896a77ce5c2e44d28e9779cea84ffe0b004eb192d4417`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01178cfe74e88e9ab78e4dd9b8f5cfa44f26647a8003a310d85c4124101fb7`  
		Last Modified: Wed, 27 Aug 2025 18:10:14 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.1` - linux; ppc64le

```console
$ docker pull traefik@sha256:e6927b5405f6cba179d82078a9890783981a8a86e0bc7ee4902386279ac3f15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:896c6dc72c0c5c9239fee2b7f6aaca26e64efda1308bfb37c7a67ce2f89425ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee15ae3a4e80bb53973164d7de904d8c2cd5b1a2d489ba18eca323de1e820f`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 450.0 KB (449958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b1143603366e8524f93ec7f3de917b3e31fe27f96c49317ab958da940d844`  
		Last Modified: Wed, 27 Aug 2025 17:09:27 GMT  
		Size: 39.4 MB (39445747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9de4741918ce13525480ffd91dc6b216b62082473a4562fb5265523ce87582e`  
		Last Modified: Wed, 27 Aug 2025 17:09:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:c3ed616eb5072d01a686dbc0be70849b3790f972bee8fa91f7afdf66a4f4783f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555dfe3dd12c79cdf713ad6cb75d9345274917ce3722c33ab1c5bcbe950985f`

```dockerfile
```

-	Layers:
	-	`sha256:e0f22fe69081680a56629c47c776443d1b08408f9e142383d1ff7e2c5ce64412`  
		Last Modified: Wed, 27 Aug 2025 18:10:17 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d31193bbec1ab84a355b5a2da10f92ea2692592ace73072e792fbfb3daba1ed`  
		Last Modified: Wed, 27 Aug 2025 18:10:18 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.1` - linux; s390x

```console
$ docker pull traefik@sha256:bc8fd0bcbef96b11674a70d3f43a2b5a1bf6883b7a4fb2e6d5c008096e9ded9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47754691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda3a5bb317f4f331a8114277c58e6ebaf160e795164a508c03fd750769a1b5a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
COPY entrypoint.sh / # buildkit
# Wed, 27 Aug 2025 09:21:20 GMT
EXPOSE map[80/tcp:{}]
# Wed, 27 Aug 2025 09:21:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 27 Aug 2025 09:21:20 GMT
CMD ["traefik"]
# Wed, 27 Aug 2025 09:21:20 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa538300aa861439853b1613ab1dff9c4b0fc8bfc64f5fd1aa4a14a93bc19873`  
		Last Modified: Wed, 27 Aug 2025 17:08:05 GMT  
		Size: 448.6 KB (448600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda85489cd9f2f30f94f1f3e7d431009ac97ba8e42352ede9b572633862d8adc`  
		Last Modified: Wed, 27 Aug 2025 17:08:10 GMT  
		Size: 43.7 MB (43660750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49270d38d651efb3f9113b69ff3a6d48e90266e6e3ed5e42576ed16a8d0593e4`  
		Last Modified: Wed, 27 Aug 2025 17:08:06 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.1` - unknown; unknown

```console
$ docker pull traefik@sha256:6b107cf683ea0df17071ad9ecd2abc9530828fa095e0499d2de91ce2f5ab7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028e1dc33803d26f10070af62f90649ee9f35e68c12008603f1f5aa8086470e2`

```dockerfile
```

-	Layers:
	-	`sha256:4e793b9108e9dd2354537ae118dcd9f447610762d3531112105809237095c203`  
		Last Modified: Wed, 27 Aug 2025 18:10:23 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c587e47439872acb4deba3d3e52a9e70b727bfd6eac624aae349cab3593a983`  
		Last Modified: Wed, 27 Aug 2025 18:10:24 GMT  
		Size: 12.8 KB (12810 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.5.1-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:e5922966178c631047e534d82f05fcca084a5f9eb086bf41a5f884057e2c5fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5.1-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:d16fbba3a116ae9b605b641394b1cdfbe37f9ef5c6e8179d507255f9be853575
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e3f6efca79296ba17e096dbb803f1f24607391d4983e2dd910265ff582d4d9`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Wed, 27 Aug 2025 16:59:49 GMT
RUN cmd /S /C #(nop) COPY file:abd9a8b820cc1b70a903e8293c4f75175a30ea1d20fc7b8259deacc8d8acb6e8 in \ 
# Wed, 27 Aug 2025 16:59:51 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 27 Aug 2025 16:59:52 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:59:53 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8513503707a98f555015c891873c823cf765c7c91d4b5df66c73c9bf6778ce`  
		Last Modified: Wed, 27 Aug 2025 17:00:43 GMT  
		Size: 46.2 MB (46223885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0493ed9f0ad984d8d03c6abf141523f091e2746bf1ed9725b641bf2651855918`  
		Last Modified: Wed, 27 Aug 2025 17:00:27 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a2f341d8d4358dfa68c8bfb516a6b6c18989822e1372750cba9e1403a348ff`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6ec331bc39da54ef1e96ed28e53983c6908a221e6d7a542a6a757dd9b8822`  
		Last Modified: Wed, 27 Aug 2025 17:00:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.1-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e4e7d77b6260491390bfd5085a4481640b2f0a0e8f653f28dbeeefe3b7073cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:c9bfe93694c87dbce8d8de8c90e58a5298be047ae5bfee82de9e6b2252a096fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328429380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd53247d0cbd73975920d06fe678a16f71974d3386d6d25a69423e0b7f3f6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:58 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:57:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983f838df296448d31c1c82c150b89bcae7404cdd75d0d1610baeea4cf5e2551`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959202625b9458dfcdc2761fcf90a6f1f2e08849ac802716a8c672ddc9af814c`  
		Last Modified: Wed, 27 Aug 2025 16:57:25 GMT  
		Size: 46.7 MB (46732219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19b9802aaf9f4dddfdf6b0a18f45fd6648a90dce24328df327692a176f3cd5`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a15cf6da19475e9ba544b5e5af0e4d1ba42dad4a29a0f383d0eb06c1828bdbf`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b0d24e3f75d640c4125d49fe8a8fa61ee0e46e50f36c3f4e989574cde314ed`  
		Last Modified: Wed, 27 Aug 2025 16:57:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e4e7d77b6260491390bfd5085a4481640b2f0a0e8f653f28dbeeefe3b7073cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:c9bfe93694c87dbce8d8de8c90e58a5298be047ae5bfee82de9e6b2252a096fc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328429380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdd53247d0cbd73975920d06fe678a16f71974d3386d6d25a69423e0b7f3f6e`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Wed, 27 Aug 2025 16:55:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 27 Aug 2025 16:56:55 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.1/traefik_v3.5.1_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 27 Aug 2025 16:56:58 GMT
EXPOSE 80
# Wed, 27 Aug 2025 16:56:59 GMT
ENTRYPOINT ["/traefik"]
# Wed, 27 Aug 2025 16:57:00 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.1 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983f838df296448d31c1c82c150b89bcae7404cdd75d0d1610baeea4cf5e2551`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959202625b9458dfcdc2761fcf90a6f1f2e08849ac802716a8c672ddc9af814c`  
		Last Modified: Wed, 27 Aug 2025 16:57:25 GMT  
		Size: 46.7 MB (46732219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc19b9802aaf9f4dddfdf6b0a18f45fd6648a90dce24328df327692a176f3cd5`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a15cf6da19475e9ba544b5e5af0e4d1ba42dad4a29a0f383d0eb06c1828bdbf`  
		Last Modified: Wed, 27 Aug 2025 16:57:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b0d24e3f75d640c4125d49fe8a8fa61ee0e46e50f36c3f4e989574cde314ed`  
		Last Modified: Wed, 27 Aug 2025 16:57:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
