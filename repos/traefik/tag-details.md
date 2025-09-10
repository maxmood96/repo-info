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
-	[`traefik:3.5.2`](#traefik352)
-	[`traefik:3.5.2-nanoserver-ltsc2022`](#traefik352-nanoserver-ltsc2022)
-	[`traefik:3.5.2-windowsservercore-ltsc2022`](#traefik352-windowsservercore-ltsc2022)
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
-	[`traefik:v3.5.2`](#traefikv352)
-	[`traefik:v3.5.2-nanoserver-ltsc2022`](#traefikv352-nanoserver-ltsc2022)
-	[`traefik:v3.5.2-windowsservercore-ltsc2022`](#traefikv352-windowsservercore-ltsc2022)
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
$ docker pull traefik@sha256:602b5fdf0ad07e6ca79609b3161e0da52da2c9d70840961d861b4687f5704c7c
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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; arm variant v6

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; arm64 variant v8

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; ppc64le

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

### `traefik:3` - unknown; unknown

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

### `traefik:3` - linux; riscv64

```console
$ docker pull traefik@sha256:c49383d6ad04b7a66f5ba071e84bb0ad8a9ec7f1c26f4a14d66ceaf196cf9cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7d1e93263542cccddc143c9b0d8d43c311294f2db1d0fb95e513b3780ead2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0ec1181f9802118503bf981688621372ccf81caa3134a66bdca7a12993e34`  
		Last Modified: Fri, 29 Aug 2025 13:22:10 GMT  
		Size: 43.8 MB (43802868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11afcaf15c102eec7f826b381b3f7d5703c63b6152de3c290fca9b345029089d`  
		Last Modified: Fri, 29 Aug 2025 13:22:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3` - unknown; unknown

```console
$ docker pull traefik@sha256:666906c10ce558cc64d2aa366edb7225c40849d402a0bbf5120101fd5f1d2a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bf17eb98701facdd5d33297f8e535c547da11bed0259b7886ebaac42e8c8c5`

```dockerfile
```

-	Layers:
	-	`sha256:f2c263176a4e5583addd0c78c43ed0369196439af51e2085f111417c129d120b`  
		Last Modified: Fri, 29 Aug 2025 15:09:43 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f146905d2669c5232f5ed1cd13ce7736bc3afcbf8601cf237ea95bd3a26a19a`  
		Last Modified: Fri, 29 Aug 2025 15:09:44 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3` - linux; s390x

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

### `traefik:3` - unknown; unknown

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

## `traefik:3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:f4e29bae91c879df00f44f64bd652ed7aa827f8e322de5306505009b26d8deef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ab24021a40f9d12a65794f3619caf893887188bc1abb1d59f9c593f3a8b3f821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d5061ec0b85a9b694ee04035dd009a772d9c44cdffae6852e2275dad8105`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 21:09:02 GMT
RUN cmd /S /C #(nop) COPY file:913e30e4d701328984dc67a125f933212d7d01eded1d08d3e810d11487b3ee0c in \ 
# Tue, 09 Sep 2025 21:09:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Sep 2025 21:09:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 21:09:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a863bb17d9e5eb5a69daf12b890a3246e5ef4eeddd4bd559e66205c1d31df57`  
		Last Modified: Tue, 09 Sep 2025 21:10:07 GMT  
		Size: 46.2 MB (46223958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cee29116a9a489b91c794dbc7705d0b26bd412cc154cb444bc306a883af1593`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d88fa9e154a0d7f8835da8c9b6069af8b09cc87dd16f596acbc757905234a9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e13dbeea4f12d02f4e2152c21432f0572448962d4ea3c9c4af47176552ca`  
		Last Modified: Tue, 09 Sep 2025 21:10:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:82a0a74cae8badddafad2dca08719b74f56c7fa53173afc9fdfb7123c3ee9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ba33f93dc5681d1e6ce6c9838d6c9e39ca82dd9c4ee5b726c15185cec1e6cb90
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328426881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3ab5714757e60c81184ec9b53090955e55759a65b1d1ac9b5d7b61f78b4b3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 20:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Sep 2025 20:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Sep 2025 20:20:04 GMT
EXPOSE 80
# Tue, 09 Sep 2025 20:20:05 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 20:20:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1e1e87a93025ab69bf4dc54b07e668c447fad4d3c3141aef0545a569ba3456a6`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bfddba5e8066be9a4ebbe3e54015a265012c6612f7889c2ff628da4c87d26`  
		Last Modified: Tue, 09 Sep 2025 20:20:44 GMT  
		Size: 46.7 MB (46729786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c38ee8c9423066a00f9c1c3d818582b11891e500ed1e0c6357e01680ea8a7`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2351f94d8a21292955aade3bb47e6291978e347a8a04a128aee55173c051afe`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312b89a4a5a2da2a9967b7732c3b08aea8e0e68f7e699bac6db2c308ad60d7b`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5`

```console
$ docker pull traefik@sha256:602b5fdf0ad07e6ca79609b3161e0da52da2c9d70840961d861b4687f5704c7c
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

### `traefik:3.5` - unknown; unknown

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

### `traefik:3.5` - linux; arm variant v6

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

### `traefik:3.5` - unknown; unknown

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

### `traefik:3.5` - linux; arm64 variant v8

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

### `traefik:3.5` - unknown; unknown

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

### `traefik:3.5` - linux; ppc64le

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

### `traefik:3.5` - unknown; unknown

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

### `traefik:3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:c49383d6ad04b7a66f5ba071e84bb0ad8a9ec7f1c26f4a14d66ceaf196cf9cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7d1e93263542cccddc143c9b0d8d43c311294f2db1d0fb95e513b3780ead2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0ec1181f9802118503bf981688621372ccf81caa3134a66bdca7a12993e34`  
		Last Modified: Fri, 29 Aug 2025 13:22:10 GMT  
		Size: 43.8 MB (43802868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11afcaf15c102eec7f826b381b3f7d5703c63b6152de3c290fca9b345029089d`  
		Last Modified: Fri, 29 Aug 2025 13:22:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:666906c10ce558cc64d2aa366edb7225c40849d402a0bbf5120101fd5f1d2a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bf17eb98701facdd5d33297f8e535c547da11bed0259b7886ebaac42e8c8c5`

```dockerfile
```

-	Layers:
	-	`sha256:f2c263176a4e5583addd0c78c43ed0369196439af51e2085f111417c129d120b`  
		Last Modified: Fri, 29 Aug 2025 15:09:43 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f146905d2669c5232f5ed1cd13ce7736bc3afcbf8601cf237ea95bd3a26a19a`  
		Last Modified: Fri, 29 Aug 2025 15:09:44 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:3.5` - linux; s390x

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

### `traefik:3.5` - unknown; unknown

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

## `traefik:3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:f4e29bae91c879df00f44f64bd652ed7aa827f8e322de5306505009b26d8deef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ab24021a40f9d12a65794f3619caf893887188bc1abb1d59f9c593f3a8b3f821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d5061ec0b85a9b694ee04035dd009a772d9c44cdffae6852e2275dad8105`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 21:09:02 GMT
RUN cmd /S /C #(nop) COPY file:913e30e4d701328984dc67a125f933212d7d01eded1d08d3e810d11487b3ee0c in \ 
# Tue, 09 Sep 2025 21:09:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Sep 2025 21:09:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 21:09:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a863bb17d9e5eb5a69daf12b890a3246e5ef4eeddd4bd559e66205c1d31df57`  
		Last Modified: Tue, 09 Sep 2025 21:10:07 GMT  
		Size: 46.2 MB (46223958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cee29116a9a489b91c794dbc7705d0b26bd412cc154cb444bc306a883af1593`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d88fa9e154a0d7f8835da8c9b6069af8b09cc87dd16f596acbc757905234a9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e13dbeea4f12d02f4e2152c21432f0572448962d4ea3c9c4af47176552ca`  
		Last Modified: Tue, 09 Sep 2025 21:10:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:82a0a74cae8badddafad2dca08719b74f56c7fa53173afc9fdfb7123c3ee9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ba33f93dc5681d1e6ce6c9838d6c9e39ca82dd9c4ee5b726c15185cec1e6cb90
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328426881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3ab5714757e60c81184ec9b53090955e55759a65b1d1ac9b5d7b61f78b4b3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 20:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Sep 2025 20:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Sep 2025 20:20:04 GMT
EXPOSE 80
# Tue, 09 Sep 2025 20:20:05 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 20:20:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1e1e87a93025ab69bf4dc54b07e668c447fad4d3c3141aef0545a569ba3456a6`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bfddba5e8066be9a4ebbe3e54015a265012c6612f7889c2ff628da4c87d26`  
		Last Modified: Tue, 09 Sep 2025 20:20:44 GMT  
		Size: 46.7 MB (46729786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c38ee8c9423066a00f9c1c3d818582b11891e500ed1e0c6357e01680ea8a7`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2351f94d8a21292955aade3bb47e6291978e347a8a04a128aee55173c051afe`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312b89a4a5a2da2a9967b7732c3b08aea8e0e68f7e699bac6db2c308ad60d7b`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.2`

```console
$ docker pull traefik@sha256:07ff0c6c2114233b82e1de8e9f4fee9974470cd8d42c22e4e158538d950e19ae
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

### `traefik:3.5.2` - linux; amd64

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

### `traefik:3.5.2` - unknown; unknown

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

### `traefik:3.5.2` - linux; arm variant v6

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

### `traefik:3.5.2` - unknown; unknown

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

### `traefik:3.5.2` - linux; arm64 variant v8

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

### `traefik:3.5.2` - unknown; unknown

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

### `traefik:3.5.2` - linux; ppc64le

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

### `traefik:3.5.2` - unknown; unknown

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

### `traefik:3.5.2` - linux; s390x

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

### `traefik:3.5.2` - unknown; unknown

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

## `traefik:3.5.2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:f4e29bae91c879df00f44f64bd652ed7aa827f8e322de5306505009b26d8deef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5.2-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ab24021a40f9d12a65794f3619caf893887188bc1abb1d59f9c593f3a8b3f821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d5061ec0b85a9b694ee04035dd009a772d9c44cdffae6852e2275dad8105`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 21:09:02 GMT
RUN cmd /S /C #(nop) COPY file:913e30e4d701328984dc67a125f933212d7d01eded1d08d3e810d11487b3ee0c in \ 
# Tue, 09 Sep 2025 21:09:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Sep 2025 21:09:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 21:09:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a863bb17d9e5eb5a69daf12b890a3246e5ef4eeddd4bd559e66205c1d31df57`  
		Last Modified: Tue, 09 Sep 2025 21:10:07 GMT  
		Size: 46.2 MB (46223958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cee29116a9a489b91c794dbc7705d0b26bd412cc154cb444bc306a883af1593`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d88fa9e154a0d7f8835da8c9b6069af8b09cc87dd16f596acbc757905234a9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e13dbeea4f12d02f4e2152c21432f0572448962d4ea3c9c4af47176552ca`  
		Last Modified: Tue, 09 Sep 2025 21:10:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:82a0a74cae8badddafad2dca08719b74f56c7fa53173afc9fdfb7123c3ee9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:3.5.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ba33f93dc5681d1e6ce6c9838d6c9e39ca82dd9c4ee5b726c15185cec1e6cb90
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328426881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3ab5714757e60c81184ec9b53090955e55759a65b1d1ac9b5d7b61f78b4b3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 20:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Sep 2025 20:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Sep 2025 20:20:04 GMT
EXPOSE 80
# Tue, 09 Sep 2025 20:20:05 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 20:20:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1e1e87a93025ab69bf4dc54b07e668c447fad4d3c3141aef0545a569ba3456a6`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bfddba5e8066be9a4ebbe3e54015a265012c6612f7889c2ff628da4c87d26`  
		Last Modified: Tue, 09 Sep 2025 20:20:44 GMT  
		Size: 46.7 MB (46729786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c38ee8c9423066a00f9c1c3d818582b11891e500ed1e0c6357e01680ea8a7`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2351f94d8a21292955aade3bb47e6291978e347a8a04a128aee55173c051afe`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312b89a4a5a2da2a9967b7732c3b08aea8e0e68f7e699bac6db2c308ad60d7b`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou`

```console
$ docker pull traefik@sha256:602b5fdf0ad07e6ca79609b3161e0da52da2c9d70840961d861b4687f5704c7c
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

### `traefik:chabichou` - unknown; unknown

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

### `traefik:chabichou` - linux; arm variant v6

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

### `traefik:chabichou` - unknown; unknown

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

### `traefik:chabichou` - linux; arm64 variant v8

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

### `traefik:chabichou` - unknown; unknown

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

### `traefik:chabichou` - linux; ppc64le

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

### `traefik:chabichou` - unknown; unknown

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

### `traefik:chabichou` - linux; riscv64

```console
$ docker pull traefik@sha256:c49383d6ad04b7a66f5ba071e84bb0ad8a9ec7f1c26f4a14d66ceaf196cf9cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7d1e93263542cccddc143c9b0d8d43c311294f2db1d0fb95e513b3780ead2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0ec1181f9802118503bf981688621372ccf81caa3134a66bdca7a12993e34`  
		Last Modified: Fri, 29 Aug 2025 13:22:10 GMT  
		Size: 43.8 MB (43802868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11afcaf15c102eec7f826b381b3f7d5703c63b6152de3c290fca9b345029089d`  
		Last Modified: Fri, 29 Aug 2025 13:22:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:chabichou` - unknown; unknown

```console
$ docker pull traefik@sha256:666906c10ce558cc64d2aa366edb7225c40849d402a0bbf5120101fd5f1d2a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bf17eb98701facdd5d33297f8e535c547da11bed0259b7886ebaac42e8c8c5`

```dockerfile
```

-	Layers:
	-	`sha256:f2c263176a4e5583addd0c78c43ed0369196439af51e2085f111417c129d120b`  
		Last Modified: Fri, 29 Aug 2025 15:09:43 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f146905d2669c5232f5ed1cd13ce7736bc3afcbf8601cf237ea95bd3a26a19a`  
		Last Modified: Fri, 29 Aug 2025 15:09:44 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:chabichou` - linux; s390x

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

### `traefik:chabichou` - unknown; unknown

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

## `traefik:chabichou-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:f4e29bae91c879df00f44f64bd652ed7aa827f8e322de5306505009b26d8deef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:chabichou-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ab24021a40f9d12a65794f3619caf893887188bc1abb1d59f9c593f3a8b3f821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d5061ec0b85a9b694ee04035dd009a772d9c44cdffae6852e2275dad8105`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 21:09:02 GMT
RUN cmd /S /C #(nop) COPY file:913e30e4d701328984dc67a125f933212d7d01eded1d08d3e810d11487b3ee0c in \ 
# Tue, 09 Sep 2025 21:09:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Sep 2025 21:09:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 21:09:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a863bb17d9e5eb5a69daf12b890a3246e5ef4eeddd4bd559e66205c1d31df57`  
		Last Modified: Tue, 09 Sep 2025 21:10:07 GMT  
		Size: 46.2 MB (46223958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cee29116a9a489b91c794dbc7705d0b26bd412cc154cb444bc306a883af1593`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d88fa9e154a0d7f8835da8c9b6069af8b09cc87dd16f596acbc757905234a9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e13dbeea4f12d02f4e2152c21432f0572448962d4ea3c9c4af47176552ca`  
		Last Modified: Tue, 09 Sep 2025 21:10:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:82a0a74cae8badddafad2dca08719b74f56c7fa53173afc9fdfb7123c3ee9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:chabichou-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ba33f93dc5681d1e6ce6c9838d6c9e39ca82dd9c4ee5b726c15185cec1e6cb90
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328426881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3ab5714757e60c81184ec9b53090955e55759a65b1d1ac9b5d7b61f78b4b3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 20:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Sep 2025 20:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Sep 2025 20:20:04 GMT
EXPOSE 80
# Tue, 09 Sep 2025 20:20:05 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 20:20:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1e1e87a93025ab69bf4dc54b07e668c447fad4d3c3141aef0545a569ba3456a6`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bfddba5e8066be9a4ebbe3e54015a265012c6612f7889c2ff628da4c87d26`  
		Last Modified: Tue, 09 Sep 2025 20:20:44 GMT  
		Size: 46.7 MB (46729786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c38ee8c9423066a00f9c1c3d818582b11891e500ed1e0c6357e01680ea8a7`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2351f94d8a21292955aade3bb47e6291978e347a8a04a128aee55173c051afe`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312b89a4a5a2da2a9967b7732c3b08aea8e0e68f7e699bac6db2c308ad60d7b`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:latest`

```console
$ docker pull traefik@sha256:602b5fdf0ad07e6ca79609b3161e0da52da2c9d70840961d861b4687f5704c7c
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
$ docker pull traefik@sha256:c49383d6ad04b7a66f5ba071e84bb0ad8a9ec7f1c26f4a14d66ceaf196cf9cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7d1e93263542cccddc143c9b0d8d43c311294f2db1d0fb95e513b3780ead2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0ec1181f9802118503bf981688621372ccf81caa3134a66bdca7a12993e34`  
		Last Modified: Fri, 29 Aug 2025 13:22:10 GMT  
		Size: 43.8 MB (43802868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11afcaf15c102eec7f826b381b3f7d5703c63b6152de3c290fca9b345029089d`  
		Last Modified: Fri, 29 Aug 2025 13:22:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:latest` - unknown; unknown

```console
$ docker pull traefik@sha256:666906c10ce558cc64d2aa366edb7225c40849d402a0bbf5120101fd5f1d2a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bf17eb98701facdd5d33297f8e535c547da11bed0259b7886ebaac42e8c8c5`

```dockerfile
```

-	Layers:
	-	`sha256:f2c263176a4e5583addd0c78c43ed0369196439af51e2085f111417c129d120b`  
		Last Modified: Fri, 29 Aug 2025 15:09:43 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f146905d2669c5232f5ed1cd13ce7736bc3afcbf8601cf237ea95bd3a26a19a`  
		Last Modified: Fri, 29 Aug 2025 15:09:44 GMT  
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
$ docker pull traefik@sha256:f4e29bae91c879df00f44f64bd652ed7aa827f8e322de5306505009b26d8deef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ab24021a40f9d12a65794f3619caf893887188bc1abb1d59f9c593f3a8b3f821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d5061ec0b85a9b694ee04035dd009a772d9c44cdffae6852e2275dad8105`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 21:09:02 GMT
RUN cmd /S /C #(nop) COPY file:913e30e4d701328984dc67a125f933212d7d01eded1d08d3e810d11487b3ee0c in \ 
# Tue, 09 Sep 2025 21:09:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Sep 2025 21:09:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 21:09:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a863bb17d9e5eb5a69daf12b890a3246e5ef4eeddd4bd559e66205c1d31df57`  
		Last Modified: Tue, 09 Sep 2025 21:10:07 GMT  
		Size: 46.2 MB (46223958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cee29116a9a489b91c794dbc7705d0b26bd412cc154cb444bc306a883af1593`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d88fa9e154a0d7f8835da8c9b6069af8b09cc87dd16f596acbc757905234a9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e13dbeea4f12d02f4e2152c21432f0572448962d4ea3c9c4af47176552ca`  
		Last Modified: Tue, 09 Sep 2025 21:10:03 GMT  
		Size: 1.0 KB (1025 bytes)  
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
$ docker pull traefik@sha256:602b5fdf0ad07e6ca79609b3161e0da52da2c9d70840961d861b4687f5704c7c
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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; arm variant v6

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; arm64 variant v8

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; ppc64le

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

### `traefik:v3` - unknown; unknown

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

### `traefik:v3` - linux; riscv64

```console
$ docker pull traefik@sha256:c49383d6ad04b7a66f5ba071e84bb0ad8a9ec7f1c26f4a14d66ceaf196cf9cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7d1e93263542cccddc143c9b0d8d43c311294f2db1d0fb95e513b3780ead2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0ec1181f9802118503bf981688621372ccf81caa3134a66bdca7a12993e34`  
		Last Modified: Fri, 29 Aug 2025 13:22:10 GMT  
		Size: 43.8 MB (43802868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11afcaf15c102eec7f826b381b3f7d5703c63b6152de3c290fca9b345029089d`  
		Last Modified: Fri, 29 Aug 2025 13:22:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3` - unknown; unknown

```console
$ docker pull traefik@sha256:666906c10ce558cc64d2aa366edb7225c40849d402a0bbf5120101fd5f1d2a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bf17eb98701facdd5d33297f8e535c547da11bed0259b7886ebaac42e8c8c5`

```dockerfile
```

-	Layers:
	-	`sha256:f2c263176a4e5583addd0c78c43ed0369196439af51e2085f111417c129d120b`  
		Last Modified: Fri, 29 Aug 2025 15:09:43 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f146905d2669c5232f5ed1cd13ce7736bc3afcbf8601cf237ea95bd3a26a19a`  
		Last Modified: Fri, 29 Aug 2025 15:09:44 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3` - linux; s390x

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

### `traefik:v3` - unknown; unknown

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

## `traefik:v3-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:f4e29bae91c879df00f44f64bd652ed7aa827f8e322de5306505009b26d8deef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ab24021a40f9d12a65794f3619caf893887188bc1abb1d59f9c593f3a8b3f821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d5061ec0b85a9b694ee04035dd009a772d9c44cdffae6852e2275dad8105`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 21:09:02 GMT
RUN cmd /S /C #(nop) COPY file:913e30e4d701328984dc67a125f933212d7d01eded1d08d3e810d11487b3ee0c in \ 
# Tue, 09 Sep 2025 21:09:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Sep 2025 21:09:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 21:09:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a863bb17d9e5eb5a69daf12b890a3246e5ef4eeddd4bd559e66205c1d31df57`  
		Last Modified: Tue, 09 Sep 2025 21:10:07 GMT  
		Size: 46.2 MB (46223958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cee29116a9a489b91c794dbc7705d0b26bd412cc154cb444bc306a883af1593`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d88fa9e154a0d7f8835da8c9b6069af8b09cc87dd16f596acbc757905234a9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e13dbeea4f12d02f4e2152c21432f0572448962d4ea3c9c4af47176552ca`  
		Last Modified: Tue, 09 Sep 2025 21:10:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:82a0a74cae8badddafad2dca08719b74f56c7fa53173afc9fdfb7123c3ee9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ba33f93dc5681d1e6ce6c9838d6c9e39ca82dd9c4ee5b726c15185cec1e6cb90
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328426881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3ab5714757e60c81184ec9b53090955e55759a65b1d1ac9b5d7b61f78b4b3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 20:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Sep 2025 20:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Sep 2025 20:20:04 GMT
EXPOSE 80
# Tue, 09 Sep 2025 20:20:05 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 20:20:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1e1e87a93025ab69bf4dc54b07e668c447fad4d3c3141aef0545a569ba3456a6`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bfddba5e8066be9a4ebbe3e54015a265012c6612f7889c2ff628da4c87d26`  
		Last Modified: Tue, 09 Sep 2025 20:20:44 GMT  
		Size: 46.7 MB (46729786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c38ee8c9423066a00f9c1c3d818582b11891e500ed1e0c6357e01680ea8a7`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2351f94d8a21292955aade3bb47e6291978e347a8a04a128aee55173c051afe`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312b89a4a5a2da2a9967b7732c3b08aea8e0e68f7e699bac6db2c308ad60d7b`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5`

```console
$ docker pull traefik@sha256:602b5fdf0ad07e6ca79609b3161e0da52da2c9d70840961d861b4687f5704c7c
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

### `traefik:v3.5` - unknown; unknown

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

### `traefik:v3.5` - linux; arm variant v6

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

### `traefik:v3.5` - unknown; unknown

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

### `traefik:v3.5` - linux; arm64 variant v8

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

### `traefik:v3.5` - unknown; unknown

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

### `traefik:v3.5` - linux; ppc64le

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

### `traefik:v3.5` - unknown; unknown

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

### `traefik:v3.5` - linux; riscv64

```console
$ docker pull traefik@sha256:c49383d6ad04b7a66f5ba071e84bb0ad8a9ec7f1c26f4a14d66ceaf196cf9cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7d1e93263542cccddc143c9b0d8d43c311294f2db1d0fb95e513b3780ead2e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["traefik"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
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
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f6bf282af6a9a44d8093033d94b5222a383d5f2144ac5c2d74fe1ee6d4aecb`  
		Last Modified: Fri, 29 Aug 2025 13:22:06 GMT  
		Size: 448.1 KB (448056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0ec1181f9802118503bf981688621372ccf81caa3134a66bdca7a12993e34`  
		Last Modified: Fri, 29 Aug 2025 13:22:10 GMT  
		Size: 43.8 MB (43802868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11afcaf15c102eec7f826b381b3f7d5703c63b6152de3c290fca9b345029089d`  
		Last Modified: Fri, 29 Aug 2025 13:22:07 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `traefik:v3.5` - unknown; unknown

```console
$ docker pull traefik@sha256:666906c10ce558cc64d2aa366edb7225c40849d402a0bbf5120101fd5f1d2a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.9 KB (840899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bf17eb98701facdd5d33297f8e535c547da11bed0259b7886ebaac42e8c8c5`

```dockerfile
```

-	Layers:
	-	`sha256:f2c263176a4e5583addd0c78c43ed0369196439af51e2085f111417c129d120b`  
		Last Modified: Fri, 29 Aug 2025 15:09:43 GMT  
		Size: 828.0 KB (828018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f146905d2669c5232f5ed1cd13ce7736bc3afcbf8601cf237ea95bd3a26a19a`  
		Last Modified: Fri, 29 Aug 2025 15:09:44 GMT  
		Size: 12.9 KB (12881 bytes)  
		MIME: application/vnd.in-toto+json

### `traefik:v3.5` - linux; s390x

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

### `traefik:v3.5` - unknown; unknown

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

## `traefik:v3.5-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:f4e29bae91c879df00f44f64bd652ed7aa827f8e322de5306505009b26d8deef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ab24021a40f9d12a65794f3619caf893887188bc1abb1d59f9c593f3a8b3f821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d5061ec0b85a9b694ee04035dd009a772d9c44cdffae6852e2275dad8105`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 21:09:02 GMT
RUN cmd /S /C #(nop) COPY file:913e30e4d701328984dc67a125f933212d7d01eded1d08d3e810d11487b3ee0c in \ 
# Tue, 09 Sep 2025 21:09:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Sep 2025 21:09:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 21:09:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a863bb17d9e5eb5a69daf12b890a3246e5ef4eeddd4bd559e66205c1d31df57`  
		Last Modified: Tue, 09 Sep 2025 21:10:07 GMT  
		Size: 46.2 MB (46223958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cee29116a9a489b91c794dbc7705d0b26bd412cc154cb444bc306a883af1593`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d88fa9e154a0d7f8835da8c9b6069af8b09cc87dd16f596acbc757905234a9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e13dbeea4f12d02f4e2152c21432f0572448962d4ea3c9c4af47176552ca`  
		Last Modified: Tue, 09 Sep 2025 21:10:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:82a0a74cae8badddafad2dca08719b74f56c7fa53173afc9fdfb7123c3ee9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ba33f93dc5681d1e6ce6c9838d6c9e39ca82dd9c4ee5b726c15185cec1e6cb90
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328426881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3ab5714757e60c81184ec9b53090955e55759a65b1d1ac9b5d7b61f78b4b3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 20:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Sep 2025 20:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Sep 2025 20:20:04 GMT
EXPOSE 80
# Tue, 09 Sep 2025 20:20:05 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 20:20:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1e1e87a93025ab69bf4dc54b07e668c447fad4d3c3141aef0545a569ba3456a6`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bfddba5e8066be9a4ebbe3e54015a265012c6612f7889c2ff628da4c87d26`  
		Last Modified: Tue, 09 Sep 2025 20:20:44 GMT  
		Size: 46.7 MB (46729786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c38ee8c9423066a00f9c1c3d818582b11891e500ed1e0c6357e01680ea8a7`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2351f94d8a21292955aade3bb47e6291978e347a8a04a128aee55173c051afe`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312b89a4a5a2da2a9967b7732c3b08aea8e0e68f7e699bac6db2c308ad60d7b`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.2`

```console
$ docker pull traefik@sha256:07ff0c6c2114233b82e1de8e9f4fee9974470cd8d42c22e4e158538d950e19ae
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

### `traefik:v3.5.2` - linux; amd64

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

### `traefik:v3.5.2` - unknown; unknown

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

### `traefik:v3.5.2` - linux; arm variant v6

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

### `traefik:v3.5.2` - unknown; unknown

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

### `traefik:v3.5.2` - linux; arm64 variant v8

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

### `traefik:v3.5.2` - unknown; unknown

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

### `traefik:v3.5.2` - linux; ppc64le

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

### `traefik:v3.5.2` - unknown; unknown

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

### `traefik:v3.5.2` - linux; s390x

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

### `traefik:v3.5.2` - unknown; unknown

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

## `traefik:v3.5.2-nanoserver-ltsc2022`

```console
$ docker pull traefik@sha256:f4e29bae91c879df00f44f64bd652ed7aa827f8e322de5306505009b26d8deef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5.2-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ab24021a40f9d12a65794f3619caf893887188bc1abb1d59f9c593f3a8b3f821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168887354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a6d5061ec0b85a9b694ee04035dd009a772d9c44cdffae6852e2275dad8105`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 09 Sep 2025 21:09:02 GMT
RUN cmd /S /C #(nop) COPY file:913e30e4d701328984dc67a125f933212d7d01eded1d08d3e810d11487b3ee0c in \ 
# Tue, 09 Sep 2025 21:09:05 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Tue, 09 Sep 2025 21:09:06 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 21:09:07 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a863bb17d9e5eb5a69daf12b890a3246e5ef4eeddd4bd559e66205c1d31df57`  
		Last Modified: Tue, 09 Sep 2025 21:10:07 GMT  
		Size: 46.2 MB (46223958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cee29116a9a489b91c794dbc7705d0b26bd412cc154cb444bc306a883af1593`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d88fa9e154a0d7f8835da8c9b6069af8b09cc87dd16f596acbc757905234a9`  
		Last Modified: Tue, 09 Sep 2025 21:10:02 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19e13dbeea4f12d02f4e2152c21432f0572448962d4ea3c9c4af47176552ca`  
		Last Modified: Tue, 09 Sep 2025 21:10:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:82a0a74cae8badddafad2dca08719b74f56c7fa53173afc9fdfb7123c3ee9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:v3.5.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ba33f93dc5681d1e6ce6c9838d6c9e39ca82dd9c4ee5b726c15185cec1e6cb90
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328426881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3ab5714757e60c81184ec9b53090955e55759a65b1d1ac9b5d7b61f78b4b3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 20:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Sep 2025 20:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Sep 2025 20:20:04 GMT
EXPOSE 80
# Tue, 09 Sep 2025 20:20:05 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 20:20:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1e1e87a93025ab69bf4dc54b07e668c447fad4d3c3141aef0545a569ba3456a6`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bfddba5e8066be9a4ebbe3e54015a265012c6612f7889c2ff628da4c87d26`  
		Last Modified: Tue, 09 Sep 2025 20:20:44 GMT  
		Size: 46.7 MB (46729786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c38ee8c9423066a00f9c1c3d818582b11891e500ed1e0c6357e01680ea8a7`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2351f94d8a21292955aade3bb47e6291978e347a8a04a128aee55173c051afe`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312b89a4a5a2da2a9967b7732c3b08aea8e0e68f7e699bac6db2c308ad60d7b`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:82a0a74cae8badddafad2dca08719b74f56c7fa53173afc9fdfb7123c3ee9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull traefik@sha256:ba33f93dc5681d1e6ce6c9838d6c9e39ca82dd9c4ee5b726c15185cec1e6cb90
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328426881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3ab5714757e60c81184ec9b53090955e55759a65b1d1ac9b5d7b61f78b4b3f`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 09 Sep 2025 20:19:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Sep 2025 20:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Tue, 09 Sep 2025 20:20:04 GMT
EXPOSE 80
# Tue, 09 Sep 2025 20:20:05 GMT
ENTRYPOINT ["/traefik"]
# Tue, 09 Sep 2025 20:20:06 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:1e1e87a93025ab69bf4dc54b07e668c447fad4d3c3141aef0545a569ba3456a6`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99bfddba5e8066be9a4ebbe3e54015a265012c6612f7889c2ff628da4c87d26`  
		Last Modified: Tue, 09 Sep 2025 20:20:44 GMT  
		Size: 46.7 MB (46729786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506c38ee8c9423066a00f9c1c3d818582b11891e500ed1e0c6357e01680ea8a7`  
		Last Modified: Tue, 09 Sep 2025 20:20:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2351f94d8a21292955aade3bb47e6291978e347a8a04a128aee55173c051afe`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312b89a4a5a2da2a9967b7732c3b08aea8e0e68f7e699bac6db2c308ad60d7b`  
		Last Modified: Tue, 09 Sep 2025 20:20:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
