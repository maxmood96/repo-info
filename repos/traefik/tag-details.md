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
-	[`traefik:3.5.3`](#traefik353)
-	[`traefik:3.5.3-nanoserver-ltsc2022`](#traefik353-nanoserver-ltsc2022)
-	[`traefik:3.5.3-windowsservercore-ltsc2022`](#traefik353-windowsservercore-ltsc2022)
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
-	[`traefik:v3.5.3`](#traefikv353)
-	[`traefik:v3.5.3-nanoserver-ltsc2022`](#traefikv353-nanoserver-ltsc2022)
-	[`traefik:v3.5.3-windowsservercore-ltsc2022`](#traefikv353-windowsservercore-ltsc2022)
-	[`traefik:windowsservercore-ltsc2022`](#traefikwindowsservercore-ltsc2022)

## `traefik:2`

```console
$ docker pull traefik@sha256:7590a0dbb5ca6af50936b50406f70b4cddd17f6ffdf36aa1fcac0a3b1f7e3113
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
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
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
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11`

```console
$ docker pull traefik@sha256:7590a0dbb5ca6af50936b50406f70b4cddd17f6ffdf36aa1fcac0a3b1f7e3113
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
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
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
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29`

```console
$ docker pull traefik@sha256:7590a0dbb5ca6af50936b50406f70b4cddd17f6ffdf36aa1fcac0a3b1f7e3113
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

### `traefik:2.11.29` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
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
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2.11.29-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:2.11.29-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:2.11.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3`

```console
$ docker pull traefik@sha256:0ddcf820b6fa9988d851e290783962092fc91d53bd183c0c0f1b742f5560eb65
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
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; riscv64

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5`

```console
$ docker pull traefik@sha256:84eb6c0e67c99fa026bf1bf4b0afd9ad44350d375b4ebc5049c5f70543a729d6
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
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.3`

```console
$ docker pull traefik@sha256:84eb6c0e67c99fa026bf1bf4b0afd9ad44350d375b4ebc5049c5f70543a729d6
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

### `traefik:3.5.3` - linux; amd64

```console
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5.3` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:3.5.3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5.3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou`

```console
$ docker pull traefik@sha256:84eb6c0e67c99fa026bf1bf4b0afd9ad44350d375b4ebc5049c5f70543a729d6
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
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:chabichou-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:chabichou-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:chabichou-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:84eb6c0e67c99fa026bf1bf4b0afd9ad44350d375b4ebc5049c5f70543a729d6
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
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:latest` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:mimolette`

```console
$ docker pull traefik@sha256:7590a0dbb5ca6af50936b50406f70b4cddd17f6ffdf36aa1fcac0a3b1f7e3113
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
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:mimolette` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
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
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:mimolette-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:mimolette-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:mimolette-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2`

```console
$ docker pull traefik@sha256:7590a0dbb5ca6af50936b50406f70b4cddd17f6ffdf36aa1fcac0a3b1f7e3113
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
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
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
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11`

```console
$ docker pull traefik@sha256:7590a0dbb5ca6af50936b50406f70b4cddd17f6ffdf36aa1fcac0a3b1f7e3113
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
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
		Size: 12.6 KB (12601 bytes)  
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
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2.11-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29`

```console
$ docker pull traefik@sha256:7590a0dbb5ca6af50936b50406f70b4cddd17f6ffdf36aa1fcac0a3b1f7e3113
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

### `traefik:v2.11.29` - linux; riscv64

```console
$ docker pull traefik@sha256:06f2d9076c6c55410fee4798125a2295db4e4261254d0d77d9c2bc6c4999760f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47276175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df97caac802fa714df9d7878c8a700edca5a4a1d9a86f17b383ef8b2c2406ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519450a542a11f54d1b0f31b0d6a41d4499634fa6233c3080bb276faed1c7a57`  
		Last Modified: Fri, 29 Aug 2025 13:27:45 GMT  
		Size: 43.3 MB (43314948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f0a64e84dc52f5e5dd3eeb0df79a0deac72196f64786b3df6099d3cf6513d5`  
		Last Modified: Fri, 29 Aug 2025 13:27:40 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v2.11.29` - unknown; unknown

```console
$ docker pull traefik@sha256:05476c8117e125f09b723744748d45e99abfb1a73517fa6a21e82b323da64517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **854.7 KB (854738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc76f0b6f30320ad1c8f1956817d4d79e6d713cbd9b3c82835ee7dc2595586`

```dockerfile
```

-	Layers:
	-	`sha256:0e67a88d5f8bf3bd66ced25d151871ecaffe169c91ede66e2b61ff389152d798`  
		Last Modified: Fri, 29 Aug 2025 15:09:30 GMT  
		Size: 842.1 KB (842137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65bfac21e38847ba42f36e04589808391c92eb05f1b92654955630dacd88d5ac`  
		Last Modified: Fri, 29 Aug 2025 15:09:31 GMT  
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
$ docker pull traefik@sha256:cd311a633e1231d6696cb2d80c234fa081fdfb35248e5ef883f3770767c8310e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2.11.29-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0f75aea2adc142ff7f07b1c0c59a65ad5c2505d7785634bccd20bffe8c314265
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.1 MB (168118507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba406aeb9212f947ed071bb82f14e9f9960e1037ad31eaca862c12857a81f2d`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:12 GMT
RUN cmd /S /C #(nop) COPY file:0585088e2501b4fe7d23696a986d69a88664ae32a0a5c6dbba826f44c90cd343 in \ 
# Wed, 10 Sep 2025 22:18:14 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:15 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518d68abbd024fd07d72b8ffc5b9fe9836e18eadaeab1a918e054c6e045c7f`  
		Last Modified: Thu, 11 Sep 2025 00:09:30 GMT  
		Size: 45.4 MB (45395358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d66e5df2dbb0889fc0c3ff2e50e14e6a8b00a520df4a52bff3c8963e9cab487`  
		Last Modified: Wed, 10 Sep 2025 22:39:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ca51b3245e8a18a5e4a52617e312ce930c7f1050d9a6379ca21bbffda0f92`  
		Last Modified: Wed, 10 Sep 2025 22:39:51 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6033fbf147dc699196a5b78976c5ca0e86f9b90078597b4f5a32d451155463f`  
		Last Modified: Wed, 10 Sep 2025 22:39:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v2.11.29-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:470caeb58072190766e4621bb4779aca2e50536121f02df79757d4153ee58f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v2.11.29-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:72cee2f8591609d581317234ce85c39d50572651991c6e3c0892b2696b7528c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328051108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8febee4a745a78638c1958f64f1f3497537325d52968e82d38a2bce853f347`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:00 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.11.29/traefik_v2.11.29_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:01 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:01 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.11.29 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092cf423890c898a0b3b984ccece14afd3ce3289fc810560277fed3b2d90a2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacbb6fd31524f801b2ad24f0c909f3211e829326910562d09b998073f3ac878`  
		Last Modified: Wed, 10 Sep 2025 21:55:36 GMT  
		Size: 45.9 MB (45900930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cdf5d68df8a7940d9b48d41751fcf40c0d8ecefb23a84b10261ca74ed2b78e`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295116fb750712e691061785819d3f712040339e7518bba2f54fb3f65d4627ba`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5697032f0db37764bd04513df2ecd9fc68ee8ca4f92ca6a851d8ef22a419b62f`  
		Last Modified: Wed, 10 Sep 2025 21:55:31 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3`

```console
$ docker pull traefik@sha256:84eb6c0e67c99fa026bf1bf4b0afd9ad44350d375b4ebc5049c5f70543a729d6
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
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5`

```console
$ docker pull traefik@sha256:84eb6c0e67c99fa026bf1bf4b0afd9ad44350d375b4ebc5049c5f70543a729d6
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
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.3`

```console
$ docker pull traefik@sha256:84eb6c0e67c99fa026bf1bf4b0afd9ad44350d375b4ebc5049c5f70543a729d6
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

### `traefik:v3.5.3` - linux; amd64

```console
$ docker pull traefik@sha256:15b1bd7e732ccff4cc480a0987c305d737e5f92c080f7ffad0d8b7ea91143c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49704160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2860160aef65a57e49849edbf51392320a9e494f746a95e50ac652c8301c5d88`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50991f7b3346ba0ba37f18e08d9765414087b9da38107e53a9f814b3f707287b`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 447.7 KB (447744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdf3fff453a21772fdb0a7e00e9816db2ac0228aa82b6e781a0c1486fb1973e`  
		Last Modified: Fri, 26 Sep 2025 16:58:10 GMT  
		Size: 45.5 MB (45456357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2c2e6bd74d1246f1d5f22a57020a68d649a1a0b9b0a292642fa72e7ba51140`  
		Last Modified: Fri, 26 Sep 2025 16:57:59 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:f5f8f803a7a1a738395ec514560b736f638c4fd68b45af3355b3fefaa0093ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.7 KB (842726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8171af4f663bce7d3903143188951d2e8582531a32df4a0ffff4a347edca644c`

```dockerfile
```

-	Layers:
	-	`sha256:a7eb3802d91d45d561e82d815646df660dfd267d629e35d741ac3032006e8bd3`  
		Last Modified: Fri, 26 Sep 2025 18:10:29 GMT  
		Size: 829.9 KB (829915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd2a8c2e4c0f2aa0a3327ad01689409f4315783b3fb414044a559d8f216daaf7`  
		Last Modified: Fri, 26 Sep 2025 18:10:30 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; arm variant v6

```console
$ docker pull traefik@sha256:ec38456a7aefbe3e29cda5ce9a6960284bffe0c036450d92d0af2b513010d2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45171815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982759a856654feafd331ca970ae2f84703981f3a7035cc059ff797774079d9f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d0dedb8cca207d1bd2fd5b7471b3cbd238d51dd63c4b891e5e3d3d62411280`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 448.3 KB (448272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5497ab8e64e72798728b8de667702e9a8025df0a7b0218f59437ea300738ac21`  
		Last Modified: Fri, 26 Sep 2025 17:09:13 GMT  
		Size: 41.2 MB (41222263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74cb6dd5fddb935996d0cb71779d5fa0497507022704bf27e212218dbabe505`  
		Last Modified: Fri, 26 Sep 2025 16:57:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:3160cbfac643c7c24fcac32f829baa5bc833b4eea030188edfc7b846fe0fdb63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 KB (12721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd110bcdae4addd225e7e11aec8594bf55fbd81e1531423e56197b641a53dc2`

```dockerfile
```

-	Layers:
	-	`sha256:65191b52248e2546280a171cffbb4b719725bb86f4893bfa7a141817b801bb3d`  
		Last Modified: Fri, 26 Sep 2025 18:10:33 GMT  
		Size: 12.7 KB (12721 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:74d368fba4cda36139a3bf8538cff4b6b97d7bdde8c2e222ea37dee43357e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45961786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae46b0c761a39fef66557edcb41904f74017370570276bf4110223c969fd2eb2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3275bec727f5723c464909172d7a52f600711811118f7a262d97c6ee33dde`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 449.6 KB (449565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381c97138128a4faccf17ebaa8396a15c0d8bc3f380479afd90a60275a3f381e`  
		Last Modified: Fri, 26 Sep 2025 16:57:13 GMT  
		Size: 41.4 MB (41381101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211638b0c204d8880a76ef0c4261f56efe54e6e8333783c3668ebe40bc70ebd`  
		Last Modified: Fri, 26 Sep 2025 16:57:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:a1d2b2eeb52b61b86a97934221a1856935480a62e0659042a53811d694040c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.0 KB (842997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaf7e446c8595c93487f291b6d15871133e1e6fcefce2aefe3fcbc4036a0fe3`

```dockerfile
```

-	Layers:
	-	`sha256:0a8790d3d16ea6ca7a104d4cb35d7ec18c559c4d21a4abffd2afa0661a182657`  
		Last Modified: Fri, 26 Sep 2025 18:10:36 GMT  
		Size: 830.0 KB (830019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f64c2993edbd2be14032ef6099de9cf2e551a94fdc71cbf8ec2cde04eba7de`  
		Last Modified: Fri, 26 Sep 2025 18:10:37 GMT  
		Size: 13.0 KB (12978 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; ppc64le

```console
$ docker pull traefik@sha256:3b6a56a80a117b3dfa022d352dc3c888905fe7bfd0ae0c69be9a30623acde9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43623639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1aed1cb8ce2b6d2b3e4862f5eb931520517d7ceba90e3f910423d8b8b4789a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58bcb245addad2454af60ac0b24db42a4dca59282f25c89cca6310039f371c3`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 450.0 KB (449967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f75617b6b6fddcf21697eb6da6d247d059800dd5b54277dabcf8e2e2b885f8b`  
		Last Modified: Fri, 26 Sep 2025 17:12:12 GMT  
		Size: 39.4 MB (39446191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95745c96cb06592e4b50d162aa45f8c964ba98fb0c2bb453b914135ae311866a`  
		Last Modified: Fri, 26 Sep 2025 17:12:01 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:baa175a1f913789dd1256cac46ce1115d6b1921d282568d07b75ff83bf855289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4335f8a69a6afc59e8a66fd4d915d190306726f7bcb73cf427987dedf2704948`

```dockerfile
```

-	Layers:
	-	`sha256:806fceb59bc0de57f4e0ca03611fda0e3084cab69458dabb3e3e4d2b2ff7966e`  
		Last Modified: Fri, 26 Sep 2025 18:10:41 GMT  
		Size: 828.0 KB (828022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22afb6654566a0426fb39ad7aa0cccc7ae1d6cca761aa7645aaf2af23de6ead2`  
		Last Modified: Fri, 26 Sep 2025 18:10:42 GMT  
		Size: 12.9 KB (12880 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; riscv64

```console
$ docker pull traefik@sha256:282d6ffe6f6188353d96c52e6faa55850a8feb2e8f7603451d00b572718e7736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cea370dff8ca8228781f57198ad70f0c83c8ed8fff3eb5ad83e9b06efded16`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbba8d647e965f0a2de541614e2c016d7555eb619caad10f049006afd8a9565`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 448.1 KB (448053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffca6fe4cedcdd10e9d493cd6ce0c2d8dd658e740e243408c7f3bb132ef602b`  
		Last Modified: Fri, 26 Sep 2025 21:04:32 GMT  
		Size: 43.8 MB (43809612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d64ae3ef30c278c6cac83ef15c76fd1fc8985143bac6f6d6d2d5e8a82bbd97`  
		Last Modified: Fri, 26 Sep 2025 21:04:19 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:edeb0271db66ce1c95836c4608d822e66cb093702b8b0d57525e4b56a33f5561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050e7c4b8517754d5bf1d2a26de851deed96c1590d4bd3c534780ad9463afdf5`

```dockerfile
```

-	Layers:
	-	`sha256:d2ecadeb8fcee681b79af16c74a8e47d3f6620d8eeb37fca82acb5e036e180ea`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79215dbd817ae97669db1d15208b2cbfd6adf1d4771fbd9ccbb7cdd3ae168623`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5.3` - linux; s390x

```console
$ docker pull traefik@sha256:92b02a21fed70b653691ab23fb03409486428393d976c44b9ea01d09eec63f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47748471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d524f91702da90253ed5993c6399503c47e837bd37c7199ac461ed60a8ae03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
RUN apk --no-cache add ca-certificates tzdata # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
RUN set -ex; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) arch='armv6' ;; 		aarch64) arch='arm64' ;; 		x86_64) arch='amd64' ;; 		riscv64) arch='riscv64' ;; 		s390x) arch='s390x' ;; 		ppc64le) arch='ppc64le' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget --quiet -O /tmp/traefik.tar.gz "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_linux_$arch.tar.gz"; 	tar xzvf /tmp/traefik.tar.gz -C /usr/local/bin traefik; 	rm -f /tmp/traefik.tar.gz; 	chmod +x /usr/local/bin/traefik # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
COPY entrypoint.sh / # buildkit
# Fri, 26 Sep 2025 09:31:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 26 Sep 2025 09:31:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Sep 2025 09:31:02 GMT
CMD ["traefik"]
# Fri, 26 Sep 2025 09:31:02 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9196fea837468d80c7511d95936862dd5a96b4f9a701f4cd7f99e2413ae5e9`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 448.6 KB (448598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9db0cfcc3ec24f7475b6a71701a0a7f5c59a80ff0113a3aea98050d8574da41`  
		Last Modified: Fri, 26 Sep 2025 18:09:24 GMT  
		Size: 43.7 MB (43654532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3f27e43aa6358a995a8365aba12cefcfc668f94f9dafb170b37f88e226a402`  
		Last Modified: Fri, 26 Sep 2025 18:09:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5.3` - unknown; unknown

```console
$ docker pull traefik@sha256:6308152adf35691ed3badf62135c3123fb1134bcaae1e22c0695ca3c214fd3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab5365c9e00c43c2e27c5440ef89b0bdecc1fc1e74dbffd49d8913accb4bcab`

```dockerfile
```

-	Layers:
	-	`sha256:894d5b3ecc880c57c507571bd83070eeda1dc08287eb89aeebb3d8984c8f83b5`  
		Last Modified: Fri, 26 Sep 2025 21:09:39 GMT  
		Size: 828.0 KB (827964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df772ec9c0cecb0380487a1aa8bcffae47c137d7abdfec17d2ad4ee2bc10c428`  
		Last Modified: Fri, 26 Sep 2025 21:09:40 GMT  
		Size: 12.8 KB (12811 bytes)  
		MIME: application/vnd.in-toto+json

## `traefik:v3.5.3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:c978598a76ae84edb8234a51b94adb8e48d2e866939db6b798fda70fbe241834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5.3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:0ed5a343ccff58480a0eabdb028dc6171fd65e71b787084afb5055f1e26f91b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168940516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab44b025f4e25b4bc45528b85336f47e2065682135e28e1541becf4fc2b6573`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Fri, 26 Sep 2025 17:09:37 GMT
RUN cmd /S /C #(nop) COPY file:870f18000e0cb042dd2edc76a8f32736793d95f3caf3ce9ad102b5290302133e in \ 
# Fri, 26 Sep 2025 17:09:38 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 17:09:40 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020b3d9e5186e58d6b6b9f80992bfec3380bd94f1a67489f919224438e5e54a`  
		Last Modified: Fri, 26 Sep 2025 17:10:19 GMT  
		Size: 46.2 MB (46217409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4543f95ca8abb90dfeef1ae83568ad3fe92ffc55985271408029c40155cfc43e`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f9160480d9602d2fa2a1a6a532430d811dc892c13eb11b35f261864b35a906`  
		Last Modified: Fri, 26 Sep 2025 17:10:13 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d022905abf031d9d253a719e6549a7ecd31e3f89ecb38ae6278af0cdc66051f0`  
		Last Modified: Fri, 26 Sep 2025 17:10:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5.3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:95d72519d3ef7b290ec4b7127a645665de659594c76c04f272a896088c031a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:b962365847ca610b31c24626e421b5e4f531fe3961c60dee7619c8dfed5850ef
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328894444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6bac80dc186a32b2da81873b24fcdd84a301e652f7592e492ec394f7bfb302`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Fri, 26 Sep 2025 16:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Sep 2025 16:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.3/traefik_v3.5.3_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Fri, 26 Sep 2025 16:58:53 GMT
EXPOSE 80
# Fri, 26 Sep 2025 16:58:53 GMT
ENTRYPOINT ["/traefik"]
# Fri, 26 Sep 2025 16:58:54 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.3 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4911f617d75faadd95ab1f0536dc26b997c765df15edbe26d10d493c04a7150a`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1d1e268ecb5aa9a3fe3a0bf49d64dea19c276ee8fd3e8d62b62bf7a8a6910d`  
		Last Modified: Fri, 26 Sep 2025 17:05:07 GMT  
		Size: 46.7 MB (46744220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ba0ce27d967c07a4661479b024fdb2ebb4ecc9871514d9c035fbde36c74cd5`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25490da9a28603d0db0c2f84fd9f3e9da2f56a9c32167905691d65ebd026fd97`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc964859f5f84bea2a41f757d6c8e84a001168c88209951e8db9a1d787e7c6d`  
		Last Modified: Fri, 26 Sep 2025 17:04:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
