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
$ docker pull traefik@sha256:8f98e904fab25aaa7cf5eb799658a0690aa6bf91e8d74cc3606527d1759eb533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:c850b679fb6311bda48e180537f04253cebc03ea6a7cab16141ba23b88b57499
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeac49ee6cd5c95bb1031fbc32b16d5df85c2841d00bcd91eac11b11ee48505`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:59 GMT
RUN cmd /S /C #(nop) COPY file:1368d6dce4ed982bfb8547b878cef8f8a5a2024c1be0b673ddbcd16aece97a5a in \ 
# Wed, 10 Sep 2025 22:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eae38821db13b372f7380c1e127dce59a3e4c30f1e740528b982e2c44025da`  
		Last Modified: Wed, 10 Sep 2025 22:19:04 GMT  
		Size: 46.2 MB (46224039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0461a5885755c025287834dfc263013831e8364f26b89049c064779b3c9`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6275934b92819657fd592f82e616af98f3cf7a6338ddf9a9e12e380d2902d`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d7f51f66b9ed4593cf0f78469461dc279be99d23f7222b50e604f86a75b05`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5`

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

### `traefik:3.5` - unknown; unknown

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
$ docker pull traefik@sha256:8f98e904fab25aaa7cf5eb799658a0690aa6bf91e8d74cc3606527d1759eb533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:c850b679fb6311bda48e180537f04253cebc03ea6a7cab16141ba23b88b57499
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeac49ee6cd5c95bb1031fbc32b16d5df85c2841d00bcd91eac11b11ee48505`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:59 GMT
RUN cmd /S /C #(nop) COPY file:1368d6dce4ed982bfb8547b878cef8f8a5a2024c1be0b673ddbcd16aece97a5a in \ 
# Wed, 10 Sep 2025 22:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eae38821db13b372f7380c1e127dce59a3e4c30f1e740528b982e2c44025da`  
		Last Modified: Wed, 10 Sep 2025 22:19:04 GMT  
		Size: 46.2 MB (46224039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0461a5885755c025287834dfc263013831e8364f26b89049c064779b3c9`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6275934b92819657fd592f82e616af98f3cf7a6338ddf9a9e12e380d2902d`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d7f51f66b9ed4593cf0f78469461dc279be99d23f7222b50e604f86a75b05`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.2`

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

### `traefik:3.5.2` - linux; riscv64

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

### `traefik:3.5.2` - unknown; unknown

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
$ docker pull traefik@sha256:8f98e904fab25aaa7cf5eb799658a0690aa6bf91e8d74cc3606527d1759eb533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5.2-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:c850b679fb6311bda48e180537f04253cebc03ea6a7cab16141ba23b88b57499
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeac49ee6cd5c95bb1031fbc32b16d5df85c2841d00bcd91eac11b11ee48505`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:59 GMT
RUN cmd /S /C #(nop) COPY file:1368d6dce4ed982bfb8547b878cef8f8a5a2024c1be0b673ddbcd16aece97a5a in \ 
# Wed, 10 Sep 2025 22:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eae38821db13b372f7380c1e127dce59a3e4c30f1e740528b982e2c44025da`  
		Last Modified: Wed, 10 Sep 2025 22:19:04 GMT  
		Size: 46.2 MB (46224039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0461a5885755c025287834dfc263013831e8364f26b89049c064779b3c9`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6275934b92819657fd592f82e616af98f3cf7a6338ddf9a9e12e380d2902d`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d7f51f66b9ed4593cf0f78469461dc279be99d23f7222b50e604f86a75b05`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:3.5.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:3.5.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou`

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

### `traefik:chabichou` - unknown; unknown

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
$ docker pull traefik@sha256:8f98e904fab25aaa7cf5eb799658a0690aa6bf91e8d74cc3606527d1759eb533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:chabichou-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:c850b679fb6311bda48e180537f04253cebc03ea6a7cab16141ba23b88b57499
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeac49ee6cd5c95bb1031fbc32b16d5df85c2841d00bcd91eac11b11ee48505`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:59 GMT
RUN cmd /S /C #(nop) COPY file:1368d6dce4ed982bfb8547b878cef8f8a5a2024c1be0b673ddbcd16aece97a5a in \ 
# Wed, 10 Sep 2025 22:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eae38821db13b372f7380c1e127dce59a3e4c30f1e740528b982e2c44025da`  
		Last Modified: Wed, 10 Sep 2025 22:19:04 GMT  
		Size: 46.2 MB (46224039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0461a5885755c025287834dfc263013831e8364f26b89049c064779b3c9`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6275934b92819657fd592f82e616af98f3cf7a6338ddf9a9e12e380d2902d`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d7f51f66b9ed4593cf0f78469461dc279be99d23f7222b50e604f86a75b05`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:chabichou-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:chabichou-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
$ docker pull traefik@sha256:8f98e904fab25aaa7cf5eb799658a0690aa6bf91e8d74cc3606527d1759eb533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:c850b679fb6311bda48e180537f04253cebc03ea6a7cab16141ba23b88b57499
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeac49ee6cd5c95bb1031fbc32b16d5df85c2841d00bcd91eac11b11ee48505`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:59 GMT
RUN cmd /S /C #(nop) COPY file:1368d6dce4ed982bfb8547b878cef8f8a5a2024c1be0b673ddbcd16aece97a5a in \ 
# Wed, 10 Sep 2025 22:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eae38821db13b372f7380c1e127dce59a3e4c30f1e740528b982e2c44025da`  
		Last Modified: Wed, 10 Sep 2025 22:19:04 GMT  
		Size: 46.2 MB (46224039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0461a5885755c025287834dfc263013831e8364f26b89049c064779b3c9`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6275934b92819657fd592f82e616af98f3cf7a6338ddf9a9e12e380d2902d`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d7f51f66b9ed4593cf0f78469461dc279be99d23f7222b50e604f86a75b05`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1076 bytes)  
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

### `traefik:v3` - unknown; unknown

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
$ docker pull traefik@sha256:8f98e904fab25aaa7cf5eb799658a0690aa6bf91e8d74cc3606527d1759eb533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:c850b679fb6311bda48e180537f04253cebc03ea6a7cab16141ba23b88b57499
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeac49ee6cd5c95bb1031fbc32b16d5df85c2841d00bcd91eac11b11ee48505`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:59 GMT
RUN cmd /S /C #(nop) COPY file:1368d6dce4ed982bfb8547b878cef8f8a5a2024c1be0b673ddbcd16aece97a5a in \ 
# Wed, 10 Sep 2025 22:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eae38821db13b372f7380c1e127dce59a3e4c30f1e740528b982e2c44025da`  
		Last Modified: Wed, 10 Sep 2025 22:19:04 GMT  
		Size: 46.2 MB (46224039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0461a5885755c025287834dfc263013831e8364f26b89049c064779b3c9`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6275934b92819657fd592f82e616af98f3cf7a6338ddf9a9e12e380d2902d`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d7f51f66b9ed4593cf0f78469461dc279be99d23f7222b50e604f86a75b05`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5`

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

### `traefik:v3.5` - unknown; unknown

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
$ docker pull traefik@sha256:8f98e904fab25aaa7cf5eb799658a0690aa6bf91e8d74cc3606527d1759eb533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:c850b679fb6311bda48e180537f04253cebc03ea6a7cab16141ba23b88b57499
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeac49ee6cd5c95bb1031fbc32b16d5df85c2841d00bcd91eac11b11ee48505`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:59 GMT
RUN cmd /S /C #(nop) COPY file:1368d6dce4ed982bfb8547b878cef8f8a5a2024c1be0b673ddbcd16aece97a5a in \ 
# Wed, 10 Sep 2025 22:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eae38821db13b372f7380c1e127dce59a3e4c30f1e740528b982e2c44025da`  
		Last Modified: Wed, 10 Sep 2025 22:19:04 GMT  
		Size: 46.2 MB (46224039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0461a5885755c025287834dfc263013831e8364f26b89049c064779b3c9`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6275934b92819657fd592f82e616af98f3cf7a6338ddf9a9e12e380d2902d`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d7f51f66b9ed4593cf0f78469461dc279be99d23f7222b50e604f86a75b05`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.2`

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

### `traefik:v3.5.2` - linux; riscv64

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

### `traefik:v3.5.2` - unknown; unknown

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
$ docker pull traefik@sha256:8f98e904fab25aaa7cf5eb799658a0690aa6bf91e8d74cc3606527d1759eb533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5.2-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:c850b679fb6311bda48e180537f04253cebc03ea6a7cab16141ba23b88b57499
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168947183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caeac49ee6cd5c95bb1031fbc32b16d5df85c2841d00bcd91eac11b11ee48505`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:17:59 GMT
RUN cmd /S /C #(nop) COPY file:1368d6dce4ed982bfb8547b878cef8f8a5a2024c1be0b673ddbcd16aece97a5a in \ 
# Wed, 10 Sep 2025 22:18:00 GMT
RUN cmd /S /C #(nop)  EXPOSE 80
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 22:18:01 GMT
RUN cmd /S /C #(nop)  LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9eae38821db13b372f7380c1e127dce59a3e4c30f1e740528b982e2c44025da`  
		Last Modified: Wed, 10 Sep 2025 22:19:04 GMT  
		Size: 46.2 MB (46224039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8663b0461a5885755c025287834dfc263013831e8364f26b89049c064779b3c9`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6275934b92819657fd592f82e616af98f3cf7a6338ddf9a9e12e380d2902d`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682d7f51f66b9ed4593cf0f78469461dc279be99d23f7222b50e604f86a75b05`  
		Last Modified: Wed, 10 Sep 2025 22:18:52 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:v3.5.2-windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:v3.5.2-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `traefik:windowsservercore-ltsc2022`

```console
$ docker pull traefik@sha256:e1ddf1c5b1d2b6632d4d0dd11b76eacd0ae489ff07bcc8dff39339aa80a04621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `traefik:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull traefik@sha256:7a4afc3c62c0974bc8c3735163317603dbbeefd0ca65b44d30f7a568e3f7a28b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328867518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3505a3d1a218c9c4a3f00fb7d98a3bb661bbede5f1a74bc39c14b6123b7c5b63`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v3.5.2/traefik_v3.5.2_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 10 Sep 2025 21:50:00 GMT
EXPOSE 80
# Wed, 10 Sep 2025 21:50:00 GMT
ENTRYPOINT ["/traefik"]
# Wed, 10 Sep 2025 21:50:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.source=https://github.com/traefik/traefik org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v3.5.2 org.opencontainers.image.documentation=https://docs.traefik.io
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
	-	`sha256:11dfa0f411d1819cedf10f818f0d607fd88a441730267c2b072a473392e9fb06`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e24f2c5210fafc103a054bc8e32f4a2fc057b771eee8986f0131176813ece7`  
		Last Modified: Wed, 10 Sep 2025 21:55:57 GMT  
		Size: 46.7 MB (46717320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cb4c4c0033840e4ef1981416af77576412b684ea33f9f642cafeebe56b01b7`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cca974f55a80e135bfc223eff6be41360dc07e7805ac6727c8e705c5daacd3`  
		Last Modified: Wed, 10 Sep 2025 21:55:46 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f1e10ecd33196a32303fca5342880095e186ef466d852a6462c2218be7c8a1`  
		Last Modified: Wed, 10 Sep 2025 21:55:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
